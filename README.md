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


## Résultats Clés (Modèle de Cox)

Le modèle de Cox a permis d'isoler l'impact de chaque variable sur le risque de rupture de contrat :
* **Âge :** Chaque année supplémentaire diminue le risque de résiliation de **2,85 %**.
* **Sexe :** Les hommes présentent un risque inférieur de **38,12 %** par rapport aux femmes (avec une médiane de survie supérieure de près de 4 ans).
* **Profession :** Le statut de cadre réduit le risque de résiliation de **85,93 %** (par rapport à la catégorie de référence des agriculteurs).
* **Propriété :** À âge et profession strictement identiques, le fait d'être propriétaire augmente le risque de résiliation de **28,50 %**.

###  Profils Types Identifiés
* **Profil le plus fidèle :** Un homme âgé, cadre et locataire (non-propriétaire).
* **Profil à fort risque de résiliation rapide :** Une femme jeune, non-cadre et propriétaire.

  
# Technologies Utilisées

* **Langage :** R
