MedShakeEHR Role
=========

Le rôle ansible qui permet d’installer MedShakeEHR

Requirements
------------

- ansible 2.9


Role Variables
--------------

| Nom                | Valeur par défaut                                      | Description                                                                                      |
|--------------------|--------------------------------------------------------|--------------------------------------------------------------------------------------------------|
| user               | vagrant                                                | Nom d’utilisateur sudo                                                                              |
| countryName        | FR                                                     | Nom du pays                                                                                     |
| localityName       | Paris                                                  | Nom de la ville                                                                                 |
| organizationName   | Dr Strange                                             | Nom de l’organisation                                                                           |
| emailAddress      | email@domain.tld                                       | Adresse e-mail                                                                                  |
| sqlRootPassword    | root                                                   | Mot de passe root pour SQL                                                                      |
| sqlUserAccount     | user                                                   | Nom du compte utilisateur SQL                                                                   |
| sqlUserPassword    | user                                                   | Mot de passe du compte utilisateur SQL                                                          |
| sqlDbName          | medshakeehr                                            | Nom de la base de données SQL                                                                   |
| msehr_base_release | 8.1.1                                                  | Version de MedShakeEHR                                                                  |
| msehr_base_repo_url| https://codeload.github.com/MedShake/MedShakeEHR-base/tar.gz/refs/tags/ | URL de MedShakeEHR                                          |
| msehr_base_checksum| sha256:5ae9ddf3e528eab4fe5882724cc00d912600a9fb1748ff31e47c6191a173b200 | Checksum  de MedShakeEHR                                        |
| msehrPath          | /opt/ehr                                               | Chemin d’installation de MedShakeEHR                                                            |
| timezone           | Europe/Paris                                           | Fuseau horaire                                                                                   |
| domain             | msehr.local                                            | Nom de domaine                                                                                   |
| uploadMaxFilesize  | upload_max_filesize = 20M                              | Taille maximale des fichiers téléversés                                                         |
| postMaxsize        | post_max_size = 20M                                    | Taille maximale des données POST                                                                |
| maxInputVars       | max_input_vars = 20000                                 | Nombre maximal de variables d’entrée                                                             |
| errorReporting     | error_reporting = E_ALL & ~E_DEPRECATED & ~E_STRICT    | Niveau de rapport d’erreurs                                                                      |
| displayErrors      | display_errors = Off                                   | Affichage des erreurs (Off : désactivé, On : activé)                                            |
| displayStartupErrors| display_startup_errors = Off                           | Affichage des erreurs de démarrage (Off : désactivé, On : activé)                               |
| msehrPackages      | [‘acl’, ‘apache2’, ‘composer’, ‘curl’, ‘ghostscript’, ‘git’, ‘grub2’, ‘imagemagick’, ‘mariadb-server’, ‘ntp’, ‘pdftk-java’, ‘php’, ‘php-bcmath’, ‘php-curl’, ‘php-gd’, ‘php-gnupg’, ‘php-imagick’, ‘php-imap’, ‘php-intl’, ‘php-json’, ‘php-mysql’, ‘php-soap’, ‘php-xml’, ‘php-yaml’, ‘php-zip’, ‘python3-mysqldb’, ‘python3-openssl’, ‘ufw’, ‘unattended-upgrades’ ] | Liste des packages requis pour MedShakeEHR |

Example Playbook
----------------


    - hosts: medshakeehr
      roles:
         - { role: marsante.medshakeehr }

License
-------

GPL v3

Author Information
------------------

- Auteur
[![](https://github.com/marsante.png?size=50)](https://github.com/marsante)
- Contributeurs
[![](https://github.com/indelog.png?size=50)](https://github.com/indelog)
