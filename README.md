# 🖧 Simulateur de Réseau Local – SAE 2.3 (BUT Informatique)

Projet réalisé dans le cadre de la SAE 2.3 – Réseaux à l'IUT Robert Schuman (Université de Strasbourg).

## 🎯 Objectifs pédagogiques

Ce projet en C vise à :

- Manipuler une structure de données représentant un graphe étiqueté
- Concevoir des structures pour modéliser un réseau local : stations, switchs, connexions
- Comprendre et simuler le protocole Ethernet (trames)
- Implémenter la diffusion de trames dans un réseau commuté
- Implémenter le protocole STP (Spanning Tree Protocol)

## 🧠 Fonctionnalités

### ✅ Étape 1 – Modélisation réseau
- Création de structures `Station`, `Switch`, `AdresseMac`, `AdresseIP`, `TrameEthernet`, etc.
- Affichage lisible des adresses MAC (hexadécimal) et IP (décimale pointée)
- Implémentation d’un graphe pour modéliser la topologie réseau

### 📂 Étape 2 – Fichier de configuration
- Chargement automatique d’un réseau depuis un fichier texte structuré
- Format lisible et réutilisable : nombre d’équipements, leur type, leurs adresses, connexions et coûts
- Exemple de format :
4 3
2;01:45:23:a6:f7:ab;8;1024
1;54:d6:a6:82:c5:23;130.79.80.21
...
0;1;4
0;2;19
0;3;4

### 📡 Étape 3 – Trames Ethernet
- Structure conforme au protocole Ethernet :
- Préambule, SFD, adresses, type, données, FCS
- Simulation d’envoi d’une trame entre deux stations à travers des switchs
- Affichage des trames en clair **et en hexadécimal**

### 🌐 Étape 4 – STP (Spanning Tree Protocol)
- Synchronisation automatique des switchs via échange de BPDU
- Suppression des boucles réseau par désactivation de ports
- Détermination de l’arbre couvrant via priorités et coûts
- Visualisation des ports actifs, bloqués, désignés, etc.

## 🛠️ Technologies

- 🧑‍💻 Langage : **C**
- 📁 Architecture modulaire : fichiers `.h` / `.c` séparés par fonctionnalités
- ⚙️ Compilation via **Makefile**
- 📚 Basé sur une librairie de graphes développée en M23 (théorie des graphes)

## 📝 Auteur

- [@Acelyamhrr](https://github.com/Acelyamhrr)

---

