# Instructions

Nous avons choisi l'algorithme YOLOv3 (version 3) car il s'agit de l'un des meilleurs algorithmes de détection d'object. 

**Better** - **Faster** - **Stronger** sont les trois adjectifs qui qualifient cet algorithme.

Nous avons donc trouvé une version du code et essayer de le comprendre. 
Nous n'avons pas entrainé le réseau de neurone sur un jeu de données d'entrainement car on avait déjà accès aux poids d'apprentissage sur le site officiel [YOLO: Real-Time Object Detection](https://pjreddie.com/darknet/yolo/).

Nous n'avons donc pas eu le besoin d'utiliser les outils GPU ou Cloud, car le temps d'exécution sur les données test étaient minimes (moins d'une seconde).

Nous avons rendu notre travail reproductible pour permettre à d'autres utilisateurs de découvrir l'algorithme. 
Pour cela, il suffit de "clone" (ou download) le répertoire et d'éxecuter le fichier [YOLO.ipynb](https://github.com/NusaibahIbr/Project-AIF-YOLO/blob/master/Code/YOLO.ipynb). 
Vérifiez bien que vous ayez installé OPENCV, pour permettre de télécharger les images et les données nécessaires.

Nous vous invitons à tester cet algorithme sur d'autres images. 
*Remarque* : Notre jeu de données d'entrainement étant restreint (80 classes), veuillez tester sur des images contenant des objects figurants dans la liste [coco.names](https://github.com/NusaibahIbr/Project-AIF-YOLO/blob/master/Code/Nom/coco.names).

**Pour aller plus loin** : vous pouvez modifier notre algorithme pour avoir un algortihe plus riche. Pour cela, lisez l'article [YOLO9000](https://github.com/NusaibahIbr/Project-AIF-YOLO/blob/master/Bibliographie/articleYOLO9000.pdf) qui explique comment entrainer le réseau de neurone de YOLO sur un jeu de données contenant 9000 classes. 




