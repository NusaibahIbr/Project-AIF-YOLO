# Instructions

Nous avons choisi l'algorithme YOLOv3 (version 3) car il s'agit de l'un des meilleurs algorithmes de détection d'object. 

**Better** - **Faster** - **Stronger** sont les trois adjectifs qui qualifient cet algorithme.

Nous avons donc trouvé une version du code et essayer de le comprendre. 
Nous n'avons pas entrainé le réseau de neurone sur un jeu de données d'entrainement car on avait déjà accès aux poids d'apprentissage sur le site officiel [YOLO: Real-Time Object Detection](https://pjreddie.com/darknet/yolo/).

Nous n'avons donc pas eu le besoin d'utiliser les outils GPU ou Cloud, car le temps d'exécution sur les données test étaient minimes (moins d'une seconde).

Nous avons rendu notre travail reproductible pour permettre à d'autres utilisateurs de découvrir l'algorithme. 
Pour cela, il suffit de "clone" (ou download) le répertoire et d'éxecuter le fichier [YOLO.ipynb](https://github.com/NusaibahIbr/Project-AIF-YOLO/blob/master/Code/YOLO.ipynb). 


**Détails pour l'exécution du fichier YOLO.ipynb**

Dans le première partie du fichier notebook, vous allez installer OPENCV pour permettre de télécharger les images et les données nécessaires. Vous allez ensuite installer torchvision qui permet d'utiliser Darknet, un réseau de neurones profond et open source écrit par les créateurs de YOLO. Ensuite on importe les packages nécessaires à l'exécution, comme matplotlib.pyplot, cv2, les packages de utils, qui est un module contenant quelques fonctions d'aide.

Dans la deuxième partie on télécharge les poids pré-entrainés avec la ligne de code !wget https://pjreddie.com/media/files/yolov3.weights puis on spécifie la localisation des fichiers qui vont nous être utiles. On a les fichiers contenant l'architecture du réseau de neuronnes (fichier cfg), des poids pré-entrainés (fichier weight) et les classes d'objets (fichier coco.names). 
Ensuite Darknet permet de setup le réseau de neuronne en utilisant l'architecture du fichier cfg et on load les poids pré-entraînés et les classes d'objets avec les commandes load_weights() et load_class_names().

La partie Loading and Resizing Our Images permet de convertir nos images dans les bonnes normes de couleur et de taille. 

Les deux parties suivantes servent à expliquer l'utilité du Non-Max Suppression Threshold et du IoU Treshold, et on fixe des valeurs à ces paramètres. 

C'est dans la dernière partie Object Detection que l'on affiche l'image choisi par l'utilisateur avec les objets que l'algorithme a détecté, associés à une probabilité de bonne classification de l'objet localisé.  

Nous vous invitons à tester cet algorithme sur d'autres images.
*Remarque* : Notre jeu de données d'entrainement étant restreint (80 classes), veuillez tester sur des images contenant des objects figurants dans la liste [coco.names](https://github.com/NusaibahIbr/Project-AIF-YOLO/blob/master/Code/Nom/coco.names) si vous voulez observer des résultats.

**Pour aller plus loin** : vous pouvez modifier notre algorithme pour avoir un algortihe plus riche. Pour cela, lisez l'article [YOLO9000](https://github.com/NusaibahIbr/Project-AIF-YOLO/blob/master/Bibliographie/articleYOLO9000.pdf) qui explique comment entrainer le réseau de neurone de YOLO sur un jeu de données contenant 9000 classes. 
