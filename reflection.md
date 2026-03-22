# 💭 Reflection: Game Glitch Investigator

Answer each question in 3 to 5 sentences. Be specific and honest about what actually happened while you worked. This is about your process, not trying to sound perfect.

## 1. What was broken when you started?

- What did the game look like the first time you ran it?
- List at least two concrete bugs you noticed at the start  
  (for example: "the hints were backwards").

The game when I first started it seemed fine until I actually started playing it. 
The first bug was the hints not being accurate. If I entered 3, it would say "Go LOWER!" and then if I entered 2, then it would say "Go HIGHER!", but then if I entered 1, then it would say "Go LOWER!". 
The second bug was that the game would not end, even if I tried various numbers that did seem to be the guess, the game would just not end. 
The third bug is that once I ran out of attempts, I had to start a new game, and even if I clicked on the New Game button and the number of attempts resetted back to 8, the game would still not proceed for me and tell me to start a new game. 
 
---

## 2. How did you use AI as a teammate?

- Which AI tools did you use on this project (for example: ChatGPT, Gemini, Copilot)?
- Give one example of an AI suggestion that was correct (including what the AI suggested and how you verified the result).
- Give one example of an AI suggestion that was incorrect or misleading (including what the AI suggested and how you verified the result).

I used Github Copilot and ChatGPT as my AI assistants for this project. 
One example of an AI suggestion that was correct was that ChatGPT/Copilot correctly identified the hint logic in check_guess and how it was reversed. The AI assistants suggested swapping the "Too High" and "Too Low" messages. I tried out this suggestion and verified it by testing out the game again and now the hints are correct and actually help in guessing the secret number efficiently. 
One example of an AI suggestion that was incorrect or misleading is that ChatGPT/Copilot first suggested me that the game was not ending correctly because of the faulty hint logic. This was a misleading suggestion because the actual issue was the secret number sometimes being converted to the string type, which caused the comparisons to fail. I tested this change by checking the type of the secret during runtime and fixing it to always stay as an integer. This allowed the game to end properly. 

---

## 3. Debugging and testing your fixes

- How did you decide whether a bug was really fixed?
- Describe at least one test you ran (manual or using pytest)  
  and what it showed you about your code.
- Did AI help you design or understand any tests? How?

To decide if a bug was really fixed, I would verify by manually testing the game and by running the automated pytest test cases as well. 
One rest that I ran manually is for when I was checking if the guess was correctly identified from the hints when compared with the secret number. check_guess returned "Too High" when the guess was higher, and "Too Low" when lower correctly. This confirmed that the hint logic was working correctly. 
AI helped me understand and know that these test cases were solid because they were targetted for the specific bugs I was testing out. This made it easy for me to confirm if the bugs were actually being thoroughly tested or not. 

---

## 4. What did you learn about Streamlit and state?

- How would you explain Streamlit "reruns" and session state to a friend who has never used Streamlit?

---

## 5. Looking ahead: your developer habits

- What is one habit or strategy from this project that you want to reuse in future labs or projects?
  - This could be a testing habit, a prompting strategy, or a way you used Git.
- What is one thing you would do differently next time you work with AI on a coding task?
- In one or two sentences, describe how this project changed the way you think about AI generated code.
