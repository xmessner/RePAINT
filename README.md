# Présentation

# OS

La cible principale de RePAINT! est avant tout Linux et ses dérivés. Les prérequis sont assez simples ce qui fait qu'il peut normalement fonctionner sans problèmes sur l'ensemble des distributions modernes.

| OS | Supporté ?|
|---:|:---:|
|Linux 64 bit|Oui|
|Windows 11 64|Prévu|
|HaikuOS|Prévu|
|BSDs|A tester|
|MacOS|Si possible|
|Web|A tester|

# Modes graphiques

| Machine | Résolution | nb Colors | Fixes | Contrainte |
|---:|:---:|:---:|:---:|:---:|
|ATARI ST LOW|320x200|16|512 0/7|N|
|ATARI ST MEDIUM|600x200|4|512 0/7|N|
|ATARI STE LOW|320x200|16|4096 0/15|N|
|ATARI STE MEDIUM|600x200|4|4096 0/15|N|
|ATARI ST HIGH|600x400|2|O|N|
|TO7|320x200|8|8|8x1|
|TO770|320x200|16|16|8x1|
|MO5|320x200|16|16|8x1|
|TO8 / MO6 BM4|||
|TO8 / MO6 BM16|(x2)160x200|16|4096 0/15|N|
|TO8 / MO6 BM59|||
|TO8 / MO6 BM5B|||
|C64 HIRES|||
|C64 MultiColor|||
|CGA Medium|||
|CPC 464 Mode 0|160x200||
|CPC 464 Mode 1|||
|CPC 464 Mode 2|||
|EXELVISION 100|||
|Hector 2 HRX|||
|Oric HIRES|||
|TMS9928 Mode 2|||
|ZX81|||

# Format de fichiers

| Machine | fonctionnalités
|---:|:---:|
|ATARI ST LOW|PI1 Degas|
|ATARI ST MEDIUM|PI2 Degas|
|ATARI STE LOW|PI1 Degas|
|ATARI STE MEDIUM|PI2 Degas|
|ATARI ST HIGH|PI3 Degas|
|TO7|*Dump|
|TO770|*Dump|
|MO5|*Dump|
|TO8 / MO6 BM4|*Dump|
|TO8 / MO6 BM16|*Dump|
|TO8 / MO6 BM59|*Dump|
|TO8 / MO6 BM5B|*Dump|
|C64 HIRES||
|C64 MultiColor||
|CGA Medium|BSAVE|
|CPC 464 Mode 0|OCP|
|CPC 464 Mode 1|OCP|
|CPC 464 Mode 2|OCP|
|EXELVISION 100|*Dump|
|Hector 2 HRX|*Dump|
|Oric HIRES|*Dump|
|TMS9928 Mode 2|SC2|
|ZX81|*Dump|

* Dump : identique à l'organisation mémoire de la machine cible. Il suffit juste de le charger à la bonne adresse ensuite dans un émulateur ou sur une machine physique.

# Fonctionnalités

| Machine | fonctionnalités
|---:|:---:|
|ATARI ST LOW||
|ATARI ST MEDIUM||
|ATARI STE LOW||
|ATARI STE MEDIUM||
|ATARI ST HIGH||
|TO7||
|TO770||
|MO5||
|TO8 / MO6 BM4||
|TO8 / MO6 BM16||
|TO8 / MO6 BM59||
|TO8 / MO6 BM5B||
|C64 HIRES||
|C64 MultiColor||
|CGA Medium||
|CPC 464 Mode 0||
|CPC 464 Mode 1||
|CPC 464 Mode 2||
|EXELVISION 100||
|Hector 2 HRX||
|Oric HIRES||
|TMS9928 Mode 2||
|ZX81||

# Travail en mémoire

Le mode *Natif* traite la donnée comme sur la machine d'origine. Cela concerne à la fois les coordonnées, la correspondance des couleurs, le traitement des bits. Il va donner une plus grande souplesse dans le traitement de l'information si on souhaite se rapprocher du fonctionnement de l'écran de la machine.
Le mode *Bitmap* au contraire va travailler en mémoire en indexé. Le seul moment où va traiter le format mémoire de la machine c'est au chargement et à la sauvegarde. Il sera plus proche d'un logiciel de dessin classique. C'est le mode choisi lorsque le mode *Natif* n'apporte rien de plus.
Cependant, la cible est que l'ensemble des modes soient en *Natif* pour une question de consommation mémoire plus faible et une meilleure compréhension de la représentation de l'information en mémoire.

Le mode *Natif*  

| Machine | (N)atif / (B)itmap
|---:|:---:|
|ATARI ST LOW|N|
|ATARI ST MEDIUM|N|
|ATARI STE LOW|N|
|ATARI STE MEDIUM|N|
|ATARI ST HIGH|N|
|TO7|B|
|TO770|B|
|MO5|B|
|TO8 / MO6 BM4|B|
|TO8 / MO6 BM16|B|
|TO8 / MO6 BM59|B|
|TO8 / MO6 BM5B|N|
|C64 HIRES|N|
|C64 MultiColor|N|
|CGA Medium|B|
|CPC 464 Mode 0|B|
|CPC 464 Mode 1|B|
|CPC 464 Mode 2|B|
|EXELVISION 100|N|
|Hector 2 HRX|N|
|Oric HIRES|N|
|TMS9928 Mode 2|N|
|ZX81|N|

# Validation

| Machine | Mode validation
|---:|:---:|
|ATARI ST LOW|Recoil WEB|
|ATARI ST MEDIUM|Recoil WEB|
|ATARI STE LOW|Recoil WEB|
|ATARI STE MEDIUM|Recoil WEB|
|ATARI ST HIGH|Recoil WEB|
|TO7|DCMoto|
|TO770|DCMoto|
|MO5|DCMoto|
|TO8 / MO6 BM4|DCMoto*|
|TO8 / MO6 BM16|DCMoto*|
|TO8 / MO6 BM59|DCMoto*|
|TO8 / MO6 BM5B|DCMoto*|
|C64 HIRES|Recoil WEB|
|C64 MultiColor|Recoil WEB|
|CGA Medium|Dosbox PCPAINT|
|CPC 464 Mode 0|Mame*|
|CPC 464 Mode 1|Mame*|
|CPC 464 Mode 2|Mame*|
|EXELVISION 100|Mame|
|Hector 2 HRX|Mame*|
|Oric HIRES|Mame|
|TMS9928 Mode 2|Recoil WEB|
|ZX81|Recoil WEB|
|Atari XL GR7|Mame*|
|Atari XL GR8|Mame*|

## Recoil Web

https://recoil.sourceforge.net/web.html

## Mame
### TO7

- Lancement de MAME
```
commande
```

# Interface

L'interface se décompose en 4 parties
* La zone de dessin qu'on peut déplacer en fonction de son envie sur la fenêtre. Elle s'adapte en fonction de la taille de l'écran. Attention cependant, il n'y a pas de contrôle sur la taille maximum possible. Il peut alors y avoir sur les très grands écrans des superpositions des éléments ou des bugs.
* La palette de couleur de 2 à 16 disponible. Un symbol en haut d'une couleur signifie la selection pour le bouton gauche, en bas, pour le bouton droit.
* La zone d'outils, en base de l'écran. Comporte l'ensemble des outils disponibles pour dessiner. Certains pourraient ne pas être activés du fait de la jeunesse du projet.
* Le live zoom est une zone qui affiche l'image agrandit en temps réel permettant d'avoir une vue différente de celle où l'on dessine
* Le panneau de contrôle va regrouper l'ensemble des éléments liés au mode de dessin en cours, comme la modification des couleurs de la palette, le menu de chargement et de sauvegarde des images, les toggles.

La sélection d'un outil le met en surbrillance.
Pour "Sortir" d'un outil comme la ligne brisée par exemple, il suffit d'en selectionner un autre. L'ergonomie va changer pour correspondre à une utilisation plus efficace.

# Souris

* Shift Gauche + Bouton Gauche : Déplacement de l'écran de dessin
* Bouton Gauche : Dessin couleur 1 (Encre)
* Bouton Droit : Dessin couleur 2 (Fonc / Papier)
* Molette (zoom): Modifie le niveau de zoom
* molette (spray): Modifie le rayon de dessin du spray

# Clavier

Le clavier est en Qwerty.

## Commun
* F8: Undo / Redo
* F10: QUIT
* F11: Reset
* F12: Capture d'écran (raylib)
* TAB: Show / Hide grid

## Spécifique
### C64 Multicolor

Changement de piceau
* 0: Fond d'écran. Un déplacement change la couleur temporairement pour tester. Un clic de souris fige la couleur de fond en fonction du bouton utilisé.
* 1: Utilise le pinceau 1
* 2: Utilise le pinceau 2
* 3: Utilise le pinceau 3

### C64 HiRes

* i: *Ink Mode* Affiche le dessin en mettant en valeur les emplacements où le dessin a été fait avec l'encre
* p: *Paper Mode* Affiche le dessin en mettant en valeur les emplacements où le dessin a été fait avec la couleur de fond
* m: *Pixel Mode* Ne fait que modifier les pixels de l'encre ou du fond sans toucher à la couleur
* f: *Paint Mode* Ne modifie pas le dessin, juste la couleur de fond ou de forme en fonction du bouton de la souris utilisée

### TMS9928a

* i: *Ink Mode* Affiche le dessin en mettant en valeur les emplacements où le dessin a été fait avec l'encre
* p: *Paper Mode* Affiche le dessin en mettant en valeur les emplacements où le dessin a été fait avec la couleur de fond
* m: *Pixel Mode* Ne fait que modifier les pixels de l'encre ou du fond sans toucher à la couleur
* f: *Paint Mode* Ne modifie pas le dessin, juste la couleur de fond ou de forme en fonction du bouton de la souris utilisée

### CGA Medium

* p: Cycle la palette de couleur CGA
* P: Cycle la palette de couleur CGA dans le sens inverse
* b: Incrémente la couleur de fond sur l'une des 16 couleurs disponibles
* B: Décrémente la couleur de fond sur l'une des 16 couleurs disponibles

### Amstrad CPC 464 Mode 0

* i: Incrémente la couleur sélectionnée parmi les 27 disponibles
* d: Décrémente la couleur sélectionnée parmi les 27 disponibles

### Oric HiRes

* a: *Attribute Mode* Modifie les attributs pour la modification de la couleur
* i: *Invert Mode* Change l'attribut d'inversion de couleur
* m: *Paint Mode* Passe en mode dessin
* f: *Fill erase attribute* Lors d'un remplissage, on écrase les bits d'attribut ou non
