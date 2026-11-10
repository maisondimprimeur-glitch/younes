# Maison d’Imprimeur — système de gestion

> Projet de gestion pour **Société Maison d’Imprimeur**, à Béni Mellal. Cette première version définit le périmètre et les étapes avant la mise en place de l’application. Elle ne contient pas encore d’application déployable.

## Objectif

Centraliser les activités du magasin dans une application web simple, utilisable sur ordinateur, tablette et téléphone, en français et en arabe (interface RTL). Le système doit suivre les clients, les demandes, les commandes, les ventes, les dépenses, le stock et les documents administratifs, avec des droits d’accès et un historique des opérations.

## Activités à gérer

- **Impression** : photocopie, impression, scan, reliure, plastification, saisie et préparation de fichiers.
- **Fournitures de bureau** : articles, prix, achats, ventes et stock.
- **Traduction** : demande, langues, échéance, tarif, état d’avancement et livraison.
- **Paiement de factures** : enregistrer le service effectué, le montant payé et les frais/commission. Une connexion à un opérateur de paiement ne sera ajoutée qu’après identification du prestataire agréé et de ses accès. Le système ne doit jamais conserver les numéros de carte ou codes secrets des clients.
- **Écrivain public / services administratifs** : enregistrer le type de prestation, le suivi et le montant. Les documents et données personnelles doivent être limités au strict nécessaire, avec accès réservé aux personnes autorisées.
- **Facturation** : devis, factures et reçus selon les besoins de l’entreprise. Les modèles et règles fiscales seront à valider avec le comptable de l’entreprise avant utilisation officielle.

## Modules proposés

1. **Tableau de bord** — ventes du jour, commandes en attente, alertes de stock et résumé de caisse.
2. **Clients** — coordonnées utiles, historique des prestations et recherche rapide.
3. **Ventes et commandes** — une commande peut contenir des lignes de plusieurs activités, avec statut (reçue, en cours, prête, livrée, annulée), échéance et notes.
4. **Catalogue et stock** — articles, catégories, prix d’achat/vente, mouvements et seuil d’alerte. Les consommables d’impression peuvent être suivis séparément des articles vendus.
5. **Devis, factures et reçus** — numérotation, impression/export PDF et suivi du paiement (non payé, partiel, payé).
6. **Caisse et dépenses** — entrées, sorties, moyen de paiement, ouverture/clôture de journée et rapprochement.
7. **Traductions et dossiers** — échéances, statut, montant et responsable; les fichiers sensibles ne sont pas inclus dans le périmètre initial.
8. **Rapports** — ventes et dépenses par période, activité et moyen de paiement; export réservé aux utilisateurs autorisés.
9. **Utilisateurs et historique** — rôles (administrateur, caisse, opérateur), permissions et journal des actions importantes.
10. **Paramètres** — informations de l’entreprise, langues, catégories, taxes/facturation à confirmer et sauvegarde.

## Première livraison (MVP)

- Connexion et rôles de base.
- Tableau de bord.
- Clients, catalogue/stock et commandes multi-activités.
- Encaissements, dépenses, reçus et rapports simples.
- Interface responsive français/arabe.
- Sauvegarde et restauration testées avant toute utilisation réelle.

Les paiements de factures connectés à un opérateur, la gestion de documents sensibles, les intégrations externes et la conformité détaillée des factures seront ajoutés seulement après validation des prestataires et des besoins métier.

## Décisions à confirmer avant l’application

Les choix par défaut proposés sont entre parenthèses :

1. L’application sera-t-elle utilisée **uniquement dans le magasin** ou aussi à distance ? (accès web à distance avec comptes protégés)
2. Combien de personnes auront un compte, et quels rôles leur attribuer ? (administrateur + caisse + opérateur)
3. Voulez-vous gérer chaque impression comme un service à tarif libre, ou aussi un tarif calculé par format/couleur/quantité ? (les deux)
4. Quel prestataire utilisez-vous pour le paiement des factures, et souhaitez-vous d’abord seulement enregistrer les paiements manuellement ? (enregistrement manuel d’abord)
5. Avez-vous déjà un modèle de facture/reçu ou un logo à intégrer ? (modèle simple à personnaliser)
6. Préférez-vous le français, l’arabe, ou les deux dans les écrans et documents ? (les deux)

## Sécurité et mise en production

Ce dépôt n’est pas encore une application de production. Avant d’y saisir des données réelles, il faudra construire et tester un serveur avec base de données, authentification, autorisations, sauvegardes chiffrées, journalisation et politique de conservation des données. Aucun secret, mot de passe, document client ou donnée de paiement réelle ne doit être ajouté au dépôt Git.

## Étapes de réalisation

1. Confirmer les décisions ci-dessus et les détails des prestations/prix.
2. Construire le modèle de données et les écrans du MVP.
3. Tester les parcours réels avec des données fictives.
4. Valider les reçus/factures avec le comptable et les règles locales applicables.
5. Déployer dans un environnement privé, former les utilisateurs et vérifier les sauvegardes.
