# YouGlitch SMP 1024

Projet JUCE/CMake pour Windows x64, avec génération des formats **VST3** et **Standalone**.

## Structure du dépôt

À la racine GitHub, on doit voir directement :

```text
.github/workflows/windows-build.yml
Source/PluginProcessor.cpp
Source/PluginProcessor.h
Source/PluginEditor.cpp
Source/PluginEditor.h
Source/StreamingSampleReader.cpp
Source/StreamingSampleReader.h
Source/StreamingVoicePool.cpp
Source/StreamingVoicePool.h
Reference/YouGlitch_SMP_1024_original.html
CMakeLists.txt
BUILD_WINDOWS.bat
.gitignore
README.md
```

Ne téléverse pas le dossier parent contenant tous ces éléments : téléverse **le contenu de ce dossier** à la racine du dépôt GitHub.

## Compilation automatique avec GitHub

1. Crée un nouveau dépôt GitHub vide (sans README, licence ni `.gitignore` générés par GitHub).
2. Ouvre ce dossier sur ton ordinateur.
3. Sélectionne tout son contenu, y compris le dossier caché `.github`.
4. Téléverse le contenu à la racine du nouveau dépôt.
5. Fais `Commit changes`.
6. Ouvre l'onglet **Actions**. Le workflow `Build YouGlitch SMP 1024 (Windows x64)` démarre automatiquement après le push sur `main` ou `master`.
7. Quand le workflow réussit, ouvre son exécution et télécharge l'artefact `YouGlitch-SMP-1024-Windows-x64`.

## Compilation locale sous Windows

Installe Visual Studio 2022 avec la charge de travail **Développement Desktop en C++**, ainsi que CMake et Git. Puis double-clique sur `BUILD_WINDOWS.bat`.

## Important

- JUCE 8.0.6 est récupéré automatiquement depuis GitHub pendant la configuration CMake : une connexion Internet est nécessaire.
- Les documents d'étapes `.md` ne sont pas requis pour compiler ; ils ont été retirés de ce paquet de dépôt propre.
- Le projet doit encore être validé par un build Windows réel. La présence des fichiers et la configuration du workflow ne garantissent pas à elles seules une compilation sans erreur.
