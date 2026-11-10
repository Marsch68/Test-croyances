Cartographie des Systèmes de Croyance (Boussole Philosophique & Religieuse)
Un outil d'évaluation interactive qui dépasse la simple question binaire "Êtes-vous croyant ou athée ?" pour positionner avec précision la vision du monde d'un utilisateur parmi les grands courants religieux et philosophiques.

🎯 Le Concept
L'appartenance nominale à une religion masque souvent une grande diversité de convictions réelles (du déisme culturel au théisme dogmatique). Deux personnes se déclarant de la même confession peuvent avoir des lectures du monde diamétralement opposées. Ce projet propose un sondage algorithmique permettant de calculer l'affinité réelle d'une personne avec différentes écoles de pensée historiques (Catholicisme, Calvinisme, Soufisme, Spinozisme, Existentialisme, Bouddhisme, Athéisme matérialiste, etc.) en se basant sur des lignes de fracture épistémologiques, ontologiques et éthiques.

✨ Fonctionnalités Principales
Scoring Multidimensionnel : Les questions n'enferment pas l'utilisateur dans un choix unique. Chaque réponse (sur une échelle d'accord de -2 à +2) distribue des pondérations mathématiques positives ou négatives à plusieurs profils simultanément.

Test d'Orthodoxie (Crash Test) : Le sondage débute par une auto-identification ("Je me considère comme..."), déclenchant des questions ciblées sur les dogmes non-négociables de ce courant pour mesurer l'écart entre l'étiquette sociologique revendiquée et la croyance réelle.

Détecteur de Dissonance Cognitive : Le moteur croise les réponses pour identifier les paradoxes dans le système de pensée de l'utilisateur (ex: affirmer que l'univers obéit à la stricte nécessité tout en revendiquant un libre-arbitre absolu, ou rejeter la transsubstantiation tout en défendant le magistère dogmatique).

🛠 Architecture Technique
Le projet est conçu comme une application web front-end légère (SPA - Single Page Application), séparant strictement la logique d'interface des données de configuration, ce qui permet un hébergement simple (ex: GitHub Pages).

Interface : HTML5 / CSS3 (UI épurée, affichage séquentiel, barres de progression).

Moteur Logique : Vanilla JavaScript. Gère le cycle de vie du sondage, calcule les scores relatifs (points obtenus par rapport au maximum théorique de chaque profil) et exécute les règles dynamiques de contradiction.

Modèle de Données : Fichier JSON externe. Les questions, les profils, les pondérations et les règles d'exclusion mutuelle sont modélisés en JSON, permettant d'enrichir ou de corriger le questionnaire sans altérer le code source.

📦 Structure des Données (Exemple JSON)
Le cœur de l'algorithme repose sur une distribution fine des affinités :

JSON
{
  "id": "q_spinoza",
  "texte": "Dieu n'est pas une personne, c'est l'ordre absolu et géométrique de la Nature.",
  "scores": {
    "Spinozisme": 5,
    "Déisme": 2,
    "Catholicisme": -5,
    "Salafisme": -5
  }
}
