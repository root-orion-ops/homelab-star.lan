# Documentation PROXMOX
Installation et configuration de PROXMOX dans l'infrastructure LAN de mon homelab

### 1. CONFIGURATION PROXMOX
<details>
  <summary>
    Détails (cliquez pour dérouler)
  </summary><br>
  <b>(!) POUR LE MOMENT SCREENSHOT SEULEMENT EN COURS DE DOCUMENTATION (!)</b><br><br>

Une fois Proxmox VE 9.2 installé sur le serveur (pour mon cas ça sera un vieux PC portable recyclé) il faut accéder à son interface web (IP de la machine:8006) ici 192.168.0.12:8006
<img src="./assets/image.png" />
<img src="./assets/image1.png" />
<img src="./assets/image2.png" />
<img src="./assets/image3.png" />
<img src="./assets/image4.png" />
<img src="./assets/image5.png" />
<img src="./assets/image6.png" />
<img src="./assets/image7.png" />

apt update && apt dist-upgrade -y pour vérifier que tout est bon encore une fois
<img src="./assets/image8.png" />
<img src="./assets/image9.png" />
</details>

### 2. CARTE GRAPHIQUE ET INTEGRATION DE L'HÔTE PROXMOX DANS LE LAN
<details>
  <summary>
    Détails (cliquez pour dérouler)
  </summary><br>
  <b>(!) POUR LE MOMENT SCREENSHOT SEULEMENT EN COURS DE DOCUMENTATION (!)</b><br><br>
Commande pour detecter la présence des carte graphique, (hors celui présent sur le chipset du processeur)
`lspci -nnk | grep -A 3 -i vga`
<img src="./assets/image10.png" />
présence de la gtx 1650 -> possibilité de faire du passthrough vers une VM plus tard, ou une IA locale
  
#

Basculer et intégrer l'hôte PROXMOX dans le LAN
<img src="./assets/image11.png" />
<img src="./assets/image12.png" />
<img src="./assets/image13.png" />
<img src="./assets/image14.png" />
<img src="./assets/image15.png" />
<img src="./assets/image16.png" /><br>
Ping vers l'extérieur (internet) pour confirmer que l'hôte est bien isolé<br>
<img src="./assets/image17.png" />
</details>

### 3. CREATION CONTENEUR LXC
<details>
  <summary>
    Détails (cliquez pour dérouler)
  </summary><br>
  <b>(!) POUR LE MOMENT SCREENSHOT SEULEMENT EN COURS DE DOCUMENTATION (!)</b><br><br>

<img src="./assets/image18.png" />
<img src="./assets/image19.png" />
<img src="./assets/image20.png" />
<img src="./assets/image21.png" />
<img src="./assets/image22.png" />
<img src="./assets/image23.png" />
<img src="./assets/image24.png" />
<img src="./assets/image25.png" />
<img src="./assets/image26.png" />
<img src="./assets/image27.png" />
<img src="./assets/image28.png" />
</details>


## ISSUES/AMELIORATION ANNEXE
- [Faire disparaître le pop up No subscription](https://github.com/root-orion-ops/homelab-star.lan/issues/1#issue-5552468003)
- [Ajouter le support du wi-fi](https://github.com/root-orion-ops/homelab-star.lan/issues/2)
- [Empêcher la mise en veille/shutdown à la fermeture du capot](https://github.com/root-orion-ops/homelab-star.lan/issues/3)
- [Routage NAT](https://github.com/root-orion-ops/homelab-star.lan/issues/4)


#
[Page principale](https://github.com/root-orion-ops/homelab-star.lan)
