📌 Overview
This project demonstrates the power of system messages by creating multiple AI personas that share the same model but behave differently.
Each persona maintains its own conversation history and response style, showing how behavior can change using carefully crafted prompts.
🎯 Objectives


Implement 5+ distinct AI personas with unique behavior


Each persona has its own system prompt & memory


Support persona switching with preserved history


Stream responses token-by-token


Compare personas on the same question


Reset & export conversations


Count tokens used per chat



🤖 Personas Implemented
PersonaBehaviorPython TutorPatient teacher, step-by-step explanations + examplesShakespearean TranslatorConverts modern English to Shakespeare styleSocratic TeacherAnswers with questions to spark critical thinkingELI5 ExplainerExplains concepts in the simplest way possibleTechnical WriterPrecise, structured, bullet-formatted answers(Optional) Motivational CoachEncouraging and emotional support tone
Each persona has a custom “system_message” defining:


Tone


Response style


Rules


Optional examples



🧠 Design Decisions
✅ Why system messages?
System messages enforce persona behavior consistently and persist across the conversation.
✅ Why separate histories?
To simulate independent personalities and memory, each persona keeps a separate chat history.
✅ Streaming responses
Streaming creates more natural chatbot feel and shows incremental thinking.
✅ Comparison mode
Lets you send the same user prompt to multiple personas to see different reasoning styles.

🧩 Conversation Features
FeatureDescription/switch <persona>Switch persona & keep history/resetReset current persona memory/compare p1 p2 p3Ask same question to multiple personas/exportSave history to fileToken CountTracks tokens per persona

📚 Example Conversations
Python Tutor — 5 Turns
User: What is a function in Python?
Tutor: A function is a reusable block of code…
User: Show me an example
Tutor:
def greet(name):
    print("Hello", name)

User: Why use functions?
Tutor: To organize code, re-use logic…
User: Explain with analogy
Tutor: Think of a function like a lunchbox…

Shakespearean Persona — 5 Turns
User: I feel tired
Shakespeare: Mine spirit droops with weary sorrow…
User: Translate "You're amazing"
Shakespeare: Thou art a marvel most divine…
User: Ask me how my day was
Shakespeare: Pray, how hath thy day unfolded?

Socratic Teacher — 5 Turns
User: What is AI?
Socratic: What do you think intelligence means?
User: Learning and thinking
Socratic: And what separates machine learning from human thought?
User: Data vs experience
Socratic: So is AI truly thinking — or mimicking patterns?

ELI5 Explainer — 5 Turns
User: Explain blockchain
ELI5: Imagine a notebook everyone can see…
User: Why safe?
ELI5: Because no one can erase a page…

Technical Writer — 5 Turns
User: What is an API?
Tech Writer:


Interface allowing systems to communicate


Standard request/response format


Example: REST/JSON



🆚 Comparison Example
Prompt: “Explain recursion”
Python Tutor
“Recursion occurs when a function calls itself… Example: Fibonacci…”
Socratic Teacher
“What happens if a function repeats its steps? And what stops it from repeating forever?”
ELI5 Explainer
“Imagine two mirrors facing each other — reflections forever!”

🧠 Conversation State Management


Each persona has isolated history list


System message inserted at index 0


Switching persona does not erase memory


Reset clears and reloads only system prompt



⚙️ Challenges & Solutions
ChallengeSolutionPersonas sounded similarStrengthened system prompts & constraintsMemory bleed across personasSeparate memory object per personaStreaming issuesUsed token streaming loopComparing personasParallel calls + labeled output

✅ Conclusion
This project highlights how AI personality and behavior can be engineered using:


System prompts


Conversation memory


Controlled chat flow
