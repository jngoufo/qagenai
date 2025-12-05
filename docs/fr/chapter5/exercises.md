# 🧪 Labo Pratique : stratège de l'IA

Bienvenue dans la salle de réunion de la direction de **FrigoMagique**.
Ici, on ne parle plus de code, mais de gouvernance, de budget et d'humain. Votre mission est de déployer l'IA sans mettre l'entreprise en danger.

---

## Exercice 1 : la traque de l'IA fantôme 👻
*(Objectif : identifier les risques du Shadow AI - LO 5.1.1)*

**Situation :** lors d'un audit, vous découvrez qu'un développeur junior a copié l'intégralité du code source du module "Paiement Bancaire" de FrigoMagique dans *ChatGenius* (un outil d'IA public et gratuit) pour lui demander de l'optimiser.

!!! question "Quel est le risque immédiat majeur ?"

    **Votre diagnostic**

    <div style="margin-bottom: 15px;">
    ● <button onclick="alert('😔 Non. Le code peut être optimisé correctement, ce n\'est pas le souci principal ici.')" style="cursor: pointer;">Risque de qualité (Code non fonctionnel)</button><br>
    ● <button onclick="alert('🥳 EXACT ! En envoyant du code propriétaire sur un serveur public, il a potentiellement cédé la propriété intellectuelle (PI) et exposé des failles de sécurité critiques.')" style="cursor: pointer;">Risque de fuite de propriété intellectuelle</button><br>
    ● <button onclick="alert('😔 C\'est un risque, mais moins grave que la perte du code source critique.')" style="cursor: pointer;">Risque de coût (Tokens)</button>
    </div>

---

## Exercice 2 : choisir la bonne arme (LLM vs SLM) ⚔️
*(Objectif : sélectionner le modèle approprié - LO 5.1.3)*

**Projet :** FrigoMagique veut lancer une fonctionnalité **"Assistant Offline"** : l'utilisateur doit pouvoir demander une recette en langage naturel même au fond d'un supermarché sans connexion internet (l'IA tourne directement sur le téléphone).

**Quel type de modèle choisissez-vous ?**

!!! question "Le choix de l'architecte"

    <div style="margin-bottom: 15px;">
    <button onclick="alert('😔 Impossible. Un LLM est trop gros pour tenir sur un téléphone et nécessite une connexion internet pour l\'API.')" style="cursor: pointer;">Option A : un **Grand Modèle de Langage (LLM)** comme Claude 4.</button><br>
    <button onclick="alert('🥳 BRAVO ! Un SLM est compact, consomme peu de batterie et peut tourner en local (Edge AI), ce qui est parfait pour le mode hors-ligne.')" style="cursor: pointer;">Option B : un **Petit Modèle de Langage (SLM)** optimisé</button>
    </div>

---

## Exercice 3 : l'évolution du métier 💼
*(Objectif : comprendre les nouvelles compétences - LO 5.2.1)*

**Contexte :** vous rédigez la fiche de poste pour recruter une nouvelle "Testeuse QA GenAI".
Parmi ces trois compétences, laquelle est **spécifique** à ce nouveau rôle (et non au test classique) ?

1.  Savoir rédiger des cas de test en Gherkin.
2.  Savoir évaluer la température et la fenêtre de contexte d'un modèle.
3.  Savoir utiliser Jira pour le suivi des bugs.

??? success "Voir la réponse"
    **Réponse : 2. Savoir évaluer la température et la fenêtre de contexte.**
    
    *   **Pourquoi ?** C'est une compétence technique purement liée au fonctionnement des LLM.
    *   Les compétences 1 et 3 sont des compétences de test logiciel classiques (et toujours nécessaires !), mais pas spécifiques à la GenAI.

---

## Exercice 4 : le dilemme du déploiement 🚀
*(Objectif : gérer le changement et les risques - LO 5.1.4)*

**Situation :** la direction est impatiente. Le CEO veut déployer GUS partout, tout de suite, pour remplacer le service client dès lundi prochain.
L'équipe QA n'a fait que quelques tests exploratoires prometteurs (Phase de Découverte).

**Quelle est votre recommandation de Test Manager ?**

1.  "Allons-y ! L'IA apprendra sur le tas avec les vrais clients."
2.  "Stop. Il faut passer par la phase d'Initiation et Définition de l'usage avant de généraliser."

??? failure "Voir la recommandation"
    **Réponse : 2. Stop.**
    
    Sauter les étapes est la recette d'un désastre (hallucinations massives, colère des clients).
    Il faut d'abord :

    1.  Sélectionner un cas d'usage pilote.
    2.  Mettre en place des garde-fous (RAG, filtres).
    3.  Mesurer la qualité avant d'ouvrir les vannes.

---

<br>
<hr>

!!! quote "Formation Terminée !"
    🎉 **Félicitations !** Vous avez parcouru l'intégralité du programme.
    
    Si ce cours gratuit vous a aidé à vous sentir prêt pour votre examen de certification, pensez au guide :
    
    <div style="text-align: center; margin-top: 15px;">
        <a href='https://ko-fi.com/monwebmestre' target='_blank'>
            <img height='36' style='border:0px;height:36px;' src='https://storage.ko-fi.com/cdn/kofi2.png?v=3' border='0' alt='Offrez-moi un dernier café' />
        </a>
    </div>