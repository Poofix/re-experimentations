Groupe Model : GLORIES Ancelin  CESCHIN Quentin


# RequirementEngineeringExperimentations

Dans ce read me vous trouverez les diff�rents diagrammes mod�lisant les exigences de ce projet.


## Le digramme des cas d'utilisations

### D�finition des acteurs : 

Par rapport aux exigences, nous allons ajouter un sc�nario d'utilisation : l'utlisateur souhaite se d�placer en voiture tous les jours � 16h30.
On souhaite mesurer diff�rentes grandeurs afin de pouvoir afficher � l'utilisateur l'�tat de sant� de sa maison. La maison va devoir synth�tiser une conclusion compr�hensible pour un humain � partir des donn�es mesur�es et les rendres visibles pour l'utilisateur.


![UseCaseImage](./diagrams/PNGs/SysML_1_4_Use_Case_Diagram.PNG)

## Le diagramme de d�finition de blocs

Une maison va posseder plusieurs capteurs qui s'occuperont de mesurer les diff�rentes grandeurs. Il en va de m�me pour la voiture. De cette fa�on, ces deux derniers n'ont pas s'occuper des messures.
Ainsi on peut attacher une liste de capteurs avec un ou plusieurs poste de contr�le (si utilisation d'un �v�nement sur un bus de communication).

On aurait pu ajouter une batterie � la voiture, mais cela reste du d�tails pour le fonctionnement global, il n'y a donc pas d'obligation sur �a pr�sence. De plus le capteur le voiture, permet de la repr�senter indirectement.

![BlockDefinitionDiagram](./diagrams/PNGs/SysML_1_4_Block_Definition_Diagram.PNG)

## Le diagramme de blocs internes 

![InternalBlockDiagram](./diagrams/PNGs/SysML_1_4_Internal_Block_Diagram.PNG)

## Le diagramme dynamique
![InternalBlockDiagram](./diagrams/PNGs/SysML_1_4_Sequence_Diagram.PNG)