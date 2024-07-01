## Données

- 🔵 **Transactions** : Quel client a acheté quel panier contenant quel produit.
- 🟢 **Caractéristiques produits** : Catégories de produits, prix.
- 🟢 **Caractéristiques clients** : Genre, âge, localisation.
- 🟡 **Temporalité des transactions** : Délai entre deux transactions, ordre de constitution du panier.
- 🟡 **Contraintes métier** : Produits à forte valeur ajouter, produits en destockage, poids personnalisés ...
- 🔴 **Feedbacks clients** : Algorithmes adaptatifs en fonction des résultats d'une campagne.

## Méthodes

- 🔵 **User-Based CF** : Basée sur les similarités entre les comportements d'achat des clients.
- 🟢 **Item-Based CF** : Basée sur les similarités entre les comportements d'achet des produits.
- 🟢 **Ticket-Based CF** : Recommandations ciblées sur un panier pour le compléter, basées sur les similarités entre paniers.
- 🟢 **Market Basket Analysis** : Analyse des produits achetés généralement ensemble.
- 🟡 **Factorization Machines** : Modélisation des interactions entre variables en utilisant des vecteurs de facteurs latents.
- 🟡 **Bandit Methods** : Sélection des articles pour maximiser les récompenses cumulées par équilibre exploration-exploitation.
- 🔴 **Sequence-Aware Models** : Modèle qui tiennent compte de l'ordre de constitution des paniers.

## Algorithmes

- ### Matrix Factorization
    - 🔵 **SVD Matrix Factorization** : Factorisation de la matrice d'interactions par décomposition SVD.
    - 🟢 **ALS Matrix Factorization** : Factorisation de la matrice d'interactions par optimisation ALS.
    - 🟡 **NMF Matrix Factorization** : Factorisation de la matrice d'interactions positive pour interpréter les corrélations.
    - 🟡 **PMF Matrix Factorization** : Factorisation probabiliste de la matrice d'interactions.

- ### Deep Learning
    - 🟢 **Neural Collaborative Filtering** : Utilisation de réseaux de neurones pour modéliser les interactions utilisateurs-articles.
    - 🟢 **DeepFM** : Combinaison de la factorisation matricielle et du deep learning pour capturer les interactions non linéaires.
    - 🟡 **Autoencoders** : Réseaux de neurones utilisés pour apprendre une représentation compacte des données d'interactions.
    - 🔴 **Sequence-Aware RNN** : RNN pour complétion de paniers en tenant compte de l'ordre des interactions.
    - 🔴 **Attention** : Complétion de paniers basée sur le mécanisme d'attention pour pondérer l'importance des interactions passées.

- ### Clustering
    - 🟢 **K-Means** : Moyenne des plus proches voisins pour regrouper les utilisateurs ou articles similaires.
    - 🟡 **DBSCAN** : Clustering basé sur la densité pour identifier les clusters denses et isoler le bruit.
    - 🟡 **Hierarchical Clustering** : Clustering hiérarchique pour créer une hiérarchie de clusters imbriqués.

- ### Association Rules
    - 🔵 **Apriori Algorithm** : Algorithme classique pour l'analyse de panier d'achat (Market Basket Analysis).
    - 🟢 **FP-Growth Algorithm** : Algorithme scalable pour découvrir des motifs fréquents sans génération de candidats explicite.
    - 🟡 **Eclat Algorithm** : Algorithme simple et efficace pour trouver des ensembles d'éléments fréquents via l'intersection de listes.

- ### Reinforcement Learning
    - 🟡 **Q-Learning** : Apprentissage par renforcement basé sur une table de Q-valeurs pour maximiser les récompenses cumulées.
    - 🟡 **Deep Q-Learning** : Utilisation de réseaux de neurones pour approximer les Q-valeurs dans des environnements complexes.
    - 🟡 **Policy Gradient** : Optimisation directe des politiques par descente de gradient pour maximiser la récompense attendue.
    - 🔴 **Actor-Critic** : Combinaison de la politique et de la valeur pour améliorer la stabilité et la performance de l'apprentissage.

- ### Bandit Algorithms
    - 🟡 **`ε`-Greedy** : Sélection d'actions équilibrant exploration et exploitation avec une probabilité `ε`.
    - 🔴 **UCB** : Utilisation de la borne supérieure de confiance pour l'équilibre exploration-exploitation.
    - 🔴 **Thompson Sampling** : Stratégie pour sélectionner les actions dans la distribution de probabilité des récompenses.
    - 🔴 **LinUCB** : Extension de UCB utilisant des modèles linéaires pour capturer les dépendances contextuelles.
    - 🔴 **LinThompson** : Version contextuelle de Thompson Sampling utilisant des modèles linéaires pour la sélection d'actions.

### Combinaison de méthodes

- ### Hybrid Methods
    - 🟢 **Weighted Hybrid** : Moyenne pondérée des scores de deux méthodes.
    - 🟡 **Switching Hybrid** : Application d'une méthode parmi plusieurs en fonction de critères.
    - 🟡 **Meta-Level Hybrid** : Entraînement d'une méthode sur les résultats d'une autre méthode.
    - 🔴 **Cascade Hybrid** : Chaque méthode affine les résultats de la précédente.
    - 🔴 **Feature Augmentation Hybrid** : Sorties d'une méthode comme variables pour une autre.

- ### Ensemble Methods
    - 🟡 **Bagging** : Combinaison des prédictions de modèles entraînés sur des sous-échantillons.
    - 🔴 **Boosting** : Chaque modèle corrige les erreurs des précédents.
    - 🔴 **Stacking** : Sorties de plusieurs modèles comme entrée d'un modèle final.

## Evaluation

- 🔵 **Précision@K** : Part des produits tests ayant été placés dans le top K des recommandations.
- 🟡 **Multi-Objective Optimization** : Objectifs personnalisés de précision, diversité ...
- 🟡 **Rule-Based Optimization** : Objectifs de vente particuliers aux besoin du métier.

## Se renseigner

- Bayesian Personalized Ranking
- Bayesian Networks
- Adversarial Learning Methods
- Factorization Machines
- Deep Matrix Factorization
- Sequence-Aware Recommender Systems