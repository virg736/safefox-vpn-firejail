<h1 align="center">SafeFox VPN Firejail</h1>

<p align="center">
<img src="firefox.PNG" alt="Illustration SafeFox VPN" style="max-width: 100%; height: auto;" />
</p>

<p align="center">
<a href="https://opensource.org/licenses/MIT">
<img src="https://img.shields.io/badge/License-MIT-blue.svg" alt="Licence MIT" />
</a>
<img src="https://img.shields.io/badge/stabilité-stable-brightgreen" alt="Stabilité stable" />
</p>

<p align="center"><i>© 2025 Virginie Lechene — Tous droits réservés</i><br/>
<i>Reproduction interdite sans autorisation. Usage pédagogique uniquement.</i></p>

<p align="center">
<a href="https://creativecommons.org/licenses/by-nd/4.0/">
<img src="https://licensebuttons.net/l/by-nd/4.0/88x31.png" alt="Licence CC BY-ND 4.0" />
</a>
</p>

---

# SafeFox VPN Firejail

Navigateur sécurisé basé Firejail et un VPN, conçu pour les tests d'intrusion, l’analyse web et la cybersécurité.

---

## Sommaire

- [Avertissement](#avertissement)
- [Objectif](#objectif)
- [Fonctionnement global](#fonctionnement-global)
- [Configuration mise en place](#configuration-mise-en-place)
- [Prérequis](#prérequis)
- [Commandes à exécuter](#commandes-à-exécuter)
- [VPN : ce qu’il faut comprendre](#vpn--ce-quil-faut-comprendre)
- [À savoir](#à-savoir)
- [Licence](#licence)

---

## Avertissement

**Usage strictement pédagogique.**
L’auteure décline toute responsabilité en cas d’utilisation malveillante ou illégale.

---

## Objectif

Fournir une méthode simple pour lancer un navigateur **sécurisé et isolé**, dans le cadre :
- de tests de sécurité (pentests),
- d’analyses web ou réseau,
- de formations à la cybersécurité.

---

## Fonctionnement global

- **VPN** : chiffre le trafic et masque l’adresse IP réelle.
- **Firejail** : bac de sable (sandbox) Linux restreignant l’environnement de Firefox.
- **Option `--private`** : empêche tout accès aux fichiers personnels.
- **Alias `safefox`** : permet un lancement rapide depuis terminal.

---

## Configuration mise en place

| Élément | Statut attendu |
|---------------------------------|----------------|
| VPN actif | ✅ |
| Firejail installé | ✅ |
| Firefox installé | ✅ |
| Alias `safefox` fonctionnel | ✅ |
| Exécution en utilisateur normal| ✅ |

---

## Prérequis

- **Système** : Kali Linux, Debian ou Ubuntu
- **Logiciels nécessaires** :
- `firejail`
- `firefox-esr`
- Un **client VPN actif** (ex : NordVPN, ProtonVPN)
- Les **droits sudo** sont requis pour l'installation

---

## Commandes à exécuter

### 1. Télécharger le script

En tant qu’utilisateur (non-root) :

curl -L https://raw.githubusercontent.com/virg736/safefox-vpn-firejail/main/Script-safefox-vpn-firejail -o install-safefox.sh


2. Rendre le script exécutable
chmod +x install-safefox.sh

3. Lancer le script
./install-safefox.sh

💡 Le script installe Firejail, Firefox-Esr et configure l’alias safefox.

Vérification après installation

Une fois l’installation terminée, ouvrez un nouveau terminal ou rechargez le fichier de configuration pour activer l'alias safefox :

source ~/.zshrc

ou
source ~/.bashrc

Ensuite, lancez :
safefox

---

 ## VPN : ce qu’il faut comprendre


Ce script ne configure pas de VPN. Il part du principe que vous disposez déjà un VPN fonctionnel.


Deux scénarios possibles :

1. VPN installé sur l’ordinateur hôte :
- La machine virtuelle (ex. Kali VirtualBox) accède à  Internet via NAT.
- Dans ce cas, le  VPN de l’hôte protège également la VM.


2. VPN installé directement dans la VM :
L’utilisateur lance le VPN depuis Kali.

Commande de exemple :

nordvpn connecte

Dans tous les cas, le VPN doit être activé avant d’utiliser safefox.

---

# À savoir

Le script vérifie que vous n’êtes pas en tant que root

Il détecte automatiquement le fichier de configuration .bashrc ou .zshrc

Il ajoute l’alias safefox='firejail --private firefox'

Firefox est lancé sans cookies ni historique (mode isolé)

Pour garantir une navigations sécuritée, il est recommandé d’utiliser un VPN fiable.

---

 ## Licence

le Script est publié sous la licence MIT

Ce projet est exclusivement destiné à des fins éducatives, dans le cadre d'une formation en cybersécurité.
 L’auteure ne cautionne ni n’autorise l’utilisation de ces techniques en dehors d’un cadre légal strictement défini.
 Toute utilisation non autorisée est interdite et relève de la seule responsabilité de l’utilisateur.

---

##  Auteur / Droits

## Droits sur les contenus visuels

Les visuels, images ou illustrations présents dans ce dépôt sont la propriété exclusive de l’auteure.
Toute reproduction, modification ou réutilisation sans accord préalable est strictement interdite.
© 2025 Virginie Lechene – Tous droits réservés.



















  

