Exercice sur les dictionnaires
==============================

Exercice 1
----------

On donne le dictionnaire suivant:

.. code-block:: python

   animaux={
       'chien':'rouky',\
       'chat':'berlioz',\
       'éléphant':'dumbo',\
       'ours':'baloo',\
       'panthère': 'bagheera',\
       'serpent':'kaa',\
       'renard':'rox'
   }

#. Est-il possible d’ajouter la clé ``tigre`` avec la valeur ``shere khan`` au dictionnaire? Justifier.
#. Est-il possible d’ajouter la clé ``chien`` avec la valeur ``pongo`` au dictionnaire? Justifier.
#. Comment récupérer la valeur ``berlioz`` de ce dictionnaire ?
#. Comment récupérer la valeur de la clé ``panthère`` du dictionnaire?
#. Comment ajouter la souris nommée bernard au dictionnaire ?
#. Comment ajouter aussi la souris nommée Bianca au dictionnaire ?
#. Comment remplacer la clé ``serpent`` par la clé ``snake`` en gardant la valeur ``kaa``?
#. Comment récupérer dans une liste python toutes les clés du dictionnaire ?
#. Comment récupérer dans une liste python toutes les valeurs du dictionnaire ?
#. Comment connaitre le nombre d’éléments de ce dictionnaire ?

Exercice 2
----------

On considère le dictionnaire suivant: 

>>> loisir = {'jeu':'minecraft', 'sport':'basket-ball', 'instrument':'guitare'}

#. On donne le code Python suivant:
   
   .. literalinclude:: ../python/code_python.py
      :lines: 3-7

   a. On réalise l'appel ``mystere_1(loisir,'guitare')``. Quelle est la valeur renvoyée par cet appel de la fonction ``mystere_1`` ?
   b. On réalise l'appel ``mystere_1(loisir,'football')``. Quelle est la valeur renvoyée par cet appel de la fonction ``mystere_1`` ?

#. On donne le code Python de la fonction ``mystere_2``.

   .. literalinclude:: ../python/code_python.py
      :lines: 9-16

   a. Que renvoie l'appel ``mystere_2(loisir,'sport','football')`` ? Justifier.
   b. Que renvoie l'appel ``mystere_2(loisir,'lecture','Billy Summers')`` ? Justifier.


Exercice 3
----------
On considère le dictionnaire ``notes`` suivant: ``{'maths':12,'francais':11,'nsi':14,'anglais':13,'eps':10}``

On précise que pour ce dictionnaire:

-  Les clés sont des matières sous forme de chaines de caractères (maths, français,...);
-  Les valeurs sont des moyennes de type entier ou float.

#. En utilisant uniquement des instructions Python sur le dictionnaire ``notes``:

   a. Ajouter la matière espagnol et la note :math:`17`.
   b. Modifier la note de nsi avec la valeur :math:`15`.

#. On veut calculer la moyenne des notes d'un dictionnaire.
   Écrire une fonction ``moyenne`` qui a pour paramètre un dictionnaire ``dico`` et qui calcule la moyenne des notes du dictionnaire.

   Par exemple, ``moyenne(notes)`` renvoie la valeur 13 (après modifications).

#. On veut connaitre la note la plus faible du dictionnaire ``notes``.
   Écrire la fonction ``valeur_mini`` qui prend en argument un dictionnaire ``dico`` et renvoie la valeur minimale du dictionnaire passé en argument. On admet que les valeurs sont comprises entre 0 et 20 (inclus).

#. On souhaite maintenant connaitre la matière qui a la note la plus faible dans le dictionnaire.
   Écrire la fonction ``matiere_faible`` qui prend en paramètre un dictionnaire et qui renvoie la matière qui a la note la plus faible. On peut utiliser la fonction précédente ``valeur_mini``.



Exercice 4
----------

Un restaurant utilise un dictionnaire défini par les clés ``entrée``, ``plat``, ``dessert`` et ``prix`` permettant de stocker les informations sur les menus qu'il propose à chacun de ses clients.

Ce restaurant propose 3 menus A, B et C :

.. rubric:: menu A

-  Entrée : avocat crevettes
-  Plat : lasagnes de légumes
-  Dessert : tarte aux pommes
-  Prix : 12 euros

.. rubric:: menu B

-  Entrée : tomate mozarella
-  Plat : sole meunière et légumes
-  Dessert : tiramisu
-  Prix : 16 euros

.. rubric:: menu C

-  Entrée : macédoine de légumes
-  Plat : filet mignon et frites
-  Dessert : mousse au chocolat
-  Prix : 15 euros

#. Créer pour chaque menu le dictionnaire associé. On les notera respectivement ``menu_a``, ``menu_b`` et ``menu_c``.
#. Une erreur a été repérée dans le menu B. Le fromage "mozzarella" s'écrit avec deux "z". Proposer une instruction python pour corriger cette erreur.
#. Le restaurant a servi 10 menus A, 21 menus B et 9 menus C. Calculer la recette du restaurant pour ce service.

Le restaurant souhaite calculer directement la recette d'un service à partir des commandes des clients selon les menus A, B et C.

#. La fonction ``recette`` prend en paramètres ``a``, ``b`` et ``c`` associés respectivement aux nombres de menus A, B et C servis. La fonction renvoie la recette totale du service.

   a. Écrire un code en Python de la fonction recette.
   b. Appliquer cette fonction aux valeurs de la question précédente.

#. On change le prix du menu A dans le dictionnaire qui passe à 13 euros. 

   a. La fonction ``recette`` est-elle toujours fonctionnelle ? 
   b. Effectuer les modifications pour que la fonction reste toujours fonctionnelle quel que soit le prix des menus.

Le restaurant accepte, pour un prix de 17 euros, de servir aux clients des menus composés à partir des trois menus A, B et C. Pour réaliser ce menu spécial, on crée un dictionnaire dont les clés sont ``entree``, ``plat`` et ``dessert`` et dont les valeurs sont les lettres ``"A"``, ``"B"`` et ``"C"`` associés aux choix des clients selon les menus A, B et C.

Par exemple, un client nommé Bob, prend l'entrée du menu A, le plat du menu C et le dessert du menu B. Le dictionnaire associé à son choix est ``{ 'entree':"A", 'plat':"C", 'dessert':"B" }``.

#. La fonction ``compose`` prend en paramètre un dictionnaire menu spécial et renvoie le dictionnaire correspondant au menu composé par le client. Écrire la fonction ``compose`` en Python.
#. L'entrée du menu A est changée par des carottes rapées. Vérifier que la composition du menu spécial renvoie le bon menu avec la nouvelle entrée. Si ce n'est pas le cas, adapter votre code.

Exercice 5
----------

Le fichier ``capitales.py`` contient les différents pays du monde et leurs capitales réunis dans un même dictionnaire nommé ``capitales``. Les clés de ce dictionnaire sont les noms des pays et les valeurs sont les capitales de chacun de ces pyas. Toutes les valeurs sont des chaines de caractère. 

Voici un extrait de ce dictionnaire:

.. literalinclude:: ../python/capitales.py
   :lines: 1-10
   
Pour utiliser ce dictionnaire, vous devez enregistrer ce fichier dans le même dossier que votre fichier de travail, puis réaliser un import.

.. code-block:: python
   
   from capitales import capitales

Télécharger le fichier ``capitales.py`` disponible sur l'ENT puis importer le dans un nouveau fichier de travail python.

Pour vérifier le bon import du dictionnaire, vous pouvez afficher le nombre de valeurs contenues dans le dictionnaire avec l'instruction ``len(capitales)`` en console.

#. En console, écrire une instruction python qui affiche la capitale de l'**Uruguay**.
#. En console, écrire une instruction Python qui donne le pays dont la capiltale est **Oulan-Bator**.

#. On veut créer un tableau ``pays`` qui contient tous les pays du dictionnaire ``capitales`` dont le nom commence par une lettre donnée. 

   a.  Écrire une fonction ``cle_par_initiale`` qui prend en paramètres un dictionnaire ``dico`` et une lettre ``lettre``. Cette fonction renvoie un tableau contenant toutes les clés du dictionnaire dont l'initiale est donnée par l'argument ``lettre``. Si aucune clé ne convient, la fonction renvoie un tableau vide.

      Par exemple, pour le dictionnaire ``dico = {'cle':6,'clou':4,'vis':8,'ecrou':6}``, l'appel ``cle_par_initiale(dico,'c')`` renvoie le tableau ``['cle','clou']`` et l'appel ``cle_par_initiale(dico,'s')`` renvoie ``[]``.

   b.  Quel appel doit-on écrire avec la fonction précédente pour obtenir les pays dont le nom commence par la lettre **P** ?

#. On veut créer un tableau ``capitales`` qui contient toutes les capitales du dictionnaire dont le nom commence par une lettre donnée. 
 
   a. En vous inspirant du code précédent, écrire une fonction ``valeur_par_initiale`` qui crée ce tableau.
   b. Comment peut-on créer le tableau contenant toutes les capitales commençant par la lettre **L** ?

#. Certains pays ont un nom de capitale identique au nom du pays. Cela revient à chercher dans un dictionnaire tous les items dont la clé est égale à la valeur. 
 
   Par exemple, le dictionnaire ``{'a':'a' , 'b':'b', 'c':'ab'}`` possède 2 items dont les clés et les valeurs sont identiques.

   a. Écrire la fonction ``cle_egale_valeur`` qui prend en paramètre un dictionnaire et renvoie dans un tableau les clés ou les valeurs lorsque celle-ci sont égales. S'il n'y en a pas, un tableau vide est renvoyé.
   b. Combien de pays ont un nom de capitale identique au nom du pays ?