# 📄 Extraction de Texte depuis des CVs

## 🚀 Description
Ce projet permet d'extraire du texte à partir de CVs sous différents formats :
- **PDF (textuel et scanné)**
- **Images (JPG, PNG, TIFF, etc.)**
- **Documents Word (DOCX)**

Il utilise la bibliothèque `PyMuPDF` pour les PDF textuels, `Tesseract OCR` pour les PDF scannés et les images, et `python-docx` pour les fichiers Word.

---

## 📌 Fonctionnalités
✅ Extraction de texte depuis des fichiers PDF textuels et scannés.
✅ Extraction de texte depuis des images.
✅ Extraction de texte depuis des documents Word.
✅ Détection automatique de la langue (français ou anglais).
✅ Nettoyage du texte extrait pour une meilleure lisibilité.

---

## 🛠️ Installation
### 1️⃣ **Cloner le projet**
```sh
git clone https://github.com/ismailtarik/text-extraction.git
cd text-extraction
```

### 2️⃣ **Créer un environnement virtuel** (optionnel mais recommandé)
```sh
python -m venv venv
source venv/bin/activate  # Sous Windows : venv\Scripts\activate
```

### 3️⃣ **Installer Tesseract OCR** (si non installé)
#### 📌 Sous Windows :
Télécharger et installer [Tesseract OCR](https://github.com/UB-Mannheim/tesseract/wiki).
Ajoutez le chemin de Tesseract (`C:\Program Files\Tesseract-OCR\tesseract.exe`) à votre variable d'environnement.

#### 📌 Sous Linux/Mac :
```sh
sudo apt install tesseract-ocr  # Ubuntu/Debian
brew install tesseract          # macOS
```

---

## 📜 Utilisation
### 1️⃣ **Exécuter le script sur un CV**
```sh
python extract_text.py cv_exemple.pdf
```

### 2️⃣ **Exemple de code pour utilisation en Python**
```python
from extract_text import extract_text_from_cv

cv_file = "cv_exemple.pdf"  # Remplacez par le fichier de votre choix
extracted_text = extract_text_from_cv(cv_file)
print(extracted_text)
```

---

## 📦 Dépendances
- `PyMuPDF (fitz)` - Lecture des fichiers PDF.
- `pytesseract` - OCR pour les images et PDF scannés.
- `Pillow` - Gestion des images.
- `python-docx` - Extraction de texte depuis les fichiers Word.
- `langdetect` - Détection automatique de la langue.
- `unicodedata` - Nettoyage du texte extrait.

---

## 📝 Exemple de sortie
**Fichier PDF textuel** :
```
Nom : Jean Dupont
Email : jean.dupont@example.com
Expérience : 5 ans en développement Python
```

**Fichier PDF scanné / Image** :
```
Nom : Alice Martin
Compétences : Machine Learning, Data Science
```

---

## 📌 Améliorations futures
🚀 Améliorer la précision de l'OCR sur les documents complexes.
🚀 Ajouter un modèle de classification des CVs (ex : développeur, data scientist, etc.).
🚀 Intégration d'une interface graphique pour l'upload et l'extraction.
