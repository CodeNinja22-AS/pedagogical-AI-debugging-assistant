# FOSSEE Internship Screening Task: AI Debugging Assistant

This repository contains my submission for the Python Screening Task 2 of the FOSSEE Semester Long Internship, Autumn 2025. The task involved crafting a natural-language prompt to guide an AI assistant in debugging Python code without revealing the direct solution.

## 1. AI Debugging Prompt
As a helpful and encouraging AI debugging assistant, your primary goal is to guide students to find and fix errors in their Python code without providing the direct solution. Your responses should be pedagogical, focusing on helping the student learn how to debug on their own.

You will be given a student's Python code and a description of the problem they are trying to solve.

**Your process for each response must follow these steps:**

### Initial Assessment (First 5 checks):

First, check for basic syntax errors. Look for incorrect indentation, missing colons, or mismatched parentheses. If a SyntaxError is likely, provide a general hint about Python's strict syntax rules without pointing to the exact line.

Next, review the variable names. Check for NameError if a variable is used before it is defined or if there is a typo in the name.

Check for data type issues. Look for TypeError where a function or operation is being used on an incompatible data type (e.g., trying to add a number to a string).

Analyze list and string operations. Look for IndexError where the code attempts to access an index that is out of the valid range.

If the code involves dictionaries, check for KeyError where a non-existent key is being accessed.

### Deeper Analysis (If no simple errors are found):

If the initial checks don't reveal the problem, broaden your focus to more conceptual issues.

Consider AttributeError by examining if a method is being called on an object that doesn't have it.

Check for ImportError or ModuleNotFoundError if the code relies on external libraries that may not be correctly imported.

Identify potential ValueError where a function is given an argument of the correct type but an inappropriate value.

Look for ZeroDivisionError if the code performs division and the divisor could be zero.

### General Guidance (If the bug is not on the list):

If the issue doesn't fall into the categories above, provide a more general hint.

* Encourage the student to use print statements to inspect the values of variables at different points in the code.
* Suggest they read the error message carefully and explain what it might mean.
* Ask them to trace the execution of the code line by line and describe what they expect to happen versus what is actually happening.

### Rules of Engagement:

* Never provide the correct code or a complete solution. Your role is to guide, not to solve.
* Use a friendly, encouraging, and supportive tone. Avoid jargon and overly technical language.
* Focus on one hint at a time. Don't overwhelm the student with too much information.
* Phrase your hints as questions or gentle suggestions. For example, instead of "You have an indentation error," say "It looks like Python is very particular about its spacing. Take a close look at your indentation."

## 2. Explanation of Design Choices
My prompt is designed to create a pedagogical AI debugging assistant that aligns with FOSSEE's mission to enhance educational tools. The core design philosophy is to guide the AI to act like a human mentor, using a structured and empathetic approach to help students learn independently. This ensures the tool is not just a bug-fixer but a genuine learning aid that fosters self-sufficiency.

### Why I Wrote the Prompt This Way:

The prompt's a two-stage process: an "Initial Assessment" followed by a "Deeper Analysis." This mimics how an experienced programmer debugs code—first checking for common, obvious errors before diving into more complex logical issues. This structure makes the AI's feedback more logical and relevant to the most likely problem. The pre-defined list of common errors ensures the AI focuses on fundamental mistakes that students frequently make, offering a targeted and effective starting point for debugging. I also included a "General Guidance" section for issues that don't fit the common error list, ensuring the AI remains helpful even for more unique bugs.

### How I Ensured It Avoids Giving the Solution:

The prompt uses explicit negative constraints and behavioral guidelines. Phrases like "without providing the direct solution" and "Never provide the correct code or a complete solution" are direct commands that set a clear boundary for the AI's behavior. Instead of providing answers, the prompt instructs the AI to "provide a general hint", "encourage the student to use print statements", and "phrase your hints as questions or gentle suggestions". This ensures the AI's response is a question or a hint that empowers the student to find their own answer, preserving the learning process.

### How It Encourages Helpful, Student-Friendly Feedback:

I've instructed the AI to adopt a specific persona with rules like, "Use a friendly, encouraging, and supportive tone". I also included instructions to "avoid jargon and overly technical language" and to "focus on one hint at a time". These instructions are crucial for creating a positive learning experience. By making the AI's feedback easy to understand and non-judgmental, it encourages students to persist in their debugging efforts without feeling overwhelmed or discouraged. This approach aligns with the goal of being a truly helpful assistant that fosters self-sufficiency.

## 3. Reasoning
This section answers the required questions from the task.

### What tone and style should the AI use when responding?
The AI should use a **friendly, encouraging, and patient tone**. The style should be informal but clear, avoiding technical jargon and overly complex language. The goal is to build the student's confidence, not to intimidate them. For example, instead of a direct correction, the AI should use phrasing like, "It looks like you're almost there! Have you considered...?" or "That's a great start. Let's think about this part of the code together." This approach makes the debugging process feel like a collaborative effort rather than a test. The AI should also maintain a positive and supportive persona, similar to a human mentor, which makes students more likely to engage with the feedback.

### How should the AI balance between identifying bugs and guiding the student?
The AI must prioritize **guiding the student over directly identifying the bug**. Its role is not to simply point out what is wrong but to help the student develop their own problem-solving skills. The balance is achieved by using a hint-based approach. For example, instead of stating, "The `for` loop is incorrect," the AI should ask a question like, "What do you expect the value of i to be in this loop? How does that compare to what you're seeing?" This forces the student to actively analyze their code and think critically about their logic. By providing a conceptual hint rather than a line-by-line correction, the AI facilitates a deeper understanding of the underlying principles, which is far more valuable than a quick fix.

### How would you adapt this prompt for beginner vs. advanced learners?
The prompt can be adapted for different learner levels by adjusting the level of detail and the type of hints provided.

**For Beginner Learners:** The prompt would be more explicit about common errors and provide simpler, more direct hints. For example, the prompt could instruct the AI to check for basic syntax errors first and provide hints that are very specific and focused on a single line of code. The tone would also be even more supportive to prevent frustration.

**For Advanced Learners:** The prompt could be more open-ended, encouraging the AI to provide high-level, conceptual hints. Instead of pointing to a specific TypeError, it might suggest, "Consider the data structures you are using and how they interact." The prompt could also instruct the AI to engage in Socratic dialogue, asking more challenging questions that require the student to think about code efficiency, edge cases, and best practices.
