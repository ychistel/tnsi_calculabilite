Calculabilité - Décidabilité
=============================

Machine de Turing
-------------------

Alan Turing est un mathématicien et informaticien anglais du 20 ième siècle (1912-1954). Il est considéré comme l'inventeur de l'informatique moderne. Il a créé une machine qui porte son nom. La machine de Turing est une machine virtuelle qui effectue des calculs d'une manière mécanique sans intervention de l'homme à part pour
l'entrée des données et la lecture du résultat.

Une machine de Turing comprend:

-   un ruban **infini** divisé en plusieurs cases;
-   une tête de lecture et d'écriture pour lire et écrire sur le ruban;
-   une table de transition qui contient les instructions du programme à réaliser.

La table de transition est divisée en plusieurs états. À chaque état, des informations de lecture et d'écriture sont données selon la valeur lue sur le ruban. Pour chaque information, un nouvel état est indiqué.

.. rubric:: Représentation d'une machine de Turing:
    :name: représentation-dune-machine-de-turing

.. figure:: ../img/machine-turing.png
    :width: 560px
    :alt: machine-turing.png

-   Les cases du ruban sont blanches. Un alphabet est défini à l'avance. Par exemple, pour le binaire, on définit un alphabet de 3 symboles : ``0``, ``1`` et ``blanc``.
-   La tête de "lecture - écriture" peut se déplacer à droite ou à gauche. Elle peut lire ou écrire les symboles de l'alphabet sur le ruban. 
-   Les différents états de la table de transition indiquent si la tête de "lecture - écriture" doit lire ou écrire un symbole de l'alphabet et se déplacer à droite ou à gauche.
-   À l'issue du traitement, un nouvel état (ou la répétition du même état) est indiqué.
-   Un état final met fin à l'exécution du programme.

.. rubric:: Simuler une machine de Turing
    :name: simuler-une-machine-de-turing

Il existe des concepteurs de machines de Turing. Il existe également des programmes qui permettent d'appliquer une machine de Turing à un ruban virtuel. Ci-dessous, un programme **javascript**, qui simule une machine de Turing.

|simulateur-machine-turing.png|

Vous pouvez compléter la table de transition pour vérifier votre code. **Attention**, la tête de lecture est située sous le chiffre de gauche et peut nécessiter un état supplémentaire.

Machine universelle
--------------------

Turing a montré qu'il existe une machine de Turing **universelle** qui peut simuler n'importe quelle autre machine de Turing et donc exécuter n'importe quel programme. La table de transition d'une machine de Turing  est donnée à la machine universelle. Cette table de transition devient une donnée de la machine universelle codée sur le ruban qu'elle va lire.

.. important::

    Un programme peut donc être une donnée d'un autre programme. 

Nous avons différents exemples de situations ou des programmes sont des données d'un autre programme:

#.  Un système d'exploitation est un ensemble de programmes capbles d'exécuter différents programmes. Cela signifie qu'il sont les données des programmes du système d'exploitation.
#.  Les logiciels sont pour la plupart des programmes compilés, par souci d'optimisation. Cela signifie qu'ils sont transformés en fichiers binaires directement lisibles par le processeur et donc rapide à l'exécution. La compilation est un programme qui prend en donnée un programme écrit dans un certain langage et le transforme en fichier binaire exécutable. Par exemple, sur le système Linux, on a le compilateur **gcc**.
#.  Python est un langage **interprété**. L'interpréteur de python est un programme qui prend en donnée chaque instruction du programme écrit en Python et la rend exécutable par l'ordinateur. 


Calculabilité - Décidabilité
-----------------------------

Un ordinateur peut-il tout calculer ? Tout problème peut-il être résolu par un algorithme ? Cette question a été résolue dans les années 1936 - 1937 par Alan Turing et Alonso Church. Ils ont montré, par deux approches différentes, que certains problèmes étéient **indécidable** et que des nombres sont non **calculables**.

.. rubric:: Calculabilité

Un nombre est **calculable** s'il peut être obtenu par une machine de Turing. Aujourd'hui un nombre est **calculable** s'il existe un algorithme ou un programme capable de donner les chiffres de son écriture décimale qui peut être infinie. Cela s'applique également aux fonctions qui donnent une valeur numérique en retour.

.. rubric:: Décidabilité

En logique, une proposition peut être vraie ou fausse. Lorsqu'on est capable de démontrer qu'une proposition est vraie ou fausse, on dit que la proposition est **décidable**. Si on est incapable de montrer qu'elle est vraie ou fausse, la proposition est **indécidable**.

.. rubric:: Preuve de l'indécidabilité

Alan Turing a montré en 1936, qu'il y a des problèmes indécidables. Il l'a montré avec le **problème de l'arrêt**.

On considère que les algorithmes sont de 2 natures. Ceux qui s'arrêtent et ceux qui ne s'arrêtent pas. 

La preuve repose sur un raisonnement par l'absurde qui suppose qu'il existe une fonction ``Arret`` qui dit si une fonction s'arrête ou ne s'arrête pas.

.. figure:: ../img/probleme_arret.svg
    :align: center

On construit un programme ``P`` qui prend une donnée ``x`` en entrée, utilise la fonction ``Arret`` et qui:

-   tombe dans une boucle infinie si la fonction ``Arret`` renvoie ``oui``;
-   s'arrrête si la fonction ``Arret`` renvoie ``non``.

.. figure:: ../img/probleme_arret_2.svg
    :align: center
    :width: 560px

Si on applique le programme ``P`` en prenant ``P`` donnée, on a deux cas à envisager:

#.  Soit le programme ``P`` s'arrête et alors il tombe dans une boucle infinie et donc il ne s'arrête pas;
#.  Soit le programme ``P`` ne s'arrête pas et alors il renvoie STOP et donc s'arrête.

Dans les 2 cas nous avons une contradiction. Cela signifie que l'hypothèse initiale est fausse et donc que le problème de l'arrêt n'existe pas.

Le problème de l'arrêt ne peux pas se résoudre par un algorithme donc c'est un problème **indécidable**.

Il existe d'autres problèmes indécidables et fonctions non calculables. Cela prouve qu'un ordinateur ne peut pas tout calculer ou tout décider.

Voici 2 vidéos de la démonstration du **problème de l'arrêt**:

#.  |problème de l'arrêt|

#.  |preuve du problème de l'arrêt|

.. rubric:: Sitographie
    :name: sitographie

Les liens des sites qui ont documenté cette page et pour approfonfir la notion.

-  `Un prototype programmable pour concrétiser la machine de Turing <https://machinedeturing.com/>`__
-  `Comment fonctionne une machine de Turing ? <https://interstices.info/comment-fonctionne-une-machine-de-turing/>`__
-  `Du carreau de Truchet au carreau de Wang : atteindre l’atome de l’apériodique et du calculable <https://images.math.cnrs.fr/Du-carreau-de-Truchet-au-carreau-de-Wang-atteindre-l-atome-de-l-aperiodique-et.html>`__


.. |simulateur-machine-turing.png| image:: ../img/simulateur-machine-turing.png
    :target: https://morphett.info/turing/turing.html
.. |problème de l'arrêt| image:: http://img.youtube.com/vi/92WHN-pAFCs/0.jpg 
    :target: https://www.youtube.com/watch?v=92WHN-pAFCs
    :class: margin-0-auto
.. |preuve du problème de l'arrêt| image:: ../img/video_pb_arret.png
    :target: https://www.youtube.com/watch?v=13O1qhX4Bqo
    :class: margin-0-auto