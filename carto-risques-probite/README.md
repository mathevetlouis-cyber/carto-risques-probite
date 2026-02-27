# 🛡️ Cartographie des Risques d'Atteintes à la Probité

Outil professionnel de cartographie et d'analyse des risques d'atteintes à la probité pour les collectivités territoriales françaises.

![Version](https://img.shields.io/badge/version-2.1_Pro-blue)
![License](https://img.shields.io/badge/licence-MIT-green)
![HTML](https://img.shields.io/badge/HTML-CSS--JS-orange)

## 📋 Description

Cet outil permet aux collectivités territoriales, centres de gestion (CDG), établissements publics et référents déontologues de réaliser et gérer leur **cartographie des risques d'atteintes à la probité**, conformément aux recommandations de l'Agence Française Anticorruption (AFA) et de la Haute Autorité pour la Transparence de la Vie Publique (HATVP).

### Fonctionnalités principales

- **Gestion multi-cartographies** : créez, dupliquez, renommez et gérez plusieurs cartographies indépendantes
- **Saisie complète des risques** : processus, scénarios, types de risques (corruption, favoritisme, prise illégale d'intérêts, etc.), cotation probabilité × gravité
- **Moyens de maîtrise** : organisationnels, humains et techniques, avec système de suggestions personnalisables
- **Matrice de criticité** interactive (5×5) avec visualisation des risques par cellule
- **Tableau de bord statistique** : répartition par criticité, par processus, par type de risque
- **Filtres et tri** : recherche textuelle, filtrage par processus et par niveau de criticité
- **Export** : JSON (import/export), DOC (Word), PDF (impression)
- **Paramétrage complet** : processus, types de risques et suggestions entièrement personnalisables

## 🚀 Démarrage rapide

### Utilisation en ligne

Ouvrez directement le fichier `index.html` dans votre navigateur. Aucune installation requise.

```
# Cloner le dépôt
git clone https://github.com/VOTRE-UTILISATEUR/carto-risques-probite.git

# Ouvrir dans le navigateur
open index.html
```

### Déploiement sur GitHub Pages

1. Forkez ce dépôt
2. Allez dans **Settings** → **Pages**
3. Sélectionnez la branche `main` et le dossier `/ (root)`
4. Votre cartographie sera accessible à `https://VOTRE-UTILISATEUR.github.io/carto-risques-probite/`

## 🏗️ Architecture

L'application est un fichier HTML unique (Single Page Application) sans dépendance serveur :

```
carto-risques-probite/
├── index.html          # Application complète (HTML + CSS + JS)
├── README.md           # Documentation
├── LICENSE             # Licence MIT
└── .gitignore          # Fichiers ignorés par Git
```

### Technologies

- **HTML5 / CSS3 / JavaScript** (vanilla, aucun framework)
- **localStorage** pour la persistance des données côté client
- **FileSaver.js** (CDN) pour les exports de fichiers

## 📊 Structure des données

Chaque risque contient les champs suivants :

| Champ | Description |
|-------|-------------|
| `process` | Processus métier concerné |
| `scenario` | Description du scénario de risque |
| `riskType` | Type(s) de risque / responsabilité |
| `probability` | Probabilité d'occurrence (1 à 5) |
| `impact` | Gravité / impact (1 à 5) |
| `criticity` | Risque brut = probabilité × gravité |
| `mitigationOrg` | Moyens de maîtrise organisationnels |
| `mitigationHum` | Moyens de maîtrise humains |
| `mitigationTech` | Moyens de maîtrise techniques |
| `netRisk` | Risque résiduel après maîtrise (1 à 5) |
| `actions` | Actions préventives/correctives |

### Échelle de criticité

| Niveau | Score | Couleur |
|--------|-------|---------|
| Faible | 1 – 4 | 🟢 Vert |
| Moyen | 5 – 12 | 🟡 Jaune |
| Élevé | 15 – 25 | 🔴 Rouge |

## 🔧 Personnalisation

### Processus par défaut

L'outil est pré-configuré avec des processus typiques des collectivités territoriales : Concours, RH interne, Commande publique, Gestion financière, Élus locaux, Subventions, etc.

### Types de risques par défaut

Corruption, Favoritisme, Concussion, Prise illégale d'intérêts, Détournement de fonds publics, Trafic d'influence, Conflit d'intérêts, Pantouflage, RGPD.

Tous ces paramètres sont modifiables via l'onglet **⚙️ Paramètres**.

## 📤 Import / Export

- **Export JSON** : sauvegarde complète de la cartographie (risques + paramètres)
- **Import JSON** : restauration ou partage de cartographies entre utilisateurs
- **Export DOC** : génération d'un document Word avec le tableau des risques
- **Export PDF** : impression via la fonction `window.print()`

## 🔒 Confidentialité

Toutes les données sont stockées **localement** dans le navigateur (localStorage). **Aucune donnée n'est envoyée à un serveur.** Cela garantit la confidentialité des informations sensibles relatives aux risques de probité.

## 👤 Auteur

**Louis MATHEVET-BIDINI**
- Président de l'AP2DFP (Association pour la Promotion et le Développement de la Déontologie dans la Fonction Publique)
- Secrétaire Général National de l'ARDT (Association des Référents Déontologues Territoriaux)
- Doctorant en droit public – Université de Lorraine

## 📄 Licence

Ce projet est distribué sous licence MIT. Voir le fichier [LICENSE](LICENSE) pour plus de détails.

## 🤝 Contribuer

Les contributions sont les bienvenues ! N'hésitez pas à :

1. Forker le projet
2. Créer une branche (`git checkout -b feature/amelioration`)
3. Commiter vos changements (`git commit -m 'Ajout d'une fonctionnalité'`)
4. Pousser la branche (`git push origin feature/amelioration`)
5. Ouvrir une Pull Request

## 📞 Contact

Pour toute question relative à l'utilisation de cet outil dans le cadre de vos obligations déontologiques, contactez l'AP2DFP.
