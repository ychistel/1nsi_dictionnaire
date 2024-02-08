Épreuve pratique
================

Exercice 1
----------

Les résultats d'un vote ayant trois issues possibles \'A\', \'B\' et \'C\' sont stockés dans un tableau.

.. admonition:: Exemple

   Urne = [ \'A\', \'A\', \'A\', \'B\', \'C\', \'B\', \'C\', \'B\', \'C\', \'B\' ]

La fonction ``depouille`` doit permettre de compter le nombre de votes exprimés pour chacune des issues. Elle prend en paramètre un tableau et renvoie le résultat dans un dictionnaire dont les clés sont les noms des issues et les valeurs le nombre de votes en leur faveur.

La fonction ``vainqueur`` doit désigner le nom du ou des gagnants. Elle prend en paramètre un dictionnaire dont la structure est celle du dictionnaire renvoyé par la fonction depouille et renvoie un tableau. Ce tableau peut donc contenir plusieurs éléments s’il y a des ex-aequo.

Compléter les fonctions ``depouille`` et ``vainqueur`` fournies ci-après pour qu’elles renvoient les résultats attendus.

.. literalinclude:: ../python/BCG_NSI_1.py

.. admonition:: Exemples d’utilisation
   
   >>> election = depouille(urne)
   >>> election
   {'B': 4, 'A': 3, 'C': 3}
   >>> vainqueur(election)
   ['B']

Exercice 2
----------

Sur le réseau social TipTop, on s’intéresse au nombre de « like » des abonnés. Les données sont stockées dans des dictionnaires où les clés sont les pseudos et les valeurs correspondantes sont les nombres de « like » comme ci-après : ``{'Bob': 102, 'Ada': 201, 'Alice': 103, 'Tim': 50}``

Écrire une fonction ``max_dico`` qui :

-  prend en paramètre un dictionnaire dico non vide dont les clés sont des chaînes de caractères et les valeurs associées sont des entiers positifs ou nuls ;
-  renvoie un tuple dont :
    
   - la première valeur est une clé du dictionnaire associée à la valeur maximale ;
   - la seconde valeur est la valeur maximale présente dans le dictionnaire.

.. admonition:: Exemples

   >>> max_dico({'Bob': 102, 'Ada': 201, 'Alice': 103, 'Tim': 50})
   ('Ada', 201)
   >>> max_dico({'Alan': 222, 'Ada': 201, 'Eve': 220, 'Tim': 50})
   ('Alan', 222)

Exercice 3
----------

Un professeur de NSI décide de gérer les résultats de sa classe sous la forme d’un dictionnaire :

-  les clefs sont les noms des élèves ;
-  les valeurs sont des dictionnaires dont les clefs sont les types d’épreuves sous forme de chaîne de caractères et les valeurs sont les notes obtenues associées à leurs coefficients dans une liste.

Avec :

.. code-block:: python

   resultats = {'Dupont': {
                  'DS1': [15.5, 4],
                  'DM1': [14.5, 1],
                  'DS2': [13, 4],
                  'PROJET1': [16, 3],
                  'DS3': [14, 4]
               },
                  'Durand': {
                  'DS1': [6 , 4],
                  'DM1': [14.5, 1],
                  'DS2': [8, 4],
                  'PROJET1': [9, 3],
                  'IE1': [7, 2],
                  'DS3': [8, 4],
                  'DS4':[15, 4]
               }
   }

L’élève dont le nom est Durand a ainsi obtenu au DS2 la note de 8 avec un coefficient 4.

Le professeur crée une fonction moyenne qui prend en paramètre le nom d’un de ses élèves et renvoie sa moyenne arrondie au dixième.

Compléter le code du professeur ci-dessous :

.. literalinclude:: ../python/BCG_NSI_16.py

Exercice 4
----------

Le nombre d’occurrences d’un caractère dans une chaîne de caractère est le nombre d’apparitions de ce caractère dans la chaîne.

.. admonition:: Exemples
   
   -  le nombre d’occurrences du caractère \'o\' dans \'bonjour\' est 2 ;
   -  le nombre d’occurrences du caractère \'b\' dans \'Bébé\' est 1 ;
   -  le nombre d’occurrences du caractère \'B\' dans \'Bébé\' est 1 ;
   -  le nombre d’occurrences du caractère \' \' dans \'Hello world !\' est 2.

On cherche le nombre d’occurrences des caractères dans une chaîne de caractères. On souhaite stocker ces nombres d’occurrences dans un dictionnaire dont les clefs seraient les caractères de la chaîne et les valeurs le nombre d’occurrences de ces caractères.

.. admonition:: Exemple
   
   Avec la phrase 'Hello world !' le dictionnaire est le suivant :

   ``{'H': 1, 'e': 1, 'l': 3, 'o': 2, ' ': 2, 'w': 1,'r': 1, 'd': 1, '!': 1}``
   
   L’ordre des clefs n’a pas d’importance. 
   
Écrire une fonction ``nbr_occurrences`` prenant comme paramètre une chaîne de caractères ``chaine`` et renvoyant le dictionnaire des nombres d’occurrences des caractères de cette chaîne.

Exercice 5
----------

Écrire une fonction ``enumere`` qui prend en paramètre une liste ``L`` et renvoie un dictionnaire ``d`` dont les clés sont les éléments de ``L`` avec pour valeur associée la liste des indices de l’élément dans la liste ``L``.

.. admonition:: Exemple

   >>> enumere([1, 1, 2, 3, 2, 1])
   {1: [0, 1, 5], 2: [2, 4], 3: [3]}

Exercice 6
----------

On considère au plus 26 personnes A, B, C, D, E, F ... qui peuvent s'envoyer des messages avec deux règles à respecter :

- chaque personne ne peut envoyer des messages qu'à une seule personne (éventuellement elle-même),
- chaque personne ne peut recevoir des messages qu'en provenance d'une seule personne (éventuellement elle-même).

.. admonition:: Exemple

   Avec 6 personnes - de « plan d'envoi des messages » qui respecte les règles ci-dessus, puisque chaque personne est présente une seule fois dans chaque colonne :

   - A envoie ses messages à E
   - E envoie ses messages à B
   - B envoie ses messages à F
   - F envoie ses messages à A
   - C envoie ses messages à D
   - D envoie ses messages à C

   Le dictionnaire correspondant à au plan d'envoi ci-dessus est le suivant :
   
   ``plan_a = {'A':'E', 'B':'F', 'C':'D', 'D':'C', 'E':'B', 'F':'A'}``

Un cycle est une suite de personnes dans laquelle la dernière est la même que la première.
Sur le plan d'envoi ``plan_a`` des messages ci-dessus, il y a deux cycles distincts : un
premier cycle avec A, E, B, F et un second cycle avec C et D.

En revanche, le plan d’envoi ``plan_b = {'A':'C', 'B':'F', 'C':'E', 'D':'A', 'E':'B', 'F':'D'}`` comporte un unique cycle : A, C, E, B, F, D. Dans ce cas, lorsqu’un plan d’envoi comporte un unique cycle, on dit que le plan d’envoi est cyclique.

Pour savoir si un plan d'envoi de messages comportant N personnes est cyclique, on peut utiliser l'algorithme ci-dessous :

-  on part d’un expéditeur (ici A) et on inspecte son destinataire dans le plan d'envoi,
-  chaque destinataire devient à son tour expéditeur, selon le plan d’envoi, tant qu’on ne « retombe » pas sur l’expéditeur initial,
-  le plan d’envoi est cyclique si on l’a parcouru en entier.

Compléter la fonction ``est_cyclique`` suivante en respectant la spécification.

.. literalinclude:: ../python/BCG_NSI_38.py

.. hint::
   
   la fonction Python ``len`` permet d'obtenir la longueur d'un dictionnaire.