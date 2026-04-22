# CompaDevis - Comparateur de Devis avec IA

Application mobile Android pour comparer des devis de travaux de renovation.
Import PDF avec OCR + analyse IA (Mistral), comparateur intelligent, synthese par corps de metier.

## Fonctionnalites

- Import PDF par IA (Mistral) avec OCR pour les scans
- Saisie manuelle de devis
- Comparateur interactif avec regroupement IA
- Analyse des prix par rapport au marche
- Synthese globale par corps de metier (imprimable)
- Export Excel
- Fonctionne hors-ligne (PWA)

## Comment compiler l'APK

### Methode 1 : Automatique (GitHub Actions)

1. Poussez ce depot sur GitHub
2. Allez dans l'onglet "Actions"
3. Le workflow "Build Android APK" se lance automatiquement
4. Une fois termine (~5 min), telechargez l'APK dans "Artifacts"

### Methode 2 : Locale (si Android Studio installe)

```bash
npm install
npx cap add android
npx cap sync android
cd android
./gradlew assembleDebug
```

L'APK sera dans `android/app/build/outputs/apk/debug/app-debug.apk`

## Installation sur telephone

1. Telechargez l'APK sur votre telephone
2. Ouvrez le fichier APK
3. Autorisez l'installation depuis "sources inconnues" si demande
4. L'app s'installe comme une app normale

## Configuration

1. Ouvrez l'app
2. Allez dans Parametres (icone engrenage)
3. Entrez votre cle API Mistral (gratuite sur console.mistral.ai)
4. Commencez a importer vos devis !

## Technologies

- HTML/CSS/JS (vanilla, pas de framework)
- Capacitor 6 (bridge web -> natif)
- Mistral AI (analyse PDF + regroupement)
- Tesseract.js (OCR navigateur)
- SheetJS (export Excel)
- pdf.js (lecture PDF)
