# 🎧 Générateur de Compréhension Orale - Allemand# 🎧 Générateur de Compréhension Orale - Allemand



Application GUI pour créer automatiquement des exercices de compréhension orale en allemand avec vocabulaire, texte et audio MP3.Application interactive pour créer automatiquement des exercices de compréhension orale en allemand avec génération de vocabulaire et audio MP3.



## ✨ Fonctionnalités## ✨ Fonctionnalités



- 🤖 **Génération automatique** de vocabulaire (GPT-4o)- 🤖 **Génération automatique de vocabulaire** : L'IA génère 15 mots en allemand sur le thème de votre choix

- ✍️ **Saisie manuelle** avec traduction automatique- ✅ **Sélection interactive** : Cases à cocher pour choisir les mots à utiliser

- 📝 **Texte adapté** au niveau CECRL (A1-C2)- ➕ **Ajout de mots personnalisés** : Possibilité d'ajouter vos propres mots

- 🎤 **Audio MP3** avec voix homme/femme (Neural TTS)- 📝 **Génération de texte** : Création d'un texte cohérent en allemand utilisant le vocabulaire sélectionné

- 🎚️ **Vitesse réglable** (0% à -30%)- 🎤 **Audio haute qualité** : Génération automatique d'un fichier MP3 avec voix allemande naturelle (Microsoft Edge TTS)

- 📕 **PDF complet** avec vocabulaire, texte et QR code- 📊 **Contrôle de la longueur** : Choisissez le nombre de mots du texte (±10%)

- ➕ **Ajout de mots** à la liste existante

## 🚀 Installation

## 🚀 Installation

### 1. Créer un environnement virtuel (si ce n'est pas déjà fait)

### 1. Prérequis

```bash

- Python 3.12 avec Tk 9.0 (installé via Homebrew)python3 -m venv .venv

- Clé API OpenAIsource .venv/bin/activate  # Sur macOS/Linux

```

### 2. Installation des dépendances

### 2. Installer les dépendances

```bash

# Activer l'environnement virtuel```bash

source .venv312/bin/activatepip3 install --user openai edge-tts python-dotenv

```

# Les dépendances sont déjà installées :

# - openai### 3. Configurer la clé API

# - edge-tts

# - python-dotenv1. Créez un compte sur [OpenAI Platform](https://platform.openai.com/)

# - reportlab2. Obtenez votre clé API sur https://platform.openai.com/api-keys

# - qrcode3. Éditez le fichier `.env` :

# - pillow

``````bash

nano .env

### 3. Configuration```



Créez un fichier `.env` avec votre clé API OpenAI :4. Remplacez `sk-votre_clé_openai_ici` par votre vraie clé API :



``````

OPENAI_API_KEY=votre_clé_iciOPENAI_API_KEY=sk-proj-votre_vraie_clé_ici

``````



## 📖 Utilisation## 📖 Utilisation



### Lancer l'application### Lancer l'application



```bash```bash

source .venv312/bin/activate && python app.pypython app_comprehension_orale.py

``````



### Workflow typique### Workflow



**Option 1 : Génération automatique**1. **Étape 1** : Entrez un thème (ex: "les droits de la femme", "l'environnement", "la technologie")

1. Entrez un thème (ex: "la météo")2. **Étape 2** : Cliquez sur "🤖 Générer le vocabulaire (IA)"

2. Cliquez "Générer vocabulaire"3. **Étape 3** : Sélectionnez/désélectionnez les mots avec les cases à cocher

3. Sélectionnez les mots désirés4. **Étape 4** : Ajoutez des mots personnalisés si souhaité avec "➕ Ajouter un mot personnalisé"

4. Choisissez niveau, voix, vitesse5. **Étape 5** : Choisissez le nombre de mots du texte (par défaut : 300)

5. Cliquez "🚀 GÉNÉRER TEXTE ET AUDIO MP3 🚀"6. **Étape 6** : Cliquez sur "🚀 Générer le texte et l'audio MP3"

7. **Résultat** : L'application crée automatiquement :

**Option 2 : Saisie manuelle**   - Un fichier `.txt` avec le texte allemand

1. Cliquez "Saisie manuelle"   - Un fichier `.md` avec le vocabulaire et le texte

2. Entrez vos mots (format simple : `Haus` ou complet : `das Haus | la maison`)   - Un fichier `.mp3` avec l'audio

3. Cliquez "Valider et traduire"

4. Sélectionnez les mots## 📁 Fichiers générés

5. Générez texte et audio

Les fichiers sont nommés automatiquement avec le format :

**Option 3 : Mode mixte**- `texte_[theme]_[date_heure].txt`

1. Générez du vocabulaire automatiquement- `texte_[theme]_[date_heure].md`

2. Cliquez "➕ Ajouter mots" pour compléter- `audio_[theme]_[date_heure].mp3`

3. Générez l'exercice

Exemple :

## 🎛️ Paramètres- `texte_droits_femme_20251021_143022.txt`

- `texte_droits_femme_20251021_143022.md`

### Niveau CECRL- `audio_droits_femme_20251021_143022.mp3`

- **A1** : Débutant (phrases très simples)

- **A2** : Élémentaire (situations quotidiennes)## 🎨 Mode Manuel

- **B1** : Intermédiaire (recommandé)

- **B2** : Intermédiaire avancéSi vous n'avez pas de clé API ou préférez travailler sans IA :

- **C1** : Avancé1. Cliquez sur "✏️ Mode manuel"

- **C2** : Maîtrise2. Ajoutez vos mots manuellement avec "➕ Ajouter un mot personnalisé"

3. Note : La génération de texte nécessite quand même l'API IA

### Voix

- **👩 Femme** : Katja Neural (par défaut)## 🔧 Configuration avancée

- **👨 Homme** : Conrad Neural

### Changer la voix allemande

### Vitesse audio

- **0%** : Vitesse normaleDans `app_comprehension_orale.py`, ligne ~480, modifiez :

- **-5%** : Légèrement ralenti (recommandé)

- **-10% à -30%** : Pour débutants```python

voice="de-DE-KatjaNeural",  # Voix féminine

## 📂 Fichiers générés```



Pour chaque exercice :Autres voix disponibles :

- 📄 `texte_theme_timestamp.txt` - Texte allemand- `de-DE-ConradNeural` - Voix masculine allemande

- 🎧 `audio_theme_timestamp.mp3` - Audio avec voix choisie- `de-AT-IngridNeural` - Voix autrichienne féminine

- 📕 `texte_theme_timestamp.pdf` - PDF avec vocabulaire, texte et QR code- `de-CH-LeniNeural` - Voix suisse féminine



## 💰 Coûts### Ajuster la vitesse de lecture



- **OpenAI GPT-4o** : ~$0.002 par exercice (~2500 exercices avec $10)Modifiez le paramètre `rate` :

- **Edge TTS** : Gratuit et illimité

- **Total** : Très économique ! 💚```python

rate="-5%"   # 5% plus lent

## 🗂️ Structure du projetrate="0%"    # Vitesse normale

rate="+10%"  # 10% plus rapide

``````

comprehension_orale/

├── app.py                  # Application principale ✨## 🐛 Dépannage

├── .env                    # Clé API OpenAI (à créer)

├── .venv312/               # Environnement Python 3.12### Erreur "OPENAI_API_KEY non trouvée"

├── _archive/               # Anciennes versions- Vérifiez que le fichier `.env` existe

├── texte_*.txt             # Textes générés- Vérifiez que la clé API est correcte (commence par `sk-proj-` ou `sk-`)

├── audio_*.mp3             # Audios générés- Pas d'espaces autour du `=`

└── texte_*.pdf             # PDFs générés- Relancez l'application

```

### Erreur lors de la génération audio

## 🐛 Dépannage- Vérifiez votre connexion internet (edge-tts nécessite internet)

- Essayez de relancer la génération

### L'interface est noire ou invisible

Vous utilisez probablement Python 3.9 avec Tk 8.5. Utilisez Python 3.12 avec Tk 9.0 :### Interface ne s'affiche pas

```bash- Vérifiez que tkinter est installé (inclus par défaut sur macOS)

source .venv312/bin/activate && python app.py- Sur Linux : `sudo apt-get install python3-tk`

```

## 📚 Exemples de thèmes

### Erreur "No module named 'openai'"

```bash- Les droits de la femme

source .venv312/bin/activate- L'environnement et le climat

pip install openai edge-tts python-dotenv reportlab qrcode pillow- La technologie et l'intelligence artificielle

```- Les voyages et le tourisme

- La santé et l'alimentation

### Erreur "API key not found"- L'éducation

Vérifiez que le fichier `.env` existe et contient :- Le sport

```- La culture allemande

OPENAI_API_KEY=votre_clé_ici- Les médias sociaux

```- L'économie



## 📝 Notes## 🤝 Contribution



- **Minimum 2 mots** requis pour générer un exerciceN'hésitez pas à améliorer l'application et à partager vos suggestions !

- Les mots peuvent être entrés avec ou sans traduction (traduction auto si absente)

- Le QR code dans le PDF pointe vers le fichier MP3 local## 📄 Licence

- Les fichiers sont sauvegardés avec horodatage pour éviter les écrasements

Libre d'utilisation pour un usage éducatif.

## 🔄 Historique

- **Version actuelle** : app.py (Python 3.12 + Tk 9.0 + OpenAI)
- **Versions archivées** : Voir dossier `_archive/`

## 📧 Support

Pour toute question ou amélioration, consultez la documentation ou les fichiers dans `_archive/` pour l'historique des modifications.

---

**Bon apprentissage de l'allemand ! 🇩🇪 🎧**
