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

Navigateur sécurisé via Firejail + VPN, pensé pour les pentests, l’analyse web et la cybersécurité.

---

## Sommaire

- [Avertissement](#avertissement)
- [Objectif](#objectif)
- [Fonctionnement global](#fonctionnement-global)
- [Configuration mise en place](#configuration-mise-en-place)
- [Prérequis](#prérequis)
- [Commandes à exécuter](#commandes-à-exécuter)
- [Vérification après installation](#vérification-après-installation)
- [VPN : ce qu’il faut comprendre](#vpn--ce-quil-faut-comprendre)
- [À savoir](#à-savoir)
- [Licence](#licence)

---

## Avertissement

**Usage strictement pédagogique.**
L’auteure décline toute responsabilité en cas d’usage malveillant ou illégal.

---

## Objectif

Fournir une méthode simple pour lancer un navigateur **sécurisé et isolé**, dans le cadre :
- de tests de sécurité (pentest),
- d’analyses web ou réseau,
- de formation à la cybersécurité.

---

## Fonctionnement global

- **VPN** : chiffre le trafic et masque l’adresse IP réelle.
- **Firejail** : sandbox Linux restreignant l’environnement de Firefox.
- **Option `--private`** : empêche tout accès aux fichiers personnels.
- **Alias `safefox`** : permet un lancement rapide via terminal.

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
- **Logiciels** :
- `firejail`
- `firefox-esr`
- un **client VPN actif** (ex : NordVPN, ProtonVPN)
- **Accès sudo** requis pour l'installation

---

## Commandes à exécuter

### 1. Télécharger le script

En tant qu’utilisateur (non-root) :

curl -L https://raw.githubusercontent.com/virg736/safefox-vpn-firejail/main/Script-safefox-vpn-firejail -o install-safefox.sh


2. Rendre le script exécutable
chmod +x install-safefox.sh

3. Lancer le script
./install-safefox.sh

💡 Le script installe firejail, firefox-esr et configure l’alias safefox.

Vérification après installation

Après l’installation, ouvrez un nouveau terminal ou rechargez le fichier de configuration :

source ~/.zshrc

ou
source ~/.bashrc

Ensuite, lancez :
safefox

---

 ## VPN : ce qu’il faut comprendre


Le script ne configure pas de VPN. Il suppose que vous utilisez déjà un VPN fonctionnel.


Deux possibilités :

1. VPN sur l’ordinateur hôte :
La VM (ex. Kali VirtualBox) utilise Internet via NAT.

Le VPN de l’hôte couvre aussi la VM.


2. VPN directement installé dans la VM :
L’utilisateur lance le VPN depuis Kali.

Commande exemple :

nordvpn connecte

Dans tous les cas, le VPN doit être activé avant d’utiliser safefox.

---

# À savoir

Le script vérifie que vous n’êtes pas en root

Il détecte automatiquement .bashrc ou .zshrc

Il ajoute l’alias safefox : firejail --private firefox

Firefox s’ouvre sans cookies ni historique

Pour des raisons de sécurité, il est conseillé d’utiliser un VPN sérieux et fiable

---

 ## Licence

Projet sous licence MIT

Autrice : Virginie










  

