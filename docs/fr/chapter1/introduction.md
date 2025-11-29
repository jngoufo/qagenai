# Introduction au Chapitre 1

Bienvenue dans ce premier chapitre de votre préparation à la certification **ISTQB CT-GenAI**.

Ce premier chapitre pose les fondations théoriques indispensables. Avant d'apprendre à "prompter" ou à tester avec une IA, il est crucial de comprendre ce qui se passe sous le capot. Nous allons définir précisément ce qu'est l'IA générative par rapport aux formes d'IA précédentes, et détailler la mécanique interne des grands modèles de langage (LLM).

## 🗺️ Le programme du chapitre

Nous allons structurer cette première partie en quatre points clés :

1.  **Le Spectre de l'IA :** Où se situe l'IA générative par rapport au Machine Learning classique ? (Section 1.1.1)
2.  **Fonctionnement des LLM :** Comprendre la tokenisation et les fenêtres contextuelles. (Section 1.1.2)
3.  **Catégories de modèles :** Distinguer les modèles de base, d'instruction et de raisonnement. (Section 1.1.3)
4.  **Multimodalité :** La capacité de l'IA à "voir" et "entendre". (Section 1.1.4)

---

## 🥑 Présentation du Fil rouge : "FrigoMagique"

Avant de plonger complètement dans ce chapitre, laissez-moi vous présenter le compagnon de route qui va nous suivre tout au long de cette formation.

Pour rendre les concepts abstraits de l'IA générative concrets, nous allons nous immerger dans les coulisses d'une entreprise fictive, mais très réaliste : **FrigoMagique**.

!!! example "Qui est FrigoMagique ?"
    **FrigoMagique** est une start-up innovante de la FoodTech. Son application mobile promet de révolutionner le quotidien de ses utilisateurs en gérant leurs courses et leurs repas.
    
    Ce n'est pas une simple liste de courses numérique ; c'est une application qui intègre une intelligence artificielle générative nommée **GUS** (**G**uide **U**niversel des **S**aveurs).
    
    **GUS** est capable de :
    
    *   Scanner les produits (Vision).
    *   Inventer des recettes personnalisées (Génération de texte).
    *   Interagir avec les utilisateurs via un Chatbot.
    
    C'est à travers les défis de test de cette application que nous illustrerons chaque point du syllabus.

Ces présentations faites, entrons maintenant dans le vif du sujet.

<br>
<hr>

!!! quote "Ce cours vous est utile ?"
    Ce contenu est **100% gratuit**. Si cette introduction vous donne envie de lire la suite :
    
    <div style="text-align: center; margin-top: 15px;">
        <a href='https://ko-fi.com/monwebmestre' target='_blank'>
            <img height='36' style='border:0px;height:36px;' src='https://storage.ko-fi.com/cdn/kofi2.png?v=3' border='0' alt='Buy Me a Coffee at ko-fi.com' />
        </a>
        <br>
        <em>C'est 0% de frais pour moi, et 100% d'énergie pour la suite ! ☕</em>
    </div>