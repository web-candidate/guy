Test Wordpress
===
Pré-requis :
 - installer la dernière version de Wordpress
 - partir du theme de base : theme.zip
 - télécharger le template PSD depuis http://www.graphicsfuel.com/wp-content/uploads/2013/07/bluebox-psd-flat-website-templates.zip

Conseils/Précisions :
 - Cet exercice se base sur un cas métier 
 - Bien lire l'ensemble des points avant de commencer
 - Il n'y a pas de limite/contrainte de temps (_prévoir une petite journée a minimum_)
 - Seule la page de contact doit être intégrée. Néanmoins les autres pages présentes (About, Services, etc ...) dans la maquette doivent être présentes et accessibles.

Delivery :
 - La documentation du delivery doit être jointe au source du projet "delivery.doc" : elle devra prévoir un déploiement "from scratch" avec une initialisation de la BDD si besoin
 - Le serveur de déploiement sera un wamp (php 5.5)
 
1) Réaliser l'intégration HTML de la page de contact (bluebox-contact) wording compris
 - intégrer la dernière version de bootstrap twitter
 - ajouter 2 champs supplémentaires après "Email Address" : "Postal Code" et "City"
 - proposer un design responsive mobile-first
 - l'intégration doit respecter la contrainte suivante : un seul sprite doit être utilisé pour la totalité de la page

2) Autocomplete du code postal
 - à la saisie et au focus sur le champ "Postal Code", s'il y a au moins 2 caractères, une autocomplétion en ajax doit être proposée avec la liste des codes postaux que renvoi le service postal_code.php à la racine du thème. (pour ce test, quels que soit les paramètres envoyés à ce service, il renverra toujours le même résultat)
 - lorsque un code postal est sélectionné les champs "Postal Code" et "City" sont pré-rempli avec les valeurs sélectionnées
 - l'utilisateur ne doit pas être en mesure de modifier le champ "City" par lui-même
 
3) Controle des données / fonctionnement
 - tous les champs sont obligatoires
 - design libre pour les messages d'erreurs
 - des message d'erreurs spécifiques doivent être prévus, pour chaque champ, de manière individuelle, si le champ est vide ou bien s'il est mal formaté.
 - Si le formulaire soumis est valide, un mail récapitulatif du contact doit être envoyé à une adresse mail paramétrable dans le backoffice
 - Le mail doit être envoyé depuis un serveur smtp avec une authentification par login et mot de passe, également paramétrable dans le backoffice
 
4) Administration
 - Une page du backoffice doit permettre de paramétrer la connexion SMTP.
 - Une page du backoffice doit permettre de paramétrer le destinataire du mail envoyé.
 - Une page du backoffice doit permettre de customiser le wording de tous les messages d'erreur.
 - Une page du backoffice doit permettre de visualiser sous la forme d'un graph (libre) le nombre de prises de contact sur les 6 derniers mois
 - Une page du backoffice doit permettre de lister l'ensemble des demandes de contact sous la forme d'un tableau paginé avec l'ensemble des informations sur une ligne.
NB : Les pages peuvent être combinées si besoin