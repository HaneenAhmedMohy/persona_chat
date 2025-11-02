# 🎭 Multi-Persona AI Chat System

## 📌 Overview  
This project demonstrates the power of **system messages** by creating multiple AI personas that share the same model but behave differently.  
Each persona has its own memory and personality, showing how prompt design can drastically change behavior.

## 🎯 Objectives  

| Feature | Description |
|---|---|
| ✅ 5+ distinct AI personas | Unique tones + behavior |
| ✅ Individual system prompts | Each persona has rules + style |
| ✅ Separate memory per persona | No history mixing |
| ✅ Persona switching | Preserve history per persona |
| ✅ Response streaming | Token-by-token output |
| ✅ Compare personas | Multi-persona answer to same prompt |
| ✅ Conversation export | Save chat logs |
| ✅ Token usage tracking | Count per-persona tokens |

---

## 🤖 Personas Implemented

| Persona | Behavior |
|---|---|
| **Python Tutor** | Patient teacher, step-by-step, examples |
| **Shakespearean Translator** | Classic Shakespearean tone & grammar |
| **Socratic Teacher** | Responds only with questions |
| **ELI5 Explainer** | Simplifies concepts like talking to a child |
| **Technical Writer** | Structured, precise, bullet-based |
| *(Optional)* Motivational Coach | Encouraging, emotional support |

Each persona has a **system prompt** defining:

- Tone & communication style  
- Rules of behavior  
- Memory scope  
- Optional examples

---

## 🧠 Design Decisions

### ✅ System Messages for Persona Control  
Guarantees consistent personality & rules across the entire conversation.

### ✅ Separate Conversation History  
Simulates independent minds — each persona remembers only its own dialogs.

### ✅ Streaming Responses  
Natural chat feel, incremental text like real model generation.

### ✅ Comparison Mode  
Ask one question → see varied reasoning styles instantly.

---

## 🧩 Supported Commands

| Command | Purpose |
|---|---|
| `/switch <persona>` | Change active persona |
| `/reset` | Reset only current persona memory |
| `/compare p1 p2 p3 <prompt>` | Ask same question to multiple personas |
| `/export` | Save conversation transcript |
| `/tokens` | Display token usage stats |

---

## 💬 Example Dialogs

### Python Tutor — 5 Turns
```
User: What is a function in Python?
Tutor: A function is a reusable block of code…
User: Show example
Tutor:
def greet(name):
    print("Hello", name)
User: Why use functions?
Tutor: To reuse logic & organize code…
User: Explain with analogy
Tutor: Like a lunchbox… pack once and reuse!
```

### Shakespearean Persona — 3 Snippets
```
User: I feel tired
Bot: Mine spirit droops with weary sorrow…

User: Translate “You're amazing”
Bot: Thou art a marvel most divine…
```

### Socratic Teacher
```
User: What is AI?
Bot: What do *you* believe intelligence means?
```

### ELI5 Explainer
```
User: Explain blockchain
Bot: Imagine a notebook everyone shares…
```

### Technical Writer
```
- Communication interface
- Defined request/response contract
- Example: REST using JSON
```

---

## 🆚 Persona Comparison Example
**Prompt:** "Explain recursion"

| Persona | Response Style |
|---|---|
| Python Tutor | “Recursion is when a function calls itself…” |
| Socratic | “What happens if a function repeats itself forever?” |
| ELI5 | “Two mirrors facing each other — reflections forever!” |

---

## 🧠 State Management

- Each persona has its own message list
- System prompt always index `0`
- Switching does **not** erase memory
- Reset wipes only persona’s history

---

## ⚙️ Challenges & Solutions

| Challenge | Fix |
|---|---|
Personas sounded similar | Strengthened prompt rules |
Memory bleed | Dedicated storage per persona |
Streaming issues | Token streaming loop |
Comparing personas | Parallel calls + labels |

---

## ✅ Conclusion  
This project shows the impact of **prompt engineering + memory control**, enabling intelligent AI “characters” with consistent:

- Tone  
- Logic  
- Behavior  
- Memory  

It demonstrates how to build **real multi-persona systems**, useful for tutoring apps, language companions, role-play chatbots, and educational platforms.