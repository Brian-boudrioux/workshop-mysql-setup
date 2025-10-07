## 🎯 Objectifs
- Installer MySQL sur Windows, macOS et Linux (Ubuntu / Debian).
- Vérifier que le serveur tourne.
- Se connecter avec l’outil en ligne de commande `mysql`.
- Créer une base de données de test.

## 🧰 Prérequis
- Accès administrateur / droits sudo.
- Internet pour télécharger les paquets.
- Terminal / invite de commandes.

---

## 1. Windows

1. Aller sur le site officiel de MySQL (mysql.com) → Downloads → MySQL Community Server → télécharger MySQL Installer pour Windows.  
2. Lancer l’installateur, choisir les composants “MySQL Server” + “Workbench” + “Shell” (optionnel).  
3. Lors de l’installation, définir un mot de passe pour l’utilisateur `root`.  
4. Terminer l’installation et lancer le service MySQL via le panneau de services Windows ou via l’installateur.  
5. Ouvrir une invite de commandes (cmd) et exécuter :
   ```bash
   mysql -u root -p
   ```
6. Créer une base de données de test :
   ```sql
   CREATE DATABASE test_db;
   SHOW DATABASES;
   ```

---

## 2. macOS

1. Si Homebrew est installé, dans le terminal :
   ```bash
   brew update
   brew install mysql
   ```
2. Démarrer MySQL :
   ```bash
   brew services start mysql
   ```
3. Vérifier que MySQL tourne :
   ```bash
   brew services list
   ```
4. Se connecter via le shell :
   ```bash
   mysql -u root
   ```
5. Créer une base :
   ```sql
   CREATE DATABASE test_db;
   ```

---

## 3. Linux (Ubuntu / Debian)

1. Mettre à jour les paquets :
   ```bash
   sudo apt update
   sudo apt upgrade
   ```
2. Installer MySQL server :
   ```bash
   sudo apt install mysql-server
   ```
3. Démarrer le service :
   ```bash
   sudo systemctl start mysql
   sudo systemctl enable mysql
   ```
4. Vérifier le statut :
   ```bash
   sudo systemctl status mysql
   ```
5. Se connecter au shell MySQL :
   ```bash
   sudo mysql
   ```
6. Créer une base de données de test :
   ```sql
   CREATE DATABASE test_db;
   SHOW DATABASES;
   ```

---

## Vérifications & dépannage

- Assurez-vous que le port 3306 est ouvert (par défaut MySQL).  
- Si la connexion refuse, vérifier que le service tourne.  
- Si “Access denied”, vérifier les privilèges de l’utilisateur root.  
- En cas d’erreurs spécifiques, consulter les logs MySQL (`/var/log/mysql`).

---

✅ **Fin de l’atelier d’installation**  
Tous les systèmes devraient maintenant disposer de MySQL opérationnel et d’une base `test_db`.
