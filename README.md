Test Wordpress
===
Pr�-requis :
 - installer la derni�re version de Wordpress
 - partir du theme de base : theme.zip
 - t�l�charger le template PSD depuis http://www.graphicsfuel.com/wp-content/uploads/2013/07/bluebox-psd-flat-website-templates.zip

Conseils/Pr�cisions :
 - Cet exercice se base sur un cas m�tier 
 - Bien lire l'ensemble des points avant de commencer
 - Il n'y a pas de limite/contrainte de temps (_pr�voir une petite journ�e a minimum_)
 - Seule la page de contact doit �tre int�gr�e. N�anmoins les autres pages pr�sentes (About, Services, etc ...) dans la maquette doivent �tre pr�sentes et accessibles.

Delivery :
 - La documentation du delivery doit �tre jointe au source du projet "delivery.doc" : elle devra pr�voir un d�ploiement "from scratch" avec une initialisation de la BDD si besoin
 - Le serveur de d�ploiement sera un wamp (php 5.5)
 
1) R�aliser l'int�gration HTML de la page de contact (bluebox-contact) wording compris
 - int�grer la derni�re version de bootstrap twitter
 - ajouter 2 champs suppl�mentaires apr�s "Email Address" : "Postal Code" et "City"
 - proposer un design responsive mobile-first
 - l'int�gration doit respecter la contrainte suivante : un seul sprite doit �tre utilis� pour la totalit� de la page

2) Autocomplete du code postal
 - � la saisie et au focus sur le champ "Postal Code", s'il y a au moins 2 caract�res, une autocompl�tion en ajax doit �tre propos�e avec la liste des codes postaux que renvoi le service postal_code.php � la racine du th�me. (pour ce test, quels que soit les param�tres envoy�s � ce service, il renverra toujours le m�me r�sultat)
 - lorsque un code postal est s�lectionn� les champs "Postal Code" et "City" sont pr�-rempli avec les valeurs s�lectionn�es
 - l'utilisateur ne doit pas �tre en mesure de modifier le champ "City" par lui-m�me
 
3) Controle des donn�es / fonctionnement
 - tous les champs sont obligatoires
 - design libre pour les messages d'erreurs
 - des message d'erreurs sp�cifiques doivent �tre pr�vus, pour chaque champ, de mani�re individuelle, si le champ est vide ou bien s'il est mal format�.
 - Si le formulaire soumis est valide, un mail r�capitulatif du contact doit �tre envoy� � une adresse mail param�trable dans le backoffice
 - Le mail doit �tre envoy� depuis un serveur smtp avec une authentification par login et mot de passe, �galement param�trable dans le backoffice
 
4) Administration
 - Une page du backoffice doit permettre de param�trer la connexion SMTP.
 - Une page du backoffice doit permettre de param�trer le destinataire du mail envoy�.
 - Une page du backoffice doit permettre de customiser le wording de tous les messages d'erreur.
 - Une page du backoffice doit permettre de visualiser sous la forme d'un graph (libre) le nombre de prises de contact sur les 6 derniers mois
 - Une page du backoffice doit permettre de lister l'ensemble des demandes de contact sous la forme d'un tableau pagin� avec l'ensemble des informations sur une ligne.
NB : Les pages peuvent �tre combin�es si besoin