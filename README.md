# Agora Francia — Plateforme e-commerce d'objets uniques

> Projet académique réalisé dans le cadre de la Piscine 2025  
> Stack : PHP · MySQL · Bootstrap 5 · JavaScript · HTML5/CSS3

## Présentation

**Agora Francia** est une plateforme web de mise en vente d'objets uniques. Les utilisateurs peuvent naviguer, filtrer et acheter des articles via trois modes de vente distincts. Le projet implémente une gestion complète des rôles utilisateurs et un système de notifications.

## Fonctionnalités principales

- **3 modes de vente** : achat immédiat, négociation vendeur-acheteur, enchères (meilleure offre)
- **3 rôles utilisateurs** : acheteur, vendeur, administrateur — chacun avec son espace dédié
- Catalogue avec filtres dynamiques (catégorie, type de vente), moteur de recherche et tri par prix
- Gestion du panier et simulation de paiement
- Système de notifications personnalisables
- Tableau de bord administrateur (gestion des utilisateurs et des articles)
- Mise en vente d'articles avec images, description, prix et vidéo optionnelle

## Stack technique

| Couche              | Technologies                         |
|---                  |---                                   |
| Back-end            | PHP 8.3                              |
| Base de données     | MySQL 9.1 (via phpMyAdmin)           |
| Front-end           | HTML5, CSS3, Bootstrap 5, JavaScript |
| Environnement local | WAMP / XAMPP                         |

---
## Architecture du systeme

<img width="1652" height="1070" alt="Story Board" src="https://github.com/user-attachments/assets/d1d62055-f3d1-49c6-bf05-e295aa6e4b43" />
<img width="993" height="1013" alt="Conception du Back " src="https://github.com/user-attachments/assets/01cf2bff-73c8-4164-8a81-307db92c614e" />
<img width="485" height="970" alt="Architecture du systeme" src="https://github.com/user-attachments/assets/f94a817e-066f-4f8a-83a9-bc87f5594c2b" />

## Design du site
Image de vue du site pour l'accueil, le panier, la validation de commande, et le catalogue d'article
<img width="1791" height="767" alt="Panier" src="https://github.com/user-attachments/assets/fa068b81-5417-497a-a4cb-2778cbd8ab7a" />
<img width="1876" height="863" alt="Page-accueil" src="https://github.com/user-attachments/assets/acc821e3-4419-4af4-a32e-507f05325fa5" />
<img width="1012" height="623" alt="Comfirmation" src="https://github.com/user-attachments/assets/f3578f58-01bd-483f-809a-38ed262090af" />
<img width="1874" height="827" alt="Catalogue" src="https://github.com/user-attachments/assets/0ede0f22-c92a-47dc-a257-8266b5721ade" />



## Installation en local

### Prérequis

- [WAMP](https://www.wampserver.com/) ou [XAMPP](https://www.apachefriends.org/) installé sur ta machine
- PHP 8.x et MySQL inclus dans WAMP/XAMPP

### Étapes

**1. Copier les fichiers du projet**

Place le dossier `agora-main` dans le répertoire web de WAMP/XAMPP :

```
# WAMP
C:\wamp64\www\agora-main\

# XAMPP
C:\xampp\htdocs\agora-main\
```

**2. Démarrer les serveurs**

Lance WAMP ou XAMPP et assure-toi que les modules **Apache** et **MySQL** sont bien démarrés (icônes vertes).

**3. Créer la base de données**

- Ouvre **phpMyAdmin** : [http://localhost/phpmyadmin](http://localhost/phpmyadmin)
- Crée une nouvelle base de données nommée **agora** (encodage : `utf8mb4_unicode_ci`)
- Importe les fichiers SQL dans cet ordre :

```
acheteur.sql
articles.sql
items.sql        
negociations.sql
notifications.sql
offres.sql
panier_nego.sql
```

**4. Lancer le site**

Ouvre ton navigateur et va sur :

```
http://localhost/evaa/main/accueil.php
```
## Comptes de test

La base de données fournie contient des comptes pré-remplis pour tester les 3 rôles :

| Rôle     | Email                            | Mot de passe |
|---       |---                               |---           |
| Acheteur | *(créer via register.php)*       | —            |
| Vendeur  | bertille.aiderobotique@gmail.com | *(voir BDD)* |
| Admin    | j.clt@ece.fr                     | *(voir BDD)* |

> Les mots de passe sont hashés en bcrypt dans la base de données. Pour tester rapidement, le plus simple est de créer un nouveau compte via la page `/register.php`.

## Structure des fichiers

main/
├── accueil.php             # Page d'accueil
├── parcourir.php           # Catalogue avec filtres et recherche
├── articles.php            # Fiche détail d'un produit
├── login.php / register.php
├── panier.php / checkout.php
├── compte.php              # Espace utilisateur (adapté au rôle)
├── espace_acheteur.php
├── espace_vendeur.php
├── espace_admin.php
├── notifications.php
├── ajouter_produit.php
├── mes_ventes.php
├── negociations.php (logique)
├── articles/               # Images des objets en vente
└── image accueil/          # Assets de la page d'accueil

## Ce que j'ai appris

- Conception et implémentation d'un système multi-rôles en PHP natif
- Modélisation d'une base de données relationnelle MySQL avec plusieurs tables liées
- Gestion de sessions PHP pour l'authentification
- Intégration d'une logique métier complexe (3 modes de vente avec workflows différents)
- Utilisation de Bootstrap 5 pour une interface responsive

## Auteur

Projet réalisé dans le cadre de la Piscine 2025
Eva Martins et son équipe 
