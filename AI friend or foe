const questions = [
  {
    question: "How do you eat your fries?",
    options: [
      { text: "With mayo, of course! 🍟", score: 10 },
      { text: "Ketchup like a tourist. 🍅", score: 5 },
      { text: "I dip them in beer. 🍺", score: 7 },
      { text: "Fries? I prefer baguettes. 🥖", score: 0 }
    ]
  },
  {
    question: "How often do you eat waffles?",
    options: [
      { text: "Daily 🏆", score: 10 },
      { text: "On special occasions 🎉", score: 7 },
      { text: "Only when tourists are watching 🤔", score: 5 },
      { text: "Waffles? Never heard of them! 😅", score: 0 }
    ]
  },
  {
    question: "What’s your favorite type of Belgian chocolate?",
    options: [
      { text: "Pralines 🍫", score: 10 },
      { text: "Dark chocolate 🍩", score: 7 },
      { text: "Milk chocolate 🍬", score: 5 },
      { text: "I don’t eat chocolate 😱", score: 0 }
    ]
  },
  {
    question: "Which Belgian comic is the best?",
    options: [
      { text: "Tintin 🏴‍☠️", score: 10 },
      { text: "The Smurfs 💙", score: 7 },
      { text: "Suske en Wiske 📖", score: 3 },
      { text: "I don’t read comics 📖", score: 0 }
    ]
  },
  {
    question: "What’s your favorite Belgian city?",
    options: [
      { text: "Brussel 🇧🇪", score: 10 },
      { text: "Brugge 🏰", score: 7 },
      { text: "Antwerpen ⚓", score: 5 },
      { text: "I prefer Paris 🇫🇷", score: 0 }
    ]
  }
];

const getResult = (score) => {
  if (score >= 40) return "Waffle Overlord 🏰 - You embrace all things Belgian!";
  if (score >= 30) return "Frites Fanatic 🍟 - You have a deep love for Belgian fries!";
  if (score >= 20) return "Chocolate Lover 🍫 - Belgian sweets are your weakness!";
  return "Casual Belgian 🇧🇪 - You enjoy Belgian culture in moderation!";
};

document.addEventListener("DOMContentLoaded", () => {
  let currentQuestion = 0;
  let score = 0;
  const quizContainer = document.getElementById("quiz");

  const renderQuestion = () => {
    if (currentQuestion < questions.length) {
      const q = questions[currentQuestion];
      quizContainer.innerHTML = `<h2>${q.question}</h2>`;
      q.options.forEach((option, index) => {
        const btn = document.createElement("button");
        btn.textContent = option.text;
        btn.classList.add("quiz-button");
        btn.onclick = () => {
          score += option.score;
          currentQuestion++;
          renderQuestion();
        };
        quizContainer.appendChild(btn);
      });
    } else {
      quizContainer.innerHTML = `<h2>Your Belgian Identity: ${getResult(score)}</h2>`;
      const restartBtn = document.createElement("button");
      restartBtn.textContent = "Play Again";
      restartBtn.classList.add("quiz-button");
      restartBtn.onclick = () => location.reload();
      quizContainer.appendChild(restartBtn);
    }
  };

  renderQuestion();
});
