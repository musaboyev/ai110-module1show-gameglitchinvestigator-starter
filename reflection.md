# 💭 Reflection: Game Glitch Investigator

Answer each question in 3 to 5 sentences. Be specific and honest about what actually happened while you worked. This is about your process, not trying to sound perfect.

## 1. What was broken when you started?

- What did the game look like the first time you ran it?
It just kept saying GO HIGHER. The range for hard difficulty was inconsistent with the rest of the difficulty levels. The new game button was not function as it was intented in logic utls.
- List at least two concrete bugs you noticed at the start
  attempts were intialized to 1 instead of 0.  Too high gave bonus points instead of deducting. The hint always said between 1 and 100 no matter what the difficulty was.

---

## 2. How did you use AI as a teammate?

- Which AI tools did you use on this project (for example: ChatGPT, Gemini, Copilot)?
Claude Code, ChatGPT
- Give one example of an AI suggestion that was correct (including what the AI suggested and how you verified the result).
AI suggesed to change the range from always 1-100 to low-high which was correct given the logic of the game
- Give one example of an AI suggestion that was incorrect or misleading (including what the AI suggested and how you verified the result).
Claude suggested that score should be reset which was a good suggestion if I lose the game but if I won the game I would want the score to carry over.

---

## 3. Debugging and testing your fixes

- How did you decide whether a bug was really fixed?
I rerun the game from the st.
- Describe at least one test you ran (manual or using pytest)
I changed the difficulty levels and rerun the game to check if the range was consistent with the levels. 
  and what it showed you about your code.
- Did AI help you design or understand any tests? How?
I did not use AI to desing the tests. 

---

## 4. What did you learn about Streamlit and state?

- In your own words, explain why the secret number kept changing in the original app.
Every time one clicks a button or type anything, Streamlit reruns the entire script. In the original buggy version, if secret wasn't protected by if "secret" not in st.session_state, calling random.randint() again on every rerun would pick a new number each time.
- How would you explain Streamlit "reruns" and session state to a friend who has never used Streamlit?
Every interaction refreshes the page and re-runs all of the Python code
- What change did you make that finally gave the game a stable secret number?
The secret was already being saved to st.session_state with the if "secret" not in st.session_state check — so it was only generated once

---

## 5. Looking ahead: your developer habits

- What is one habit or strategy from this project that you want to reuse in future labs or projects?
  - This could be a testing habit, a prompting strategy, or a way you used Git.
I understood it was very important to fully understand what functions do from files like logic_utils before trying to fix the bugs. 
- What is one thing you would do differently next time you work with AI on a coding task?
Test every AI suggestion because AI might direct the coder in the wrong direction. 
- In one or two sentences, describe how this project changed the way you think about AI generated code.
Different AI models interpret the game logic differently. 