# EvtxSpotter  	:newspaper::dark_sunglasses:

## :point_up_2: Le besoin

Obtenir rapidemment des informations des journaux de sécurité sur une machine Windows.

:pushpin: Connaître l'**état des journaux** (présence, nombre d'évennements, par type ...etc)
  
:pushpin: Visualiser les **grands évenements** (classiques et importants)

:pushpin: Sélectionner des **évenements spécifiques** (par types)

:pushpin: Afficher des **logs applicatifs informatifs**

* Informations sur les journaux en eux-même : quels journaux, combien de logs.
* Période d'activité et de connexions.
* Evenements classiques :
  - Branchement de clefs usb
  - Connexions utilisateurs, alumage machine
* Evenements importants
  - Applications bloquées (cf R1).
  - Applications  crashées.
  - Erreur système ou de service.
  - Effacements des Events Logs.
  - Installation des logiciels et des services.
  - Action utilisateurs (ex : login) et administartion utilisateur (ajout à un groupe privilégié par ex).
  - Actions Windows Defender
  - Connectios réseaux
  - Médias externes
  - Actions d'impression
  - Accès à distance
  - (-) Erreur de mise à jour de Windows.
  - (-) Actions particulières du FireWall voir [ici](https://apps.nsa.gov/iaarchive/library/ia-guidance/security-configuration/applications/assets/public/upload/Spotting-the-Adversary-with-Windows-Event-Log-Monitoring.pdf#page=31)
  - (-) Signaturre du driver du kernel.
  - (-) Erreur de GPO
  - (-) Pass the Hash [ici](https://apps.nsa.gov/iaarchive/library/ia-guidance/security-configuration/applications/assets/public/upload/Spotting-the-Adversary-with-Windows-Event-Log-Monitoring.pdf#page=37)
  - [Source](https://apps.nsa.gov/iaarchive/library/ia-guidance/security-configuration/applications/assets/public/upload/Spotting-the-Adversary-with-Windows-Event-Log-Monitoring.pdf)

## :rocket: Défis

1. Synthétiser les évenements multiples en un seul, sans perdre d'infos.
2. Bien détailler les codes d'évenements (ne pas en oublier, ne pas oublier d'évenements).
3. Afficher de manière efficace les descriptions des évenements (ergonomie + détail des descriptions).

## :writing_hand: Le testing

Il est important de pouvoir tester les évenements pour voir si le logiciel est opérationnel.

- Il faut donc pouvoir générer les évenements et voir si les fonctions de détection les détectent bien -> fichier de test.
- Il faut tester les synthèses en dur ou automatiques pour rassembler les logs multiples pointant vers le même évennement.

## :man_firefighter: Mentalité

- *Simple* : sans clic, l'utilisateur obtient directement un premier chargement avec l'état des journaux, et les logs classiques et importants sur la journée.
- *Informatif* : une fenêtre de logs applicatifs permet à l'utilisateur de connaître parfaitement le fonctionnement du logiciel (causes d'erreurs, interprétation des résultats...)
- *Ergonomique* : interface claire et dynamique. 

