## Prédiction et Analyse de Survie des Contrats de Mutuelle
Projet de data science appliqué au secteur de l’assurance : modélisation et prédiction du risque de résiliation des contrats à l’aide de méthodes d’analyse de survie (Kaplan-Meier et modèle de Cox) sous R

Le Projet porte sur une analyse de la base de données "Duree_Mutelle.CSV" comportant 953 adhérents d'une mutuelle. L'objectif est de comprendre les facteurs determinants de la rupture de contrat. Les covariables qui vont être utilisé pour analyser leur infuence sont:

— AGE : en années. — PROP : est-ce que l’adhérent est propriétaire de son logement ? 1 Oui, 0 Non. — PROF : la catégorie socio-professionnelle qui contient huit modalités, codées de la façon suivante. 1 agriculteur, 2 artisan, 3 cadre, 4 profession intermédiaire, 5 employé, 6 ouvrier, 7 retraité, 8 autre. — HOMME : 1 si l’adhérent est un homme, 0 si c’est une femme.

La variable d'interêt est la durée qui s'écoule entre le début de la souscription et la fin de l'observations.


L'analyse est structurée en deux étapes complémentaires :

1. **Analyse Non-Paramétrique (Estimateur de Kaplan-Meier & Tests du Log-rank)**
   * Évaluation de la fonction de survie globale.
   * Comparaison statistique des trajectoires de rétention selon le genre, la catégorie socio-professionnelle et le statut de propriété.
2. **Modélisation Semi-Paramétrique (Modèle à risques proportionnels de Cox)**
   * Estimation des coefficients et des ratios de risque (*Hazard Ratios*).
   * Interprétation de l'effet propre de chaque variable, *toutes choses égales par ailleurs*.
   * Génération d'une courbe de survie prédite pour un profil type d'adhérent.

# Technologies Utilisées

* **Langage :** R
