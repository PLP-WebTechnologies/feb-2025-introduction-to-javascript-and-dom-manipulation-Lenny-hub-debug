# Introduction to JavaScript and DOM Manipulation

## Objectives

Write basic JavaScript functions.
Manipulate the DOM dynamically.
Respond to user interactions.

## Instructions

- Create a script.js file and link it to a HTML.
- Structure the document using DOCTYPE, html, head, and body.

>[!NOTE]
>  - Write JavaScript that:
>  - Changes text content dynamically.
>  - Modifies CSS styles via JavaScript.
>  - Adds or removes an element when a button is clicked.


# Tasks
- Create a well-structured HTML5 document.
- Use at least 5 different HTML elements.
- Ensure semantic correctness.

Happy Coding! 💻✨



<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>DOM Manipulation Example</title>
  <link rel="stylesheet" href="style.css">
</head>
<body>
  <header>
    <h1>Welcome to My Page</h1>
  </header>

  <section id="content">
    <p id="text">This is some text that will change dynamically.</p>
    <button id="changeTextBtn">Change Text</button>
    <button id="changeStyleBtn">Change Style</button>
    <button id="addElementBtn">Add New Element</button>
    <button id="removeElementBtn">Remove Last Element</button>
  </section>

  <footer>
    <p>&copy; 2025 Your Name</p>
  </footer>

  <script src="script.js"></script>
</body>
</html>
// Change text content dynamically
const changeTextBtn = document.getElementById('changeTextBtn');
const textElement = document.getElementById('text');

changeTextBtn.addEventListener('click', () => {
  textElement.textContent = 'The text has been changed dynamically!';
});

// Modify CSS styles via JavaScript
const changeStyleBtn = document.getElementById('changeStyleBtn');

changeStyleBtn.addEventListener('click', () => {
  textElement.style.color = 'red';
  textElement.style.fontSize = '20px';
  textElement.style.fontWeight = 'bold';
});

// Add or remove an element when a button is clicked
const addElementBtn = document.getElementById('addElementBtn');
const removeElementBtn = document.getElementById('removeElementBtn');
const contentSection = document.getElementById('content');

addElementBtn.addEventListener('click', () => {
  const newElement = document.createElement('p');
  newElement.textContent = 'This is a newly added element!';
  contentSection.appendChild(newElement);
});

removeElementBtn.addEventListener('click', () => {
  const lastElement = contentSection.lastElementChild;
  if (lastElement) {
    contentSection.removeChild(lastElement);
  }
});
body {
  font-family: Arial, sans-serif;
  background-color: #f4f4f4;
  color: #333;
  margin: 0;
  padding: 0;
}

header {
  background-color: #4CAF50;
  color: white;
  padding: 10px 0;
  text-align: center;
}

section {
  padding: 20px;
}

button {
  background-color: #4CAF50;
  color: white;
  border: none;
  padding: 10px 20px;
  margin: 5px;
  cursor: pointer;
}

button:hover {
  background-color: #45a049;
}

footer {
  background-color: #333;
  color: white;
  text-align: center;
  padding: 10px 0;
  position: fixed;
  width: 100%;
  bottom: 0;
}
