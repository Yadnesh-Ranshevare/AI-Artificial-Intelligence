# Content
1. [Knowledge Representation](#knowledge-representation)
2. [Knowledge Based Agents](#knowledge-based-agents)
3. [Propositional Logic](#propositional-logic)
4. [First Order Predicate Logic](#first-order-predicate-logic)


---

# Knowledge Representation
Knowledge representation is the method of organizing facts, rules, concepts, and relationships so an AI system can use them to solve problems and make decisions.

In Artificial Intelligence, knowledge representation is used so machines can behave intelligently instead of just blindly executing instructions.

### Knowledge Base
A knowledge base is a structured repository of knowledge that an AI system uses for reasoning and decision-making.

In Artificial Intelligence, the knowledge base acts like the “memory” of the system.

### Why it matters
AI systems need more than raw data.

Example:

- Data: "Paris"
- Useful knowledge: "Paris is the capital of France"

A machine must represent this information in a structured way to reason about it.

### Goals of Knowledge Representation

A good KR system should allow:

- Storing knowledge
- Retrieving knowledge
- Reasoning/inference
- Learning new information
- Decision-making

[Go To Top](#content)

---

# Knowledge Based Agents
A knowledge-based agent is a type of intelligent agent in Artificial Intelligence that uses stored knowledge about the world to make decisions and solve problems.

Instead of just reacting to inputs, it reasons using information it already knows.  

A knowledge-based agent works by:

1. Storing knowledge (facts, rules, relationships)
2. Updating knowledge when it gets new information
3. Using reasoning to decide what to do

### Main components
- **Knowledge Base (KB):**\
A collection of facts and rules about the world\
Example: “All humans are mortal”
- **Inference Engine:**\
The reasoning system that derives new information from known facts
Example: If “Socrates is a human,” then it concludes “Socrates is mortal”
- **Perception:**\
Gets input from the environment
- **Action:**\
Performs actions based on reasoning

<img src="./Image/KBA.png" style="width:500px">


### How it works (simple cycle)
1. Perceive something
2. Add it to the knowledge base
3. Infer new knowledge
4. Decide an action

### Example

A medical diagnosis system:

- Knowledge: Symptoms and diseases
- Input: Patient symptoms
- Reasoning: Matches symptoms to possible diseases
- Output: Diagnosis or advice


[Go To Top](#content)

---
# Propositional Logic
Propositional Logic is a branch of logic where statements are represented as propositions that are either:

- True (T) or
- False (F)

It is widely used in Artificial Intelligence, mathematics, and computer science for reasoning and decision-making.

### What is a Proposition?
A proposition is a statement that has a definite truth value.

Examples:

- “It is raining” → True/False
- “2 + 2 = 4” → True
- “Mumbai is in India” → True

Not propositions:

- “Close the door” (command)
- “How are you?” (question)

Because they don't have truth values.

### Logical Operators
| Operator      | Symbol | Meaning                                       | Example |
| ------------- | ------ | --------------------------------------------- | ------- |
| AND           | ∧      | True only if both statements are true         | P ∧ Q   |
| OR            | ∨      | True if at least one statement is true        | P ∨ Q   |
| NOT           | ¬      | Reverses the truth value                      | ¬P      |
| Implication   | →      | “If P then Q”                                 | P → Q   |
| Biconditional | ↔      | True if both statements have same truth value | P ↔ Q   |

**Example**
| P         | Q          | Expression | Meaning                                |
| --------- | ---------- | ---------- | -------------------------------------- |
| It rains  | It is cold | P ∧ Q      | It rains AND it is cold                |
| It rains  | It is cold | P ∨ Q      | It rains OR it is cold                 |
| It rains  | —          | ¬P         | It is NOT raining                      |
| I study   | I pass     | P → Q      | If I study, then I pass                | 
| Switch ON | Bulb glows | P ↔ Q      | Bulb glows if and only if switch is ON |

### Limitation
Propositional logic cannot express detailed relationships.

Example:

- “All humans are mortal”

This is difficult in propositional logic.\
For such cases, Predicate Logic is used.

[Go To Top](#content)

---
# First Order Predicate Logic
Predicate Logic is an extension of propositional logic that represents:

- objects
- properties
- relationships
- quantified statements

in a much more detailed and powerful way.

It is heavily used in Artificial Intelligence for knowledge representation and reasoning.

### Why Propositional Logic was not enough
Propositional logic treats entire statements as single units.

Example:
```
P = "Ram is human"
Q = "Ram is mortal"
```
The system cannot understand:

- who Ram is
- what “human” means
- relationships between objects

Predicate logic fixes this.

### Basic Components of Predicate Logic
1. Predicates

    Describe properties or relationships.

    Examples:
    ```
    Human(x)
    Loves(x, y)
    Kill(x, y)
    ```
    Meaning:

    - Human(x) → x is human
    - Loves(x,y) → x loves y
    - Kill(x,y) → x kills y
2. Variables

    Represent objects.

    Examples:
    ```
    x, y, z
    ```
3. Constants

    Specific objects/names.

    Examples:
    ```
    Ram, Sita, India
    ```
4. Quantifiers

    - Universal Quantifier (∀)

        Means “for all”.
        ```
        ∀x Human(x)→Mortal(x)
        ```
        Meaning:\
        All humans are mortal.

    - Existential Quantifier (∃)

        Means “there exists”.
        ```
        ∃x Student(x)∧Intelligent(x)
        ```
        Meaning:\
        There exists a student who is intelligent.
    
### Using inference:
If:

- Human(Ram)
- ∀x(Human(x) → Mortal(x))

Then:

- Mortal(Ram)

[Go To Top](#content)

---