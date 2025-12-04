# 🧪 Labo Pratique : Devenez un Prompt Engineer

Bienvenue dans la salle des commandes de **FrigoMagique**.
Vous avez appris la théorie, maintenant il faut l'appliquer. Ces exercices vous mettent dans la peau d'un ingénieur qualité face à GUS (notre IA).

---

## Exercice 1 : l'anatomie d'un prompt 🦴
*(Objectif : structurer un prompt efficace - LO 2.1.1)*

**Situation :** un testeur junior vous envoie ce prompt qu'il a utilisé pour tester la fonction "Ajout au panier" :
> *"Teste si ça marche quand j'ajoute des pommes."*

**Votre mission :** ce prompt est médiocre. Identifiez 3 composants critiques qui manquent le plus cruellement pour en faire un prompt professionnel.🧐

!!! question "Analyse critique" 
    Sélectionnez les éléments manquants (mentalement), puis révélez l'analyse pour comparer.

    ??? success "Révéler l'analyse du Senior QA"
        Ce prompt est inexploitable par l'IA car il manque :
        
        1.  **Le rôle (persona) :** L'IA ne sait pas si elle doit agir comme un utilisateur final ou un testeur technique.
        2.  **Le contexte :** "Si ça marche" est trop vague. Parle-t-on de performance ? De fonctionnel ? De sécurité ?
        3.  **Le format de sortie :** L'IA va probablement répondre par une phrase banale. On veut un format structuré (Gherkin ou tableau).
        
        **Version corrigée :**
        *"Agis comme un testeur QA (rôle). Pour la fonction 'Panier' (contexte), génère 3 cas de test négatifs pour l'ajout de produits (instruction). Présente le résultat sous forme de tableau (format)."*

---

## Exercice 2 : quelle technique pour quelle tâche ? 🛠️
*(Objectif : choisir la bonne technique de prompting - LO 2.2.5)*

**Consigne :** pour chaque situation rencontrée chez FrigoMagique, déterminez, en cliquant sur la bonne réponse, la technique la plus adaptée.

!!! question "À vous de jouer"

    **1. Vous voulez que l'IA génère 50 cas de test au format Gherkin strict, sans erreur de syntaxe.**
    <div style="margin-bottom: 15px;">
    ● <button onclick="alert('😔 Non. Le Prompt Chaining est utile pour le raisonnement complexe, pas pour forcer un format répétitif.')" style="cursor: pointer;">Prompt Chaining</button><br>
    ● <button onclick="alert('🥳 EXACT ! En donnant 2 ou 3 exemples de Gherkin parfaits (shots), l\'IA va calquer sa structure dessus. C\'est la méthode reine pour le formatage.')" style="cursor: pointer;">Few-Shot Prompting</button><br>
    ● <button onclick="alert('😔 Risqué. Sans exemple, l\'IA risque d\'inventer sa propre syntaxe.')" style="cursor: pointer;">Zero-Shot Prompting</button>
    </div>

    **2. Vous voulez que l'IA analyse une User Story complexe, identifie les règles métier, puis dérive les tests.**
    <div style="margin-bottom: 15px;">
    ● <button onclick="alert('🥳 BRAVO ! On découpe : 1. Analyse, 2. Extraction règles, 3. Génération tests. Cela évite que l\'IA ne s\'embrouille.')" style="cursor: pointer;">Prompt Chaining</button><br>
    ● <button onclick="alert('😔 Pas adapté. Les exemples ne suffisent pas ici, il faut un raisonnement logique étape par étape.')" style="cursor: pointer;">Few-Shot Prompting</button><br>
    ● <button onclick="alert('😔 Non. Le Meta-Prompting sert à créer des prompts, pas à exécuter une analyse complexe directement.')" style="cursor: pointer;">Meta-Prompting</button>
    </div>

    **3. Vous devez tester la sécurité de l'API mais vous êtes bloqué et ne savez pas quoi demander à l'IA.**
    <div>
    ● <button onclick="alert('😔 Ce n\'est pas la meilleure option si vous ne savez même pas par où commencer.')" style="cursor: pointer;">Few-Shot Prompting</button><br>
    ● <button onclick="alert('🥳 GAGNÉ ! Demandez à l\'IA : \'Agis comme un expert en sécurité. Quels sont les meilleurs prompts pour tester une API REST ?\'. Elle fera le travail pour vous.')" style="cursor: pointer;">Meta-Prompting</button>
    </div>

---

## Exercice 3 : système ou utilisateur ? 🤖
*(Objectif : distinguer les types de prompts - LO 2.1.3)*

**Contexte :** vous configurez l'outil de test automatisé de FrigoMagique via son API. Vous avez deux zones de texte à remplir.

*   **Zone A :** "Tu es un assistant QA sarcastique qui répond toujours en rimes."
*   **Zone B :** "Génère un test pour le bouton 'Connexion'."

??? question "Laquelle est le System Prompt ?"
    **C'est la Zone A.**
    
    *   **Pourquoi ?** Elle définit le *comportement* et la *personnalité* immuable de l'IA.
    *   **La Zone B** est le **User Prompt** : c'est l'instruction spécifique à l'instant T.

---

## Exercice 4 : l'évaluation impitoyable 📉
*(Objectif : utiliser les métriques d'évaluation - LO 2.3.1)*

**Le test :** vous avez demandé à GUS de générer des scripts SQL pour insérer des utilisateurs de test dans la base de données.
Vous demandez 10 utilisateurs.

**Le résultat :** GUS génère bien 10 requêtes SQL (`INSERT INTO...`).
Cependant, en les exécutant, 4 requêtes échouent car les adresses email générées n'ont pas de `@` (contrainte de base de données non respectée).

**Quelle métrique est impactée ?**

1.  La diversité
2.  L'exactitude (accuracy) / taux de succès
3.  Le rappel

??? failure "Voir la réponse"
    **Réponse : 2. L'exactitude (et le taux de succès).**
    
    L'IA a produit du code syntaxiquement correct en apparence, mais fonctionnellement faux dans 40% des cas.
    
    *   **Action corrective :** utiliser le **Few-Shot Prompting** en donnant un exemple d'email valide, ou ajouter une **Contrainte** explicite : *"Les emails doivent respecter le format regex `*@*.*`"*.

---

<br>
<hr>

!!! quote "Vous avez validé ce chapitre ?"
    Si ces exercices vous ont aidé à y voir plus clair, un petit café pour le coach serait grandement apprécié ! 🤗
    
    <div style="text-align: center; margin-top: 15px;">
        <a href='https://ko-fi.com/monwebmestre' target='_blank'>
            <img height='36' style='border:0px;height:36px;' src='https://storage.ko-fi.com/cdn/kofi2.png?v=3' border='0' alt='Offrez-moi un café' />
        </a>
    </div>