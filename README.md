# Stratégie de Conception et de Sécurisation d'une application

## Table des matières
 1. [Introduction](#introduction)
 2. [Définitions et recommandations](#définitions-et-recommandations)
 3. [Notre application](#notre-application)
 4. [Sources](#sources)
## Introduction
<!-- Notre introduction en anglais -->



## Définitions et recommandations

<!-- Liste des termes avec définition, recommandations, exemples, couche ntier -->

<!--  Voici un Model

<details>
  <summary>

  ### I'am the HEADER
  
  </summary>

  #### Définition
  - First line.
    - Sub-First line.
  - Second line
  
  #### Recommandations
  - R1 - title of recommandation
    - Content
  - R2
    - Content

</details>

 -->
<details>
  <summary>

  ### Transport Layer Security (TLS)

  </summary>

  #### Définition
  - Transport Layer Security anciennement appelé Secure Socket Layer (SSL) est un protocole cryptographique conçu pour fournir une communications sécurisé sur un réseau informatique.
  - TLS permet de garantir 3 propriété de sécurité, 
    - `Confidentialité` : Personne d'autre ne peut lire la communication parce que elle est chiffré.
    - `Authenticité` : L'identité des participants à la communication peut être vérifier.
    - `intégrité` : Les messages de la communication ne peuvent pas être modifiées en route par un adversaire.
  #### Recommandations
  - R1 - Recommandations de sécurité relatives à TLS: 
    - Il est nécessaire de mettre en œuvre les Recommandations de sécurité relatives à TLS
    pour tout site même si celui-ci ne traite pas d’informations sensibles.
</details>

<details>
  <summary>

  ### L'Hypertext Transfer Protocol (HTTPS) 
  
  </summary>

  #### Définition
  - C'est un protocole de communication client-serveur pout accéder à des ressources sur un serveur web.
  - La mise en place de HTTPS sur un site ou une application web est une garantie de sécurité qui
    repose sur TLS pour assurer la confidentialité, l'authenticité et l’intégrité des informations échangées, ainsi que
    l’authenticité du serveur contacté.
  - les requêtes HTTP contient : une méthode, un cible et la version du protocole, contient également un en-tête.

  
  #### Recommandations
  - R2 - Mettre en œuvre HSTS
    - Il est nécessaire de mettre en œuvre `HSTS` afin de limiter les risques d’attaque de
    type **Man-In-The-Middle** dus à des accès non sécurisés générés par les utilisateurs ou
    par un attaquant.
  - R3 - Surveiller les CT logs
    - Il est recommandé que l’hébergeur ou le responsable d’un site web mette en œuvre
    un processus de surveillance des Certificate Transparency logs afin de détecter et révo￾quer les certificats illégitimes qui correspondent à des domaines sous son contrôle.

</details>


<details>
  <summary>

  ### HTTP Strict Trransort Security (HSTS)
  
  </summary>

  #### Définition
  - indique au navigateur d’utiliser automatiquement HTTPS pour tous les accès au site web.
  - HSTS permet à un site Web d'informer le navigateur qu'il ne doit jamais charger le site à l'aide de HTTP et qu'il doit automatiquement convertir toutes les tentatives d'accès au site à l'aide de HTTP en requêtes HTTPS.
  - Demander au navigateur d’utiliser exclusivement HTTPS pour se connecter au site
    visité et à ses sous-domaines, pour une durée d’un an : 
    ``` Strict−Transport−Securit : max−age =31536000 ; includeSubDomains ; ```
  - PS: HTTPS securise seulement l'echange d'informations il agit uniquement pendant l'échange
  
  #### Recommandations
  - R2 - Mettre en œuvre HSTS
    - Il est nécessaire de mettre en œuvre `HSTS` afin de limiter les risques d’attaque de
    type **Man-In-The-Middle** dus à des accès non sécurisés générés par les utilisateurs ou
    par un attaquant.
  - *Attention*
    - Attention, la pérennité de l’accès en HTTPS est un prérequis indispensable à HSTS, qui rendra l’accès en clair impossible

</details>
 

## Notre application

<!-- Ce que l'ont va mettre en place et pour quel raison -->

### Client (applicative)

### Serveur (Métier)
### BDD (Données)
## Sources

- Guide ANSSI: RECOMMANDATIONS POUR LA MISE EN ŒUVRE D'UN SITE WEB : MAÎTRISER LES STANDARDS DE SÉCURITÉ CÔTÉ NAVIGATEUR:
  https://simplonline-v3-prod.s3.eu-west-3.amazonaws.com/media/file/pdf/436f5816-a1f0-4795-a722-2046d1181db6.pdf
- GUIDE ANSSI: RECOMMANDATIONS RELATIVES À L'AUTHENTIFICATION MULTIFACTEUR ET AUX MOTS DE PASSE
  https://simplonline-v3-prod.s3.eu-west-3.amazonaws.com/media/file/pdf/6e056f88-eef5-489c-85fe-57c1c58fb165.pdf
- Guide RGPD CNIL de l'équipe de développement
  https://lincnil.github.io/Guide-RGPD-du-developpeur/

