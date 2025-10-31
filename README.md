# 🎵 Créateur de Séquences Musicales

Une application web interactive et éducative permettant aux enfants de créer et d'écouter leurs propres séquences musicales par glisser-déposer.

## 🎯 Objectif

Offrir une expérience ludique et intuitive pour que les enfants découvrent la musique, le séquençage et les rythmes musicaux de manière interactive et amusante.

## ✨ Fonctionnalités

### 🎼 Palette d'Instruments
Quatre instruments distincts avec sons authentiques:
- **🥁 Kick** - Son grave et puissant (808 Kick)
- **🎸 Snare** - Caisse claire nette et percussive
- **🎹 Hi-Hat** - Charleston aigu et sec
- **🎺 Synth** - Son mélodique synthétique brillant

### 📍 Grille de Séquençage
- Grille de 8 pas pour construire votre séquence
- Glissez-déposez les instruments sur les cases
- Remplacez facilement un instrument en le déposant sur une case occupée
- Cliquez sur un instrument placé pour le supprimer
- Supporté en tactile (mobile/tablette)

### 🎛️ Contrôles
- **▶️ Jouer** - Lance la lecture de la séquence
- **⏹️ Arrêter** - Arrête la lecture
- **🔄 Effacer Tout** - Réinitialise la grille

### 📊 Affichage en Temps Réel
- Indicateur du pas courant en lecture
- Affichage du tempo (120 BPM par défaut)
- Mise à jour visuelle immédiate lors de chaque modification

## 🚀 Utilisation

### Démarrage Rapide

1. Téléchargez ou clonez le repository
2. Ouvrez le fichier `index.html` dans un navigateur web moderne
3. C'est prêt! Aucune installation requise.

### Comment Créer une Séquence

1. **Glissez** un instrument depuis la palette à gauche
2. **Déposez** l'instrument sur une case vide dans la grille de séquençage
3. Continuez à ajouter d'autres instruments sur les autres pas
4. Appuyez sur **▶️ Jouer** pour écouter votre création
5. Modifiez en temps réel et écoutez les changements immédiatement!

### Conseils Créatifs

- Combinez les instruments pour créer des patterns intéressants
- Utilisez des séquences répétitives pour créer des rythmes
- Testez différentes combinaisons pour trouver votre groove
- Effacez et recommencez pour explorer différentes possibilités

## 💻 Technologies

### Frontend
- **HTML5** - Structure de l'application
- **CSS3** avec **Tailwind CSS CDN** - Design responsive et moderne
- **JavaScript (Vanilla)** - Logique et interactivité

### Audio
- **Tone.js** (CDN) - Synthèse audio et séquençage musical
  - MembraneSynth pour le Kick
  - MetalSynth pour le Hi-Hat
  - Synth pour le Snare et le Synth

### Drag & Drop
- **HTML5 Drag and Drop API** pour desktop
- **Touch Events** pour mobile/tablette

## 📁 Structure du Projet

```
musicalSeq/
├── index.html          # Fichier unique contenant HTML, CSS et JavaScript
└── README.md          # Ce fichier
```

## 🎨 Design

- **Palette de couleurs** adaptée aux enfants et aux petits garçons
- **Interface responsive** - Fonctionne sur desktop, tablette et mobile
- **Animations fluides** - Retours visuels pour chaque interaction
- **Gradient coloré** - Fond dynamique (bleu → cyan → lime)
- **Boutons ludiques** avec emojis

## 🔊 Sons

Tous les sons sont générés en temps réel avec Tone.js:

| Instrument | Type | Caractéristiques |
|-----------|------|------------------|
| 🥁 Kick | MembraneSynth | Grave (A0), decay long, punch authentique |
| 🎸 Snare | Synth + Filter | Square wave, highpass 5000Hz, crack net |
| 🎹 Hi-Hat | MetalSynth | Fréquence haute (250Hz), très court, sec |
| 🎺 Synth | PolySynth | Square wave, D4, enveloppe rapide |

**Tempo**: 120 BPM (battements par minute)

## 🌐 Compatibilité Navigateurs

- ✅ Chrome/Chromium (v60+)
- ✅ Firefox (v60+)
- ✅ Safari (v14+)
- ✅ Edge (v79+)
- ✅ Navigateurs mobiles (iOS Safari, Chrome Mobile)

**Requis**: Support de Web Audio API et ES6

## 📱 Responsive Design

- **Mobile** (< 768px) - Interface empilée verticalement
- **Tablette** (768px - 1024px) - Layout adapté avec columns
- **Desktop** (> 1024px) - Grille 4 colonnes optimale

## 🔧 Développement

### Modification des Instruments

Éditez la section `initializeSynths()` dans le fichier `index.html` pour:
- Changer les paramètres audio des synthétiseurs
- Ajouter de nouveaux instruments
- Modifier les enveloppes (ADSR)

### Modification des Couleurs

Changez les classes Tailwind dans:
- `<body>` - Gradient de fond
- `renderInstrumentsPalette()` - Couleurs des instruments
- `getColorForInstrument()` - Couleurs des cases de la grille

### Modification du Tempo

Changez la ligne:
```javascript
Tone.Transport.bpm.value = 120;
```

## 📝 Licence

Libre d'utilisation pour usage éducatif.

## 👨‍💻 Auteur

Créé avec [Claude Code](https://claude.com/claude-code)

---

**Amusez-vous à créer de la musique! 🎵✨**
