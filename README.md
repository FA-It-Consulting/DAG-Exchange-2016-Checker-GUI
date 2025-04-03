DAG Exchange 2016 Checker GUI - FA-IT Consulting

Description

Ce projet PowerShell fournit une interface graphique (GUI) permettant de vérifier l'état d'un DAG (Database Availability Group) Exchange Server 2016. Il permet :

D'afficher les membres du DAG.

De lister les copies de bases de données avec leurs statuts (CopyQueueLength, ReplayQueueLength, ContentIndexState).

De tester la santé de la réplication avec Test-ReplicationHealth.

De générer automatiquement un rapport HTML technique prêt à l'impression ou à la conversion en PDF.

Projet développé par FA-IT Consulting pour la supervision simplifiée d’environnements Exchange.

🚀 Lancement

1.Ouvrir une session PowerShell en tant qu'administrateur.

2.Exécuter le script principal : .\Check-DAG-GUI.ps1

3.Une interface s'ouvre. Cliquez sur "Lancer la vérification" pour démarrer l'analyse.

📃 Rapport HTML

Un fichier HTML est automatiquement généré dans C:\Logs\DAG_Report_yyyyMMdd_HHmmss.html.

Il contient : DAG, membres, copies, santé réplication.

Peut être converti en PDF avec wkhtmltopdf.

⚖️ Prérequis

PowerShell 5.1+

Droits d’administration Exchange

Accès à la console Exchange Management Shell

Création du dossier C:\Logs si absent

🌐 Conversion HTML → PDF (optionnelle)

Si wkhtmltopdf est installé : & "C:\Program Files\wkhtmltopdf\bin\wkhtmltopdf.exe" "C:\Logs\DAG_Report_*.html" "C:\Logs\DAG_Report.pdf"

💡 Astuce de personnalisation

Tu peux modifier le titre ou ajouter un logo FA-IT dans la balise HTML head.

Compatible avec une intégration dans des solutions RMM/NOC internes.

🌐 Liens utiles

Documentation officielle DAG Exchange
FA-IT Consulting

© FA-IT Consulting 2025

Toute utilisation ou redistribution commerciale sans accord explicite est interdite.
