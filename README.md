#  Modelisation du Projet AwsomeList

Wireframe, Cahier des charges, User stories, MCD, MLD.

## Cahier des Charges

---------------------------------------

Présentation et fonctionnalités

-------------------------------------

 

 

My Awesome List  est une application qui a pour vocation à la création de Listes par l’utilisateur et pour l’utilisateur.

Elle permettra a n’importe qui de pouvoir créer une Liste de choses qu’il aime ou de taches à accomplir.

L’utilisateur pourra aussi bien créer une liste de courses mais aussi la liste de séries qu’il aimerait regarder.

Quelle est la différence avec les ToDoList et autre site/application mobile du même genre disponible aujourd’hui ? 
Ici, nous proposons à notre utilisateur de créer un compte pour qu’il puisse enregistrer ces listes mais aussi la possibilité de créer et d'enregistrer chacun des mots qu’il mettra dans ses listes.
Ainsi, plus besoin de réécrire votre liste de courses toutes les semaines parce que les principaux élément que l’utilisateur a besoin seront disponible et enregistrés.

Nous proposons aussi une grand aisance de navigation entre listes grâce a une décomposition de ses dernières en sous-listes et notre système Drag and Drop, afin que les utilisateurs déplacent les “mots” a la simple navigation de son curseur.

L’utilisateur pourra créer jusqu’à 5 Listes Principales, qui seront décomposée chacune en 3 sous-Listes.
Ce qui permettra de pouvoir créer des listes différentes sans avoir à supprimer les autres.

Nous avons défini la cible comme des étant des utilisateurs lambda. De la personne qui voudra faire ses courses plus facilement à la personne qui voudra classer ses séries ou ses mangas préférés.
Le public visé utilisera essentiellement des navigateurs modernes (chrome, firefox ou Edge). Il faudra cependant gérer le cas de quelques utilisateurs safari. 

Le site sera responsive, disponible en version Web et en application mobile, nonobstant nous nous attendons à ce que l’essentiel du trafic provienne des utilisateurs mobile.
Pour la partie mobile, l’application sera disponible sur Android.

Il n’y aura que le rôle d’utilisateur et de visiteur sur l’application, étant donné que les listes sont privés à l’utilisateur, nous n’avons pas trouvé intéressant de configurer un rôle d’Admin.

Le visiteur pourra s’inscrire et/ou se connecter.
L’utilisateur pourra créer et supprimer son compte à tout moment. Le visiteur pourra créer/modifier sa liste et ses sous-listes mais ne restera pas en base de données, elle sera supprimé à chaque visite sur le site ou l’application. De même pour le création et modification des “mots”.
L’utilisateur pourra créer et modifier ses listes et sous-listes, toute modification sera permanente. Il en va de même pour la création et modification des “mots”. il pourra aussi les supprimer.
Les deux rôles pourront utiliser, sans restrictions, la fonction de Drag and Drop, cette fonction permet a l’utilisateur “d’attraper” les mots et de les déplacer dans les sous-listes avec la souris.

Un Dark mode sera visible par tous et disponible sur version Web et application mobile.

## User Stories

 | En tant que… | Je peux… | Afin de… |

| Visiteur | accéder à la page d’accueil | Modifier des Listes et créer des sous listes (non persistant) |

| Visiteur | accéder au formulaire de connexion | se connecter |

| Visiteur | accéder au formulaire d’inscription | s’inscrire |

| Visiteur | Avoir un compte | faire persister mes listes |

| Visiteur | accéder à la charte | lire la charte |

| Utilisateur | accéder au bouton logout |se déconnecter |

| Utilisateur | accéder à une liste principale | visualiser/Modifier une liste |

| Utilisateur | accéder aux sous-listes | Modifier/organiser les sous-listes |

| Utilisateur | accéder au bouton de création de mots | Ajouter les mots dans les sous-listes |

| Utilisateur | accéder au bouton de suppression de mots | Supprimer les mots dans les sous-listes |

| Utilisateur | accéder au bouton de modification de mots | Modifier les mots dans les sous-listes |

| Utilisateur | Sélectionner un mot | Déplacer/Barré ce dernier |


## Specifications Techniques

---------------------------------------

Technologies employées 

---------------------------------------

 

Logiciels :  

VSCode

PGAdmin

Insomnia

Google Chrome

 

### Front : 

Javascript

Librairies “mineures” : 

Draggable JS

eslint

 

### Back : 

Node.js

Express

Postgresql

librairies “mineures”:

Bcrypt

email-validator

nodemon

pg

body-parser

dotenv

cors

sanitize

eslint

Validateur d’email (register)

 
## Liste des routes prévues (front / back)

---------------------------------------

MLD

---------------------------------------

USER (code_user, Name, Lastname, Mail, Password),

LISTS (code_lists, List1, List2, List3, List4, List5, #userId #short_id),

SHORTLISTS (code_short, Short1, Short2, Short3, #lists_id),

WORDS (code_words, Name, #shortId),



### A TRAVAILLER

 

Front : 

“/” → landing page

“/login” → login et register

“/about” → charte

“/lists” → toutes les listes principales

“/lists/:id” → une liste principale

“/lists/:id/list” → toutes les sous-listes d’un liste principale

 

 

 

 

Back, routes GET :

 

/v1/api/login → login

 /v1/api/register → register

/v1/api/lists → toutes les listes principales

/v1/api/lists/:id → une liste principale

/v1/api/lists/:id/list → sous liste d’une liste principale

 

 

