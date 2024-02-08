Le dictionnaire en Python
=========================

Un dictionnaire est une structure de données construite par des associations ``clé : valeur``. Elle permet d'avoir plusieurs données dans une même variable.

-  Un dictionnaire est de type ``dict``.
-  Un dictionnaire est un type **non ordonné**.
-  Un dictionnaire est un type **mutable**, ce qui signifie qu'on peut modifier ses éléments.
-  Les **clés** d'un dictionnaire sont uniques et non mutables (non modifiables).
-  Les **valeurs** d'un dictionnaire peuvent être de tout type, mutable ou non mutable.
-  Chaque **item** d'un dictionnaire est composé d'une **clé** et d'une **valeur**.

En Python, on note un dictionnaire entre accolades : ``dico={clé 1 : valeur 1, clé 2 : valeur 2, ...}``

.. admonition:: Exemple
   :name: exemple

   On définit une variable ``mon_chien`` de type ``dict`` dont les clés sont ``race``, ``age`` et ``couleur``.

   À chaque clé, on associe les valeurs : ``'labrador'``, ``'noir'`` qui sont de type ``string`` et ``7`` de type ``int``.

   >>> mon_chien = {'race' : 'labrador', 'age' : 7, 'couleur' : 'noir'}
   >>> print(type(mon_chien))
   <class 'dict'>

.. rubric:: Accéder à une valeur d'un dictionnaire

On accède à une valeur d'un dictionnaire avec sa clé:

#. La variable dictionnaire est suivie de la clé notée entre 2 crochets : ``dico[clé]``.
#. La variable est suivie de la méthode ``get`` avec le paramètre ``clé`` : ``dico.get(clé)``

.. admonition:: Exemple
   :name: exemple

   On reprend la variable ``mon_chien`` de type **dict** définie dans l'exemple précédent.

   .. code:: python

      >>> mon_chien = {'race' : 'labrador', 'age' : 7, 'couleur' : 'noir'}

      # obtenir la race de mon chien:
      >>> mon_chien['race']
      'labrador'

      # obtenir l'âge de mon chien:
      >>> mon_chien['age']
      7


Créer un dictionnaire
----------------------

La création d'un dictionnaire se réalise de différentes manières selon qu'il est vide ou avec des valeurs initiales.

.. rubric:: Dictionnaire vide

La fonction ``dict()`` crée un dictionnaire vide.

.. code-block:: python

   dico_1 = dict()
   print(dico_1)
   {}

On peut aussi créer un dictionnaire vide en affectant à la variable une paire d'accolades : 

>>> dico_2 = {}

.. rubric:: Dictionnaire avec valeurs initiales

Pour créer un dictionnaire non vide, contenant des valeurs, on note les associations ``clés:valeurs`` entre accolades en les séparant par une virgule.

.. code:: python

   dico_3 = { 'cle_1' : 'une valeur', 'cle_2' : 'autre valeur'}

La fonction ``dict()`` permet de créer un dictionnaire non vide, contenant des valeurs, en passant en argument de la fonction, les clés et les valeurs associées.

.. code:: python

   dico_4 = dict(cle_1='une valeur',cle_2='autre valeur')


Modifier un dictionnaire
------------------------

.. rubric:: Ajouter ou modifier une valeur

La modification d'un dictionnaire ou l'ajout d'une nouvelle association ``clé : valeur`` se fait directement par affectation : ``dico[nouvelle clé] = valeur``.

-  Si la clé n'existe pas, elle est ajoutée au dictionnaire avec sa valeur associée;
-  Si la clé existe déjà, la valeur est remplacée par la nouvelle valeur.

.. admonition:: Exemple

   On reprend la variable ``mon_chien`` de type **dict** définie dans l'exemple précédent.

   .. code:: python

      # Afficher le dictionnaire de mon chien:
      print(mon_chien)
      {'race': 'labrador', 'age': 7, 'couleur': 'noir'}

      # Modifier la couleur de mon chien:
      >>> mon_chien['couleur'] = 'sable'

      # Modifier l'âge de mon chien:
      >>> mon_chien['age'] += 1

      # Ajouter le poids de mon chien:
      >>> mon_chien['poids'] = 40

      # Afficher le dictionnaire modifié de mon chien:
      >>> print(mon_chien)
      {'race': 'labrador', 'age': 8, 'couleur': 'sable', 'poids': 40}

.. rubric:: Modifier une clé

Il n'est pas possible de modifier une clé ! Mais on peut la supprimer puis en ajouter une nouvelle.

Pour supprimer une association ``clé : valeur``, on utilise la fonction ``del`` avec l'instruction ``del dico[clé]``.

.. admonition:: Exemple
   :name: exemple

   On supprime la clef ``'poids'`` pour la remplacer par la clé ``'masse'`` du dictionnaire ``mon_chien``.

   .. code:: python
      
      >>> mon_chien = {'race': 'labrador', 'age': 8, 'couleur': 'sable', 'poids': 40}
      >>> del mon_chien['poids']
      >>> print(mon_chien)
      {'race': 'labrador', 'age': 8, 'couleur': 'sable'}
      >>> mon_chien['masse']=40
      >>> print(mon_chien)
      {'race': 'labrador', 'age': 8, 'couleur': 'sable', 'masse': 40}

Méthodes sur les dictionnaires
------------------------------

En python, les dictionnaires sont des objets possédants des **méthodes** qui leurs sont propres. Cela signifie qu'elles ne s'appliquent qu'aux dictionnaires.

#. La méthode ``keys()`` renvoie toutes les clés du dictionnaire. La valeur renvoyée par cette méthode est de type ``dict_keys`` qui est **itérable**. Cela signifie que l'on peut accéder à chacune des clés avec une boucle ``for``.
#. La méthode ``values()`` renvoie toutes les valeurs du dictionnaire. La valeur renvoyée par cette méthode est de type
   ``dict_values`` qui est **itérable**. Cela signifie que l'on peut à chacune des valeurs avec une boucle ``for``.
#. La méthode ``items()`` renvoie toutes les assoiations ``clés : valeurs`` du dictionnaire où chaque association est un **tuple**. La valeur renvoyée par cette méthode est de type ``dict_items`` qui est **itérable**. Cela signifie que l'on peut à chacun des tuples avec une boucle ``for``.

.. important::
   
   À noter que les valeurs renvoyées par ces trois méthodes peuvent se transformer en liste avec la fonction ``list()``.

.. admonition:: Exemple

   On applique chacune de ces méthodes au dictionnaire de mon chien.

   .. code:: python

      # Récupérer les clés du dictionnaire mon_chien
      >>> print(mon_chien.keys())
      dict_keys(['race', 'age', 'couleur', 'masse'])

      # Récupérer les valeurs du dictionnaire mon_chien
      >>> print(mon_chien.values())
      dict_values(['labrador', 8, 'sable', 40])

      # Récupérer les items (clé, valeur) du dictionnaire mon_chien
      >>> print(mon_chien.items())
      dict_items([('race', 'labrador'), ('age', 8), ('couleur', 'sable'), ('masse', 40)])

      # Récupérer les valeurs du dictionnaire dans une liste
      >>> v = list(mon_chien.values())
      >>> print("les valeurs dans une liste:",v)
      les valeurs dans une liste: ['labrador', 8, 'sable', 40]

