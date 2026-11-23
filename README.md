# Prospection B2B automatisée

Automatisation qui prépare chaque matin une courte liste de prospects qualifiés pour une PME industrielle française de fabrication métallique sur mesure. Le but : trouver des **clients réguliers** (donneurs d'ordre qui font fabriquer leur métal à l'extérieur), pas des appels au hasard.

> Ce dépôt décrit la méthode. Les listes de prospects, les noms de clients, les coordonnées et les identifiants ne sont volontairement pas publiés.

## Fonctionnement

Une tâche planifiée tourne du lundi au jeudi au petit matin, sans intervention :

1. Elle relève les **signaux d'achat récents** dans des sources publiques.
2. Elle **qualifie** chaque candidat (taille, santé financière, absence d'atelier métal concurrent).
3. Elle trouve un **téléphone fiable** pour chaque prospect retenu.
4. Elle génère un **tableur** du jour et envoie un **récapitulatif par email** à l'entreprise.

## Sources de signaux

| Source | Ce qu'on y cherche |
|---|---|
| BOAMP (marchés publics) | marchés de mobilier, équipement ou présentoirs récemment attribués : le titulaire a du métal à faire fabriquer |
| BODACC | fermeture d'un fournisseur du secteur : ses clients cherchent un nouveau fabricant |
| Presse et web | ouvertures ou rénovations de réseaux de magasins, relocalisations, rachats, nouvelles gammes |
| Offres d'emploi | recrutement d'un acheteur sous-traitance ou d'un chef de projet agencement |
| Registre des entreprises et Pappers | effectif, chiffre d'affaires, dirigeant, procédures collectives |

## Critères de qualification

- Entreprise active, créée depuis plus de 3 ans, au moins 10 salariés (sauf négociants).
- Aucune procédure collective, comptes récents et sains.
- **Pas d'atelier métal en interne** : les concurrents sont écartés après vérification sur leur site.
- Besoin réel de produits métal simples en série, avec commandes récurrentes.
- Pas de doublon : une entreprise ou un groupe déjà envoyé n'est jamais renvoyé, sauf en « à rappeler » si un nouveau signal fort apparaît.

## Téléphone

Un prospect n'est compté que si le numéro est celui du bon endroit où appeler :

- numéro du site officiel (contact, mentions légales), ou
- deux sources indépendantes et concordantes.

Service client, numéros surtaxés et fiches anciennes sont écartés. Sans numéro fiable, le prospect va dans une section à part.

## Livrables

**Tableur du jour** : note sur 5, entreprise, ville, téléphone et sa source, interlocuteur à demander, signal et sa date, segment, effectif, chiffres clés, phrase d'accroche, points de vigilance, statut de suivi.

**Email** : une ligne d'intro, puis pour chaque prospect le nom, la note, le téléphone, l'interlocuteur, la raison d'appeler et une accroche d'une ligne. Trois parties possibles : nouveaux prospects, sans numéro, à rappeler.

## Outils

Automatisation planifiée, API ouvertes (BOAMP, BODACC, recherche d'entreprises), navigateur pour les pages sans API, Google Drive et Gmail pour la livraison.
