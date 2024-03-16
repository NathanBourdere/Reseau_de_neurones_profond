# README - Projet de Création d'un Réseau de Neurones Affines en Python

Ce projet consiste à développer un réseau de neurones affines en utilisant exclusivement Python, notamment la bibliothèque NumPy pour les calculs matriciels. Le but est de comprendre les principes fondamentaux du fonctionnement des réseaux de neurones et d'implémenter un modèle simple capable de résoudre des problèmes de classification.

## Installation

Avant de pouvoir lancer ce code, il faut installer les dépendances du projet, pour cela ouvrez un nouveau terminal dans le dossier courant et écrivez : 
```bash
pip install -r requirements.txt
```

## Fonctionnalités du Code :

Initialisation des Paramètres : La fonction init(dimensions) initialise les poids et les biais du réseau de neurones en fonction des dimensions spécifiées pour chaque couche.

Propagation Avant (Forward Propagation) : La fonction forward_propagation(X, parametres) calcule les activations des différentes couches du réseau de neurones en utilisant la fonction d'activation sigmoïde.

Rétropropagation (Back propagation) : La fonction backpropagation(X, y, activations, parametres) calcule les gradients des poids et des biais en utilisant la méthode de rétropropagation du gradient.

Mise à Jour des Paramètres : La fonction update(gradients, parametres, learning_rate) met à jour les poids et les biais du réseau en utilisant le gradient descendante avec un taux d'apprentissage spécifié.

Prédiction : La fonction predict(X, parametres) prédit les classes des exemples en fonction des activations de la dernière couche du réseau.

Entraînement du Réseau de Neurones : La fonction deep_neural_network(X, y, hidden_layers, learning_rate, epoches) effectue l'entraînement complet du réseau de neurones en utilisant les données d'entrée X et les étiquettes y. Elle retourne les paramètres entraînés du réseau.

## Formules Mathématiques :

Forward Propagation : 

$$ Z^{[c]} = W^{[c]}A^{[c-1]} + b^{[c]} $ A^{[c]} = \sigma(Z^{[c]}) $$

Back Propagation : 

$$ dZ^{[c]} = A^{[c]} - y $ dW^{[c]} = \frac{1}{m} dZ^{[c]} A^{[c-1]T} db^{[c]} = \frac{1}{m} \sum dZ^{[c]} $$

Log Loss : 

$$ J(y, \hat{y}) = - \frac{1}{m} \sum_{i=1}^{m} \left( y_i \log(\hat{y}_i) + (1 - y_i) \log(1 - \hat{y}_i) \right) $$

## Utilisation :

Le code fourni peut être exécuté tel quel pour entraîner et tester le réseau de neurones sur un jeu de données synthétique qui peut être généré à l'aide de bibliothèques comme scikit-learn ou alors un jeu de "vraies" données. Il est possible de modifier les paramètres du réseau, tels que le nombre de couches cachées, le taux d'apprentissage et le nombre d'itérations d'entraînement, pour voir comment cela affecte les performances du modèle.

## Exemple d'Exécution :

Après avoir exécuté le code, le réseau de neurones est entraîné ici sur les données générées par make_circles de scikit-learn, et les graphiques de la perte d'entraînement et de l'exactitude de l'entraînement sont affichés par le biais de la bibliothèque matplotlib. Les paramètres entraînés du réseau sont également affichés en sortie.

Note : Ce code a été développé dans le cadre d'un projet personnel.
