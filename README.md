# Apprentissage symbolique & non supervisé — 3 notebooks

Trois études menées dans le cadre du cours *Théorie de l'Apprentissage Symbolique* (INFO2). Chacune va au-delà
du sujet de TP : **comparaison argumentée des méthodes, vérification des résultats et choix justifiés**.

| Notebook | Thème | Points forts |
|---|---|---|
| [`TP_XAI_PyXAI/TP_XAI_explicabilite_PyXAI.ipynb`](TP_XAI_PyXAI/TP_XAI_explicabilite_PyXAI.ipynb) | **IA explicable formelle** (PyXAI) sur arbres de décision | raisons directes, suffisantes et minimales, contrastives ; **vérificateur indépendant** ; **dualité hitting sets** vérifiée ; passage à l'échelle sur UCI Adult (le nombre de raisons suffisantes explose jusqu'à 10⁸, alors que les contrastives restent ≤ 111) ; raisons suffisantes utilisées comme règles (71 règles couvrent 99 % des exemples de test) |
| [`TP_Apriori_Regles_Association/TP_Apriori_regles_association.ipynb`](TP_Apriori_Regles_Association/TP_Apriori_regles_association.ipynb) | **Règles d'association** | Apriori **écrit à la main** et validé contre mlxtend ; sensibilité au support et à la confiance ; comparaison des mesures (la confiance seule trompe) ; Apriori, FP-Growth, FP-Max, itemsets fermés ; démonstrations et vérifications ; étude réelle sur 493 étudiants en médecine (choix de spécialité, biais de genre, élagage par *improvement*) |
| [`TP_Clustering_Comparaison/TP_Clustering_comparaison.ipynb`](TP_Clustering_Comparaison/TP_Clustering_comparaison.ipynb) | **Clustering** | 8 algorithmes (K-Means, CAH ×3, GMM, spectral, DBSCAN, HDBSCAN) sur 6 jeux synthétiques, Iris et Wine ; choix de k (silhouette, DB, CH, BIC, dendrogramme) ; effet de la standardisation (ARI de 0,37 à 0,90) ; stabilité par bootstrap ; passage à l'échelle ; tableau de décision |

## Lancer
```bash
pip install -r requirements.txt
jupyter notebook
```
Les notebooks fonctionnent aussi sur **Google Colab** : la première cellule installe les dépendances manquantes. Pour
le notebook Apriori, il faut importer `data/GroceryStoreDataSet.csv` et `data/medspe.tsv` dans le panneau Fichiers (`medspe.tsv` est fourni par le cours et n'est pas publié ici). Le notebook XAI
télécharge lui-même UCI Adult.

**Compétences** : Python, scikit-learn, PyXAI, mlxtend, pandas, matplotlib · logique propositionnelle (impliquants
premiers, hitting sets) · fouille de motifs · apprentissage non supervisé · protocole expérimental, analyse de complexité,
interprétation critique des résultats.
