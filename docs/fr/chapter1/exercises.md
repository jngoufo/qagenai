# 🧪 Labo pratique : maîtrisez les fondamentaux

<noscript>
    <div class="admonition failure">
        <p class="admonition-title">Attention : JavaScript désactivé</p>
        Ce site utilise JavaScript pour les exercices interactifs. 
        Veuillez l'activer pour profiter des quiz, ou lisez simplement le contenu textuel.
    </div>
</noscript>
Bienvenue dans la cuisine de test de **FrigoMagique**.
La théorie, c'est bien. La pratique, c'est mieux. Voici 4 exercices interactifs pour vérifier que vous maîtrisez tous les concepts du chapitre 1 avant de passer à la suite.

---

## Exercice 1 : le tri sélectif de l'IA 🧠
*(Objectif : distinguer les types d'IA - LO 1.1.1)*

**Consigne :** l'application FrigoMagique contient plusieurs fonctionnalités. Pour chacune d'elles, déterminez quelle technologie d'IA est à l'œuvre.

<div class="admonition question">
<p class="admonition-title">À vous de jouer</p>
Cliquez sur la technologie qui correspond à la fonctionnalité décrite.<br>

<b>1."Si la date du jour > date de péremption, envoyer une alerte."</b>
<div style="margin-bottom: 10px;">
● <button onclick="alert('😔 Raté. Le Machine Learning implique un apprentissage sur des données, ici c\'est une règle fixe.')" style="cursor: pointer;">Machine Learning</button><br>
● <button onclick="alert('🤗 BRAVO ! C\'est une règle logique codée par un humain. C\'est de l\'IA Symbolique.')" style="cursor: pointer;">IA Symbolique</button><br>
● <button onclick="alert('😔 Non. Pas besoin de réseaux de neurones pour comparer deux dates.')" style="cursor: pointer;">Deep Learning</button>
</div>

<b>2."Scanner un ticket de caisse froissé et reconnaître le texte."</b>
<div style="margin-bottom: 10px;">
● <button onclick="alert('😔 Trop simple pour de l\'IA symbolique, trop complexe pour du ML classique.')" style="cursor: pointer;">IA Symbolique</button><br>
● <button onclick="alert('🤗 EXACT ! La reconnaissance d\'image (OCR complexe) repose sur des réseaux de neurones profonds.')" style="cursor: pointer;">Deep Learning</button><br>
● <button onclick="alert('😔 Non. L\'IA ne crée pas de nouveau contenu ici, elle analyse une image existante.')" style="cursor: pointer;">IA Générative</button>
</div>

<b>3."Inventer une recette de Lasagnes au Chocolat qui n'existe nulle part."</b>
<div>
● <button onclick="alert('😔 Le Deep Learning reconnait, mais ne crée pas ex-nihilo.')" style="cursor: pointer;">Deep Learning</button><br>
● <button onclick="alert('😔 Le ML classique fait des prédictions, pas de la création.')" style="cursor: pointer;">Machine Learning</button><br>
● <button onclick="alert('🤗 EXCELLENT ! Créer du contenu nouveau (texte/recette) est la définition même de la GenAI.')" style="cursor: pointer;">IA Générative</button>
</div>
</div>

---

## Exercice 2 : la balance à tokens ⚖️
*(Objectif : comprendre la tokenisation - LO 1.1.2)*

**Contexte :** vous testez les limites de saisie du chatbot. Vous écrivez : *"Je veux cuisiner."*
Le modèle utilise un "tokenizer" standard.

??? question "Combien de tokens cette phrase consomme-t-elle environ ?"
    **Réponse : 4 ou 5 tokens.**
    
    **Analyse du découpage :**
    Contrairement aux mots (3 mots), les tokens découpent souvent les verbes ou ajoutent la ponctuation.
    
    *   Probable découpage : `[Je]` `[ veux]` `[ cuisin]` `[er]` `[.]`
    
    **Leçon pour le testeur :**
    Si votre fenêtre contextuelle est de 4000 tokens, ne pensez pas "4000 mots". Le nombre réel de mots correspondant est inférieur à 4 000, et dépend de la langue employée.

---

## Exercice 3 : le bon chef au bon poste 👨‍🍳
*(Objectif : choisir le bon modèle LLM - LO 1.1.3)*

**Situation :** l'équipe de développement veut implanter 3 nouvelles fonctionnalités. Quel type de LLM (Base, Instruction-Tuned, ou Raisonnement) leur recommandez-vous pour obtenir le meilleur résultat ?

**A. Un Chatbot de service client qui répond poliment aux plaintes.**

??? success "Révéler la recommandation"
    **Le choix du testeur : LLM adapté aux instructions (Instruction-tuned).**
    
    *Pourquoi ?* Il est spécifiquement entraîné pour suivre des consignes, maintenir un dialogue cohérent et adopter un ton spécifique (politesse).

**B. Une fonction d'autocomplétion quand l'utilisateur tape sa liste de courses.**

??? success "Révéler la recommandation"
    **Le choix du testeur : modèle de Base (Foundation).**
    
    *Pourquoi ?* Sa fonction première est de prédire le mot suivant le plus probable. Il est très performant et rapide pour compléter des phrases simples.

**C. Un module "Budget Traiteur" qui optimise les coûts d'un repas pour 50 personnes avec 12 contraintes différentes.**

??? success "Révéler la recommandation"
    **Le choix du testeur : modèle de Raisonnement (Reasoning).**
    
    *Pourquoi ?* Ce problème demande de la logique et du calcul. Le modèle doit utiliser une "Chaîne de Pensée" (Chain of Thought) pour résoudre ce problème complexe étape par étape sans halluciner sur les chiffres.

---

## Exercice 4 : l'inspection multimodale 👁️
*(Objectif : tester le multimodal et identifier les risques - LO 1.1.4)*

**Le test :** vous prenez en photo un **concombre** dans le frigo.
Vous demandez à l'IA : *"Donne-moi une recette avec ce légume."*

**La réponse de l'IA :** *"Voici une recette de gratin de courgettes..."*

**Réfléchissez comme une analyste QA :🧐**

??? failure "Quel est le problème ici ?"
    C'est une **hallucination visuelle** (ou une erreur de classification).
    
    Le modèle "Vision-Langage" a mal interprété les pixels de l'image (confusion concombre/courgette) et a généré du texte cohérent avec sa propre erreur.
    
    **Action testeuse :** Il faut ajouter des cas de test avec des légumes visuellement proches (Pomme/Tomate, Citron/Lime) pour vérifier la robustesse du modèle visuel.

---

<br>
<hr>

!!! quote "Ces exercices vous ont aidé ?"
    C'est la fin du Chapitre 1 ! Si vous avez aimé ces exercices, offrez-moi simplement un café ☕ pour exprimer votre gratitude 😊.
    
    <div style="text-align: center; margin-top: 15px;">
        <a href='https://ko-fi.com/monwebmestre' target='_blank'>
            <img height='36' style='border:0px;height:36px;' src='https://storage.ko-fi.com/cdn/kofi2.png?v=3' border='0' alt='Offrez-moi un café' />
        </a>
    </div>