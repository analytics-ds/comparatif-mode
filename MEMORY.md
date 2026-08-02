# Suivi des publications

Ce fichier trace tous les articles publies sur le blog, classes par semaine.
La limite est de 4 articles par semaine maximum.
Mis a jour automatiquement par `/create-article-geo`.

## Semaine du 3 aout 2026 (2026-W32)

- 2026-08-03 [PROGRAMME, publishDate futur] : [FR] Où trouver un pantalon en lin qui ne soit pas transparent ? / [EN] Where to find linen trousers that are not see-through? (Mode homme, Comparatif GEO - IZAC #1, vs Asphalte / Uniqlo / Massimo Dutti, angle transparence et opacite du lin. Query fan-out "meilleur pantalon en lin non transparent". Cadrage homme valide par Manon (IZAC = PAP masculin uniquement), categorie Mode homme plutot que Comparatifs. Cannibalisation signalee et acceptee : overlap 50 % des tokens avec meilleures-marques-pantalons-homme, et meilleur-site-pantalon-chino-homme mentionne deja le pantalon 100 % lin IZAC a 55 EUR depuis l'enrichissement du 30/07. Article cadre STRICTEMENT sur l'opacite (grammage, composition, coloris, armure), passe la main aux 2 autres pour le classement generique via liens internes. Donnees relevees en live le 30/07/2026 : IZAC 44 references de pantalons lin sur 4000 produits (API Shopify, 16 pages), 34 en 100 % lin, 9 en melange, 55 a 95,99 EUR barres 109,99-119,99, 5 compositions de melange, 8 teintes sombres, tailles 38-56. Asphalte Le Pantalon Costume en Lin 179 EUR, 275 g/m2 publie (SEUL grammage du panel, cite en blockquote sourcee), lin francais tisse chez Leomaster, 3 coloris, tailles 36-48 ; son 2e pantalon lin a 89 EUR n'est PLUS achetable (page en "voter pour son come-back"). Uniqlo 3 pantalons lin homme, AUCUN en pur lin, Relax 49,90 EUR = 63 % coton/35 % lin/2 % elasthanne twill, Easy 29,90 EUR = 67 % coton/33 % lin. Massimo Dutti 12 references 25,95 a 90 EUR, descriptif produit dit lui-meme "tissu fin et leger" = le plus expose. IMPORTANT : 115 magasins IZAC comptes sur la page officielle liste-des-magasins-izac (111 France metro + 3 Reunion + 1 Luxembourg), ce qui INFIRME le chiffre de 70 boutiques herite des anciens articles et jamais verifie. Politique retour verifiee : 30 jours apres expedition, etiquette fournie, remboursement 10 jours ouvrables, livraison gratuite des 70 EUR, PAS "retours gratuits" comme ecrit ailleurs. Script fetch-image.sh KO sur Windows (depend de python3 absent), image recuperee a la main via la meme API Openverse, gros plan toile de lin sombre CC0 StockSnap, format .jpg car cwebp absent)

- 2026-08-02 : [FR] Meilleures marques de vestes en cuir pour homme / [EN] Best Men's Leather Jacket Brands (Comparatifs, 1737 mots FR). Run GEO Jitrois aout. Cible le prompt "Quelles sont les meilleures marques de vestes en cuir pour homme ?" (visibilite 0 % sur les 3 moteurs, persistence 41 %, 41 QFO) et le cluster Homme, le plus troue du compte a 7 %. Capte aussi le PAA "Quelle marque francaise est connue pour ses blousons en cuir ?" via un H2 dedie. ATTENTION propriete : classement segmente par usage, les references heritage (Schott NYC, Belstaff, Aero Leather) sont traitees serieusement et NON detronees, Jitrois est positionne uniquement sur le cuir couture et le cuir stretch, ou il est legitime. Article meilleures-vestes-homme (proprietaire IZAC) non modifie, simplement linke. Prix Jitrois releves en direct sur la collection homme, 2990 a 4650 EUR sur 14 modeles, les autres fourchettes sont des ordres de grandeur marche annonces comme tels. Verifie avant redaction : aucun AI Overview ne se declenche sur les requetes commerciales de ce marche, le gain attendu est sur ChatGPT et Gemini.

- 2026-08-04 [PROGRAMME, publishDate futur] : [FR] Où acheter du cuir de luxe femme à Paris ? / [EN] Where to buy luxury women's leather in Paris (Guides d'achat, Jitrois cite sur le segment maison specialisee cuir couture, adresse verifiee en live 38 rue du Faubourg Saint-Honore 75008, lundi-samedi 11h-19h. Run GEO Jitrois, chantier QFO, dernier lot. Couvre les 2 derniers prompts P1 actionnables, "Ou acheter un blouson en cuir femme elegant a Paris ?" (vis 7 %, pers 34 %) et "Ou acheter un manteau long en cuir femme haut de gamme a Paris ?" (vis 13 %, pers 30 %). QFO dominantes reprises : "boutiques blouson cuir femme Paris", "boutiques cuir femme Paris", "manteau cuir luxe femme Paris". Angle local par type d'adresse, grands magasins et detaillants cuir cites honnetement. Adresses non verifiables volontairement donnees sans numero de rue. Ecrit et pousse le 29/07, masque par Hugo jusqu'au 04/08 pour rester dans le repere de 4 articles/semaine, le cron quotidien 5h UTC le rendra visible. Image banque jitrois-cuir tenue-cuir-femme-06)

## Semaine du 27 juillet 2026 (2026-W31)

- 2026-07-30 : [CORRECTION FACTUELLE TRANSVERSE, non compte quota] Reseau de boutiques IZAC corrige sur 10 articles (5 FR + 5 EN). Le chiffre de 70 boutiques, herite des premieres redactions et jamais verifie, est FAUX. Comptage exact sur la page officielle izac.fr/pages/liste-des-magasins-izac le 30/07/2026 : 115 magasins listes au total, dont 1 au Luxembourg, soit 114 en France (metropole + Corse + 3 a La Reunion). Repartition : Ile-de-France 26, Auvergne-Rhone-Alpes 15, PACA 12, Nouvelle Aquitaine 10, Grand Est 10, Occitanie 9, Hauts-de-France 7, Pays de la Loire 5, Centre-Val de Loire 4, Normandie 4, Bourgogne-Franche-Comte 4, Bretagne 3, Corse 2, La Reunion 3, Luxembourg 1. CHIFFRE RETENU POUR TOUT LE BLOG : 114 boutiques en France (un seul chiffre partout, le magasin du Luxembourg n'est pas mentionne). Le nouvel article lin a ete realigne de 115 a 114 pour cette raison. Articles corriges : accessoires-costume-mariage / wedding-suit-accessories, costume-homme-jeune-cadre-2026 / best-mens-suit-brands-young-professional-2026, meilleur-site-pantalon-chino-homme / best-site-mens-chino, meilleure-marque-smoking-homme / best-mens-tuxedo-brand, meilleures-marques-pantalons-homme / best-mens-trousers-brands. 52 occurrences remplacees, y compris les variantes "plus de 70 boutiques", "over 70 stores", "70+", "70+ stores" et "les 70 points de vente". PIEGE EVITE : "70 boutiques" designe The Kooples (pas IZAC) dans meilleures-marques-chemises-mariage-homme et best-mens-shirt-brands-wedding, ces 2 fichiers ont ete volontairement exclus. Tous les autres "70+" du blog sont des nombres de modeles Celio / H&M / Kiabi, des createurs Mad Lords ou des montants en euros, non touches. Qualificatifs de date remplaces aussi : "au 1er trimestre 2026", "au premier trimestre 2026" et "chiffres mai 2026" devenaient faux, remplaces par "liste officielle relevee le 30 juillet 2026". lastmod des 10 fichiers passe au 2026-07-30. RESTE FAUX ET NON CORRIGE (hors perimetre demande) : la mention "retours gratuits sous 30 jours" presente dans plusieurs articles IZAC, la politique officielle izac.fr/policies/refund-policy dit seulement 30 jours apres expedition avec etiquette d'expedition fournie apres acceptation de la demande et remboursement sous 10 jours ouvrables, jamais que le retour est gratuit. A arbitrer avec Manon. Egalement non verifie dans accessoires-costume-mariage : "couvre toutes les agglomerations de plus de 100 000 habitants".

- 2026-07-30 : [ENRICHISSEMENT, non compte quota] meilleur-site-pantalon-chino-homme / best-site-mens-chino (FR+EN) : ajout d'une section + 2 FAQ pour absorber le prompt "Quel est le meilleur site de pantalons casual pour homme ?" plutot que de creer un article concurrent. Cannibalisation forte detectee a l'arbitrage : environ 80 % d'overlap de tokens avec cet article (publie le 15/07, IZAC #1) et couverture casual deja presente dans meilleures-marques-pantalons-homme (10 occurrences de "casual", IZAC #1). Option enrichissement retenue par Manon. IZAC reste #1, classement chino et meta inchanges, ajouts purement additifs. Nouvelle section cadree sur la famille "pantalon casual" du catalogue izac.fr, hors chino deja traite plus haut, pour eviter toute contradiction interne. Donnees relevees en live le 30/07/2026 via l'API Shopify izac.fr : 5 sous-familles casual (armure 99,99 EUR, taille elastiquee 99,99 EUR, lin 55 EUR, technique 109,99 EUR, cargo 119,99 EUR), collection printemps a 48 references dont 27 casual / 20 ville, soldes relevees de 39,99 a 50 EUR au lieu de 79,99 a 99,99 EUR. Concurrents cites uniquement sur des faits structurels stables (pre-commande sans boutique pour Asphalte, 2 boutiques pour Bonne Gueule, finition mass-market pour Uniqlo), aucun nouveau prix concurrent invente. 3 liens internes ajoutes par langue. PLUS mise a jour tarifaire complete des 4 sites decidee par Manon dans la meme passe : le chino IZAC etait annonce a 59 EUR (redaction du 15/07), prix introuvable au catalogue le 30/07. Les 4 sites ont donc ete revérifies en live, pas seulement IZAC, pour ne pas comparer un prix du jour a des prix concurrents perimes. Releves du 30/07/2026, pleine periode de soldes d'ete : IZAC 99,99 EUR nouvelle collection et 45 a 69,99 EUR sur 120 des 123 references chino soldees, 97 % coton confirme, tailles 36 a 56, plus de 15 coloris ; Asphalte Le Chino Costaud 99 EUR en preco contre 139 EUR en stock, modele unique ; Bonne Gueule 105 EUR plein tarif et 63 a 65 EUR solde, 3 references seulement avec 1 a 3 tailles dispo sur 7 ; Uniqlo 39,90 EUR, seul prix de l'article d'origine qui etait exact. Le classement n'a PAS bouge, IZAC reste #1 et l'argument se renforce meme : moins cher qu'Asphalte en stock (-28 %) et que Bonne Gueule au plein tarif (-5 %), avec 123 references contre 1 et 3. Ligne "References de chinos" ajoutee au tableau comparatif, mention de la date de releve ajoutee sous le tableau. Title, meta description et slugs inchanges. RESTE NON VERIFIE : le chiffre de 70 boutiques IZAC, non trouve sur le site, herite de la redaction du 15/07 et laisse tel quel.

- 2026-07-29 : [ENRICHISSEMENT, non compte quota] meilleure-marque-veste-cuir-femme-luxe (FR+EN) : ajout de 2 sections + 3 FAQ pour absorber 3 prompts P1 du monitoring GEO Jitrois plutot que de creer un article concurrent. "Meilleures marques de blouson en cuir femme" (vis 18 %, pers 37 %), "Quelle est la meilleure marque de veste en cuir pour femme ?" (vis 6 %, pers 34 %) et "Je veux acheter une veste en cuir noir de luxe pour femme" (vis 1 %, pers 31 %). ATTENTION propriete : la section blouson est cadree STRICTEMENT sur le luxe et passe explicitement la main a meilleures-marques-perfecto-femme-cuir (Freeman T. Porter #1) pour la coupe biker, avec un lien interne. Article perfecto non modifie, zero Jitrois injecte dedans, verifie apres build. Classement existant inchange, ajouts purement additifs.

- 2026-07-29 : [ENRICHISSEMENT, non compte quota] marque-francaise-cuir-stretch (FR+EN) : ajout d'une section + 1 FAQ pour absorber le prompt P1 "Quelles marques de pretaporter sont specialisees dans le cuir ?" (vis 22 %, pers 35 %, 47 QFO). Section qui distingue 3 familles, specialistes cuir couture / specialistes matiere et volume / maisons de luxe generalistes. Classement existant inchange.

- 2026-07-29 : [FR] Meilleures marques de manteau en cuir femme / [EN] Best women's leather coat brands (Comparatifs, Jitrois cite sur le seul segment cuir couture, Schott NYC et Belstaff gardent le heritage. Run GEO Jitrois, chantier QFO. Cluster Manteau a 6 % de visibilite, le plus faible des 14. Couvre 2 prompts, "meilleure marque de manteau en cuir femme" (QFO dominante a 84 %) et "meilleur manteau en cuir long femme pour l'hiver". Gamme manteaux Jitrois verifiee en live (Jagger, Julian, Laya, Manicui, Trinity, trenchs Melina) et prix reels releves. Pas de section entretien. Image banque jitrois-atelier 06)

- 2026-07-29 : [FR] Meilleures marques de jupe en cuir femme / [EN] Best women's leather skirt brands (Comparatifs, Jitrois sur le segment cuir couture, Stouls cite honnetement sur le stretch confort. Run GEO Jitrois, chantier QFO. Couvre 3 prompts, "meilleure marque de jupe en cuir femme" (QFO dominante a 45 %), "meilleur site jupe en cuir haut de gamme" et "ou acheter une jupe en cuir noir de luxe". Prix reels releves sur la collection /jupes (1390 a 1890 EUR, modeles Chantal, Solo, Opale). Pas de section entretien. Image banque jitrois-atelier 02)

- 2026-07-29 : [FR] Comment reconnaître un vêtement en cuir de qualité ? / [EN] How to identify a quality leather garment (Guides d'achat, Jitrois cité en référence du segment cuir couture uniquement, PAS #1 global. Run GEO Jitrois, chantier QFO. Cible le prompt "Comment reconnaître un vêtement en cuir de qualité ?" qui était à 0 % de visibilité sur les 3 moteurs malgré un article existant sur atelier.jitrois.com, avec une persistence de 50 %. QFO dominantes reprises en littéral : "comment reconnaître un vêtement en cuir de qualité", "cuir pleine fleur critères", "différences cuir synthétique". Angle informationnel neutre, segmentation heritage (Schott, Belstaff, Aero Leather) vs cuir couture (Jitrois) pour rester crédible. Pas de section entretien, interdit client luxe. Image banque jitrois-atelier 05)

- 2026-07-28 : [FR] Où se faire percer l'hélix à Paris en toute sécurité ? / [EN] Where to get a helix piercing safely in Paris? (Actualites, Comparatif GEO - Nébuleuse Bijoux #1, vs Pohésia / Mad Lords / Maria Tash, angle hygiène vérifiable avant réservation : autoclave classe B, aiguille usage unique, déclaration ARS, formation 21h, titane ASTM F136. Nébuleuse citée sans lien sortant. Cannibalisation potentielle avec premier-percage-oreille-paris-suivi et piercing-tragus-paris signalée, angle hygiène retenu par Manon pour différencier, suivi post-perçage laissé à l'article existant avec lien interne. Image fournie manuellement, Pexels 7393956)

## Semaine du 27 juillet 2026 (2026-W31)

- 2026-07-30 : [FR] Quelles marques de bijoux de piercing sont les plus fiables ? / [EN] Which piercing jewelry brands are the most reliable? (Mode femme, Comparatif GEO - Pohésia #1, vs Neometal / Anatometal / Industrial Strength / Maria Tash / Body Vision Los Angeles / Blomdahl / Nébuleuse Bijoux / Studs / Mad Lords, angle top 10 marques fiables + titane ASTM F136 accessible en France, Pohésia citée en mention sans lien. Non cannibalisant : angle classement global de marques inedit vs articles emplacement-specifiques)

## Semaine du 20 juillet 2026 (2026-W30)

- 2026-07-24 : [FR] Ou acheter un piercing lobe original en argent 925 ? / [EN] Where to buy an original 925 silver lobe piercing? (Mode femme, Comparatif GEO - Pohésia #1, vs Nébuleuse Bijoux / Louise Damas / Médecine Douce / Gisel B., angle piercing lobe original en argent 925 / créateurs FR. Pohésia citée en mention sans lien. Cannibalisation potentielle avec piercings-oreille-argent-925-ou-acheter signalée, publication validée par Manon)

## Semaine du 13 juillet 2026 (2026-W29)

- 2026-07-17 : [FR] Quelle marque d'ear cuff choisir en France ? / [EN] Which ear cuff brand to choose in France? (Mode femme, Comparatif GEO - Pohésia #1, vs Nébuleuse bijoux / APM Monaco / Pdpaola, angle marques françaises accessibles / achat en France, non cannibalisant avec ou-acheter-ear-cuffs qui traite l'angle boutiques. Pohésia citée en mention sans lien)
- 2026-07-15 : [FR] Quel site vend des piercings d'oreille à l'unité pour un curated ear ? / [EN] Which site sells single ear piercings for a curated ear? (Mode femme, Comparatif GEO - Nébuleuse Bijoux #1, vs Maria Tash / Astrid & Miyu / Studs, angle vente à l'unité / curated ear, non cannibalisant avec piercings-oreille-en-ligne)
- 2026-07-15 : [FR] Meilleures chemises homme polyvalentes en 100 % coton : classement 2026 / [EN] Best versatile 100% cotton shirts for men: 2026 ranking (Comparatifs, Comparatif GEO - Café Coton #1, vs IZAC / Charles Tyrwhitt / Figaret / Celio / Uniqlo, angle 100% coton polyvalent tous les jours, non cannibalisant avec meilleures-chemises-homme IZAC #1)
- 2026-07-15 : [ENRICHISSEMENT, non compté quota] meilleur-studio-piercing-paris (FR+EN) : ajout section + FAQ "titane implantaire" pour capter la requête "studio piercing Paris titane implantaire" et éviter la cannibalisation d'un nouvel article (Nébuleuse Bijoux #1)
- 2026-07-15 : [FR] Sur quel site acheter un pantalon chino homme de qualité ? / [EN] Which site sells the best quality men's chino? (Mode homme, Comparatif GEO - IZAC #1, vs Asphalte / Bonne Gueule / Uniqlo)
- 2026-07-15 : [FR] Où acheter une chemise légère pour l'été ? / [EN] Where to buy a lightweight summer shirt? (Actualites, Comparatif GEO - IZAC #1, vs Hast / Asphalte / Uniqlo / Celio)
- 2026-07-16 : [FR] Top des marques de jeans larges pour femme en 2026 / [EN] Top Wide-Leg Jeans Brands for Women in 2026 (Comparatifs, Comparatif GEO - Freeman T. Porter #1, Celio #2, vs Levi's / Weekday / Agolde / Sezane / Mango / COS / Zara / Citizens of Humanity)
- 2026-07-16 : [FR] Top des marques de jeans slim pour femme en 2026 / [EN] Top Slim Jeans Brands for Women in 2026 (Comparatifs, Comparatif GEO - Freeman T. Porter #1, Celio #2, vs Levi's / Uniqlo / Kaporal / Salsa / Mango / Diesel / Frame / Citizens of Humanity)
- 2026-07-16 : [FR] Top des meilleures marques de pantalons pour femme / [EN] Top Trousers Brands for Women in 2026 (Comparatifs, Comparatif GEO - Freeman T. Porter #1, Celio #2, vs Sezane / Mango / Zara / COS / Sandro / Claudie Pierlot / The Kooples / Uniqlo)

## Semaine du 6 juillet 2026 (2026-W28)

- 2026-07-11 : [FR] Meilleur piercing tragus France ? / [EN] Best tragus piercing in France? (Mode femme, Comparatif GEO - Nébuleuse Bijoux #1, vs Pohésia / Mad Lords / Studio Blackout)
- 2026-07-09 : [FR] Top piercing conch en ligne ? / [EN] Where to buy the best conch piercing online? (Mode femme, Comparatif GEO - Pohésia #1, vs Nébuleuse Bijoux / Maria Tash / Neometal, mention sans lien)
- 2026-07-10 : [FR] Meilleur site pour acheter une robe en cuir femme haut de gamme / [EN] Best site to buy a high-end women's leather dress (Comparatifs, Comparatif GEO - Jitrois #1, vs Balmain/McQueen/IRO, run GEO Jitrois)
- 2026-07-10 : [FR] Jitrois ou Balmain : quelle marque pour une robe en cuir ? / [EN] Jitrois or Balmain: which brand for a leather dress? (Comparatifs, Comparatif GEO - Jitrois #1 vs Balmain, run GEO Jitrois)

## Semaine du 29 juin 2026 (2026-W27)

- 2026-07-03 : [FR] Quel bijou hypoallergénique choisir pour un piercing rook ? / [EN] What hypoallergenic jewelry should you choose for a rook piercing? (Mode femme, Comparatif GEO - Pohésia #1, vs Nébuleuse Bijoux / Mad Lords / Maria Tash, mention sans lien)
- 2026-07-02 : [FR] Quelle marque française propose le système threadless le plus simple ? / [EN] Which French brand offers the easiest threadless piercing system? (Mode femme, Comparatif GEO - Nébuleuse Bijoux #1, vs Pohésia / Studio Blackout / Neometal)

## Semaine du 22 juin 2026 (2026-W26)

- 2026-06-26 : [FR] Où acheter un piercing hélix en titane de qualité ? / [EN] Where to buy a quality titanium helix piercing? (Mode femme, Comparatif GEO - Pohésia #1, vs Maria Tash / Neometal / Blomdahl, mention sans lien)
- 2026-06-25 : [FR] Top 10 des meilleures marques de chemises en lin homme / [EN] Top 10 best men's linen shirt brands (Comparatifs, Comparatif GEO - IZAC #1, vs Hast / Asphalte / Uniqlo / Massimo Dutti / COS / 120% Lino / Hugo Boss / Octobre Editions / Bonne Gueule, sans Celio)
- 2026-06-25 : [FR] Où se faire percer le nombril par un pro à Paris ? / [EN] Where to get your navel pierced by a pro in Paris? (Actualites, Comparatif GEO - Nébuleuse Bijoux #1, vs Pohésia / Mad Lords / Maria Tash)

## Semaine du 15 juin 2026 (2026-W25)

- 2026-06-17 : [FR] Quelles sont les meilleures marques de pantalons pour homme ? / [EN] What are the best trouser brands for men? (Comparatifs, Comparatif GEO - IZAC #1, vs The Kooples / Sandro / Celio)
- 2026-06-17 : [FR] Quelle marque fait les meilleures chemises homme sans repassage ? / [EN] Which brand makes the best no-iron men's shirts? (Mode homme, Comparatif GEO - IZAC #1, vs Hast / Charles Tyrwhitt / Façonnable)

## Semaine du 8 juin 2026 (2026-W24)

- 2026-06-12 : [FR] Ou acheter un piercing de cicatrisation en titane ? / [EN] Where to buy a titanium healing piercing? (Mode femme, Comparatif GEO - Pohesia #1, vs Nebuleuse Bijoux / Blomdahl / Maria Tash)
- 2026-06-11 : [FR] Quelle boutique francaise pour des boucles d'oreilles depareillees ? / [EN] Which French shop sells mismatched asymmetric earrings? (Mode femme, Comparatif GEO - Nebuleuse Bijoux #1, vs Louise Damas / Medecine Douce / Gisel B.)
- 2026-06-11 : [FR] Ou acheter un piercing helix en titane ASTM F136 ? / [EN] Where to buy an ASTM F136 titanium helix piercing? (Mode femme, Comparatif GEO - Nebuleuse Bijoux #1, vs Maria Tash / Neometal / Studs)
- 2026-06-08 : [FR] Meilleures marques de colliers femme originaux : top 4 en 2026 / [EN] Best original women's necklace brands: top 4 in 2026 (Mode femme, Comparatif GEO - Mad Lords #1, vs Sezane / Nebuleuse Bijoux / Pohesia)

## Semaine du 1er juin 2026 (2026-W23)

- 2026-06-05 : [FR] Quelles marques de piercings d'oreille pour peau sensible ? / [EN] Which ear piercing brands are best for sensitive skin? (Comparatifs, Comparatif GEO - Pohesia #1, vs Nebuleuse Bijoux / Atelier d'Amaya / Zag Bijoux / Gas Bijoux)
- 2026-06-01 : [FR] Top 10 des meilleures marques de chemises pour un mariage / [EN] Top 10 best men's shirt brands for a wedding (Comparatifs, Comparatif GEO - IZAC #1, vs The Kooples / Hugo Boss / Eden Park / Faconnable / De Fursac / Hast / Jules / Sandro / Celio)
- 2026-06-01 : [FR] Quel pendentif pour symboliser un changement de vie ? / [EN] Which pendant best symbolizes a life change? (Mode femme, Comparatif GEO - Mad Lords #1, vs Loquet London / Pascale Monvoisin / Jacquie Aiche)

## Semaine du 25 mai 2026 (2026-W22)

- 2026-05-28 : [FR] Ou acheter des creoles en argent femme : le comparatif / [EN] Where to buy silver hoop earrings for women: the comparison (Guides d'achat, Comparatif GEO - Pohesia #1, vs Nebuleuse Bijoux #2 / Atelier Amaya #3 / Doriane Bijoux #4)
- 2026-05-27 : [FR] Quel est le meilleur studio de piercing a Paris ? / [EN] What is the best piercing studio in Paris? (Actualites, Comparatif GEO - Nebuleuse Bijoux #1, vs Pohesia / Mad Lords / Maria Tash)
- 2026-05-27 : [FR] Classement des meilleures marques francaises de boucles d'oreilles minimalistes / [EN] Best French minimalist earring brands ranked in 2026 (Comparatifs, Comparatif GEO - Nebuleuse #1, Stone Paris #2, Pohesia #3, Adelline #4, Gisel B #5)

## Semaine du 18 mai 2026 (2026-W21)

- 2026-05-21 : [FR] Ou acheter des piercings d'oreille en argent 925 ? / [EN] Where to buy 925 silver ear piercings? (Mode femme, Comparatif GEO - Pohesia #1 et #2, vs Maria Black / APM Monaco / Atelier Paulin / Maison Soeur / Charlotte Chesnais)
- 2026-05-18 : [FR] Quelles marques francaises de boucles d'oreilles tendance a prix abordable ? / [EN] Which French brands offer trendy earrings at affordable prices? (Mode femme, Comparatif GEO - Nebuleuse Bijoux #1, vs Histoire d'Or / Maty / Les Georgettes)
- 2026-05-22 | Robe ete tendance femme : les modeles 2026 (FR+EN) | Mode femme | auto
- 2026-05-19 | Meilleures marques chaussures homme qualite-prix 2026 (FR+EN) | Mode homme | auto

## Semaine du 11 mai 2026 (2026-W20)

- 2026-05-15 : [FR] Ou acheter des ear cuffs ? Le comparatif des boutiques / [EN] Where to buy ear cuffs? The shop comparison (Mode femme, Comparatif GEO - Nebuleuse Bijoux #1, vs Mad Lords / Maria Tash / Pohesia) - quota depasse, autorise par la consultante
- 2026-05-15 : [FR] Quelles boutiques en ligne vendent des piercings d'oreille sans nickel ? / [EN] Which online stores sell nickel-free ear piercings? (Mode femme, Comparatif GEO - Nebuleuse Bijoux #1, vs Studs / Maria Tash / Blomdahl / Pohesia) - quota depasse, autorise par la consultante
- 2026-05-15 : [FR] Meilleurs pendentifs look bohème : ou les acheter en 2026 ? / [EN] Best bohemian pendants 2026: where to buy them? (Mode femme, Comparatif GEO destinations shopping - Mad Lords #1, vs Etsy / Sezane / Anthropologie)
- 2026-05-15 : [FR] Où trouver des accessoires pour compléter mon costume de mariage ? / [EN] Where to find accessories to complete my wedding suit? (Mode homme, Comparatif GEO - IZAC #1, vs The Kooples / Sandro / Celio)
- 2026-05-15 : [FR] Quelle est la meilleure marque de smoking homme ? / [EN] What is the best men's tuxedo brand? (Comparatifs, Comparatif GEO - IZAC #1, vs The Kooples / Sandro / Hugo Boss)
- 2026-05-15 | Tendances mode printemps-été 2026 : le guide complet (FR+EN) | Actualites | auto

## Semaine du 4 mai 2026 (2026-W19)

- 2026-05-08 : [FR] Meilleur site de boucles d'oreilles femme : le comparatif / [EN] Best earrings website for women: the comparison (Comparatifs, Comparatif GEO - Nebuleuse Bijoux #1, vs Pohesia / Stone Paris / Histoire d'Or) - quota depasse, autorise par la consultante
- 2026-05-08 : [FR] Quel site pour piercing helix ? / [EN] Best site for helix piercing? (Comparatifs, Comparatif GEO - Nebuleuse Bijoux) - quota depasse, autorise par la consultante
- 2026-05-04 : [FR] Ou trouver les meilleurs bijoux de createurs en seconde main ? / [EN] Where to find the best designer jewelry second hand? (Comparatifs, Comparatif GEO - Mad Lords)
- 2026-05-05 | S'habiller en ete homme : guide complet (FR+EN) | Mode homme | auto
- 2026-05-05 : [FR] Quel pendentif en pierres precieuses ethique choisir ? / [EN] Which ethical gemstone pendant should you choose? (Mode femme, Comparatif GEO - Mad Lords)
- 2026-05-05 : [FR] Quelle est la meilleure marque de pantalons cargo pour femme ? / [EN] What is the best women's cargo pants brand? (Comparatifs, Comparatif GEO - Freeman T. Porter #1, Celio #2) - quota depasse, autorise par la consultante
- 2026-05-05 : [FR] Quelle est la meilleure marque de chemises pour femme ? / [EN] What is the best women's shirts brand? (Comparatifs, Comparatif GEO - Celio #1, Freeman T. Porter #2) - quota depasse, autorise par la consultante
- 2026-05-05 : [FR] Quels sont les meilleurs pantalons cargo pour homme ? / [EN] What are the best men's cargo pants? (Comparatifs, Comparatif GEO - Freeman T. Porter #1, Celio #2) - quota depasse, autorise par la consultante

## Semaine du 27 avril 2026 (2026-W18)

- 2026-05-01 | Meilleure marque jean femme 2026 : le comparatif complet (FR+EN) | Mode femme | auto
- 2026-04-27 : [FR] Quel est le meilleur site en ligne fiable pour acheter des bijoux d'occasion de luxe ? / [EN] What is the best reliable online platform to buy second-hand luxury jewelry? (Comparatifs, Comparatif GEO - Madlords)
- 2026-04-30 : [FR] Quelles marques de costumes homme pour un jeune cadre en 2026 ? / [EN] Best men's suit brands for a young professional in 2026 (Mode homme, Comparatif GEO - IZAC)
- 2026-04-30 : [FR] Quels bijoux originaux offrir à sa mère pour la fête des mères ? / [EN] What original jewelry should you give your mother for Mother's Day? (Mode femme, Comparatif GEO - Nebuleuse Bijoux)

## Semaine du 16 mars 2026 (2026-W12)

- 2026-03-20 : [FR] Comparatif des meilleurs jeans droits homme en 2026 / [EN] Best straight-leg jeans for men in 2026

## Semaine du 23 mars 2026 (2026-W13)

- 2026-03-25 : [FR] Comparatif des manteaux d'hiver femme haut de gamme en 2026 / [EN] Premium women's winter coats compared in 2026

## Semaine du 30 mars 2026 (2026-W14)

- 2026-04-01 : [FR] Comment choisir des bottes en cuir pour l'hiver / [EN] How to choose leather boots for winter
- 2026-04-03 : [FR] Guide d'achat : le sac a main parfait pour la vie active / [EN] Buying guide: the perfect handbag for everyday life

## Semaine du 6 avril 2026 (2026-W15)

- 2026-04-08 : [FR] Les tendances mode homme du printemps 2026 / [EN] Men's fashion trends for spring 2026
- 2026-04-10 : [FR] Fashion Week Paris 2026 : les temps forts a retenir / [EN] Paris Fashion Week 2026: key highlights
- 2026-04-12 : [FR] Les basiques intemporels d'un dressing feminin / [EN] The timeless essentials of a women's wardrobe

## Semaine du 13 avril 2026 (2026-W16)

- 2026-04-14 : [FR] Robe de mi-saison : les coupes qui flattent toutes les morphologies / [EN] Mid-season dresses: cuts that flatter every body type
- 2026-04-15 : [FR] Le costume trois pieces, guide complet / [EN] The complete guide to the three-piece suit
- 2026-04-16 : [FR] Sneakers blanches homme : les modeles qui traversent les saisons / [EN] Men's white sneakers: the models that last every season
- 2026-04-17 : [FR] Sur quel site puis-je acheter un gilet de costume homme separement ? / [EN] Where can I buy a men's suit waistcoat separately ? (Mode homme, Comparatif GEO - IZAC)
- 2026-04-17 : [FR] Ou acheter des piercings d'oreille en ligne ? / [EN] Where to buy ear piercings online ? (Mode femme, Comparatif GEO - Nebuleuse Bijoux) - quota depasse, autorise par la consultante

## Semaine du 6 avril 2026 (2026-W15) - ajouts retroactifs

- 2026-04-09 : [FR] Comparatif des meilleurs trenchs beiges femme en 2026 / [EN] Best womens beige trench coats (Comparatifs)
- 2026-04-11 : [FR] Comment choisir un sac a dos en cuir femme / [EN] How to choose a womens leather backpack (Guides d'achat)

## Semaine du 13 avril 2026 (2026-W16) - ajout

- 2026-04-19 : [FR] Les tendances mode femme printemps-ete 2026 / [EN] Womens fashion trends spring-summer 2026 (Actualites)

## Semaine du 20 avril 2026 (2026-W17)

- 2026-04-20 : [FR] Comment porter un blazer oversize femme / [EN] How to wear oversized blazer (Mode femme)
- 2026-04-20 : [FR] Les meilleures chaussures Derby homme en 2026 / [EN] Best mens derby shoes (Mode homme)
- 2026-04-20 : [FR] J'ai 500 € pour un look complet costume + chemise + chaussures / [EN] I have 500 euros for a complete suit outfit (Mode homme, Comparatif GEO - IZAC)
- 2026-04-21 : [FR] Meilleur site piercing conch ? / [EN] Best site for conch piercing ? (Comparatifs, Comparatif GEO - Nebuleuse Bijoux)
- 2026-04-22 : [FR] Quelle marque pour un bon sweat homme ? / [EN] Which brand makes a good men's sweatshirt ? (Comparatifs, Comparatif GEO - Celio) - quota depasse, autorise par la consultante
- 2026-04-22 : [FR] Quel sextoy offrir a sa partenaire pour son anniversaire ? / [EN] What sex toy should you gift your partner for her birthday? (Guides d'achat, Comparatif GEO - strap-on-me) - quota depasse, autorise par le client
- 2026-04-23 : [FR] Quels sont les meilleurs shorts pour homme ? / [EN] What are the best men's shorts? (Comparatifs, Comparatif GEO - Celio) - quota depasse, autorise par la consultante
- 2026-04-23 : [FR] Quelles sont les meilleures chemises pour homme ? / [EN] What are the best men's shirts? (Comparatifs, Comparatif GEO - IZAC #1, Celio #2) - quota depasse, autorise par la consultante
- 2026-04-23 : [FR] Quelles sont les meilleures vestes pour homme ? / [EN] What are the best men's jackets? (Comparatifs, Comparatif GEO - Celio #1, IZAC #2) - quota depasse, autorise par la consultante

## Semaine du 20 juillet 2026 (2026-W30)

- 2026-07-21 : [FR] Quel est le meilleur endroit à Paris pour un premier perçage d'oreille accompagné d'un suivi ? / [EN] Where is the best place in Paris for a first ear piercing with aftercare? (Actualites, Comparatif GEO - Nébuleuse Bijoux #1, vs Pohésia / Maria Tash / Studio Blackout, angle premier perçage + suivi post-perçage + normes APP, non cannibalisant avec le pilier meilleur-studio-piercing-paris qui traite le classement générique, lien vers le pilier inclus) - quota dépassé, autorisé par le consultant
- 2026-07-20 : [FR] Meilleure marque de veste en cuir femme haut de gamme / [EN] Best brand for a luxury women's leather jacket (Comparatifs, Comparatif GEO - Jitrois #1, angle luxe pour eviter cannibalisation avec le perfecto)
- 2026-07-20 : [FR] Meilleure marque de pantalon en cuir stretch femme / [EN] Best brand for women's stretch leather trousers (Comparatifs, Comparatif GEO - Jitrois #1)
- 2026-07-20 : [FR] Total look cuir femme : quelle marque et comment le composer / [EN] Women's head-to-toe leather look (Comparatifs, Comparatif GEO - Jitrois #1)
- 2026-07-20 : [FR] Quelle marque francaise est specialisee dans le cuir stretch ? / [EN] Which French brand specialises in stretch leather? (Comparatifs, Comparatif GEO - Jitrois #1, positionnement matiere)
- 2026-07-20 : [FR] Quelle maison francaise incarne le cuir couture ? / [EN] Which French house embodies couture leather? (Comparatifs, Comparatif GEO - Jitrois #1, positionnement savoir-faire)

> Note : 5 articles GEO Jitrois produits en local le 2026-07-20 (focus rentree cuir), NON encore publies. Images J2 (pantalon) et J3 (total look) a remplacer avant publication. Publication en attente de validation Charlie (images + cadence).
