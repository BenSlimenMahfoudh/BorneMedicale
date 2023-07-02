# BORNE MEDICALE PFE 2022-2023

- Ce projet est mon projet de fin d'études en licence d'ingénierie des systèmes informatiques, avec une spécialité en systèmes embarqués et Internet des objets à la Faculté des Sciences de Bizerte. L'objectif de ce projet est de concevoir et réaliser une borne médicale. La société Wincom est responsable de sa réalisation.

La borne médicale que j'ai développée permet de collecter différents paramètres vitaux des patients tels que la tension artérielle, le taux d'oxygène, la température, la fréquence cardiaque, le poids et la taille. Pour cela, j'ai utilisé la carte Raspberry Pi 3B, ainsi que plusieurs capteurs. Le capteur Max30100 est utilisé pour mesurer l'oxygène et les pulsations cardiaques, le capteur MLX90614 à infrarouge est utilisé pour mesurer la température, le capteur HC-SR04 à ultrasons est utilisé pour mesurer la taille du patient. J'ai également utilisé un module relais 1HC pour contrôler l'alimentation du tensiomètre à distance. Enfin, j'ai intégré un capteur de poids avec un amplificateur HX711 pour mesurer le poids du patient.

Toutes les données collectées sont ensuite envoyées à l'application de la borne en utilisant le protocole MQTT. Cette application est en charge de recevoir les mesures en temps réel et de les traiter de manière appropriée.
- Une fois les données collectées par la borne médicale, elles sont affichées dans l'application de la borne elle-même. L'application permet au patient qui effectue les tests de visualiser ses propres mesures. Une fois le test terminé, le système de l'application enregistre les mesures collectées dans une base de données MongoDB.

La base de données MongoDB offre la possibilité aux médecins de suivre les patients en temps réel à l'aide d'une interface web. Grâce à cette interface, les médecins peuvent accéder aux données enregistrées dans la base de données et surveiller l'évolution des paramètres vitaux des patients.

Cela permet aux médecins de disposer d'un outil pratique pour suivre et analyser les données des patients, facilitant ainsi la prise de décision médicale et le suivi des traitements, telque de rechercher un patient et consulter l'historique des mesures.

- Pour que les médecins aient l'autorisation de consulter la liste des patients, il est nécessaire que l'administrateur ajoute les médecins au système. L'administrateur dispose d'une application web dédiée pour gérer les médecins. Cette application web offre des fonctionnalités telles que l'ajout, la modification et la suppression de médecins.

L'administrateur peut utiliser l'application web pour créer de nouveaux comptes médecins en fournissant les informations nécessaires, telles que le nom, l'adresse e-mail, les identifiants de connexion, etc. Une fois qu'un médecin est ajouté avec succès, il obtient un compte et les autorisations nécessaires pour accéder à l'interface web du système.

Cela permet à l'administrateur de gérer facilement les médecins du système en leur attribuant les droits d'accès appropriés. Les médecins peuvent alors se connecter à l'application web à l'aide de leurs identifiants et consulter la liste des patients autorisés.