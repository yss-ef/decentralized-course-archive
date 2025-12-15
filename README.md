# CoursNetX - Application Décentralisée d'Archivage de Cours

## À propos du projet

**CoursNetX** est une application décentralisée (dApp) développée dans le cadre de mon Projet de Fin d'Études pour la Licence en Ingénierie Logicielle à la FST d'Errachidia (noté **17/20**).

Ce projet explore le potentiel des technologies du **Web3** pour créer une plateforme d'archivage de ressources pédagogiques qui soit **sécurisée, transparente et résistante à la censure**. Contrairement aux systèmes centralisés traditionnels, CoursNetX redonne le contrôle des données aux utilisateurs en s'appuyant sur la blockchain Ethereum et le système de stockage décentralisé IPFS.

---

## Technologies utilisées

Ce projet a été construit avec les technologies suivantes :

* **Frontend :**
    * [**React.js**](https://reactjs.org/) : Bibliothèque JavaScript pour construire l'interface utilisateur.
    * [**Web3.js**](https://web3js.readthedocs.io/) : Pour la communication entre l'application et la blockchain Ethereum.
    * [**MetaMask**](https://metamask.io/) : Utilisé comme portefeuille pour l'authentification et la signature des transactions.
* **Backend (Smart Contract) :**
    * [**Solidity**](https://soliditylang.org/) : Langage de programmation pour écrire le contrat intelligent.
    * [**Ethereum**](https://ethereum.org/) : La blockchain sur laquelle le contrat est déployé.
* **Stockage :**
    * [**IPFS (InterPlanetary File System)**](https://ipfs.io/) : Pour le stockage distribué et immuable des fichiers de cours.
    * [**Pinata**](https://www.pinata.cloud/) : Service pour faciliter l'ancrage des fichiers sur IPFS.
* **Environnement de développement :**
    * [**Truffle Suite**](https://www.trufflesuite.com/) : Framework de développement pour la compilation, le déploiement et le test des smart contracts.
    * [**Ganache**](https://www.trufflesuite.com/ganache) : Blockchain locale pour le développement et les tests.

---

## Fonctionnalités

* **Authentification décentralisée** via le portefeuille MetaMask.
* **Gestion des rôles** (Administrateur, Enseignant, Étudiant) directement inscrite sur la blockchain.
* **Dépôt de cours sécurisé :** Les fichiers sont stockés sur IPFS, et seul leur hash (empreinte numérique) est enregistré sur la blockchain, garantissant l'intégrité et la permanence des données.
* **Consultation des cours** avec un système de droits d'accès géré par le smart contract.
* **Historique transparent :** Toutes les actions importantes (dépôt d'un cours, création d'une filière...) sont enregistrées comme des transactions publiquement vérifiables sur la blockchain.

---

## Installation et Lancement

Pour lancer ce projet en local, suivez les étapes ci-dessous.

### Prérequis

* Node.js (version 16 ou supérieure)
* Un portefeuille MetaMask installé sur votre navigateur
* Truffle et Ganache installés globalement :
    ```bash
    npm install -g truffle ganache
    ```

### Étapes d'installation

1.  **Clonez le dépôt :**
    ```bash
    git clone [https://github.com/yss-ef/NOM-DE-TON-DEPOT.git](https://github.com/yss-ef/NOM-DE-TON-DEPOT.git)
    cd NOM-DE-TON-DEPOT
    ```

2.  **Installez les dépendances (côté client) :**
    ```bash
    # Si ton projet a un dossier client/frontend, navigue dedans
    # cd client
    npm install
    ```

3.  **Configurez l'environnement :**
    * Lancez **Ganache** pour démarrer une blockchain locale.
    * Configurez MetaMask pour se connecter au réseau local Ganache.
    * Importez un ou plusieurs comptes de Ganache dans MetaMask.

4.  **Déployez le Smart Contract :**
    ```bash
    truffle migrate --reset
    ```

5.  **Lancez l'application React :**
    ```bash
    npm start
    ```

L'application devrait maintenant être accessible sur `http://localhost:3000`.
