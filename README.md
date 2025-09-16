%%writefile index.html
<!DOCTYPE html>
<html>
<head>
    <title>Simple Question Form</title>
</head>
<body>
    <h1>Ask a Question</h1>
    <label for="questionInput">Faça sua pergunta</label><br>
    <input type="text" id="questionInput"><br><br>
    <button id="sendButton">Enviar pergunta</button>
    <p id="responseArea"></p>
</body>
</html> %%writefile style.css
body {
    font-family: sans-serif;
    margin: 20px;
}

input[type="text"] {
    padding: 8px;
    margin-bottom: 10px;
}

button {
    padding: 10px 15px;
    background-color: #4CAF50;
    color: white;
    border: none;
    cursor: pointer;
    margin-bottom: 10px;
}

button:hover {
    opacity: 0.8;
}

#responseArea {
    margin-top: 10px;
    font-style: italic;
}
%%writefile index.html
<!DOCTYPE html>
<html>
<head>
    <title>Simple Question Form</title>
    <link rel="stylesheet" href="style.css">
</head>
<body>
    <h1>Ask a Question</h1>
    <label for="questionInput">Faça sua pergunta</label><br>
    <input type="text" id="questionInput"><br><br>
    <button id="sendButton">Enviar pergunta</button>
    <p id="responseArea"></p>
</body>
</html> 
%%writefile script.js
document.addEventListener('DOMContentLoaded', function() {
    const sendButton = document.getElementById('sendButton');
    const responseArea = document.getElementById('responseArea');

    if (sendButton && responseArea) {
        sendButton.addEventListener('click', function() {
            responseArea.textContent = "carregando...";

            setTimeout(function() {
                responseArea.textContent = "Mas essa pergunta é muito fácil, faz uma mais difícil";
            }, 500); // Simulate a 500ms delay
        });
    } else {
        console.error("Could not find sendButton or responseArea element.");
    }
});%%writefile index.html
<!DOCTYPE html>
<html>
<head>
    <title>Simple Question Form</title>
    <link rel="stylesheet" href="style.css">
</head>
<body>
    <h1>Ask a Question</h1>
    <label for="questionInput">Faça sua pergunta</label><br>
    <input type="text" id="questionInput"><br><br>
    <button id="sendButton">Enviar pergunta</button>
    <p id="responseArea"></p>

    <script src="script.js"></script>
</body>
</html>
