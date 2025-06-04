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
- [Structure du projet](#structure-du-projet)
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
```bash
curl -L https://raw.githubusercontent.com/virg736/safefox-vpn-firejail/main/Script-safefox-vpn-firejail -o install-safefox.sh





  

