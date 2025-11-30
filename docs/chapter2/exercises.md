# 🧪 Practice lab: become a prompt engineer

Welcome to the control room of **MagicFridge**.
You have learned the theory, now you must apply it. These exercises put you in the shoes of a quality engineer facing GUS (our AI).

---

## Exercise 1: the anatomy of a prompt 🦴
*(Objective: structure an effective prompt - LO 2.1.1)*

**Situation:** a junior tester sends you this prompt she used to test the "Add to cart" function:
> *"Test if it works when I add apples."*

**Your mission:** this prompt is mediocre. Identify 3 critical components that are most sorely missing to make it a pro-level prompt.🧐

!!! question "Critical analysis" 
    Select the missing elements (mentally), then reveal the analysis to compare.

    ??? success "Reveal the Senior QA's analysis"
        This prompt is unusable by the AI because it lacks:
        
        1.  **The role (persona):** the AI does not know if it should act as an end-user or a technical tester.
        2.  **The context:** "If it works" is too vague. Are we talking about performance? Functionality? Security?
        3.  **The output format:** the AI will probably answer with a trivial sentence. We want a structured format (Gherkin or table).
        
        **Corrected version:**
        *"Act as a QA tester (role). For the 'Cart' function (context), generate 3 negative test cases for adding products (instruction). Present the result as a table (format)."*

---

## Exercise 2: which technique for which task? 🛠️
*(Objective: choose the right prompting technique - LO 2.2.5)*

**Task:** for each situation encountered at MagicFridge, click on the most suitable technique.

!!! question "Your turn"

    **1. You want the AI to generate 50 test cases in strict Gherkin format, without syntax errors.**
    <div style="margin-bottom: 15px;">
    ● <button onclick="alert('😔 No. Prompt chaining is useful for complex reasoning, not for forcing a repetitive format.')" style="cursor: pointer;">Prompt chaining</button><br>
    ● <button onclick="alert('🥳 EXACT! By giving 2 or 3 perfect Gherkin examples (shots), the AI will mimic their structure. This is the king method for formatting.')" style="cursor: pointer;">Few-shot prompting</button><br>
    ● <button onclick="alert('😔 Risky. Without an example, the AI might invent its own syntax.')" style="cursor: pointer;">Zero-shot prompting</button>
    </div>

    **2. You want the AI to analyze a complex user story, identify business rules, and then derive tests.**
    <div style="margin-bottom: 15px;">
    ● <button onclick="alert('🥳 BRAVO! We break it down: 1. Analysis, 2. Rule extraction, 3. Test generation. This prevents the AI from getting confused.')" style="cursor: pointer;">Prompt chaining</button><br>
    ● <button onclick="alert('😔 Not suitable. Examples are not enough here; logical step-by-step reasoning is needed.')" style="cursor: pointer;">Few-shot prompting</button><br>
    ● <button onclick="alert('😔 No. Meta-prompting is used to create prompts, not to execute a complex analysis directly.')" style="cursor: pointer;">Meta-prompting</button>
    </div>

    **3. You need to test the API security but you are stuck and don't know what to ask the AI.**
    <div>
    ● <button onclick="alert('😔 This is not the best option if you don\'t even know where to start.')" style="cursor: pointer;">Few-shot prompting</button><br>
    ● <button onclick="alert('🥳 WON! Ask the AI: \'Act as a security expert. What are the best prompts to test a REST API?\'. It will do the work for you.')" style="cursor: pointer;">Meta-prompting</button>
    </div>

---

## Exercise 3: system or user? 🤖
*(Objective: distinguish prompt types - LO 2.1.3)*

**Context:** you are configuring the MagicFridge automated test tool via its API. You have two text areas to fill.

*   **Zone A:** "You are a sarcastic QA assistant who always answers in rhymes."
*   **Zone B:** "Generate a test for the 'Login' button."

??? question "Which one is the System Prompt?"
    **It is Zone A.**
    
    *   **Why?** It defines the immutable *behavior* and *personality* of the AI.
    *   **Zone B** is the **user prompt**: it is the specific instruction at time T.

---

## Exercise 4: the ruthless evaluation 📉
*(Objective: use evaluation metrics - LO 2.3.1)*

**The test:** you asked GUS to generate SQL scripts to insert test users into the database.
You ask for 10 users.

**The result:** GUS successfully generates 10 SQL queries (`INSERT INTO...`).
However, when executing them, 4 queries fail because the generated email addresses lack an `@` (database constraint violation).

**Which metric is impacted?**

1.  Diversity
2.  Accuracy / success rate
3.  Recall

??? failure "See the answer"
    **Answer: 2. Accuracy (and success rate).**
    
    The AI produced code that looks syntactically correct, but is functionally wrong in 40% of cases.
    
    *   **Corrective action:** use **few-shot prompting** by giving a valid email example, or add an explicit **constraint**: *"Emails must respect the regex format `*@*.*`"*.

---

<br>
<hr>

!!! quote "Have you validated this chapter?"
    If these exercises helped you see things more clearly, a small coffee for the coach would be greatly appreciated! ☕
    
    <div style="text-align: center; margin-top: 15px;">
        <a href='https://ko-fi.com/monwebmestre' target='_blank'>
            <img height='36' style='border:0px;height:36px;' src='https://storage.ko-fi.com/cdn/kofi2.png?v=3' border='0' alt='Buy Me a Coffee' />
        </a>
    </div>