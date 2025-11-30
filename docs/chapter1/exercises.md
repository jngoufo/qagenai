# 🧪 Practice lab: master the fundamentals

<noscript>
    <div class="admonition failure">
        <p class="admonition-title">Attention : JavaScript désactivé</p>
        Ce site utilise JavaScript pour les exercices interactifs. 
        Veuillez l'activer pour profiter des quiz, ou lisez simplement le contenu textuel.
    </div>
</noscript>
Welcome to the **MagicFridge** test kitchen.
Theory is good. Practice is better. Here are 4 interactive exercises to verify that you have mastered all Chapter 1 concepts before moving on.

---

## Exercise 1: AI sorting hat 🧠
*(Objective: distinguish AI types - LO 1.1.1)*

**Task:** the MagicFridge application contains several features. For each one, determine which AI technology is at work.

<div class="admonition question">
<p class="admonition-title">Your turn</p>
Click on the technology that matches the described feature.<br>

<b>1. "IF today > expiration date, send an alert."</b>
<div style="margin-bottom: 10px;">
● <button onclick="alert('😔 Missed. Machine Learning implies learning from data, here it is a fixed rule.')" style="cursor: pointer;">Machine Learning</button><br>
● <button onclick="alert('🤗 BRAVO! It is a logical rule coded by a human. This is Symbolic AI.')" style="cursor: pointer;">Symbolic AI</button><br>
● <button onclick="alert('😔 No. No need for neural networks to compare two dates.')" style="cursor: pointer;">Deep Learning</button>
</div>

<b>2. "Scanning a crumpled receipt and recognizing the text."</b>
<div style="margin-bottom: 10px;">
● <button onclick="alert('😔 Too simple for Symbolic AI, too complex for classical ML.')" style="cursor: pointer;">Symbolic AI</button><br>
● <button onclick="alert('🤗 EXACT! Image recognition (complex OCR) relies on deep neural networks.')" style="cursor: pointer;">Deep Learning</button><br>
● <button onclick="alert('😔 No. The AI is not creating new content here, it analyzes an existing image.')" style="cursor: pointer;">Generative AI</button>
</div>

<b>3. "Inventing a recipe for Chocolate Lasagna that exists nowhere else."</b>
<div>
● <button onclick="alert('😔 Deep Learning recognizes, but does not create ex-nihilo.')" style="cursor: pointer;">Deep Learning</button><br>
● <button onclick="alert('😔 Classical ML makes predictions, not creation.')" style="cursor: pointer;">Machine Learning</button><br>
● <button onclick="alert('🤗 CORRECT! Creating new content (text/recipe) is the very definition of GenAI.')" style="cursor: pointer;">Generative AI</button>
</div>
</div>

---

## Exercise 2 : the token scale ⚖️
*(Objective: understand tokenization - LO 1.1.2)*

**Context :** you are testing the chatbot input limits. You type: *"I want to cook."*
The model uses a standard tokenizer.

??? question "How many tokens does this sentence roughly consume?"
    **Answer: 5 to 6 tokens.**
    
    **Breakdown analysis:**
    unlike words (4 words), tokens often split verbs or add punctuation.
    
    *   Probable breakdown: `[I]` `[ want]` `[ to]` `[ cook]` `[.]`
    
    **Tester's lesson:**
    if your context window is 4000 tokens, do not think "4000 words". The actual number of corresponding words is lower than 4,000, and depends on the language used.

---

## Exercise 3 : the right chef for the job 👨‍🍳
*(Objective: select the right LLM model - LO 1.1.3)*

**Situation:** the dev team wants to implement 3 new features. Which LLM type (Base, Instruction-tuned, or Reasoning) do you recommend for the best result?

**A. A customer service chatbot that answers complaints politely.**

??? success "Reveal recommendation"
    **Tester's choice: Instruction-tuned LLM.**
    
    *Why?* It is specifically trained to follow guidelines, maintain a coherent dialogue, and adopt a specific tone (politeness).

**B. An autocomplete feature when the user types their shopping list.**

??? success "Reveal recommendation"
    **Tester's choice: Base model (Foundation).**
    
    *Why?* Its primary function is to predict the next most probable word. It is very performant and fast for completing simple phrases.

**C. A "Catering Budget" module that optimizes costs for 50 people with 12 constraints.**

??? success "Reveal recommendation"
    **Tester's choice: Reasoning model.**
    
    *Why?* This problem requires logic and calculation. The model must use a "Chain of Thought" to solve this complex logical problem step-by-step without hallucinating numbers.

---

## Exercise 4: multimodal inspection 👁️
*(Objective: test multimodal capabilities and identify risks - LO 1.1.4)*

**The test:** you take a picture of a **cucumber** in the fridge.
You ask the AI: *"Give me a recipe with this vegetable."*

**The AI response:** *"Here is a recipe for zucchini gratin..."*

**Think like a QA analyst :🧐**

??? failure "What is the problem here?"
    This is a **visual hallucination** (or a classification error).
    
    The "Vision-Language" model misinterpreted the image pixels (cucumber/zucchini confusion) and generated text consistent with its own mistake.
    
    **Tester action:** you must add test cases with visually similar vegetables (Apple/Tomato, Lemon/Lime) to verify the visual model's robustness.

---

<br>
<hr>

!!! quote "Did these exercises help?"
    This is the end of Chapter 1! If you enjoyed these exercises, simply buy me a coffee ☕ to express your gratitude 😊.
    
    <div style="text-align: center; margin-top: 15px;">
        <a href='https://ko-fi.com/monwebmestre' target='_blank'>
            <img height='36' style='border:0px;height:36px;' src='https://storage.ko-fi.com/cdn/kofi2.png?v=3' border='0' alt='Buy Me a Coffee' />
        </a>
    </div>