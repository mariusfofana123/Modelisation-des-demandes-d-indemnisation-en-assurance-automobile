# 🚗 Car Insurance Claim Prediction

## 🎯 Objectif du Projet
Ce projet vise à assister l'assureur *On the Road* dans l'optimisation de ses tarifs en identifiant la variable prédictive la plus performante pour estimer la probabilité qu'un client effectue une demande d'indemnisation pendant sa période de couverture.

## 🛠️ Technologies & Bibliothèques
* **Python 3.x**
* **Pandas & NumPy** : Exploration, nettoyage des données et manipulation de tableaux
* **Statsmodels (`logit`)** : Modélisation statistique par régression logistique pour l'évaluation des caractéristiques
* **Scikit-Learn** : Calcul des métriques d'évaluation (`accuracy_score`)

## 📊 Données Utilisées
Le jeu de données `car_insurance.csv` contient les profils clients et historiques d'assurance :
* **Informations démographiques :** `age`, `gender`, `education`, `income`, `credit_score`, `married`, `children`.
* **Historique de conduite & véhicule :** `driving_experience`, `vehicle_ownership`, `vehicle_year`, `annual_mileage`, `vehicle_type`.
* **Infractions & Accidents :** `speeding_violations`, `duis`, `past_accidents`.
* **Variable Cible (`outcome`) :** Indique si une demande d'indemnisation a été effectuée (`1`) ou non (`0`).

## 🔬 Méthodologie
1. **Exploration & Préparation :** Imputation des valeurs manquantes (`credit_score`, `annual_mileage`) et encodage des variables.
2. **Évaluation Feature par Feature :** Entraînement d'un modèle de régression logistique indépendant (`logit`) pour chaque caractéristique du jeu de données.
3. **Sélection du Modèle :** Identification de la variable unique fournissant l'exactitude (*accuracy*) la plus élevée pour une mise en production simple et efficace.

## 🚀 Comment exécuter le projet

**1. Cloner le dépôt :**
```bash
git clone https://github.com/mariusfofana123/Modelisation-des-demandes-d-indemnisation-en-assurance-automobile.git
cd Modelisation-des-demandes-d-indemnisation-en-assurance-automobile

2. Créer et activer un environnement virtuel :
'''bash
python3 -m venv venv
source venv/bin/activate

3. Installer les dépendances :
'''bash
pip install -r requirements.txt

4. Lancer le notebook :
'''bash
jupyter notebook Notebooks/analyse.ipynb
jupyter notebook Notebooks/analyse2.ipynb
