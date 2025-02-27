# 🚀 CmdAdmin - Lancez CMD en mode Admin depuis n'importe quel dossier

[![Licence](https://img.shields.io/badge/Licence-MIT-blue.svg)](LICENSE)
[![Version](https://img.shields.io/badge/Version-1.2.0-green.svg)]()
[![Windows](https://img.shields.io/badge/Windows-10%2F11-success.svg)]()

**Ouvrez instantanément l'Invite de Commandes en mode Administrateur depuis la barre d'adresse de l'Explorateur Windows**  
*(Sans raccourcis clavier complexes !)*

---

## 📋 Table des matières
- [Fonctionnalités](#⭐-fonctionnalités)
- [Prérequis](#⚙️-prérequis)
- [Installation](#🚀-installation)
- [Utilisation](#🎯-utilisation)
- [Désinstallation](#🗑️-désinstallation)
- [Dépannage](#🔧-dépannage)
- [Contribuer](#🤝-contribuer)
- [Licence](#📄-licence)

---

## ⭐ Fonctionnalités
- **Exécution en un mot** : Tapez `cmdadmin` dans n'importe quelle barre d'adresse de l'Explorateur
- **Conservation du dossier courant** : CMD s'ouvre dans le répertoire actuel
- **Compatibilité totale** : Windows 10/11 (32 et 64 bits)
- **Aucun logiciel tiers** : Solution native PowerShell + Registre

---

## ⚙️ Prérequis
- Droits d'**Administrateur** sur le PC
- PowerShell 5.1+ (activé par défaut)
- UAC (Contrôle de compte d'utilisateur) au niveau **2/4 minimum**

---

## 🚀 Installation

### Méthode 1 : Script Automatique (Recommandé)
1. Téléchargez [install_cmdadmin.bat](https://lien-vers-votre-fichier/install_cmdadmin.bat)
2. **Exécutez en Admin** :

Right-click > Exécuter en tant qu'administrateur

### Méthode 2 : Manuellement
1. Créez `cmdadmin.bat` :

@echo off

powershell -Command "Start-Process cmd -Verb RunAs -ArgumentList '/k cd /d %CD%'"

2. Placez-le dans `C:\Windows\System32\`  
3. Testez dans l'Explorateur :

cmdadmin


---

## 🎯 Utilisation
1. Ouvrez un dossier dans l'**Explorateur de fichiers**
2. Dans la **barre d'adresse** :


cmdadmin

3. Validez l'alerte **UAC**  
4. ✅ CMD s'ouvre en admin dans ce dossier !

---

## 🗑️ Désinstallation
1. Supprimez le fichier :

del C:\Windows\System32\cmdadmin.bat

2. (Optionnel) Nettoyez le registre :

Windows Registry Editor Version 5.00

[-HKEY_CLASSES_ROOT\Directory\Background\shell\AdminCmd]


---

## 🔧 Dépannage
| Problème                          | Solution                          |
|-----------------------------------|-----------------------------------|
| Fenêtre qui se ferme instantanément | Vérifiez l'[UAC](https://support.microsoft.com/fr-fr/windows/paramètres-du-contrôle-de-compte-d-utilisateur-ua-c7b045b5-6bdb-8d1e-dde8-5d729326b2d3) |
| Erreur "Fichier introuvable"      | Vérifiez le PATH système          |
| Accès refusé                      | Exécutez l'installation en Admin  |

---

## 🤝 Contribuer
1. Forkez le projet  
2. Créez une branche (`git checkout -b feature/amélioration`)  
3. Commitez (`git commit -m 'Nouvelle fonctionnalité'`)  
4. Pushez (`git push origin feature/amélioration`)  
5. Ouvrez une **Pull Request**

---

## 📄 Licence
Distribué sous licence MIT. Voir [LICENSE](LICENSE) pour plus de détails.

---

**Développé avec ❤️ par [KHERRAF Anis](https://github.com/1nis)**  
📧 Contact : anis@kherraf.fr | [💼 LinkedIn](https://linkedin.com/in/anis-kherraf/)
