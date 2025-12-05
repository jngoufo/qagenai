# 🧪 Practice Lab: AI Strategist

Welcome to the executive boardroom of **MagicFridge**.
Here, we no longer talk about code, but about governance, budget, and people. Your mission is to deploy AI without putting the company in danger.

---

## Exercise 1: Tracking Shadow AI 👻
*(Objective: identify shadow AI risks - LO 5.1.1)*

**Situation:** during an audit, you discover that a junior developer copied the entire source code of the MagicFridge "Bank Payment" module into *ChatGenius* (a free, public AI tool) to ask it for optimizations.

!!! question "What is the major immediate risk?"

    **Your diagnosis**

    <div style="margin-bottom: 15px;">
    ● <button onclick="alert('😔 No. The code might be optimized correctly; that is not the main concern here.')" style="cursor: pointer;">Quality risk (Non-functional code)</button><br>
    ● <button onclick="alert('🥳 EXACT! By sending proprietary code to a public server, he potentially surrendered intellectual property (IP) and exposed critical security vulnerabilities.')" style="cursor: pointer;">Intellectual property leak risk</button><br>
    ● <button onclick="alert('😔 It is a risk, but less severe than the loss of critical source code.')" style="cursor: pointer;">Cost risk (Tokens)</button>
    </div>

---

## Exercise 2: Choosing the Right Weapon (LLM vs. SLM) ⚔️
*(Objective: select the appropriate model - LO 5.1.3)*

**Project:** MagicFridge wants to launch an **"Offline Assistant"** feature: the user must be able to ask for a recipe in natural language even at the back of a supermarket without an internet connection (the AI runs directly on the phone).

**Which type of model do you choose?**

!!! question "The architect's choice"

    <div style="margin-bottom: 15px;">
    <button onclick="alert('😔 Impossible. An LLM is too big to fit on a phone and requires an internet connection for the API.')" style="cursor: pointer;">Option A: a **Large Language Model (LLM)**</button><br>
    <button onclick="alert('🥳 BRAVO! An SLM is compact, consumes little battery, and can run locally (Edge AI), which is perfect for offline mode.')" style="cursor: pointer;">Option B: an optimized **Small Language Model (SLM)**</button>
    </div>

---

## Exercise 3: Job Evolution 💼
*(Objective: understand new skills - LO 5.2.1)*

**Context:** you are writing the job description to recruit a new "GenAI QA Tester".
Among these three skills, which one is **specific** to this new role (and not classic testing)?

1.  Knowing how to write test cases in Gherkin.
2.  Knowing how to evaluate model temperature and context window.
3.  Knowing how to use Jira for bug tracking.

??? success "See the answer"
    **Answer: 2. Knowing how to evaluate model temperature and context window.**
    
    *   **Why?** This is a technical skill purely related to how LLMs function.
    *   Skills 1 and 3 are classic software testing skills (and still necessary!), but not specific to GenAI.

---

## Exercise 4: The Deployment Dilemma 🚀
*(Objective: manage change and risks - LO 5.1.4)*

**Situation:** management is impatient. The CEO wants to deploy GUS everywhere, immediately, to replace customer service by next Monday.
The QA team has only done a few promising exploratory tests (Discovery Phase).

**What is your recommendation as a Test Manager?**

1.  "Let's go! The AI will learn on the job with real customers."
2.  "Stop. We must go through the Initiation and Usage Definition phase before generalizing."

??? failure "See the recommendation"
    **Answer: 2. Stop.**
    
    Skipping steps is a recipe for disaster (massive hallucinations, angry customers).
    We must first:

    1.  Select a pilot use case.
    2.  Set up guardrails (RAG, filters).
    3.  Measure quality before opening the floodgates.

---

<br>
<hr>

!!! quote "Training Complete!"
    🎉 **Congratulations!** You have covered the entire curriculum.
    
    If this free course helped you feel ready for your certification exam, consider supporting the guide:
    
    <div style="text-align: center; margin-top: 15px;">
        <a href='https://ko-fi.com/monwebmestre' target='_blank'>
            <img height='36' style='border:0px;height:36px;' src='https://storage.ko-fi.com/cdn/kofi2.png?v=3' border='0' alt='Buy Me a Coffee' />
        </a>
    </div>