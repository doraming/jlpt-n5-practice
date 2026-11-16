QUIZ — SEPARATE QUESTION BANK

1. Extract both index.html and questions.json into the same folder.
2. Open index.html in your browser.
3. Click the question-bank file chooser and select questions.json.
4. To add/remove questions, edit questions.json in a plain-text editor, save as UTF-8, and select it again. Loading a bank resets the active quiz.

When hosted over HTTP/HTTPS, the page automatically loads questions.json from the same folder. When opened directly as a local file, select the JSON manually; no local server is required. File selection is local and does not upload the question bank.

QUESTION FORMAT
Copy an existing object. Keep a unique id, a category (Lesson 1 through Lesson 9, or Advanced 10 through Advanced 12), question, exactly four options, answerIndex, and explanation.
answerIndex uses zero-based numbering: 0 = first, 1 = second, 2 = third, 3 = fourth.
Separate objects with commas. Do not put a comma after the last object. Keep the outer [ and ]. Use double quotes for JSON keys and strings. Use \n inside a string for a line break.
Delete the whole object to remove a question, adjusting the neighboring comma. No need to renumber other IDs. Empty lesson groups are hidden.
Sorting questions remain four-choice position questions and are displayed with their original text.
The existing lesson titles/descriptions are defined in index.html; adding a completely new lesson requires changing those definitions.

Validation covers JSON parsing, non-empty bank, unique IDs, supported categories, four options, answer range, and required text fields. Question content/answer correctness is not reviewed.
