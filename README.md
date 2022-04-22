# EvtxSpotter

## :man_firefighter: Mentalité

Simplicité.

## :point_up_2: Le besoin

1. Obtenir rapidemment des informations de sécurité sur une machine Windows.
* Informations sur les journaux en eux-même : quels journaux, combien de logs.
* Période d'activité et de connexions.
* Evenements majeurs et classiques :
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

## :writing_hand: Le testing

IL est important de pouvoir tester les évennements pour voir si le logiciel est opérationnel.

- Il faut donc pouvoir générer les évennements et voir si les fonctions de détection les détectent bien.
- Il faut tester les synthèses en dur ou automatiques pour rassembler les logs multiples pointant vers le même évennement.
