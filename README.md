Groupe Model : GLORIES Ancelin  CESCHIN Quentin


# RequirementEngineeringExperimentations

Dans ce read me vous trouverez les diff�rents diagrammes mod�lisant les exigences de ce projet.


## Le diagramme des cas d'utilisations

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

###  Voiture
Voici comment la voiture est compos�, un capteur se charge d'�valuer le niveau de la batterie et de transmettre l'information via un port sortant.
La batterie va �tre charg� via une prise secteur en passant par le port d'entr�e.

![InternalBlockDiagram](./diagrams/PNGs/SysML_1_4_Internal_Block_Diagram.PNG)

### Poste de Contr�le
Il s'agit du poste de contr�le qui va centraliser l'analyse et la manipulation des donn�es issues de chaque capteur. Ains via un port entrant, il va �couter les capteurs afin de pouvoir faire ses calculs.
Une fois les calculs finis les r�sultats seront soit redirig�s vers une interface graphique, soit vers un port de sortie s'il s'agit d'une d�cision sur une action � mener.(exemple : lancer le chargement de la voiture).	  

![InternalBlockDiagram](./diagrams/PNGs/SysML1_4InternalBlockDiagram_PC.PNG)

## Le diagramme dynamique : Diagrame Machine � �tat

Nous allons supposer que la voiture met 1h � charger (il faudrait les specs de la voitures pour utiliser le bon temps)

Lors qu'il sera 16h30 - 1h soit 15h30 (ainsi on est sur d'avoir le temps de recharger totalement ou partiellement la batterie) , nous interrogeons le capteur de charge de la voiture afin de d�terminer s'il faut recharger la voiture.
* Si oui, on lance alors la charge pour une petite p�riode puis on reboucle sur l'�valuation du capteur.
* Si non, la voiture est pr�te, le capteur va notifier l'unit� centrale afin d'indiquer que la voiture est charg�e.


![StateMachineDiagram](./diagrams/PNGs/NewSysML1_4StateMachineDiagram.PNG)