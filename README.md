<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <title>Riddle Me This</title>
  <style>
    body {
      font-family: 'Segoe UI', sans-serif;
      background-color: #e8f0fe;
      display: flex;
      flex-direction: column;
      align-items: center;
      justify-content: center;
      height: 100vh;
      margin: 0;
      padding: 20px;
      text-align: center;
    }

    .riddle-box {
      background: #ffffff;
      border-radius: 10px;
      padding: 30px;
      box-shadow: 0 4px 10px rgba(0,0,0,0.1);
      max-width: 600px;
    }

    button {
      background-color: #0d6efd;
      color: white;
      border: none;
      padding: 10px 20px;
      font-size: 16px;
      border-radius: 8px;
      margin-top: 20px;
      cursor: pointer;
    }

    button:hover {
      background-color: #0b5ed7;
    }

    .answer {
      margin-top: 10px;
      color: #2c2c2c;
      font-style: italic;
    }

    .back {
      margin-top: 40px;
    }

    .back a {
      text-decoration: none;
      color: #0d6efd;
      font-weight: bold;
    }
  </style>
</head>
<body>

  <div class="riddle-box">
    <h1>🧠 Riddle Me This</h1>
    <p id="riddle">Click below to get a riddle!</p>
    <p id="answer" class="answer"></p>
    <button onclick="generateRiddle()">New Riddle</button>
  </div>

  <div class="back">
    <a href="scratch.html">← Back to Scratch Page</a>
  </div>

  <script>
    const riddles = [
      {
        question: "I speak without a mouth and hear without ears. I have no body, but I come alive with wind. What am I?",
        answer: "An echo."
      },
      {
        question: "What can run but never walks, has a bed but never sleeps, and has a mouth but never eats?",
        answer: "A river."
      },
      {
        question: "I’m tall when I’m young, and I’m short when I’m old. What am I?",
        answer: "A candle."
      },
      {
        question: "I have keys but no locks. I have space but no room. You can enter, but you can’t go outside. What am I?",
        answer: "A keyboard."
      },
      {
        question: "What has to be broken before you can use it?",
        answer: "An egg."
      },
      {
        question: "BONUS: What do you call a riddle that doesn’t make sense?",
        answer: "A ChatGPT original 😅"
      }
    ];

    function generateRiddle() {
      const randIndex = Math.floor(Math.random() * riddles.length);
      document.getElementById('riddle').textContent = riddles[randIndex].question;
      document.getElementById('answer').textContent = "🤫 Click again to reveal the answer...";
      
      // Change answer after delay
      setTimeout(() => {
        document.getElementById('answer').textContent = riddles[randIndex].answer;
      }, 3500);
    }
  </script>

</body>
</html>
