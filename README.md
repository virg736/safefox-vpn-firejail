# safefox-vpn-firejail
Navigateur sécurisé via Firejail+VPN, pensépour les pentest, l'analyse web et la cybesécurité.

# Sommaire
- [Objectif](#-objectif)
- [Configuration mise en place](#️-configuration-mise-en-place)
- [Comment ça fonctionne](#-comment-ça-fonctionne)
- [Comment l’utiliser](#-comment-lutiliser)
- [Prérequis](#-prérequis)
- [Structure du projet](#-structure-du-projet)
- [À savoir](#-à-savoir)
- [Script d'installation](#-script-dinstallation)
- [Initialisation du projet Git](#-initialisation-du-projet-git)

___

# Configuration mise en place

  Élément                            
 
 VPN actif  ✅          
 Firejail installé ✅          
 Firefox isolé via `--private`✅          
 Alias `safefox` fonctionnel ✅          
  Utilisateur non-root ✅    


---

#  Comment ça fonctionne

- **VPN** : masque votre adresse IP et chiffre le trafic réseau.
- **Firejail** : isole Firefox dans un environnement restreint.
- **`--private`** : lance le navigateur sans accès à vos fichiers persos.
- **Alias `safefox`** : une commande simple pour lancer le tout.

---

# Comment l'utiliser

 1. Se connecter au VPN (ex : NordVPN, ProtonVPN)
nordvpn connect

2. Lancer le navigateur sécurisé
safefox

safefox est un alias pour firejail --private firefox

2. Lancer le navigateur sécurisé
safefox

safefox est un alias pour firejail --private firefox
Prérequis
Kali Linux

firejail

firefox ou chromium

Un client VPN installé et fonctionnel




  

