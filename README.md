# Infrastructure du homelab

<li><a href="https://github.com/root-orion-ops/homelab-star.lan#documentation-proxmox"><b>PROXMOX</b></a></li>
<li><a href="https://github.com/root-orion-ops/homelab-star.lan/blob/main/README.md#documentation-lxc-pour-sambanfs"><b>Conteneur LXC pour Samba/NFS</b></a></li>
<li><a href="https://github.com/root-orion-ops/homelab-star.lan/blob/main/README.md#documentation-windows-server"><b>Windows SERVER</b></a></li>
<li><b href="https://github.com/root-orion-ops/homelab-star.lan/tree/doc-lancache"><b>LAN Cache</b></a></li>
<li><b href="https://github.com/root-orion-ops/homelab-star.lan/tree/doc-jellyfin"><b>Jellyfin</b></a></li>
<li><b href="https://github.com/root-orion-ops/homelab-star.lan/tree/doc-kubernetes"><b>Kubernetes</b></a></li>
<br> <li><a href="https://github.com/root-orion-ops/homelab-star.lan/blob/main/README.md#issuesamelioration-annexe"><b>Améliorations Annexe</b></a></li>
<br>
  
![diagramme](./assets/labd.png)


# Documentation PROXMOX
Installation et configuration de PROXMOX dans l'infrastructure LAN de mon homelab

### 1. CONFIGURATION PROXMOX
<details>
  <summary>
    Détails (cliquez pour dérouler)
  </summary><br>
  <b>(!) POUR LE MOMENT SCREENSHOT SEULEMENT EN COURS DE DOCUMENTATION (!)</b><br><br>

Une fois Proxmox VE 9.2 installé sur le serveur (pour mon cas ça sera un vieux PC portable recyclé) il faut accéder à son interface web (IP de la machine:8006) ici 192.168.0.12:8006
<img src="./assets/proxmox/image.png" />
<img src="./assets/proxmox/image1.png" />
<img src="./assets/proxmox/image2.png" />
<img src="./assets/proxmox/image3.png" />
<img src="./assets/proxmox/image4.png" />
<img src="./assets/proxmox/image5.png" />
<img src="./assets/proxmox/image6.png" />
<img src="./assets/proxmox/image7.png" />

apt update && apt dist-upgrade -y pour vérifier que tout est bon encore une fois
<img src="./assets/proxmox/image8.png" />
<img src="./assets/proxmox/image9.png" />
</details>

### 2. CARTE GRAPHIQUE ET INTEGRATION DE L'HÔTE PROXMOX DANS LE LAN
<details>
  <summary>
    Détails (cliquez pour dérouler)
  </summary><br>
  <b>(!) POUR LE MOMENT SCREENSHOT SEULEMENT EN COURS DE DOCUMENTATION (!)</b><br><br>
Commande pour detecter la présence des carte graphique, (hors celui présent sur le chipset du processeur)
`lspci -nnk | grep -A 3 -i vga`
<img src="./assets/proxmox/image10.png" />
présence de la gtx 1650 -> possibilité de faire du passthrough vers une VM plus tard, ou une IA locale
  
#

Basculer et intégrer l'hôte PROXMOX dans le LAN
<img src="./assets/proxmox/image11.png" />
<img src="./assets/proxmox/image12.png" />
<img src="./assets/proxmox/image13.png" />
<img src="./assets/proxmox/image14.png" />
<img src="./assets/proxmox/image15.png" />
<img src="./assets/proxmox/image16.png" /><br>
Ping vers l'extérieur (internet) pour confirmer que l'hôte est bien isolé<br>
<img src="./assets/proxmox/image17.png" />
</details>

### 3. CREATION CONTENEUR LXC
<details>
  <summary>
    Détails (cliquez pour dérouler)
  </summary><br>
  <b>(!) POUR LE MOMENT SCREENSHOT SEULEMENT EN COURS DE DOCUMENTATION (!)</b><br><br>

<img src="./assets/proxmox/image18.png" />
<img src="./assets/proxmox/image19.png" />
<img src="./assets/proxmox/image20.png" />
<img src="./assets/proxmox/image21.png" />
<img src="./assets/proxmox/image22.png" />
<img src="./assets/proxmox/image23.png" />
<img src="./assets/proxmox/image24.png" />
<img src="./assets/proxmox/image25.png" />
<img src="./assets/proxmox/image26.png" />
<img src="./assets/proxmox/image27.png" />
<img src="./assets/proxmox/image28.png" />
</details>

### 4. CREATION VM Windows Server
<details>
  <summary>
    Détails (cliquez pour dérouler)
  </summary><br>
  <b>(!) POUR LE MOMENT SCREENSHOT SEULEMENT EN COURS DE DOCUMENTATION (!)</b><br><br>

<img src="./assets/proxmox/image29.png" />
</details>


# Documentation LXC pour Samba/NFS

Configuration du conteneur

# Documentation Windows SERVER

Configuration du serveur

# Documentation Lan cache

## ISSUES/AMELIORATION ANNEXE
- [Faire disparaître le pop up No subscription](https://github.com/root-orion-ops/homelab-star.lan/issues/1#issue-5552468003)
- [Ajouter le support du wi-fi](https://github.com/root-orion-ops/homelab-star.lan/issues/2)
- [Empêcher la mise en veille/shutdown à la fermeture du capot](https://github.com/root-orion-ops/homelab-star.lan/issues/3)
- [Routage NAT](https://github.com/root-orion-ops/homelab-star.lan/issues/4)
