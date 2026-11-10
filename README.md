# Maison d’Imprimeur — système de gestion

> Projet de gestion pour **Société Maison d’Imprimeur**, à Béni Mellal. Cette première version définit les besoins confirmés et le périmètre avant la construction de l’application.

## Besoins confirmés

- Utilisation **uniquement dans le magasin**, sans accès depuis l’extérieur. Le fonctionnement hors ligne est souhaité; le mode de partage sur plusieurs postes reste à confirmer.
- Jusqu’à **10 utilisateurs** au total, avec un compte administrateur et un compte manager. Les autres comptes auront des droits limités selon leur rôle.
- Interface en **français et en arabe**, avec prise en charge de l’affichage RTL pour l’arabe.
- Paiements de factures enregistrés **manuellement**; aucune intégration d’opérateur dans la première version.
- Le logo existe et sera fourni pour son intégration.

## Objectif

Centraliser les activités du magasin dans une application adaptée à l’ordinateur et éventuellement à plusieurs postes du magasin. Le système doit suivre les clients, les demandes, les commandes, les ventes, les dépenses, le stock et les documents, avec des droits d’accès et un historique des opérations.

## Activités à gérer

- **Impression** : photocopie, impression, scan, reliure, plastification, saisie et préparation de fichiers.
- **Fournitures de bureau** : articles, prix, achats, ventes et stock.
- **Traduction** : demande, langues, échéance, tarif, état d’avancement et livraison.
- **Paiement de factures** : enregistrer le service effectué, le montant payé et les frais/commission. Le suivi est manuel dans la première version. Ne jamais conserver les numéros de carte ou codes secrets des clients.
- **Écrivain public / services administratifs** : enregistrer le type de prestation, le suivi et le montant. Limiter les données personnelles au strict nécessaire et réserver leur accès aux personnes autorisées.
- **Facturation** : devis, factures et reçus selon les besoins de l’entreprise. Les modèles et règles fiscales seront à valider avec le comptable avant utilisation officielle.

## Modules proposés

1. **Tableau de bord** — ventes du jour, commandes en attente, alertes de stock et résumé de caisse.
2. **Clients** — coordonnées utiles, historique des prestations et recherche rapide.
3. **Ventes et commandes** — une commande peut contenir plusieurs activités, avec statut (reçue, en cours, prête, livrée, annulée), échéance et notes.
4. **Catalogue et stock** — articles, catégories, prix d’achat/vente, mouvements et seuil d’alerte. Suivi séparé des consommables d’impression et des articles vendus.
5. **Devis, factures et reçus** — numérotation, impression/export PDF et suivi du paiement (non payé, partiel, payé).
6. **Caisse et dépenses** — entrées, sorties, moyen de paiement, ouverture/clôture de journée et rapprochement.
7. **Traductions et dossiers** — échéances, statut, montant et responsable; les fichiers sensibles ne sont pas inclus dans le périmètre initial.
8. **Rapports** — ventes et dépenses par période, activité et moyen de paiement; export réservé aux utilisateurs autorisés.
9. **Utilisateurs et historique** — jusqu’à 10 comptes; administrateur, manager et rôles limités pour les employés; journal des actions importantes.
10. **Paramètres** — informations de l’entreprise, langues, catégories, logo, règles de facturation à confirmer et sauvegarde.

## Première livraison (MVP)

- Connexion et rôles de base pour les utilisateurs du magasin.
- Tableau de bord.
- Clients, catalogue/stock et commandes multi-activités.
- Encaissements, dépenses, paiements de factures saisis manuellement, reçus et rapports simples.
- Interface bilingue français/arabe.
- Intégration du logo fourni.
- Sauvegarde et restauration testées avant toute utilisation réelle.

Les paiements connectés à un opérateur, la gestion de documents sensibles, les intégrations externes et la conformité détaillée des factures seront ajoutés seulement après validation des prestataires et des besoins métier.

## Points techniques à confirmer

L’utilisation dans le magasin est confirmée, mais il reste à choisir entre **un seul ordinateur** et **plusieurs ordinateurs connectés au réseau local**. Pour plusieurs postes, une base de données et un serveur local sont nécessaires; pour un seul poste, une application locale est plus simple. Il faut également confirmer si le total de 10 comptes inclut les comptes administrateur et manager (par défaut : oui).

## Sécurité et mise en production

Ce dépôt ne contient pas encore d’application de production. Avant d’y saisir des données réelles, il faudra construire et tester un serveur/base de données adaptés au mode choisi, des autorisations, des sauvegardes et une restauration. Un système hors ligne n’est pas automatiquement sécurisé : protéger les ordinateurs et les sauvegardes, et ne jamais ajouter de secret, mot de passe, document client ou donnée de paiement réelle au dépôt Git.

Les modèles de reçus/factures et les règles fiscales locales doivent être validés avec le comptable avant leur utilisation officielle.

## Étapes de réalisation

1. Confirmer le nombre de postes et transmettre le logo.
2. Confirmer les prestations, prix et informations à afficher sur les reçus.
3. Construire le modèle de données et les écrans du MVP.
4. Tester les parcours réels avec des données fictives.
5. Valider les reçus/factures avec le comptable.
6. Installer dans le magasin, former les utilisateurs et vérifier les sauvegardes.
