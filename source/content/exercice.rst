Exercices
=========

.. exercice::

    .. figure:: ../img/machine-turing.png
        :width: 560px
        :align: center
        
    L'exemple de la machine de Turing ci-dessus est appliqué au nombre binaire 111 avec la tête de lecture située sous le chiffre 1 situé le plus à droite. Quel est le résultat écrit sur le ruban après exécution de la machine de Turing ?
    
.. exercice::
    
    On donne la table de transition suivante:

    .. figure:: ../img/table_transition_2.png
        :align: center
    
    #.  Appliquer la machine de turing avec cette table de transition sur le nombre binaire ``1001`` en positionnant la tête de "lecture - écriture" sous le bit de poids faible (le plus à droite).
    #.  Ajouter une étape à la table de transition pour que la tête de lecture soit positionnée sous le bit de poids faible en fin de programme.

.. exercice::

    #.  Écrire la table de transition d'une machine de Turing qui ajoute 1 à un nombre binaire inscrit sur le ruban.
    #.  Écrire la table de transition d'une machine de Turing qui multiplie par 2 un nombre binaire inscrit sur le ruban.


.. exercice::

    En binaire, un nombre positif a un bit de poids fort égal à 0 et un nombre négatif a un bit de poids fort égal à 1. 
    
    Pour connaître la valeur absolue d’un nombre, on applique la méthode du complément à 2 : complément à 1 puis ajout de 1. 

    Écrire la table de transition d'une machine de Turing qui donne la valeur absolue d'un nombre binaire inscrit sur le ruban.

.. exercice::

    Le langage Python possède deux instructions, **eval** et **exec**, qui prennent en entrée des chaines de caractères et cherchent à les exécuter.

    #.  Ouvrir l'éditeur Python Thonny et créer un fichier python nommé ``donnée-programme.py``.
    #.  Écrire l'instruction python qui affiche le message ``machine de Turing``.
    #.  Transformer cette instruction en chaine de caractères puis procéder à son exécution avec l'instruction ``eval``.
    #.  Écrire un programme qui vérifie la parité d'un nombre entier saisi par l'utilisateur sous forme d'une chaîne de caractères. Procéder à son exécution dans l'interpréteur python.
    #.  Écrire la création d'une liste de nombres entiers positifs multiples de 3 compris entre 1 et 20 sous forme d'une chaine de caractères. Procéder à son exécution et contrôler le résultat.