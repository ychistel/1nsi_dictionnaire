Activité sur les dictionnaires
==============================

En python, un **dictionnaire** est une structure de données native notée entre **accolades**. Chaque ``valeur`` du dictionnaire est repèrée par une ``clé`` unique.

Le dictionnaire : ``{clé_1:valeur 1, clé_2: valeur 2, clé_3 : valeur 3}`` contient trois items. 

- Les clés du dictionnaires sont ``clé_1``, ``clé_2`` et ``clé_3``. 
- Les valeurs sont ``valeur 1``, ``valeur 2`` et ``valeur 3``.

Dans cette activité, on construit un dictionnaire contenant des informations sur une personne :

-  son prénom
-  son âge
-  son animal
-  sa couleur préférée

On définit pour ce dictionnaire les clés : ``prénom``, ``age``, ``animal`` et ``couleur``. Les quatres clés sont de type ``str`` (chaine de caractères).

Les valeurs associées à ces clés sont de type ``str`` sauf pour la clé ``age`` dont la valeur est de type ``int``.

Créer un dictionnaire
---------------------

#. Donner l'écriture du dictionnaire contenant les informations sur un individu qui s'appelle ``Bob`` agé de 20 ans, qui a un chien et dont la couleur préférée est le bleu.
#. Écrire ce dictionnaire en Python affecté à la variable ``dico``.
#. La fonction ``len`` renvoie le nombre d’éléments d’un dictionnaire.
   Écrire une instruction python donnant le nombre d'items ``clé:valeur`` du dictionnaire ``dico``.
#. Créer un dictionnaire contenant des informations relatives à vous-même enregistré dans la variable ``mon_dico``.

Accéder à un dictionnaire
-------------------------

Voici 4 méthodes que l'ont peut utiliser sur les dictionnaires:

-  La méthode ``get(clé)`` prend en paramètre une ``clé`` du dictionnaire et renvoie la valeur associée à cette clé. Par exemple ``dico.get('prénom')`` renvoie la valeur ``Bob``.
-  La méthode ``keys()`` renvoie les clés d’un dictionnaire; Le type renvoyé est objet itérable, ce qui permet de parcourir son contenu avec une boucle. Par exemple ``dico.keys()`` renvoie les clés ``prénom``, ``age``, ``animal`` et ``couleur``.
-  La méthode ``values()`` renvoie les valeurs d’un dictionnaire; Le type renvoyé est objet itérable, ce qui permet de parcourir son contenu avec une boucle. Par exemple, ``dico.values()`` renvoie toutes les valeurs du dicionnaire ``dico``.
-  La méthode ``items()`` renvoie les paires ``(clé, valeur)`` d’un dictionnaire; Le type renvoyé est objet itérable, ce qui permet de parcourir son contenu avec une boucle.

Écrire des instructions en Python pour:

#. afficher la couleur préférée du dictionnaire ``dico``
#. afficher l'âge enregistré dans le dictionnaire ``dico``
#. afficher les clefs du dictionnaire ``dico``.
#. afficher les valeurs du dictionnaire ``dico``

Modifier les valeurs d'un dictionnaire
--------------------------------------

Chaque valeur d'un dictionnaire peut être modifiée avec une affectation. La syntaxe est la suivante:

.. code:: python

   dico['clé'] = nouvelle_valeur

#. Remplacer l'animal préféré de ``Bob`` par la valeur ``escargot``
#. Remplacer l'âge dans votre dictionnaire par celui que vous aurez l'an prochain.

On peut ajouter une valeur supplémentaire dans un dictionnaire (non prévue à la création). Pour cela il suffit de créer une nouvelle clé avec une nouvelle valeur en suivant la syntaxe:

.. code:: python
   
   dico['nouvelle_clé'] = nouvelle_valeur

#. Ajouter au dictionnaire ``dico`` la clé ``instrument`` et la valeur ``harmonica``.
#. Ajouter dans votre dictionnaire votre instrument préféré.
