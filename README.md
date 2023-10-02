
# Apprentissage actif profond pour la segmentation d'images

Ce travail d’étude et de recherche traite le sujet de l’apprentissage actif profond pour la segmentation d’image, L’apprentissage actif est une méthode de l'apprentissage automatique qui vise à améliorer les performances du modèle en sélectionnant de manière proactive les données les plus utiles. Dans le contexte de la segmentation d'image, l'apprentissage actif permet de cibler les images les plus complexes à segmenter, afin de guider l'annotation manuelle et d'optimiser ainsi la qualité de la segmentation obtenue.

Dans le cadre de ce projet, nous nous sommes inspirés de la méthode proposée par (Di Scandalea, 2019). Cette méthode se base sur l’utilisation d’un premier ensemble de données étiquetées pour former un réseau neuronal entièrement convolutif. Ensuite, un ensemble d'images non étiquetées est introduit dans le réseau formé et une mesure de l'incertitude est calculée pour chaque échantillon non étiqueté.

Le réseau neuronal utilisé ici est basé sur l'architecture **U-Net**. Ce réseau est composé de deux blocs, un **encodeur** et un **décodeur**.

Nous avons utilisé une base de données d'images de feuilles de plantes malades pour entraîner notre modèle. Cette base de données est composée de 503 images au format jpg et de 503 masques correspondants en format png, représentant la vérité terrain pour chaque image. Nous avons redimensionné toutes les images et masques à la même taille de 256*256 pour une uniformité de traitement. Lors de l'entraînement initial, nous avons sélectionné 150 images avec leurs masques pour le modèle, 50 images pour la validation, 25 images pour les tests et 278 images pour l'ensemble non étiqueté.
Les annotations de vérité terrain ont été créées manuellement en utilisant un outil d'annotation graphique d'images : **Labelme**.

## 1. Prérequis
Ce projet nécessite les packages suivants pour fonctionner :
* [Python 3](https://www.python.org/)
* [Pandas](https://pandas.pydata.org/)
* [NumPy](https://numpy.org/)
* [MatPlotLib](https://matplotlib.org/)
* [Sklearn](https://scikit-learn.org/stable/)
* [Opencv](https://opencv.org/)
* [Keras](https://keras.io/)
* [SciPy](https://scipy.org/)

## 2. Fichiers
Ce projet est composé des fichiers suivants:
* **Deep_Active_Learning_simulation_framework_for_Image_Segmentation.ipynb ->** Fichier principal qui contient le code adapté à notre base de données.
* Le dossier **Dataset ->** contient deux fichier npy de l'ensemble d'images et masques de notre base de données que vous pouvez directement utiliser, sinon testez et réadappter avec votre ensemble de données.

## 3. Execution du projet
1. Pour mettre en marche ce projet, importez et executez le fichier **Deep_Active_Learning_simulation_framework_for_Image_Segmentation.ipynb** dans Google Colab. Cela vous permettra de l'exécuter en utilisant le processeur graphique de colab, réduisant ainsi les temps d'apprentissage. 

## 4. Résultats 
![Resultat](https://github.com/YoucefAnis/Apprentissage-actif-profond-pour-la-segmentation-images/blob/main/R%C3%A9sultats/R%C3%A9sultat%201.png "Test 1")

## 5. Références
* Di Scandalea Melanie Lubrano and Perone, Christian S and Boudreau, Mathieu and CohenAdad, Julien Deep active learning for axon-myelin segmentation on histology data [Livre]. - [s.l.] : arXiv preprint arXiv:1907.05143, 2019.

* https://github.com/neuropoly/deep-active-learning/tree/master

* Ren Pengzhen and Xiao, Yun and Chang, Xiaojun and Huang, Po-Yao and Li, Zhihui and Gupta,Brij B and Chen, Xiaojiang and Wang, Xin A survey of deep active learning [Livre]. - [s.l.] : ACM New York, NY, 2021.

* Ronneberger Olaf and Fischer, Philipp and Brox, Thomas U-net: Convolutional networks for biomedical image segmentation [Livre]. - [s.l.] : Springer, 2015.


