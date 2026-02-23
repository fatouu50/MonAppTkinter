# 🕸️ Algorithme des Graphes
### *Application desktop de visualisation et d'analyse de graphes*

[![Python](https://img.shields.io/badge/Python-3.8+-blue?style=flat-square&logo=python)](.)
[![Tkinter](https://img.shields.io/badge/GUI-Tkinter-green?style=flat-square)](.)
[![License](https://img.shields.io/badge/License-MIT-lightgrey?style=flat-square)](.)
[![Dependencies](https://img.shields.io/badge/Dependencies-None-brightgreen?style=flat-square)](.)

> Application graphique permettant de créer, visualiser et analyser des graphes orientés et non orientés, avec implémentation des principaux algorithmes de la théorie des graphes.

---

## 📸 Fonctionnalités

### ✏️ Création de graphes
- Ajout de **sommets** par clic sur le canvas
- Ajout d'**arêtes orientées** (avec flèches directionnelles)
- Ajout d'**arêtes non orientées**
- Gestion multi-onglets (plusieurs graphes simultanés)
- Étiquetage automatique des arêtes (A1, A2, ...)

### 💾 Gestion des fichiers
- **Nouveau** graphe dans un onglet dédié
- **Ouvrir** un graphe depuis un fichier `.py`
- **Enregistrer** / **Enregistrer sous** au format `.py`
- **Fermer** un onglet sans affecter les autres

### 📊 Matrices
| Matrice | Description |
|:---|:---|
| **Matrice d'Adjacence** | Représentation des connexions entre sommets |
| **Matrice d'Incidence** | Représentation des relations sommets-arêtes |

### 🔍 Algorithmes implémentés
| Algorithme | Description |
|:---|:---|
| **Chaîne Hamiltonienne** | Parcours passant par chaque sommet exactement une fois |
| **Chaîne Eulérienne** | Parcours empruntant chaque arête exactement une fois (Algorithme de Fleury) |
| **Parcours en Largeur (BFS)** | Exploration niveau par niveau avec arbre couvrant |
| **Dijkstra** | Plus court chemin entre deux sommets avec poids sur les arêtes |
| **Trouver Chemins** | Tous les chemins possibles entre deux sommets donnés |

---

## 🛠️ Prérequis

- **Python 3.8** ou supérieur
- **Tkinter** (inclus avec Python sur Windows et macOS)

> ⚠️ **Linux uniquement** — Tkinter doit parfois être installé séparément :
> ```bash
> # Ubuntu / Debian
> sudo apt-get install python3-tk
>
> # Fedora
> sudo dnf install python3-tkinter
> ```

---

## ⚡ Installation & Lancement

### 1. Cloner le projet
```bash
git clone https://github.com/fatouu50/MonAppTkinter.git
cd MonAppTkinter
```

### 2. Créer un environnement virtuel *(recommandé)*
```bash
# Sur Windows
python -m venv venv
.\venv\Scripts\activate

# Sur macOS / Linux
python3 -m venv venv
source venv/bin/activate
```

### 3. Vérifier les dépendances
```bash
# Aucune installation requise — uniquement la bibliothèque standard Python
python -c "import tkinter; print('Tkinter OK')"
```

### 4. Lancer l'application
```bash
python main.py
```

---

## 🗂️ Structure du Projet

```
MonAppTkinter/
├── main.py              # Application principale
├── requirements.txt     # Dépendances (stdlib uniquement)
└── README.md            # Documentation
```

---

## 📖 Guide d'utilisation

### Créer un graphe
1. **Fichier → Nouveau** pour ouvrir un onglet vide
2. **Création → Graphe → Sommet** puis cliquer sur le canvas pour placer des sommets
3. **Création → Graphe → Arête → Orientée** (ou Non-orientée), puis cliquer sur deux sommets pour les relier

> ⚠️ Un onglet ne peut pas contenir à la fois des arêtes orientées et non orientées.

### Lancer un algorithme
1. Créer ou ouvrir un graphe
2. **Exécution → Algorithme de Dijkstra** (saisir les poids dans la fenêtre qui s'ouvre)
3. **Affichage → Chaînes → Hamiltonienne** ou **Eulérienne**
4. **Exécution → Parcours en largeur** pour visualiser l'arbre couvrant

### Sauvegarder un graphe
- **Fichier → Enregistrer sous** → choisir un emplacement `.py`
- Le fichier peut être rouvert avec **Fichier → Ouvrir**

---

## 📋 Format de sauvegarde

Les graphes sont sauvegardés en Python natif, ce qui les rend lisibles et modifiables à la main :

```python
sommets = [(150, 200), (300, 100), (450, 200)]
aretes = [(0, 1, False), (1, 2, True), (0, 2, False)]
```

Chaque arête est un tuple `(sommet_départ, sommet_arrivée, orientée)`.

---

## ⚠️ Limitations connues

- La détection de proximité des sommets utilise un seuil fixe de 20px
- L'algorithme de Dijkstra commence toujours depuis le sommet 1
- L'affichage de l'arbre couvrant utilise des positions prédéfinies pour les grands graphes

---

*Built with 🐍 Python & Tkinter*
