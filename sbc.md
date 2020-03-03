# Choix du SBC

Requis:

- 1x SPI (requis: module NRF24L01)
- 1x UART (requis: module GPS) [préférablement 2x, car un UART est dédié au DEBUG]
- 1x USB (requis: lien USB au Arduino qui pilote les DELs). [préférablement 2x, ça évite l'achat d'un HUB]
- Bas prix 

«Nice to have»:

- BlueTooth intégré (Alternative: un module BlueTooth / un adapteur USB Bluetooth)
- IR intégré (Alternative: un capteur IR + une PIN de IO)
- 1x RJ45 Ethernet (Pas requis, mais pratique pour: debug / mises à jour)
- EMMC (Pas requis, mais plus fiable, mieux adapté aux vibrations)

## BeagleBone Black

Le BBB est une des options les plus dispendieux pour notre SBC.
En effet, son prix oscille aux alentours de 90$ pour chaque unité.
Par contre, nous avons une douzaine de BBB en stock dans nos réserves.
Ainsi, ce choix aurait un coût effectif de 12 x 0$ = 0$.
Finalement, dans notre situation, c'est l'option la moins dispendieuse.

- SoC:  Sitara™ XAM3359AZCZ100, 1-GHz ARM®Cortex®-A8 32‑Bit RISC Processor
- RAM: 512MB DDR3L 606MHZ
- eMMC: 2G
- 1x USB 2.0 Client miniUSB (Power 5V)
- 1x USB 2.0 Type A Socket
- Ethernet 10/100, RJ45

Le BBB a beaucoups d'avantages qui le démarques des autres options.

Une documentation exhaustive.

De nombreuses options de configuration disponibles qui offre une flexibilité sans pareil.
Par contre, la mise en oeuvre initiale est plus complexe.

Il dispose de deux PRU qui rends possible le contrôle des LEDs ws2912b sans l'intermédiaire d'un arduino.

Il dispose d'un connecteur USB Mini-B fiable et robuste qui permet de
l'alimenter en même temps que d'assurer la connectivité IP.  On peut envisager
tirer avantage de cette capacité pour faciliter les mises à jour et le débug une fois
le module installé sur le vélo.

Le connecteur Ethernet est disponible pour access rapide via une connection
cablé au SBC, on peut même activer un boot de l'OS au complet via la
connection Ethernet. C'est l'idéal afin de pouvoir flasher un firmware
corompu, sans l'intermédiaire d'une carte uSD.

Le SOC Sitara permet du "CPU Frequency scaling" avec un "governor", idéal pour
réduire la consommation du CPU lorsque ce dernier n'est pas solicité.

Il y a 6xUART, c'est plus qu'il en faut. Il en faut un pour la connection serie au GPS.

Il y a 2xSPI, c'est plus qu'il en faut. Il en faut un pour le module NRF24L01.

Il y a un seul connecteur USB (plus exactement deux, en comptant le Mini-B).
Donc, il faut acheter un HUB environ 4$/ch, pour obtenir 4 sortie USB.

In n'y a aucune connectivité sans-fil. Donc, pour un haut-parleur sans-fil, il
faut acheter un adapteur USB-Bluetooth-5.0, environ 4$/ch. Un autre option,
est de se procurer un module comme le BK8000L (j'en ai déja 4 en stock).

Enfin, on peut imaginer une construction ultra-clean, avec un design de "Cape"
qui a sa propre EEPROM pour s'identifier et fournir les options de
configuration. Il y aurait le module audio Bluetooth BK8000L, le module
sans-file NRF24L01, le module GPS et les connecteur pour les bandes DELs
ws2812b.

## Raspberry PI Zero W.

À première vu, son bas prix est attrayant, moins de 15$ pour le Pi Zero W
sur buyapi.ca. Par contre, sa faible disponibilité fait rapidement disparaitre
cet avantage. Il revient 25$ chez ABRA et il faut attendre une à deux semaines pour
le recevoir.

De plus, Il faut ajouter l'achat d'un Hat avec 4xUSB
spécialement adapté au connecteur micro-USB, au coût de 12$. 

Au final, le prix est autour de 40$ avec les taxes.

Le format compact est un plus.

On a le Bluetooth intégré, c'est un plus.

La uSD au lieu de la eMMC, c'est un moins.

L'immense popularité de la plateforme Raspberry PI facilite et accélère la
mise en oeuvre, plus qu'avec n'importe quels des autres plateformes.

L'option PI Zero sans WiFi/Bluetooth est à considérer pour réduire les coûts,
puisque le Bluetooth n'est pas un requis, mais un «nice to have».

## Orange Pi Zero LTS

Alternative intéressant au PI Zero, car le coût final est 23$, ou moins
puisque c'est a peine 20$/ch à l'achat de 5 ou plus.

Le kit "Orange Pi Zero LTS 512MB + Expansion Board" offre 3 ports USB et le IR intégré.
Mais il n'y a pas de eMMC ni de Bluetooth.

- Allwinner H2+ ARM Cortex-A7 Quad-core 
- Ethernet 10/100 RJ45
- MicroUSB OTG + Power Supply
- RAM: 256MB DDR3 SDRAM
- WiFi: XR819, IEEE 802.11 b/g/n (Probablement non utilisable)
- 2MB Spi Flash
- 3x USB 2.0 HOST (2x sur Expansion Board)
- 1x USB 2.0 OTG + power supply (microUSB)
- 1x IR (sur Expansion Board)

## Orange Pi Zero Plus 2 H3

Alternative intéressant au PI Zero W. Le coût final est 40$, ou moins
puisque c'est a peine 37$/ch à l'achat de 5 ou plus.

Avec le kit "Orange Pi Zero Plus 2 H3 + Expansion Board" on a le setup suivant:

- eMMC: 8GB
- RAM: 512MB DDR3
- SoC: Allwinner H3 - 1.2GHz, quad-core, Cortex-A7
- WiFi/Bluetooth: AP6212, IEEE 802.11 b/g/n, BT4.2
- 1x USB 2.0 OTG + power supply (microUSB)
- 2x USB 2.0 HOST (Expansion Board)
- 1x IR (Expansion Board)

Il n'y a pas de connecteur Ethernet RJ45, mais il est peut-être possible d'utilise le USB OTG + Power pour cette function, sinon le WiFi peut prendre le relai.

## NanoPi NEO Plus2 V2.0 (Friendly ARM)

Ce SBC à 59$US, est un monstre avec son 4x coeurs 64 bits à 1.2 GHz, 1 Gb de RAM et 8 GB de EMMC.
Étrangement, sur le site du manufacturier le prix est de 29$ USD, ce qui semble trop bas.

Son Bluetooth intégré et ses 4 connection USB (2 connecteur physique et 2 sur
le header) sont les options que nous recherchons pour les besoin du projet.

- CPU: Allwinner H5, 4x Cortex-A53 1.2GHz (64-bit)
- RAM: 1GB DDR3 (32-bit)
- eMMC: 8GB
- Ethernet: RJ45 Gbps Ethernet
- WIFI: 802.11b/g/n (RTL8211E-VB-CG chip)
- Bluetooth: 4.0 dual mode
- Antenna x1: IPX-I Connector
- USB: 4x 2.0 Host (2x USB Type-A Ports, 2x USB pin header)
- Power: DC 5V/2A (MicroUSB power only)

## NanoPi NEO Air-LTS (Friendly ARM)

Setup minimal, mais avec EMMC. Le manufacturier le vends pour 20$, mais sur Aliexpress, c'est 40$.

- Allwinner H3, 4x Cortex-A7 1.2GHz
- 512 MB RAM
- 8 GB EMMC
- WiFi/Bluetooth: AP6212, IEEE 802.11 b/g/n, BT4.0 dual mode
- 1x MicroUSB 2.0 Type A OTG & Power In
- 2x USB (pin header)
- 1x IR (pin header)

## Quelques alternatives possibles

### Orange Pi 3G-IOT-B

Reviens à 41$ CDN, par contre, il semble que c'est une solution tout intégrée.

- 4 Gb EMMC
- 512 MB RAM
- GPS ???
- Bluetooth ?

Il y a un un seul connecteur USB et beaucoup d'incertide avec ce SBC.

### MPM

(Recyclage)

Nous avons plus d'une douzaine de MPM disponible. Par contre, il y a peu d'avantages à utiliser ce SBC.

### CL3 (MPM-2)

(Recyclage)

Nous avons plus d'une douzaine de CL3 disponible. Par contre, il y a peu d'avantages à utiliser ce SBC.

### PCT1 (WiserAir)

(Recyclage)

Nous avons plus d'une vingtaine de PCT1 disponible.

Il y a peu d'avantage à utiliser cette plateforme, par contre il y a un écran et du WiFi/ZigBee de disponible.

L'inconvénient majeur, c'est que les pins pour le SPI et I2S ne sont probablement pas accessible.

### Khadas VIM1 Basic

Alternative exotique à 62$ USD

Le SoC est un Amlogic S905X 1.5GHz 64-bit Quad-Core ARM Cortex-A53.

- 8GB de EMMC
- 2G de RAM
- IR intégré
- Bluetooth intégré

### Firefly-RK3128

Alternative exotique à 60 $USD

- 8Gb EMMC
- 1Gb EMMC
- IR intégré
- Bluetooth intégré
- 4x USB

### Banana Pi BPI M4

Alternative exotique à 60 $CAD

- Realtek RTD1395 ARM Cortex-A53 Quad-Core 64 Bit
- 1 GB DDR4 
- 8G eMMC flash
- 10/100 Mbit/s
- RTL8821 module support Wi-Fi 802.11 b/g/n/AC + Bluetooth 4.2
- 4 x USB 2.0 TYPE C

### Atomic Pi - SBC 

Alternative surprenante. Seulement 58$ CDN sur amazon.ca

- 16 GB EMMC
- Bluetooth
- 2 GB RAM
- 1x USB3
- Intel ATOM

Consommation courant élevée: 5V @ 3A

### MiniZed-single-core Zynq 7Z007S SoC Development Board

Le problème de ce SBC, c'est son prix trop élevé 89$ USD.

Alternative "overkill", c'est le SBC pour faire de la programmation FPGA

- 8 GB EMMC
- 512 MB RAM
- Bluetooth
- 1x USB
- 1x Accelerometre

Le "feature" en puissance, c'est le FPGA pour la programmation des trames à envoyer aux LEDs ws2812b.
