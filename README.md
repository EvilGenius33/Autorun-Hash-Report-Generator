🧬 Autorun Hash Report Generator
Auteur : Xenoz
Nom du script : Autorun_Hash_Report.ps1
Version : 1.0
Utilisation : Locale uniquement – Usage défensif

🎯 Objectif :
Ce script génère un rapport local des programmes configurés pour s’exécuter automatiquement au démarrage de Windows, avec le chemin exact et le hash SHA256 de chaque exécutable détecté.

✅ Fonctionnalités :
🔍 Analyse des clés "Run" dans le registre (HKLM & HKCU) :

Ces clés sont souvent utilisées pour la persistance par les malwares ou outils légitimes.

🔒 Récupération et hachage SHA256 :

Pour chaque exécutable référencé, le script calcule le hash SHA256 s’il existe.

Les chemins manquants ou inaccessibles sont signalés.

🧾 Génération d’un rapport clair :

Le fichier autorun_hash_report.txt est généré sur le bureau avec :

Le nom de la valeur

Le chemin exécutable

Le hash SHA256 ou un message d’erreur clair

📂 Exemple de sortie :
mathematica
Copier
Modifier
=== Autorun Hash Report ===
Generated: 2025-06-02 13:41:00

[HKLM:\Software\Microsoft\Windows\CurrentVersion\Run]
SecurityAgent → C:\Program Files\Security\agent.exe → SHA256: 9A2F3B...

[HKCU:\Software\Microsoft\Windows\CurrentVersion\Run]
Steam → C:\Program Files\Steam\steam.exe → SHA256: B42D1E...
🔐 Pourquoi ce script est utile :
Permet de repérer rapidement des binaires suspects ou modifiés dans les entrées d’autorun.

Fournit un hash exploitable pour une vérification sur VirusTotal ou tout outil de threat intel.

Pratique pour des audits manuels, forensic ou durcissement.

🛡️ Protection offerte :
✅ Utile en post-exploitation défensive, détection de persistance locale, ou recherche d’implant dissimulé.
🚫 Ne protège pas directement contre une attaque active.


© 2025 Xenoz. Tous droits réservés.

Ce script est fourni à des fins d’analyse défensive. Toute reproduction, modification ou distribution sans autorisation explicite est interdite.


