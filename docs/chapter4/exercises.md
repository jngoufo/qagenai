# 🧪 Practice lab: Quality Architect

Welcome to the architecture office of **MagicFridge**.
Here, we are no longer playing with the chat. We are building the factory. Your mission is to choose the right technological building blocks to solve industrial-scale problems.

---

## Exercise 1: the RAG vs Fine-tuning dilemma 🏗️
*(Objective: choose the right adaptation strategy - LO 4.1.2 vs 4.2.1)*

**Situation:** The marketing team is launching a "Christmas 2026" campaign with very complex discount rules that change every day. GUS (the AI) is completely hallucinating on these rules.

**The Project Manager asks you:** *"Should we retrain the model (Fine-tuning) so it learns these rules?"*

!!! question "Your technical recommendation"

    **What is the best approach?**

    <div style="margin-bottom: 15px;">
    ● <button onclick="alert('😔 Bad idea. Fine-tuning is slow and expensive. If rules change every day, your model will always be obsolete.')" style="cursor: pointer;">Yes, let's launch a Fine-tuning every night.</button><br>
    ● <button onclick="alert('🥳 EXACT! RAG allows connecting the AI to documentation in real-time. If we update the rules PDF, GUS is up to date to the second.')" style="cursor: pointer;">No, let's use RAG (Retrieval-Augmented Generation).</button>
    </div>

---

## Exercise 2: the secret agent 🕵️
*(Objective: identify an autonomous agent - LO 4.1.3)*

**Observation:** You observe two different behaviors of GUS in the logs. Which one corresponds to the definition of an **Autonomous Agent**?

!!! question "You be the judge"

    **Case A:** The user asks "Delete my account". GUS replies: "To delete your account, go to Settings > Profile."
    
    **Case B:** The user asks "Delete my account". GUS connects to the Admin API, checks the balance, executes the SQL `DELETE` command, and sends a confirmation email.

    In which of these cases is GUS an agent?

    <div style="margin-bottom: 15px;">
    ● <button onclick="alert('😔 No. Here, GUS only generates text (an instruction). It does not act on the system.')" style="cursor: pointer;">Case A</button><br>
    ● <button onclick="alert('🥳 BRAVO! Here, GUS uses tools (API, SQL, Email) to execute a real action on the world. This is the definition of an Agent.')" style="cursor: pointer;">Case B</button>
    </div>

---

## Exercise 3: inside the database 🛢️
*(Objective: understand architectural components - LO 4.1.1)*

**Context:** To make RAG work, MagicFridge must store its thousands of recipes in a way that the AI can "understand" semantically (for example, knowing that "Tomato" is close to "Red Sauce").

**Question:** What type of database should the architect install?

1.  A Relational Database (SQL)
2.  A Vector Database (Vector DB)
3.  A shared Excel file

??? success "See the answer"
    **Answer: 2. A Vector Database.**
    
    It allows storing the **Embeddings** (numerical vectors) of documents. This is what enables the system to perform a semantic search ("find me something that looks like a tomato") rather than an exact keyword search.

---

## Exercise 4: crisis in production (LLMOps) 🚨
*(Objective: manage operational lifecycle - LO 4.2.2)*

**Alert:** Since this morning's model update, API costs have multiplied by 10, and GUS answers in German half the time.

**Which LLMOps practice failed?**

1.  Fine-tuning
2.  Monitoring
3.  Orchestration

??? failure "See the answer"
    **Answer: 2. Monitoring.**
    
    A good LLMOps strategy includes automatic alerts on:
    
    *   **Cost** (to detect abnormal spikes).
    *   **Quality/Drift** (to detect that the AI changes language without reason).
    
    *Corrective action:* Immediate rollback to the previous model version.

---

<br>
<hr>

!!! quote "Have you validated the architecture?"
    If these exercises helped you understand the inner workings, a small coffee for the coach would be greatly appreciated! ☕
    
    <div style="text-align: center; margin-top: 15px;">
        <a href='https://ko-fi.com/monwebmestre' target='_blank'>
            <img height='36' style='border:0px;height:36px;' src='https://storage.ko-fi.com/cdn/kofi2.png?v=3' border='0' alt='Buy Me a Coffee' />
        </a>
    </div>