# Lumivelo 2020

Montréal, vendredi 5 juin

But: Les dispositifs doivent fonctionner beau temps/mauvais temps, qu'il fait
froid où qu'il y ait de la pluie, tout doit opérationnel et agréable à
utiliser. [Strech] Pour un utilisation au délà du tours la nuit, aussi
considérer le cas d'utilisation en saison hivernale.

But: On veux maximiser l'impact du "Wow! factor" pour l'ensemble des
participant et les spectateur du tour la nuit. On veut
minimiser les irritants pour les participants de notre groupe.

## Idées par fonctions et/ou sous-projet

- 0. Thématique
- 1. Chandail
- 2. Décoration de casque
- 3. Gestion de l'énergie (sous-Projet)
- 4. Mesure de l'effort (sous-projet)
- 5. Demi-sphère en acrylique
- 6. Ampli audio (sous-projet demi-sphere)
- 7. Mat avec avatar/mascote
- 8. Projection au sol
- 9. Identification des positions relatives
- 10. Tesla Coil (sous-projet du mat)
- 11. Peinture fluorescente
- 12. Identification du trajet
- 13. Lumière dans la roue
- 14. Lumières aux extrémités des poignées
- 15. Affichage de message
- 16. Editeur d'effets lumineux LEDs
- 17. Communication entre les cyclistes
- 18. Collecte des données (télémétrie) (sous-projet)
- 19. Lentille fresnelle dans le triangle du vélo
- 20. Recouvrir les côtés des roues
- 21. Ballon gonflé à l'helium
- 22. Identifier le groupe Lumivélo
- 23. Boule disco
- 24. Feu d'artifice
- 25. Ligne vertical vs image 2D
- 26. Acrylique gravée au laser

- 99. Interactions avec/entre modules
  - A. Interrupteur mécanique d'alimentatoin (ON/OFF)
  - B. Reed switch (avec aiment)
  - C. Porte clef RF de voiture
  - D. Carte/Jeton RFID
  - E. Touch sensor
  - F. Télécommand IR
  - G. Communication entre les vélos de la flotte
  - H. Interface sur appareil mobile

# 0. Thématique

Mes filles ont proposé l'espace comme thématique.

Nos avatars au dessus des vélos pourrait être des planètes, la lune, des étoiles et une ou des fusés parmis ce décor.

Proposition de lumière blanche et bleuté scintillante pour reproduire le ciel étoilé.

Décorer les casques de vélo pour donner l'impression d'un casque d'astronaute.

La demi-sphère en acrylique pourrait servir pour afficher une planète qui toune en utilisant la technique de persistance de la vision (POV).

# 1. Chandail

Il faut tenir compte des éventuels manteaux, imperméables. De plus, Il ne faut pas oublier la présence du dossard officiel du Tour-la-nuit.

En utilisatant comme roue de vélo chacun des 0 dans 2020 on peut former un logo intéressant. Une symétrie avec le double cercle des lunettes du logo papas inventeurs est même possible.

Pour l'ajout de lumière sur le chandail considére l'utilisation de EL-WIRE. On peut les coudre.

Un zone blanche ou mirroir sur le tissu pourrait être utilisé comme surface de projection.

Faire participer les enfants pour créer le texte et le image à apposer sur le
chandail ou encore l'indentification des lignes a faire avec EL-Wire.

## 2. Decoration de casque

On peut utiliser les petites piles LiPo ou encore un ensemble 25550, pour alimenter un petit montage LED avec un petit mcu. Il pourrait être amusant de faire changer la couleur des casques avec les manettes (IR).

# 3. Gestion de l'énergie

Mesure de la consommation de l'énergie en fonction:
- De l'intensité des LED, du nombre des LED, de la couleur des LED
- De l'amplification audio
- De l'échange données UltraSon
- De la consommation bluetooth.

- Utilisation des pile LiPo pour une meilleur ratio poids/energie
- Module électronique de protextion contre la décharge à zéro (utile pour pile aux plomb aussi).
- Chargeurs: Confection d'un dispositif qui peut charger l'ensemble de toutes les piles simultanément. Consultation des logs des courbes de charge. Identification des piles au branchement.
- Pile interchangeable entre les modules lumivélo possible ? 6v, 12v, 14v, 20v, etc.
- Caractérisation de la charge/décharge des piles.
- Lecture de la charge courante des piles.
- Impression 3D de boitier (protection intempéries)
- Utilisation de néoprène et élastiques pour fixation durable (test avec rebond)

## 4. Mesure de l'effort

Un gauje de contrainte sur le pédalier permettrait d'identifer l'effort appliquer pour pédaler, d'autant plus si on Couple cette informatoin avec: l'inclinaison, la vitesse, le nombre de tour de pédalier, le nombre de tour de roue.

## 5. Phare autonome avec demi-sphere plexi:
- WS2812B circulaire, ou en spiral
- Crochets fixe pour ajouter/retirer le modules une fois en route.
- Module autonome avec ses piles.
- Belle opportunité d'ajouter un haut-parleur.
- On peut profiter de l'encapsulation pour faire du POV sur une demi-sphere.
- Evaluer si un moteur brush-less donnerait de bon résultat
- Peut s'attacher à l'avant, l'arrière, sur les côtés du porte bagage.

## 6. Ampli Audio

Trouver où et comment installer une haut parleur avec ampli. Possiblement un module haut-parleur et un module ampli.

Une façon ludique serait de les monter sur les casques.

L'effet de groupe serait plus fort avec cette décoration unique, d'autant plus si nous sommes en mesure d'y faire jouer des sons simultanément ou en harmonie (chaque casque fait la note d'une musique)


## 7. Mat avec avatar/mascote

Une option est de rendre le mat invisible (aucune lumière tout le long de son parcours)

Identification du matériel pour la structure du mat
- Rigide: tige acier / aluminium
- Semi-Rigide: tube plastique
- Flex: Fibre de verre (arceau de tente)
- Bamboo: a essayer

Conception d'une structure avatar/mascote en fonction du thème qu'on aura choisi.

Ex. Lune, Nuage, Soleil, Étoile pour objets célestes.

## 8. Projection

Afficher une images au sol par projection, des lignes de contour ou une
silhouette. Le projecteur peut-être installé sur le porte bagage avant par
exemple.

Une tige en hauteur qui envoie des motifs lumineux au sol. Une idée serait de
mettre sur une pièce de tissue des payette et d'éclairer avec une LED
puissante pour voir les reflets animé au sol.

Projection sur jet d'eau. Par capilarité ou par dispersion de goutte fine, on
forme une surface de projection avec de l'eau. L'idéal serait de récupérer
l'eau ainsi utilisé, car le transport de l'eau est délicat.

Une simple lumière sous le vélo qui éclaire intensément le sol peut apporter
un effet de brillance intéressant au vélo, en le découpant du sol.

Le corps du cycliste peut servir d'écran de projection, en particulier si le
cycliste porte un habit tout blanc ou encore mirroir.

## 9. Identification des positions relatives (sous-projet du mat)

Le vrai problème à régler est la dispersion des participants 

Mesure de la distance/direction entre chacun des vélos de la flotte

- Utilisation d'Ultra-son
- Sync temporel parfaite des modules (un master ?)
- Émission d'un packet de donné avec un timestamp via les ultra-son, récepteur calcule le délai. On peut tenter le coups dans le spectre des ondes audibles pour voir l'effet.

L'idée d'utiliser les UltraSon ne fonctionne pas. Les petits
micro/haut-parleur ultrason que nous avons permet un calcul sur une distance
de 2 mètres tout au plus. C'est logique, puisque le haut-parleur est
minuscule. Un grand 'transducer' UltraSon a un coût de l'ordre de 300$. De
plus, la portée resterait courte, a peine plus de 100 m.

Il semble plus facile que chaque module identifie sa position absolue, et qu'à
la demande les modules échangent cette information afin de pouvoir déterminer les
positions relatives entre les modules.

Stratégie:
- Module GPS Standard
- Module communication Sans Fil (NRF24L01 ou LoRa pour plus de porté)

Pour le rendu de l'information, puisque tout les vélo suivent le même trajet,
une courte bande DEL dans le sens du cadre peut-être utilisé pour montrer si
les autres cycliste sont devant ou derrière nous.

Technologie à regarder:
- UWB
- VHF Direction finding
- Radio direction finding

## 10. Tesla coil

Abriter sous de l'acylique un Tesla Coil

Remarque: Pour avoir des portées intéressante le module ultra-son doit être puissant et probablement de grande taille, ce qui peut être un bloquant pour la mise en oeuvre.

## 11. Peinture fluorescente sur les jantes.

Appliquer de la peinture fluo sur les jantes 'freins a disque requis' et les
rayons. Puis, de puissantes LED sur les aubans permet de les charger
lumineusement lorsque les roues tournent.

Si on a pas de frein à disque, on peut insérer entre les rayon une matière pour appliquer la peinture fluo.

## 12. Identification du trajet

Option 1: Collecte du trajet avec données GPS (module autonome ou téléphone ?)
Option 2: Utilisation de la DB hotspot WiFi de Google (est-ce possible ?)

## 13. Lumière dans la roue

Démonter les rayons et placer un disque de plastique avec moteur autour du moyeu pour activer un module POV.
Thermoformation du moule plastique translucide.
Pile statique au milieux de la roue, ex. autour du moyeux.

Alternative plus facile a réalser, poser des disque à l'extérieur de la roue.
Un moteur fixé sur le porte bagage avec des engrenage pour atteindre le centre du
disque.

## 14. Lumières aux extrémitées des poignées

Lumières au poigné, avec girlande pour effet lumineux.

Il y avait même eu une idée d'avoir des jets de feu à un certain moment.

## 15. Affichage de message

Panneau qui peut afficher du texte déroulant.

Il est possible d'utiliser la demi-sphère en acrylique avec du POV pour faire ça.


Réutilisation des codes de son porte clef RF de voiture. Une excellente porté.

## 16. Éditeur d'effets lumineux LEDs:

Pour les bandes DELs WS2012B on a:

- Couleurs unique: Blanc, Bleu, Rouge
- Pulsation: onde carré(blink), en dent de scie, Sin(pulsation progressive) (affecte la luminosité)
- Palette de couleur: Chanque cycle de la pulsation marque une transition d'un position de la palette à une autre.

## 17. Communication audio entre les cyclistes

Adaptation du casque de vélo pour permettre la communication entre cycliste.

- écouteurs intégré au casque de vélo
- micro intégré au casque de vélo

## 18. Collecte des données et Télémétrie

La collecte des donnée peut faciliter les expériementation pour faire évoluer le produit.

On peut imaginer collecter sur uSD ou EMMC les données suivantes:
- Vitesses, accélération, moment en movement ou immobite.
- Charge des piles, la consommation énergétique.
- Les commandes reçues et envoyées.

Pour plus de granularité, on peut envisager la télémérie.

- Accéloromètre
- Gyroscope
- Magnétomètre
- Consommation énergétique
- Statu des piles
- Tour de roue
- Tour de pédalier
- Pression sur le pédales

## 19. Lentilles fresnelle dans le triangle du vélo.

À quoi ressemblerait un éclairage derrière la fresnelle d'une vielle TV à projection jeté au poubelle.

## 20. Recouvrir les côtés des roues

Ajouter de grands pompom avec frou-frou vis-à-vis les roues pour cacher tout
les rayons et illuminer le tout puor un effet dynamique.

Dans la même optique, placer de grand disque avec LED vis-à-vis les roues et
faire une rotation (ex. inverse) pour créer des effets lumineux indépendant de
la rotation des roues.

## 21. Ballon gonflé à l'helium

Effet de hauteurs sans ajouter de poids.


## 22. Identifier le groupe Lumivélo

Écrire "Lumivélo" sur les vélo ou les casques pour identifier le groupe et publiciser le projet.

Un projection sur plexi-glass graver au laser permet d'y metter beaucoup de
détails graphiques: logo, texte, silhouette, etc.

## 23. Boule disco

## 24. Feu d'artifice

Système pour allumer des feux de Bingale à interval régulier. Doit produire
une chaleur très intense pour un court laps de temps afin d'allumer le feu.

## 25. Ligne vertical vs image 2D

Une bande DEL vertical avec un cycle pour afficher une image si on prends une
photo avec un long temps d'exposition.

On pourrait faire des flammes courte pour accommoder le temps d'exposition des
caméra la nuit.

## 26. Acrylique gravée au laser

Une projection lumineuse sous une plaque d'acrylique gravée au laser, fait
apparaitre les motifs gravés de la couleur des LED et le reste de l'acylique
n'est pas affecté par la lumière, à l'exception des countours. L'endroit
naturel pour placer ce montage sur le vélo est dans le triangle principale du
cadre, ou dans les triangles des deux hauban. C'est un excellent endroit pour
le logo des papas inventeur ou encore faire la publicité de notre bidouillage
Lumivélo 2020. Il pourrait même y avoir un QR-Code.

## 99. Interactions avec/entre module

### 99(A) Interrupteur ON/OFF

Il est très utile d'avoir un interrupteur mécanique principal pour couper et réactiver l'alimentation. Un voyant lumineux donne le feedback si le système est sous-tension ou non.

### 99(B) Reed switch

Une Reed switch activé par un aiment peut servir de code secret pour activer une fonctionnalité cachée.

### 99(C) Porte clef RF de voiture

### 99(D) Carte/Jeton Rfid

Autre façon de communiquer à l'aide de code secret au module.

### 99(E) Touch Sensor (MPR121)

Moyen économique de faire l'interface.

Un bel exemple, c'est l'implémentation d'un pattern circulaire sur un PBC. Par la suite, on peut ajuster l'intensité par rotation virtuelle, ce qui est un excellent HMI.


### 99(F) Télécommande - Communication IR

Recyclage de manette pour la communication IR.

Fonctions:
- Controle des options de son Lumivélo
- Envoyer une commande aux autres lumivélo de la flotte (Ex. tout le monde en blanc).

### 99(G) Communication entre les vélos de la flotte

- WiFi
- LoRa
- NRF24L01:  
  - 2.4 GHz band
  - 250 kbps up to 2 Mbps
  - open space and with lower baud rate its range can reach up to 100 meters
  - can use 125 different channels
  - up to 6 addresses, or each unit can communicate with up to 6 other units at the same time
- IR
- ZigBee ?

Dans tout les cas, il y aura des effets de synchronisation. Il faut rendre
visible cette synchronisaiton, par exemple faire clignoter tout les vélos en
même temps lors de la réception d'un nouvelle commande ou d'une transition
entre effets lumineux. Un scintillement en blanc est une effet intéressant
pour marque le moment où c'est sync.

### 99(H) Interface sur appareil mobile

Utilisation du Bluetooth pour la connectivité.

Utilisation de Flutter pour le UI.

Possibilité d'afficher des représentations graphique.

Ex. Position relative de tous les autres vélo de la flotte.
Ex. Édition du pattern de couleur: Type de Tween + palatte de couleur.

## Design modulaire:
- Module Pile
- Module Mat
- Module Casque
- Module Poigné
- Module T-Shirt
- Module Roue
- Module IR

- Module télémétrie (software)
- Module éditeur d'effets lumineux (software)

- Module demi-sphère est une partie autonome, tout est à l'intérieur.

## BOM

### Options pour les Composants électroniques:
- Accéléromètre/Gyro/Compas
- Ampli audio (module MP3 ? ex klaxon, FX, rif d'une chasson)
- Micro (commandes vocale ?)
- Recepteur IR
- Récepteur UltraSon
- Récepteur luminosité
- Mesure température/humidité
- WS2812B (connecteurs) * 3
- LED 12V * 2
- Module mémoire (uSD ou emmc)
- Module de mesure de la consommation énergétique (Volts/ampères)
- MPR121 (commandes tactiles ?)

### Option pour LEDs

- WS2812B
- PL
- LED monochrome 12V

### Options pour le controlleur:
- Arduino nano/micro
- ESP8266
- ESP32
- BluePill
- SBC (Pi nano, BeagleBone, OrangePI)

### Option pour la communication sans fil
- WiFi
- Bleutooth
- IR
- RF standard

## Échéancier

1er Mars: Identification des projets/fonctions retenues.
