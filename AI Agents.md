# Content
1. [Introduction to AI](#introduction-to-ai)
2. [Agents](#agents)
3. [Types of AI Agents](#types-of-ai-agents)
4. [Problem Solving Agent & Problem formulation](#problem-solving-agent--problem-formulation)
5. [Rational Agent](#rational-agent)
6. [PEAS Properties of AI Agents](#peas-properties-of-ai-agents)


---

# Introduction to AI
Artificial Intelligence (AI) is a branch of Computer Science that focuses on creating machines or software capable of performing tasks that normally require human intelligence.

AI systems are designed to:

- Learn from data (like recognizing patterns)
- Understand language (chatbots, translation)
- Make decisions (recommendations, predictions)
- Solve problems (games, logistics, medical diagnosis)

### Applications of Artificial Intelligence (AI)
1. **Healthcare**
    - Disease detection (X-rays, MRI analysis)
    - Drug discovery (faster research)
    - Personalized treatment plans  

    **Example:** AI helps doctors detect diseases like cancer earlier and more accurately.
2. **Finance**
    - Fraud detection (real-time monitoring)
    - Algorithmic trading
    - Credit scoring  

    **Key Point:** AI detects suspicious transactions instantly, which is not possible manually.
3.  **E-commerce & Marketing**
    - Product recommendation systems
    - Customer behavior prediction
    - Dynamic pricing  

    **Example:** Platforms like Amazon and Flipkart suggest products based on your activity.
4. **Manufacturing**
    - Predictive maintenance
    - Quality control using computer vision
    - Industrial automation  

    **Key Point:** Reduces machine downtime and increases efficiency.
5. **Education**
    - Personalized learning platforms
    - AI tutors
    - Automated grading systems  

    **Example:** Systems adapt learning based on student performance.
6. **Cybersecurity**
    - Threat detection
    - Malware identification
    - Anomaly detection  

    **Key Point:** AI helps detect attacks before they cause damage.
7. **Agriculture**
    - Crop monitoring using drones
    - Yield prediction
    - Smart irrigation systems  

    **Example:** Farmers use AI to optimize resources and increase productivity.




[Go To Top](#content)

---

# Agents
An AI agent is an entity that perceives its environment, makes decisions, and takes actions to achieve a goal.

<img src="./Image/agents.webp" style="width:500px">

### Sensors and Actuators in AI Agents

These are the input and output parts of any agent.

**Sensor:**
- A sensor is anything that collects information from the environment.
- It tells the agent what’s happening.
- Examples:
    - Camera (captures images)
    - Microphone (captures sound)
    - Temperature sensor
    - GPS location data

**Actuator:**
- An actuator is anything that takes action based on decisions.
- It’s how the agent affects the environment.
- Examples:
    - Motors (move a robot)
    - Speakers (produce sound)
    - Display screen (show output)
    - Sending a notification

> Think like a human:
>- Sensors = eyes, ears, skin (input)
>- Actuators = hands, legs, mouth (output)

In AI Agent Terms
- Sensors → Perception
- Actuators → Action

Without sensors → agent is blind\
Without actuators → agent is useless

**Sensors gather data. Actuators execute decisions.**

### Example: Navigation Agent (like Google Maps)
**Goal:** get you from point A → point B as fast as possible

**Sensors (Input)**
- GPS location (where you are)
- Traffic data (live congestion)
- Road conditions (accidents, closures)

**Decision-Making**
- Calculates multiple routes
- Predicts travel time using past + real-time data
- Chooses the optimal path

**Actuators (Output)**
- Displays route on screen
- Gives voice directions
- Reroutes if traffic changes

**it is a real agent Because it continuously:**
- Observes (location + traffic)
- Decides (best route)
- Acts (guides you)
- Updates (reroutes if needed)

That loop is the key. Not a one-time response.

[Go To Top](#content)

---

# Types of AI Agents
These are the standard 5 types you’ll see in real systems.

### 1. Simple Reflex Agents
Act only on current input. No memory. No thinking ahead.

- Rule-based: if condition → action
- Works only in fully observable environments

<img src="./Image/simple-eflex-agent.webp" style="width:500px">

Example:\
A basic thermostat (if temp > 25°C → turn AC on)

**Limitation**
- very less intelligent
- Fails in complex or changing environments

**Advantages**
- Very fast (no computation overhead)
- Easy to design and implement
- Works well in fully predictable environments

### 2. Model-Based Agents
Maintain an internal model (memory of the environnement).
- Keep track of past states
- Handle partially observable environments

<img src="./Image/model-based-agent.png" style="width:500px">

Example:\
A robot that remembers obstacles it has already seen

**Limitations**
- Needs accurate internal model
- More complex to design
- Still doesn’t “plan” or optimize deeply

**Advantages**
- Handles partial observability
- Uses memory to track environment
- More flexible than reflex agents

### 3. Goal-Based Agents

Act to achieve a specific goal.

- Evaluate different possible actions
- Choose path that leads to goal

<img src="./Image/goal-based-agent.webp" style="width:500px">

Example:\
Route planning in Google Maps

**Limitations**
- Computationally expensive (search/planning)
- Doesn’t consider how good a solution is—just reaches goal
- Slower than simpler agents

**Advantages**
- Works toward clear objectives
- Can evaluate multiple paths
- More intelligent decision-making
### 4. Utility-Based Agents

Don’t just achieve a goal—choose the best outcome.

- Use a utility function (score system)
- Optimize for efficiency, cost, time, etc.

<img src="./Image/utility-based-agent.webp" style="width:500px">

Example:\
Choosing the fastest + cheapest route, not just any route

**Limitations**
- Designing a good utility function is hard
- High computation cost
- Can become overly complex

**Advantages**
- Chooses best possible outcome, not just any
- Handles trade-offs (time vs cost vs comfort)
- More realistic for real-world problems

### 5. Learning Agents

Improve performance over time using data.

- Learn from experience
- Adapt to new situations
- Most modern AI = this category

<img src="./Image/learning-agent.webp" style="width:500px">

Example:\
Recommendation systems in YouTube or Netflix

**Limitations**
- Requires large amounts of data
- Training can be expensive (time + compute)
- Can make unpredictable or biased decisions
- Hard to debug

**Advantages**
- Improves over time
- Adapts to new environments
- Handles complex, dynamic problems

[Go To Top](#content)

---
# Problem Solving Agent & Problem formulation
A problem-solving agent in AI is an intelligent agent that decides what actions to take by searching for a sequence of steps that solves a problem and reaches a goal.

It works mainly in situations where:

- The environment is known
- The goal is clearly defined
- The agent can predict the result of actions

Instead of reacting randomly, the agent:

1. Understands the current situation
2. Defines a goal
3. Formulates the problem
4. Searches for a solution
5. Executes the actions

### Characteristics

A problem-solving agent:

- Is goal-based
- Uses reasoning and search
- Chooses actions intelligently
- Works step-by-step toward a solution

### Limitation

These agents struggle when:

- Environment changes rapidly
- Information is incomplete
- Real-time decisions are needed

Because classical problem-solving assumes the world is mostly predictable.


## Problem formulation
Problem formulation in AI is the process of clearly defining a problem so that an AI system can understand it and work toward a solution.

In simple terms, it means converting a real-world situation into a structured form that a computer can solve.

> Problem-solving agent uses problem formulation to understand what exactly it needs to solve.

When formulating a problem in AI, we usually specify:

1. **Initial state**\
The starting situation of the problem.\
Example: A robot is at position A.
2. **Goal state**\
The desired outcome.\
Example: The robot needs to reach position B.\
3. **Actions (operators)**\
The possible moves or steps that can be taken.\
Example: Move left, right, forward, backward.\
4. **State space**
All possible states reachable from the initial state.
Path / solution\
A sequence of actions that leads from the initial state to the goal state.\

5. **Cost (optional)**\
A measure to evaluate solutions (e.g., shortest path, least time, minimum energy).

### Example

**Problem**: Finding the shortest route on a map

- Initial state: Starting city
- Goal state: Destination city
- Actions: Travel between connected cities
- Cost: Distance or time


[Go To Top](#content)

---
# Rational Agent
Rational means thinking and acting logically based on reason, facts, and available information.

A rational person or system tries to make the best possible decision, not a random or emotional one.

A rational agent in AI is an agent that always chooses the action that gives the best possible outcome based on the information it has.

It does not mean the agent is always correct.
It means the agent acts logically and optimally according to its knowledge and goals.

### Definition
A rational agent selects the action that maximizes its performance measure in a given situation.


A rational agent does not know everything.

It only uses:

- Current percepts
- Past knowledge
- Available actions

If information is incomplete, even a rational agent can make mistakes.

### Characteristics of rational agents

A rational agent:

- Is goal-oriented
- Makes decisions logically
- Tries to maximize success
- Adapts based on environment

### Types of agents related to rationality
- Simple reflex agents
- Model-based agents
- Goal-based agents
- Utility-based agents
- Learning agents

All aim to behave rationally in different ways.

[Go To Top](#content)

---

# PEAS Properties of AI Agents
PEAS is a framework used in AI to describe how an AI agent works.

PEAS stands for:
| Letter | Meaning             | Simple Meaning                      |
| ------ | ------------------- | ----------------------------------- |
| P      | Performance Measure | What defines success                |
| E      | Environment         | Where the agent works               |
| A      | Actuators           | How the agent acts                  |
| S      | Sensors             | How the agent sees/gets information |

It helps define:

- What the agent should achieve
- Where it works
- How it acts
- How it observes the environment

### 1. Performance Measure (P)
Defines how success of the agent is evaluated.

Examples
- Accuracy
- Speed
- Safety
- Minimum cost
- User satisfaction

**Self-driving car Performance Measure**

- Reach destination safely
- Avoid accidents
- Minimize fuel usage
- Follow traffic rules

### 2. Environment (E)
The surroundings where the agent operates.

Examples
- Roads
- Chess board
- Hospital
- Internet

**Self-driving car environment**
- Roads
- Traffic signals
- Pedestrians
- Weather
- Other vehicles

### 3. Actuators (A)
The mechanisms used by the agent to perform actions.

Examples
- Wheels
- Robotic arms
- Display screen
- Speakers

**Self-driving car actuators**
- Steering
- Brakes
- Accelerator
- Horn

### 4. Sensors (S)
Used to collect information from the environment.

Examples
- Camera
- Microphone
- GPS
- Temperature sensor

**Self-driving car sensors**
- Cameras
- Radar
- LiDAR
- GPS
- Speed sensors

### Why PEAS is important
PEAS helps AI developers:

- Clearly define the agent
- Understand task requirements
- Design intelligent behavior properly

Without defining PEAS properly, the AI system becomes vague and inefficient.

[Go To Top](#content)

---