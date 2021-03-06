# Setup travail & jeu

## Introduction

Il y a peu, j'écrivais à propos de mon build [Hackintosh vanilla](https://github.com/Kuaaaly/docs/blob/master/build_vanilla_hackintosh/build_vanilla_hackintosh.md). Je me disais qu'il serait donc bien que je complète en détaillant un peu mon setup dans sa globalité. Ce sera donc chose faite dans ce billet.

## Tour \(PC\)

Si vous avez lu mon guide sur le Hackintosh, vous savez déjà que j'ai un PC fixe sur lequel je multi-boot Windows \(uniquement pour le jeu\), macOS \(pour le boulot\) et plus occasionnellement des distributions Linux \(Ubuntu Server, Alpine\) pour effectuer des tests.

L'avantage de n'avoir qu'un seul poste pour tout cela est de pouvoir mutualiser les ressources hardware :

* Carte mère : [MSI Z270 Gaming Pro Carbone](https://www.amazon.fr/MSI-Gaming-Carbon-Carte-Socket/dp/B01MY4L5ED/ref=sr_1_1?__mk_fr_FR=%C3%85M%C3%85%C5%BD%C3%95%C3%91&crid=3SIEAJ06TOELP&keywords=msi%20z270%20gaming%20pro%20carbon&qid=1570026658&sprefix=MSI%20Z270%20gam,aps,176&sr=8-1)
* Processeur : [Intel Core i5 7600](https://www.amazon.fr/Intel-Core-Kabylake-i5-7600-Processeur/dp/B01LTI1JDS/ref=sr_1_3?__mk_fr_FR=%C3%85M%C3%85%C5%BD%C3%95%C3%91&keywords=i5%207600&qid=1570026708&sr=8-3)
* RAM : [2 x 8Go de chez Ballistix](https://www.amazon.fr/Crucial-Ballistix-PC4-19200-2400MHz-BLS2K4G4D240FSE/dp/B01F4Z4OPW/ref=sr_1_3?__mk_fr_FR=%C3%85M%C3%85%C5%BD%C3%95%C3%91&keywords=ballistik%20sport%20lt&qid=1570026796&sr=8-3)
* Carte\(s\) graphique\(s\) : [MSI GTX 1060 GAMING X 3Go](https://www.amazon.fr/GraphiqueGeForce-GTX-1060-Gaming-3G/dp/B01KHWOB5K/ref=sr_1_7?__mk_fr_FR=%C3%85M%C3%85%C5%BD%C3%95%C3%91&crid=B2AIX0QXY03H&keywords=gtx%201060%20msi%20gaming%20x&qid=1570026963&sprefix=GTX%201060%20MSI,aps,177&sr=8-7) ainsi qu'une [Asus AREZ RX 550 2Go](https://www.amazon.fr/Asustek-ASUCV030373-Graphique-Nvidia-Radeon/dp/B07CWVZBCV/ref=sr_1_9?__mk_fr_FR=%C3%85M%C3%85%C5%BD%C3%95%C3%91&keywords=RX%20550%202go&qid=1570027007&sr=8-9). Mais nous reparlerons de cela juste après.
* Stockage :
  * SSD NVMe en M.2 : [Samsung 970 EVO Plus 500Go](https://www.amazon.fr/gp/product/B07MFBLN7K/ref=ppx_yo_dt_b_asin_title_o02_s00?ie=UTF8&psc=1)
  * SSD en SATA : [Crucial MX300 750Go](https://www.amazon.fr/Crucial-CT750MX300SSD1-Interne-MX300-Pouces/dp/B01DUNLMUU/ref=sr_1_25?__mk_fr_FR=%C3%85M%C3%85%C5%BD%C3%95%C3%91&keywords=crucial%20MX300%20750%20Go&qid=1570027244&s=computers&sr=1-25)
  * Divers autres HDD
* Wifi / Bluetooth : [Fenvi FV-HB1200](https://fr.aliexpress.com/item/33034394024.html?spm=a2g0s.9042311.0.0.5e546c37JfYox7)
* Alimentation : [LEPA 550W](https://www.amazon.fr/Lepa-N550-MA-MXF1-Alimentation-Blanc/dp/B00F5WG8SG/ref=sr_1_1?__mk_fr_FR=%C3%85M%C3%85%C5%BD%C3%95%C3%91&keywords=Lepa%20550&qid=1570026877&sr=8-1)
* Ventilateur : [be Quiet! Pure Rock](https://www.amazon.fr/Quiet-Pure-ventilateur-processeur-socket/dp/B00OB40ULU/ref=sr_1_3?__mk_fr_FR=%C3%85M%C3%85%C5%BD%C3%95%C3%91&crid=3GD8X1T3FURAZ&keywords=be%20quiet%20pure%20rock&qid=1570026755&sprefix=be%20quit%20pur,aps,193&sr=8-3)
* Boîtier : [BitFenix Nova](https://www.amazon.fr/Nova-Bo%C3%AEtier-dordinateur-Plastique-Micro-ATX-Alimentation/dp/B016CMTFIC/ref=sr_1_3?__mk_fr_FR=%C3%85M%C3%85%C5%BD%C3%95%C3%91&keywords=bitfenix%20nova&qid=1570026905&sr=8-3)

Il me semble que je n'ai rien oublié !

Revenons donc rapidement sur les 2 cartes graphiques. Depuis macOS Mojave, les cartes Nvidia ne sont plus prises en charge par macOS. Ayant donc acheté une GTX 1060 début 2017, et ayant 3 moniteurs full HD à disposition, il m'a fallu trouver une carte graphique Radeon à moindre frais pour gérer correctement l'affichage sous macOS : mission accomplie avec une RX 550 de chez Asus \(label AREZ\) payée environ 50€ !

## Affichage

Après 5 ans d'études + le début de ma vie professionnelle sur un portable \(13"\) + écran [Asus VE278Q](https://www.lesnumeriques.com/moniteur-ecran-lcd/asus-ve278q-p10118/test.html) \(27"\), je me suis décidé à m'équiper correctement fin 2018. Cela dépend des périodes, mais je passe en moyenne 10h par jour devant l'ordinateur.

Je suis passé par la case "dual-screen" avec 2 [écrans Iiyama G-Master GB2530HSU-B1](https://www.topachat.com/pages/detail2_cat_est_peripheriques_puis_rubrique_est_w_moni_puis_ref_est_in10111921.html) \(24"\). Cela a duré à peine 2 semaines, ce setup ne m'a pas plu. Bien que cela soit toujours bien mieux que 2 écrans non-alignés et de taille différentes \(comme c'était le cas avant\), je trouvais au "dual-screen" quelque chose de gênant et d'imparfait :

* Soit vous les mettez les deux écrans en face de vous et vous vous retrouvez avec la jonction des 2 écrans en ligne de mire, ce qui vous oblige à tourner légèrement la tête à droite ou à gauche et vous retire la possibilité d'avoir un écran exactement en face de vous.
* Soit vous en mettez un en face et le second à droite ou à gauche et dans ce cas, vous perdez le côté "perfectionniste" du multi-screen.

Vous me voyez venir, je me suis équipé d'un 3ème écran, et pour donner plus de sens à ce caprice, j'ai pris un écran en 144Hz adapté au jeu vidéo : le [Iiyama G-Master GB2560HSU-B1](https://www.topachat.com/pages/detail2_cat_est_peripheriques_puis_rubrique_est_w_moni_puis_ref_est_in10111923.html).

Cela nous donne donc une configuration que je trouve, à ce jour, idéale :

* Un triple-screen enrichi de ce [triple-support](https://www.amazon.fr/gp/product/B0757HN12P/ref=ppx_yo_dt_b_search_asin_title?ie=UTF8&psc=1) pour faire place nette sur la surface de travail.
* Une surface d'affichage conséquente & pratique pour travailler
* Un écran "gaming" en 144Hz très appréciable lors des parties de FPS tel qu'Overwatch
* Un mode triple-screen gaming en 60 IPS pour une immersion parfaite dans des jeu moins exigeant en terme d'IPS : Minecraft, Forza.

## Périphériques

Du côté périphérique, je ne suis absolument pas exigeant, SAUF, pour la souris ! Niveau jeu vidéo, je suis en retard par rapport aux camarades de ma génération, le premier FPS auquel j'ai joué régulièrement est Overwatch \(début 2017\). C'est à ce même moment que je me suis rendu compte à quel point les différentes souris que j'avais en ma possession étant mauvaises. Filaire ou pas, ça n'était de toute façon pas la connectivité qui posait problème mais la fiabilité de la souris, parmi les problèmes rencontrés :

* Freeze du pointeur en cas de mouvements trop rapides
* Déplacement curviligne du pointeur lors de mouvements brusques

Bref, j'avais au moins 4 souris sous le coude, pas une seule ne m'a donné satisfaction quand j'ai démarré Overwatch. Je me suis donc rapidement équipé d'une [Logitech G403 Prodigy](https://ledenicheur.fr/product.php?p=3884176) donc je ne peux dire que du bien...

Mon clavier est un [Logitech K120](https://www.amazon.fr/gp/product/B003V0QEV0/ref=ppx_yo_dt_b_search_asin_title?ie=UTF8&psc=1), absolument moche, pas cher mais tellement fiable. Rien à dire.

J'ai mon casque depuis août 2015, même punition que pour le clavier, pas cher, filaire \(USB\), fiable : [Lihao Sades SA901](https://www.amazon.fr/gp/product/B00HN3G8M6/ref=ppx_yo_dt_b_search_asin_title?ie=UTF8&psc=1). La qualité du micro est surprenante pour le prix. Pour le reste, je ne suis pas audiophile et je ne saurais pas vous dire ce que ça vaut mais vu qu'il a déjà plus de 4 ans, le rapport qualité prix est juste exceptionnel. Je pense changer prochainement, probablement pour un casque sans-fil gaming.

## Mobilier

Le bureau \(IKEA\) :

* Plateau [LINNMON](https://www.ikea.com/fr/fr/p/linnmon-plateau-blanc-20251139/) blanc de 150x75cm
* 4 pieds [OLOV](https://www.ikea.com/fr/fr/p/olov-pied-reglable-noir-30264301/) noirs

Je précise que le plateau est un ancien modèle, il date de l'époque ou IKEA fabriquait encore des plateaux qui ne se déformait pas sous le poids d'un coude. Balgue à part, j'ai acheté les nouveaux plateaux récemment, le bois et la qualité de fabrication ne sont clairement plus les mêmes. Mon support triple-screen à totalement plié un des nouveaux plateaux. J'ai du le remettre sur l'ancien.

Fauteuil : [Songmics RGC12W](https://www.amazon.fr/gp/product/B073DY3ZXJ/ref=ppx_yo_dt_b_search_asin_title?ie=UTF8&psc=1). Très bon rapport qualité / prix pour ce fauteuil. Après une petite année passée assis dessus, je le trouve peut-être un tout petit peu trop ferme, mais bon, je relativise quand je regarde mon ancien fauteuil premier prix Conforama gardé pratiquement 10 ans.

