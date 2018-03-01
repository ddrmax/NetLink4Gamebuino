# NetLink4Gamebuino
A Gameduino Wireless multiplayer library using NRF24L01+ chipset in the same way as the GameBoy Link and MultiLink Cable

https://gamebuino.com/fr/creations/gamebuino-link-le-multiplayer-sans-fil-pour-gamebuino-meta

## PETIT TEASER  
* Avec une vitesse de 250 kbits/s a 2Mbits/s on pourrait faire du realtime (check des buffers de réception a chaque frame)
* Avec l'utilisation de maxi 6 canaux:
** on peut faire un Multi a 6 joueurs (tour par tour et "pseudo realtime")
** ou trois joueurs (realtime) via une vraie communication bi-directionnelle
* si j'arrive a faire une communication sans overhead (par exemple garder quel joueur est sur quel canal):
** vous avez la possibilité d'utiliser 32 octets
** avec un overhead on serait du genre entre 16 et 20 octets
* Pas besoin de forcer le CPU a faire de gros checks de perte de packets (en configurant bien la puce NRF24 s'en occupe)
* Mode de Téléchargement (DS et 3DS Like)?


## BUT:
Une librairie de multijoueur pour les jeux Gamebuino pour un multijoueur sans fil.

Mon but final est de vous fournir:

* Une librairie qui:  
  * est rapide  
  * impacte un minimum les performances  
  * facile a utiliser  
  * complète  
  * supporter 2+ connexions entre gamebuino (3 voir 6 joueurs)  
  * permettre aux apps et jeux de fonctionner même si le NRF24L01 n'est pas connecté  
* Un Hardware qui:  
  * est peu onéreux  
  * facile a dupliquer  
  * plug and play (Sur le BackPack)  


Mon materiel:  
* Plein d'arduino nano (10+)  
* Plein de NRF24L01(des versions + normalement)  
* Une Gamebuino (et prochainement une seconde pour tests en condition réelles)  



### LIBRAIRIE:
Convention d'appel: `Link.fonction();`

Exemples de fonctions:  
```C
Link.SetServer(nbPlayers); //Pour l'hôte Multijoueur  
Link.SearchServer(timeout);//Pour les Clients  
Link.Player{X}//classe joueur contenant les données spécifiques de chaque joueur  
Link.SendData(Data);  
```

### To-Do List:  
- [x] Creer le Repo  
- [x] Mettre en place le materiel nécessaire  
- [ ] Creer la librairie  


Petites informations importantes  

datasheet: https://www.sparkfun.com/datasheets/Components/SMD/nRF24L01Pluss_Preliminary_Product_Specification_v1_0.pdf

### APERÇU BRANCHEMENT:

![](https://gamebuino.com/froala/uploads/images/1b0f3fbb57a8cd1fe9f94c397aae5c299ad7dd4b.jpg)

![](https://gamebuino.com/froala/uploads/images/a4fe9f4509f3fd16160d5a8f8f322de11cbe826c.jpg)

Voila pour le moment :)

