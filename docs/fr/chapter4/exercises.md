# 🧪 Labo Pratique : Architecte de la Qualité

Bienvenue dans le bureau d'architecture de **FrigoMagique**.
Ici, on ne joue plus avec le chat. On construit l'usine. Votre mission est de choisir les bonnes briques technologiques pour résoudre des problèmes d'échelle industrielle.

---

## Exercice 1 : le dilemme RAG vs Fine-tuning 🏗️
*(Objectif : choisir la bonne stratégie d'adaptation - LO 4.1.2 vs 4.2.1)*

**Situation :** l'équipe marketing lance une campagne "Noël 2026" avec des règles de réduction très complexes qui changent tous les jours. GUS (l'IA) hallucine complètement sur ces règles.

**La Cheffe de Projet vous demande :** *"Est-ce qu'on doit ré-entraîner le modèle (Fine-tuning) pour qu'il apprenne ces règles ?"*

!!! question Votre recommandation technique

    **Quelle est la meilleure approche ?**

    <div style="margin-bottom: 15px;">
    ● <button onclick="alert('😔 Mauvaise idée. Le Fine-Tuning est lent et coûteux. Si les règles changent tous les jours, votre modèle sera toujours obsolète.')" style="cursor: pointer;">Oui, lançons un Fine-Tuning chaque nuit.</button><br>
    ● <button onclick="alert('🥳 EXACT ! Le RAG permet de connecter l\'IA à la documentation en temps réel. Si on met à jour le PDF des règles, GUS est à jour à la seconde près.')" style="cursor: pointer;">Non, utilisons le RAG (Retrieval-Augmented Generation).</button>
    </div>

---

## Exercice 2 : l'agent secret 🕵️
*(Objectif : identifier un agent autonome - LO 4.1.3)*

**Observation :** vous observez deux comportements différents de GUS dans les logs. Lequel correspond à la définition d'un **Agent Autonome** ?

!!! question "À vous de juger"

    **Cas A :** l'utilisateur demande "Supprime mon compte". GUS répond : "Pour supprimer votre compte, allez dans Paramètres > Profil."
    
    **Cas B :** l'utilisateur demande "Supprime mon compte". GUS se connecte à l'API Admin, vérifie le solde, exécute la commande SQL `DELETE`, et envoie un email de confirmation.

    Dans lequel de ces cas, GUS est un agent ?

    <div style="margin-bottom: 15px;">
    ● <button onclick="alert('😔 Non. Ici, GUS ne fait que générer du texte (une instruction). Il n\'agit pas sur le système.')" style="cursor: pointer;">Le Cas A</button><br>
    ● <button onclick="alert('🥳 BRAVO ! Ici, GUS utilise des outils (API, SQL, Email) pour exécuter une action réelle sur le monde. C\'est la définition d\'un Agent.')" style="cursor: pointer;">Le Cas B</button>
    </div>

---

## Exercice 3 : au cœur de la base de données 🛢️
*(Objectif : comprendre les composants architecturaux - LO 4.1.1)*

**Contexte :** pour faire fonctionner le RAG, FrigoMagique doit stocker ses milliers de recettes d'une manière que l'IA puisse "comprendre" sémantiquement (par exemple, savoir que "Tomate" est proche de "Sauce Rouge").

**Question :** quel type de base de données l'architecte doit-il installer ?

1.  Une base de données Relationnelle (SQL)
2.  Une base de données Vectorielle (Vector DB)
3.  Un fichier Excel partagé

??? success "Voir la réponse"
    **Réponse : 2. Une base de données Vectorielle.**
    
    Elle permet de stocker les **Embeddings** (les vecteurs numériques) des documents. C'est ce qui permet au système de faire une recherche par sens ("trouve-moi un truc qui ressemble à une tomate") plutôt que par mot-clé exact.

---

## Exercice 4 : crise en production (LLMOps) 🚨
*(Objectif : gérer le cycle de vie opérationnel - LO 4.2.2)*

**Alerte :** depuis la mise à jour du modèle ce matin, le coût de l'API a été multiplié par 10, et GUS répond en allemand une fois sur deux.

**Quelle pratique LLMOps a failli ?**

1.  Le Fine-Tuning
2.  Le Monitoring
3.  L'Orchestration

??? failure "Voir la réponse"
    **Réponse : 2. Le Monitoring.**
    
    Une bonne stratégie LLMOps inclut des alertes automatiques sur :
    
    *   **Le Coût** (pour détecter les pics anormaux).
    *   **La Qualité/Dérive** (pour détecter que l'IA change de langue sans raison).
    
    *Action corrective :* Rollback immédiat à la version précédente du modèle.

---

<br>
<hr>

!!! quote "Vous avez validé l'architecture ?"
    Si ces exercices vous ont aidé à comprendre les rouages, un petit café pour le coach serait grandement apprécié ! ☕
    
    <div style="text-align: center; margin-top: 15px;">
        <a href='https://ko-fi.com/monwebmestre' target='_blank'>
            <img height='36' style='border:0px;height:36px;' src='https://storage.ko-fi.com/cdn/kofi2.png?v=3' border='0' alt='Offrez-moi un café' />
        </a>
    </div>