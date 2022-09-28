# Space-feeders

## Authentification

---

  * Formationline

Appelons notre site internet de formation en ligne "formationline" afin d'éviter les répétitions de "site internet".

Dans formationline nous auront besoins d'un utilisateur appelé formateur, un utilisateur appelé apprenant puis un administrateur. 

Ce qui change entre ces utilisateur sera les droits d'utilisation sur formationline, un apprenant n'a pas utilité à poster des foramtions, sont buts c'est de les suivrent donc un identifiant est un mot de passe complexe suffise étant donné qu'il ne possède pas le droit de poster des formations, donc les apprenants ne pourront pas publié des vidéos, documents. En revanche les formateurs eux, possèdent le droit de poster des vidéos, documents donc necessite une sécurité plus appronfondi sur leur compte. Une connexion avec une double authentification est donc necessaire, un identifiant, un mot de passe et si possible une empreinte digitale serait la sécurité maximale. Dans le cas ou l'empreinte digitale n'est pas possible nous devons nous rendre à l'évidence et utiliser l'authentification à double facteur avec un code envoyé dans la boite mail à rentrer après la validation de connexion avec
identifiant et mot de passe. Sur un site internet recpecter le système : ce que je sais, ce je posséde et ce que je suis, reste très compliqué. L'administrateur doit possède la sécruité maximal, un lien reçu par mail avec une validité dans le temps, ce lien fera passer l'administrateur devant une interface de connexion ou il faudra : un identifiant, un mot de passe complexe.

Il faut également que les sessions soit limité dans le temps. Il ne faut pas laisser une sessions connecté indefiniment, par exemple si le formateurs n'est plus aller sur la platforme depuis plus de 24 heures il faut déconnecter sa session. Pour les apprenants cela peut s'élargir puis qu'il possède moins de droit donc nous pouvons élargir le temps de la session à 48 heures par exemple, par contre pour l'administrateur la session doit se déconnecter des qu'il quitte la page. 

Un système de journalisation est également important : la conservation des historiques des évènements liés à l'authentification (autrement appelée journalisation ) a pour objectifs une supervision de la sécurité et une investigation en cas d'incidents de sécurité, tous cela dans la réglementation du RGPD. 

Une fois tous cela mise en place il faut maintenant que dans la base de donnée les mots de passe soit hasher, afin d'éviter que si un pirate arrive à s'introduir dans la base de donnée possède le moyen d'usurpé l'identité de chaque utilisateur. Sur formationline il est également obligatoire de posséder le protocole HTTPS afin de garantir la sécurité des données et de l'utilisation de l'application à l'utilisateur. C'est ici qu'intervient le TLS (script SSL amélioré). Les TLS sont des protocoles de sécurisation des échanges par réseau informatique, notamment par internet.

Il faut également s'assurer de la sécurité du DNS. Le Domain Name System ou DNS est un service informatique distribué utilisé qui traduit les noms de domaine Internet en adresse IP ou autres enregistrements. Le DNS simplifie la navigation sur internet, cela nous permet de ne pas apprendre ou retenir les adresse ip de chaque site internet. 


 ## Définitions : 
 
  * L'attaque du point d'eau : comparons cette attaque à lion qui chasse. L'animal que le lion chasse sait qu'il à besoins de boire pour survivre alors il va attendre sagement qu'un animal aille au point d'eau et attaquera lorsqu'il sera occupé à boire. Sur internet c'est la même histoire, l'utilisateur sera forcer de faire certaines manipulation sur l'application web alors le hacker attendre sagement que l'utilisateur agisse de la sorte. 
  
  * Journalisation : La conservation des historiques des évènements liés à l’authentification (autrement appelée journalisation) a pour objectifs une supervision de la sécurité et une investigation a posteriori en cas
d’incidents de sécurité.

 * sha256 : SHA-2 est une famille de fonctions de hachage qui ont été conçues par la National Security Agency des États-Unis, sur le modèle des fonctions SHA-1 et SHA-0, elles-mêmes fortement inspirées de la fonction MD4 de Ron Rivest. 
 
 * RGPD : Le règlement général sur la protection des données. Il est important de respecté cette réglementation afin de ne pas avoir de probléme juridique avec la CNIL. Exemple : si un site internet conserve des données d'un utilisateur (adresse mail, nom, prénom, ...), l'utilisateur doit être prévenu, il doit également avoir la possibilité de modifier ces données, de les supprimer également à sa guise. 
 
 * Bug bunty : Une prime aux bugs est un programme de récompenses proposé par de nombreux sites web et développeurs de logiciel qui offre des récompenses aux personnes qui rapportent des bugs, surtout ceux associés à des vulnérabilités.
 
 * Le mode strict : Le mode strict permet de détecter les problèmes dans votre code. Des exceptions sont alors émises. Si des actions potentiellement dangereuses, par exemple accéder à une variable globale, sont effectuées, le mode strict peut les prévenir ou bien émettre une erreur.
 
 * Hashage : On nomme fonction de hachage, de l'anglais hash function par analogie avec la cuisine, une fonction particulière qui, à partir d'une donnée fournie en entrée, calcule une empreinte numérique servant à identifier rapidement la donnée initiale, au même titre qu'une signature pour identifier une personne.
 
 * Salage : Le salage est une méthode permettant de renforcer la sécurité des informations qui sont destinées à être hachées en y ajoutant une donnée supplémentaire afin d’empêcher que deux informations identiques ne conduisent à la même empreinte.
 
 * RBAC : Le contrôle d'accès basé sur les rôles est un modèle de contrôle d'accès à un système d'information dans lequel chaque décision d'accès est basée sur le rôle auquel l'utilisateur est associé.

  * Faille CSS : 

Autres exemples : prenons un site d’article, ou les articles sont payants mais en fond nous pouvons apercevoir que les texte qui est présent mais flouté sa possibilité de scroll et avec une div en plein milieu de l’écran qui nous explique qu’il faut payer pour y remédier. Solution ? Utiliser l’inspecteur afin de désactiver ce qui nous gêne et avoir la possibilité de l’utiliser à notre guise.
