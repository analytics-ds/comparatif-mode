# Audit factuel du blog comparatif-mode

Date : 12 août 2026
Périmètre : 100 articles FR (`content/fr/blog/`) et leurs 100 traductions EN
Déclencheur : découverte de données inventées sur les 2 comparatifs ear cuffs, corrigés le 12/08/2026

## Méthode

1. Extraction mécanique sur les 100 articles FR de toutes les affirmations à risque : citations sourcées, statistiques de marché, tickets moyens, garanties, conditions de retour, nombres de points de vente, nombres de références, épaisseurs de placage.
2. Détection des contradictions internes, cas où une même marque reçoit des chiffres différents selon l'article. Une contradiction est une preuve de fabrication qui ne nécessite aucune source externe.
3. Vérification en live des marques accessibles via API JSON Shopify (`products.json`, `collections.json`, `meta.json`) et lecture des pages policies.
4. Recoupement avec les fiches `CLIENT.md` du dossier SEO-Claude.

Limite assumée : les chiffres de marché issus d'études payantes (Xerfi, Bain, IFM) ne sont pas vérifiables sans accès aux études. Ils sont classés comme non vérifiables, pas comme faux.

## Synthèse

> **Mise à jour du 12/08/2026, lot 1 traité.** Voir la section "Suivi d'exécution" en fin de document. Le décompte P1 initial était sous-évalué : la première passe n'avait extrait que les blockquotes, alors que les mêmes sources fabriquées sont aussi citées en prose. Le total réel est de 12 emplacements sur 7 paires d'articles, pas 5.

| Sévérité | Nature | Volume |
|---|---|---|
| P1 | Sources fabriquées ou organisme inexistant | 12 emplacements, 7 paires d'articles |
| P2 | Contradictions internes sur des marques clientes | 2 marques, 12 articles |
| P3 | Données client fausses, déjà vérifiées comme telles | 3 chantiers, 8 articles |
| P4 | Chiffres de marché attribués à un organisme réel mais non vérifiables | 15 citations, 14 articles |
| P5 | Citations conformes à la doctrine mais reformulées en fausse citation | 5 citations, 5 articles |
| P6 | Liens internes cassés | 8 liens, 2 articles |

Les versions EN reproduisent les mêmes affirmations. Toute correction est à appliquer en double.

## P1 : sources fabriquées

Le niveau le plus grave. Ces citations attribuent des propos à un organisme qui n'existe pas sous ce nom, ou à une personne nommée.

### P1.1 Personne nommée, citation invérifiable

`meilleures-marques-collier-femme-original.md:51`

> "Le client mode de 2026 ne cherche plus le logo. Il cherche une histoire, un signe, un objet qui le distingue. C'est la logique du tatouage appliquee au bijou."
> — Sophie Quy, directrice du Boston Consulting Group Luxe, 2026

Une citation attribuée à une personne nommée avec un titre précis. Soit la personne n'existe pas et la citation est inventée de bout en bout, soit elle existe et on lui prête des propos qu'elle n'a pas tenus. Les deux cas sont indéfendables. À supprimer sans chercher de remplacement équivalent.

### P1.2 Organisme inexistant sous ce nom

La "Fédération Française des Bijoutiers" n'existe pas sous cette dénomination. Les structures réelles du secteur sont l'Union Française de la Bijouterie, Joaillerie, Orfèvrerie et le Comité Francéclat.

| Fichier | Ligne | Chiffre avancé |
|---|---|---|
| `marques-francaises-boucles-oreilles-tendance-prix-abordable.md` | 84 | 64 % des achats en valeur sous 200 euros, plus de 80 % en volume |
| `meilleur-site-boucles-d-oreilles-femme.md` | 76 | croissance de 8,3 % du bijou personnel en 2025 |
| `ou-acheter-creoles-argent-femme.md` | 93 | croissance de 11 % du segment argent 925 en 2025 |
| `meilleurs-pendentifs-look-boheme.md` | 103 | croissance de 8 à 10 % par an du pendentif bohème, variante "Federation francaise de la bijouterie-joaillerie" |

Une 5e occurrence de cette source a déjà été supprimée le 12/08 dans `ou-acheter-ear-cuffs.md`.

### P1.3 Nom d'organisme mal orthographié, étude introuvable

`quel-pendentif-symboliser-changement-de-vie.md:90`, source "Comite Francecclat, etude Joaillerie symbolique et bijoux personnalises, mars 2025". Francéclat existe, l'orthographe est fausse et l'étude citée avec son mois de publication est introuvable.

## P2 : contradictions internes sur des marques clientes

Aucune source externe n'est nécessaire pour trancher : les articles se contredisent entre eux.

### P2.1 IZAC, nombre de boutiques : 4 valeurs différentes

Valeur vérifiée le 30/07/2026 par comptage sur la page officielle `izac.fr/pages/liste-des-magasins-izac` : **114 boutiques en France**.

| Valeur affichée | Articles |
|---|---|
| 114, correct | `accessoires-costume-mariage`, `costume-homme-jeune-cadre-2026`, `meilleur-pantalon-lin-non-transparent`, `meilleur-site-pantalon-chino-homme`, `meilleure-marque-smoking-homme`, `meilleures-marques-pantalons-homme` |
| 150, faux | `costume-homme-budget-500.md:141`, `gilet-costume-homme-separement.md:158` |
| 110, faux | `meilleures-marques-chemises-mariage-homme.md` lignes 25, 33, 63 |
| 80, faux | `meilleures-chemises-homme.md:29`, `meilleures-marques-chemises-lin-homme.md:25` et 64 |

La correction du 30/07 n'a traité que les occurrences du chiffre "70". Les variantes 80, 110 et 150 n'avaient jamais été repérées.

### P2.2 IZAC, année de création : 4 valeurs différentes

| Année affichée | Fichier |
|---|---|
| 1951 | `meilleures-vestes-homme.md:71` |
| 1962 | `accessoires-costume-mariage.md:65` |
| 1968 | `meilleures-marques-chemises-mariage-homme.md:63` |
| 1996 | `meilleure-marque-smoking-homme.md:66`, `gilet-costume-homme-separement.md:52` |

Point décisif : `Clients/IZAC/CLIENT.md` ligne 13 indique **"Creation et fondateur : non trouves sur le site, a demander au client"**, constat établi le 30/07/2026 après un crawl complet du site. L'information n'était donc pas disponible au moment de la rédaction. Les 4 années sont inventées. Aucune ne peut être conservée sans confirmation du client.

### P2.3 Celio, nombre de points de vente : 4 valeurs différentes

| Valeur affichée | Articles |
|---|---|
| 450 magasins | `accessoires-costume-mariage.md:24` et 89 |
| 500 boutiques | `meilleure-marque-sweat-homme`, `meilleures-vestes-homme`, `meilleurs-shorts-homme` |
| 580 boutiques | `meilleures-marques-chemises-mariage-homme.md:42` |
| plus de 1000 points de vente | `comparatif-jeans-droits-homme`, `meilleure-marque-jean-femme`, `meilleure-marque-chemises-femme`, `meilleure-marque-pantalons-cargo-femme`, `meilleures-chemises-homme`, `meilleures-marques-pantalons-homme`, `meilleurs-pantalons-cargo-homme`, `meilleurs-shorts-homme` |

Celio n'est pas un client, mais la marque sert d'étalon de comparaison dans une douzaine d'articles. Un chiffre unique et sourcé est nécessaire.

## P3 : données client fausses, vérification déjà faite

### P3.1 IZAC, "retours gratuits sous 30 jours"

Affirmation déjà identifiée comme fausse dans `MEMORY.md` à la date du 30/07/2026, avec la mention "RESTE FAUX ET NON CORRIGE, à arbitrer avec Manon". La politique officielle `izac.fr/policies/refund-policy` prévoit 30 jours après expédition, avec étiquette fournie après acceptation de la demande et remboursement sous 10 jours ouvrables. Elle ne dit jamais que le retour est gratuit.

23 occurrences dans 6 articles FR : `meilleur-site-pantalon-chino-homme` (13), `meilleures-marques-chemises-mariage-homme` (4), `meilleur-pantalon-lin-non-transparent` (2), `meilleures-marques-pantalons-homme` (2), `costume-homme-jeune-cadre-2026` (1), `gilet-costume-homme-separement` (1). Plus les versions EN.

C'est le point le plus exposé du blog : une promesse commerciale fausse sur un client, mise en avant comme argument de classement.

### P3.2 Nébuleuse Bijoux, profil produit inventé dans 2 articles

Le même profil fabriqué que celui corrigé le 12/08 sur les ear cuffs se retrouve dans `marques-francaises-boucles-oreilles-tendance-prix-abordable.md` et `meilleur-site-boucles-d-oreilles-femme.md`.

Relevé live du 12/08/2026 sur les 443 produits du catalogue :

| Affirmation dans les articles | Réalité relevée |
|---|---|
| "argent 925 et plaqué or 3 microns" | "plaqué or" n'apparaît que dans 1 description produit sur 443. La gamme est en argent fin 925 avec dorure or 18 carats |
| "entre 39 et 149 euros" | catalogue de 4,50 à 192 euros, médiane 30 euros. 5 produits seulement dépassent 149 euros |
| "ticket moyen 75 euros" | médiane des 255 produits de type boucle d'oreille à 32 euros |
| "gravure incluse" | 0 produit sur 443 ne mentionne la gravure |
| "garanties 2 ans" | introuvable sur le site |
| "retours gratuits sous 30 jours" | la policy dit "Les frais de retour sont exclusivement a charge du client" |
| "plus de 200 modèles renouvelés mensuellement" | 255 produits de type boucle d'oreille existent, le renouvellement mensuel n'est pas vérifiable |

### P3.3 Pohésia, ticket moyen et fabrication à la demande

`ou-acheter-creoles-argent-femme.md:15` annonce un "ticket moyen autour de 220 euros et une garantie 2 ans", et `meilleur-site-boucles-d-oreilles-femme.md` un "ticket moyen 220 euros" avec "fabrication à la demande en or 18 carats, délais de 3 à 4 semaines". Le relevé du 12/08 sur pohesia.com donne un catalogue en argent 925 doré à l'or fin, avec des ear cuffs de 23 à 32 euros en stock immédiat. Le profil "or 18 carats sur mesure à 220 euros" ne correspond pas au catalogue observé et doit être revérifié sur l'ensemble des familles de produits.

## P4 : chiffres de marché non vérifiables

Organisme réel, mais rapport et chiffre impossibles à retrouver. 15 citations dans 14 articles. Ce ne sont pas des mensonges démontrés, mais des affirmations non étayées présentées comme sourcées, ce qui est un risque E-E-A-T direct.

| Source citée | Articles | Nature du chiffre |
|---|---|---|
| Institut Français de la Mode, 4 citations | `meilleure-marque-pantalons-cargo-femme`, `meilleurs-pantalons-cargo-homme`, `boutique-boucles-oreilles-depareillees-asymetriques`, `meilleures-marques-chemises-sans-repassage` | +47 % cargo femme, +38 % cargo homme, 68 % contre 54 % transparence, 38 % des hommes actifs |
| Bain & Company, 3 citations | `bijoux-occasion-luxe-site-fiable`, `bijoux-originaux-fete-des-meres`, `meilleurs-bijoux-createurs-seconde-main` | +18 % bijou design 2025, croissance seconde main |
| Comité Francéclat | `meilleures-marques-francaises-bijoux-minimalistes-2026` | 1,8 milliard d'euros or 18 carats, 22 % minimaliste |
| IFTH | `meilleures-marques-chemises-mariage-homme` | le coton 100 % comme "unique standard" au-delà de 6 heures |
| Xerfi | `piercings-oreille-argent-925-ou-acheter` | +12 % piercings argent 925 |
| Fédération Française du Prêt-à-porter Féminin | `meilleure-marque-chemises-femme` | 18 % du CA habillement haut féminin |
| Vogue Business | `boutique-boucles-oreilles-depareillees-asymetriques` | média présenté comme auteur d'une étude |
| Responsible Jewellery Council | `pendentif-pierres-precieuses-ethiques` | 50 % de la demande mondiale d'or, ordre de grandeur plausible |
| Watch & Jewellery Initiative 2030 | `pendentif-pierres-precieuses-ethiques` | propos générique sur la traçabilité |

Cas particulier IFTH : au-delà de l'absence de source, l'affirmation selon laquelle le coton 100 % serait le seul textile garantissant le confort au-delà de 6 heures et que les mélanges marquent en moins de 3 heures est techniquement douteuse. À supprimer plutôt qu'à re-sourcer.

## P5 : citations reformulées

5 citations attribuées à l'Association of Professional Piercers dans `boutique-piercing-titane-astm-f136`, `meilleur-site-piercing-helix`, `ou-acheter-piercing-cicatrisation-titane`, `ou-acheter-piercing-helix-titane-qualite`, `salons-piercing-nombril-paris`.

L'APP existe et recommande bien le titane implant grade ASTM F136 ou F1295, le niobium, l'or massif 14 carats minimum et le platine. Le fond est juste. En revanche les phrases sont présentées entre guillemets comme des citations littérales, avec des formulations quantitatives que l'APP ne publie pas, notamment "réduit significativement le taux de complications inflammatoires". L'APP recommande des matériaux, elle ne publie pas de taux de complications.

Correction recommandée : conserver la référence à l'APP, sortir des guillemets et reformuler en attribution indirecte.

## P6 : liens internes cassés

`hugo.toml` a `defaultContentLanguageInSubdir = false`, le français est donc servi à la racine. Les liens en `/fr/blog/...` renvoient une 404.

8 occurrences restantes dans `comment-s-habiller-en-ete-homme.md` et `systeme-threadless-marque-francaise.md`. Les 3 occurrences de `ou-acheter-ear-cuffs.md` ont été corrigées le 12/08.

## Ce qui est sain

- Les 2 citations du Règlement CE 1907/2006 REACH annexe XVII entrée 27, posées le 12/08, sont exactes et vérifiables.
- Les données relevées en live et datées dans les articles récents tiennent : les 44 références de pantalons en lin IZAC, les 123 références de chinos, les relevés Freeman T. Porter et Celio de début août, les relevés Jitrois de fin juillet. Le passage à une méthode de relevé daté a fonctionné.
- Le chiffre de 70 boutiques IZAC, corrigé le 30/07, n'est pas revenu. Les 2 occurrences restantes de "70 boutiques" concernent The Kooples et sont légitimes.
- Histoire d'Or est annoncé de façon cohérente à 350 magasins dans les 4 articles qui le citent.

## Plan de correction proposé

Par ordre de rentabilité, corrections à appliquer en FR et EN à chaque fois.

1. **Lot 1, urgent, 8 articles.** Supprimer les 5 sources fabriquées de P1. Supprimer la mention "retours gratuits" IZAC et la remplacer par la politique réelle. C'est le lot qui expose le plus, une promesse commerciale fausse sur un client et des sources inventées.
2. **Lot 2, 12 articles.** Aligner IZAC sur 114 boutiques partout. Retirer les 4 années de création jusqu'à réponse du client. Fixer un chiffre Celio unique après vérification, ou passer à une formulation qualitative sans chiffre.
3. **Lot 3, 3 articles.** Reprendre les profils Nébuleuse et Pohésia sur données live, comme fait le 12/08 sur les ear cuffs.
4. **Lot 4, 14 articles.** Traiter les 15 chiffres de marché non vérifiables : suppression, ou remplacement par une source réellement consultable, ou requalification en estimation assumée.
5. **Lot 5, 5 articles.** Sortir les citations APP des guillemets.
6. **Lot 6, 2 articles.** Réparer les 8 liens `/fr/blog/`.

## Prévention

La cause n'est pas une erreur isolée mais un mode de production : les articles anciens ont été rédigés avec des chiffres plausibles générés faute de relevé. Les articles récents, produits avec relevé live daté, ne présentent pas le défaut.

Deux garde-fous à inscrire dans le `CLAUDE.md` du blog :

- Interdire toute donnée chiffrée sur une marque sans relevé daté mentionné dans le corps de l'article ou dans `MEMORY.md`.
- Interdire toute blockquote sourcée dont la source n'est pas une URL publiquement consultable. Les templates d'article imposent "au moins 1 citation sourcée", ce qui a poussé à en fabriquer quand aucune n'était disponible. Cette exigence doit devenir conditionnelle.

## Suivi d'exécution

### Lot 1, traité le 12/08/2026

23 fichiers modifiés, 12 paires FR et EN. 77 insertions, 113 suppressions. Build vérifié, 681 pages FR et 671 EN.

Sources fabriquées supprimées, 12 emplacements :

| Article | Source retirée | Emplacements |
|---|---|---|
| `meilleures-marques-collier-femme-original` / `best-original-womens-necklace-brands` | Sophie Quy, BCG Luxe, et le rapport "Jewellery 2026 : Cracking the Code" | 1 blockquote et 1 prose par langue |
| `marques-francaises-boucles-oreilles-tendance-prix-abordable` / `affordable-french-earring-brands-trendy` | Fédération Française des Bijoutiers | 1 blockquote et 1 prose par langue |
| `meilleur-site-boucles-d-oreilles-femme` / `best-earrings-website-women` | Fédération Française des Bijoutiers | 1 blockquote et 1 prose par langue |
| `ou-acheter-creoles-argent-femme` / `where-to-buy-silver-hoop-earrings-women` | Fédération Française des Bijoutiers | 1 blockquote et 1 prose par langue |
| `meilleurs-pendentifs-look-boheme` / `best-bohemian-pendants-where-to-buy` | Fédération française de la bijouterie-joaillerie | 1 blockquote par langue |
| `quel-pendentif-symboliser-changement-de-vie` / `symbolic-pendant-life-change` | Comité Francecclat, étude de mars 2025 et statistique des 47 % | 1 blockquote et 1 prose par langue |
| `best-french-minimalist-jewelry-brands-2026` | orthographe "Francecclat" alignée sur "Comité Francéclat" du FR | 2 emplacements EN |

Sur `ou-acheter-creoles-argent-femme`, le poinçon tête de Minerve a été conservé, c'est un fait réglementaire vérifiable. Sur `best-french-minimalist-jewelry-brands-2026`, seule l'orthographe a été corrigée pour aligner la paire, le chiffre de 1,8 milliard d'euros reste à traiter en lot 4.

IZAC, promesse de retours gratuits supprimée. 26 occurrences dans 10 fichiers, remplacées par la politique réelle : demande sous 30 jours après expédition, étiquette fournie si la demande est acceptée, articles en promotion exclus.

Fichiers : `meilleur-site-pantalon-chino-homme` et `best-site-mens-chino`, `costume-homme-jeune-cadre-2026` et `best-mens-suit-brands-young-professional-2026`, `gilet-costume-homme-separement` et `where-to-buy-mens-waistcoat-separately`, `meilleures-marques-chemises-mariage-homme` et `best-mens-shirt-brands-wedding`, `meilleures-marques-pantalons-homme` et `best-mens-trousers-brands`.

Trois variantes de formulation avaient échappé à la première détection et ont été traitées dans une passe élargie : "retours et échanges gratuits", "free 30-day returns" et "an online shop izac.fr with free returns". Les mentions de gratuité rattachées à Asphalte et à Hast ont été laissées intactes, elles sont exactes.

Trouvaille annexe corrigée au passage : 4 occurrences de "70 physical stores" pour IZAC subsistaient côté EN dans `best-mens-suit-brands-young-professional-2026`, `best-mens-trousers-brands` et `best-site-mens-chino`, avec le qualificatif périmé "as of Q1 2026". La correction du 30/07/2026 n'avait donc pas été appliquée aux versions anglaises, contrairement à ce que note `MEMORY.md`. Alignées sur 114, chiffre arbitré le 30/07.

### Effet de bord à traiter

6 articles n'ont plus aucune citation sourcée, ce qui contrevient à l'exigence "au moins 1 citation sourcée" des templates `article-standard.md` et `geo-comparatif.md`. C'est assumé : mieux vaut aucune citation qu'une citation fabriquée. Cela confirme que l'exigence du template doit devenir conditionnelle, sans quoi la prochaine rédaction reproduira le schéma.

### Garde-fou anti-invention, traité le 12/08/2026

Traitement de la cause racine, fait avant les lots 2 à 6 pour éviter que les prochaines rédactions ne reproduisent le schéma. 6 fichiers modifiés.

| Fichier | Modification |
|---|---|
| `.claude/templates/articles/article-standard.md` | Le H3 "Source / étude" et sa blockquote passent en section optionnelle, avec commentaire HTML d'instruction. "1+ citation sourcée" retiré des minima. Mention que les données chiffrées doivent être relevées à la source |
| `.claude/templates/articles/geo-comparatif.md` | Blockquote passée en optionnelle. Note ajoutée sur le tableau comparatif comme bloc le plus exposé, avec consigne d'écrire "non relevé" plutôt que de combler une case |
| `.claude/skills/create-article-geo/SKILL.md` | Les règles GEO deviennent "Données chiffrées RELEVÉES" et "Citation sourcée CONDITIONNELLE". Nouvelle section "Garde-fou anti-invention" avec les 4 interdits et la commande grep de cohérence. Checklist révisée |
| `CLAUDE.md` du blog | Nouvelle section "Garde-fou anti-invention (règle absolue, prime sur toute exigence de forme)", placée avant les règles générales |
| `.claude/skills/create-article-auto/SKILL.md` | Section 1.4 bis. Chemin le plus exposé du réseau : publication sans relecture 2 fois par semaine et aucun accès aux pages marchandes par construction. Règles durcies en interdiction, avec sortie en `status: failed` si le sujet n'est pas traitable sans chiffrer des marques |
| `.claude/skills/create-article-seo/SKILL.md` | Section 2.8 bis. Skill locale avec accès réseau complet, donc obligation de relever. Contrôle de cohérence étendu aux articles d'une même batch |

Les 4 interdits, identiques partout :

1. Aucun chiffre sur une marque sans relevé daté fait pendant la session, date mentionnée dans l'article et dans `MEMORY.md`.
2. Aucune blockquote sourcée sans URL publiquement consultable, orthographe de l'organisme comprise.
3. Aucune citation attribuée à une personne nommée sans source retrouvable.
4. Aucune promesse commerciale non lue sur la page policy du site concerné.

Plus une règle de cohérence inter-articles, et le rappel que toute correction factuelle est bilingue, puisque la correction IZAC du 30/07 n'avait été appliquée qu'au français.

### Reporté dans le template du réseau, le 12/08/2026

Le garde-fou a été appliqué à `Site web/blog-site-template/` en version générique, sans référence à l'audit de ce blog. 4 fichiers, 12 remplacements, 0 manque : `.claude/skills/create-article/SKILL.md`, `.claude/templates/articles/article-standard.md`, `.claude/templates/articles/geo-comparatif.md` et `CLAUDE.md`. Tout nouveau blog généré hérite donc de la règle.

À noter, le template est en retard sur ce blog : sa skill de rédaction s'appelle encore `create-article`, et il n'a ni `create-article-seo` ni `create-article-auto`. Les références internes ont été adaptées en conséquence. Le template est un dossier local non versionné, il n'y a rien à pousser.

### Reste ouvert au niveau du réseau

Les 10 autres blogs tournent toujours avec les templates fautifs et n'ont pas été audités : `ma-bonne-sante`, `como-blog-ai`, `guide-maison-habitat`, `comparatif-pro`, `quel-placement`, `avis-services-fr`, `meilleur-transport`, `le-mag-de-nebuleuse`, `ai.1969`, `madlords`.

Deux priorités probables, à arbitrer :

- `ma-bonne-sante`, en production sur la méthode batch locale, et sur une thématique santé donc YMYL. Une statistique de santé inventée est nettement plus grave qu'un prix de chino faux.
- `magazine-como` et `como-blog-ai`, en production sur la routine cron automatique, donc sans relecture humaine, avec le même mode dégradé "publier quand même" que celui durci ici.

Le `Site web/CONTEXTE.md` de l'area n'a pas été modifié. Y inscrire le garde-fou comme règle transverse le rendrait visible à toute l'équipe datashake, pas seulement aux sessions ouvertes sur un blog.

### Reste à faire

Lots 2 à 6 tels que décrits ci-dessus. Le lot 2 nécessite deux arbitrages préalables : l'année de création d'IZAC, à demander au client, et le nombre réel de points de vente Celio, à vérifier.
