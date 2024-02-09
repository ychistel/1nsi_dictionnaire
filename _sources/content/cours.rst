Le dictionnaire en Python
=========================

.. admonition:: Définition
   :class: definition

   Un dictionnaire est une structure de données construite par des associations ``clé : valeur``. Elle permet d'avoir plusieurs données dans une même variable.

   -  Un dictionnaire est de type ``dict``.
   -  Un dictionnaire est un type **mutable**, ce qui signifie qu'on peut modifier ses éléments.
   -  Les **clés** d'un dictionnaire sont uniques et non mutables (non modifiables).
   -  Les **valeurs** d'un dictionnaire peuvent être de tout type, mutable ou non mutable.
   -  Chaque **item** d'un dictionnaire est composé d'une **clé** et d'une **valeur**.

En Python, on note un dictionnaire entre accolades. Par exemple, on définit une variable ``mon_chien`` de type ``dict`` dont les clés sont ``race``, ``age`` et ``couleur``.
À chaque clé, on associe les valeurs : ``'labrador'``, ``'noir'`` qui sont de type ``string`` et la valeur ``7`` de type ``int``.

Dans la console Python:

>>> mon_chien = {'race' : 'labrador', 'age' : 7, 'couleur' : 'noir'}
>>> print(type(mon_chien))
<class 'dict'>

.. rubric:: Accéder à une valeur d'un dictionnaire

.. admonition:: Syntaxe
   :class: propriete

   On accède à une valeur d'un dictionnaire avec sa clé:

   #. La variable dictionnaire est suivie de la clé notée entre 2 crochets : ``dico[clé]``.
   #. La variable est suivie de la méthode ``get`` avec le paramètre ``clé`` : ``dico.get(clé)``


On reprend la variable ``mon_chien`` de type **dict** définie dans l'exemple précédent.

>>> mon_chien = {'race' : 'labrador', 'age' : 7, 'couleur' : 'noir'}

Pour obtenir la race de mon chien:

>>> mon_chien['race']
'labrador'
>>> mon_chien.get('race')
'labrador'

Pour obtenir l'âge de mon chien:

>>> mon_chien['age']
7
>>> mon_chien.get('age')
7

Créer un dictionnaire
----------------------

La création d'un dictionnaire se réalise de différentes manières selon qu'il est vide ou avec des valeurs initiales.

.. rubric:: Dictionnaire vide

La fonction ``dict()`` crée un dictionnaire vide.

>>> dico_1 = dict()
>>> print(dico_1)
{}

On peut aussi créer un dictionnaire vide en affectant à la variable une paire d'accolades : 

>>> dico_2 = {}

.. rubric:: Dictionnaire avec valeurs initiales

Pour créer un dictionnaire contenant des valeurs, on note les associations ``clés:valeurs`` entre accolades en les séparant par une virgule.

.. code:: python

   dico_3 = { 'cle_1' : 'une valeur', 'cle_2' : 'autre valeur'}

La fonction ``dict()`` permet de créer un dictionnaire non vide, contenant des valeurs, en passant en argument de la fonction, les clés et les valeurs associées.

.. code:: python

   dico_4 = dict(cle_1='une valeur',cle_2='autre valeur')


Modifier un dictionnaire
------------------------

.. rubric:: Ajouter ou modifier une valeur

.. admonition:: Syntaxe
   :class: propriete

   La modification d'un dictionnaire ou l'ajout d'une nouvelle association ``clé : valeur`` se fait directement par affectation : ``dico[nouvelle clé] = valeur``.

   -  Si la clé n'existe pas, elle est ajoutée au dictionnaire avec sa valeur associée;
   -  Si la clé existe déjà, la valeur est remplacée par la nouvelle valeur.

On reprend la variable ``mon_chien`` de type **dict** définie dans l'exemple précédent.

On affiche le dictionnaire ``mon_chien``

>>> print(mon_chien)
{'race': 'labrador', 'age': 7, 'couleur': 'noir'}

On modifie la couleur de mon chien par la valeur ``sable``

>>> mon_chien['couleur'] = 'sable'

On modifie l'âge de mon chien

>>> mon_chien['age'] += 1

On ajoute le poids de mon chien en créant la clé ``poids`` 

>>> mon_chien['poids'] = 40

Afficher le dictionnaire modifié de mon chien:

>>> print(mon_chien)
{'race': 'labrador', 'age': 8, 'couleur': 'sable', 'poids': 40}

.. rubric:: Modifier une clé

.. warning::

   Il n'est pas possible de modifier une clé ! Mais on peut la supprimer puis en ajouter une nouvelle.

   La suppression de la clé d'un dictionnaire entraine la suppression de la valeur!

   Pour supprimer une ``clé``, on utilise la fonction ``del`` avec l'instruction ``del dico[clé]``.

Dans l'exemple suivant, on définit un dictionnaire ``mon_chien`` avec la clé ``poids``. Ensuite, on supprime la clé ``'poids'`` pour la remplacer par la clé ``'masse'``. On donne ci-dessous les différentes instructions pour le réaliser.

On définit notre dictionnaire ``mon_chien``

>>> mon_chien = {'race': 'labrador', 'age': 8, 'couleur': 'sable', 'poids': 40}

On supprime la clé ``poids`` du dictionnaire et on l'affiche

>>> del mon_chien['poids']
>>> print(mon_chien)
{'race': 'labrador', 'age': 8, 'couleur': 'sable'}

On ajoute la nouvelle clé ``masse`` associée à la valeur ``40`` au dictionnaire et on l'affiche

>>> mon_chien['masse']=40
>>> print(mon_chien)
{'race': 'labrador', 'age': 8, 'couleur': 'sable', 'masse': 40}

Méthodes sur les dictionnaires
------------------------------

.. admonition:: Définition
   :class: definition
      
   En python, les dictionnaires sont des objets possédants des **méthodes** qui leurs sont propres. Cela signifie qu'elles ne s'appliquent qu'aux dictionnaires.

   Les **méthodes** sont des fonctions qui s'appliquent avec la notation **pointée**. Cela signfie qu'on les appelle en les plaçant après la variable de type dictionnaire séparée par un **point**.

.. admonition:: Méthodes
   :class: propriete

   #. La méthode ``keys()`` renvoie toutes les clés du dictionnaire. La valeur renvoyée par cette méthode est de type ``dict_keys``.
   #. La méthode ``values()`` renvoie toutes les valeurs du dictionnaire. La valeur renvoyée par cette méthode est de type ``dict_values``.
   #. La méthode ``items()`` renvoie toutes les assoiations ``clés : valeurs`` du dictionnaire où chaque association est un **tuple**. La valeur renvoyée par cette méthode est de type ``dict_items``.

.. important::
   
   #. Les types ``dict_keys``, ``dict_values`` et ``dict_items`` sont **itérables**. Cela signifie qu'on peut accéder à chacune des valeurs avec une boucle (``for`` ou ``while``).
   #. Les types ``dict_keys``, ``dict_values`` et ``dict_items`` peuvent se transformer en liste avec la fonction ``list()``.


On applique chacune de ces méthodes au dictionnaire ``mon_chien``.

Récupérer les clés du dictionnaire ``mon_chien``

>>> print(mon_chien.keys())
dict_keys(['race', 'age', 'couleur', 'masse'])

Récupérer les valeurs du dictionnaire ``mon_chien``

>>> print(mon_chien.values())
dict_values(['labrador', 8, 'sable', 40])

Récupérer les items (clé, valeur) du dictionnaire ``mon_chien``

>>> print(mon_chien.items())
dict_items([('race', 'labrador'), ('age', 8), ('couleur', 'sable'), ('masse', 40)])

Récupérer les valeurs du dictionnaire ``mon_chien`` dans une liste

>>> v = list(mon_chien.values())
>>> print("les valeurs dans une liste:",v)
les valeurs dans une liste: ['labrador', 8, 'sable', 40]