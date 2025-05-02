# rock-paper-scissors
Classic game with score tracking and responsive design
HTML CODE
<div class="project-card" data-category="javascript">
                <div class="rps-game">
                  <h3>Rock Paper Scissors</h3>
                  <div class="game-container">
                    <div class="choices">
                      <button class="choice-btn" data-choice="rock">✊</button>
                      <button class="choice-btn" data-choice="paper">✋</button>
                      <button class="choice-btn" data-choice="scissors">✌️</button>
                    </div>
                    <div id="game-result" class="result-box">
                      <p>Make your choice!</p>
                    </div>
                    <div class="scoreboard">
                      <p>You: <span id="player-score">0</span></p>
                      <p>Computer: <span id="computer-score">0</span></p>
                    </div>
                  </div>
                </div>
                <div class="project-info">
                  <h3>Rock Paper Scissors</h3>
                  <p>Classic game with score tracking and responsive design.</p>
                  <div class="tech-used">
                    <span>HTML5</span>
                    <span>CSS3</span>
                    <span>JavaScript</span>
                  </div>
                </div>
              </div>
        </div>
JS CODE
const choices = ['rock', 'paper', 'scissors'];
let playerScore = 0;
let computerScore = 0;

document.querySelectorAll('.choice-btn').forEach(button => {
  button.addEventListener('click', function() {
    const playerChoice = this.dataset.choice;
    const computerChoice = choices[Math.floor(Math.random() * 3)];
    const result = determineWinner(playerChoice, computerChoice);
    
    updateScore(result);
    displayResult(playerChoice, computerChoice, result);
  });
});

function determineWinner(player, computer) {
  if (player === computer) return 'draw';
  if (
    (player === 'rock' && computer === 'scissors') ||
    (player === 'paper' && computer === 'rock') ||
    (player === 'scissors' && computer === 'paper')
  ) {
    return 'player';
  }
  return 'computer';
}

function updateScore(result) {
  if (result === 'player') playerScore++;
  if (result === 'computer') computerScore++;
  document.getElementById('player-score').textContent = playerScore;
  document.getElementById('computer-score').textContent = computerScore;
}

function displayResult(player, computer, result) {
  const resultText = {
    player: 'You win!',
    computer: 'Computer wins!',
    draw: "It's a draw!"
  };
  
  document.getElementById('game-result').innerHTML = `
    <p>You chose <strong>${player}</strong></p>
    <p>Computer chose <strong>${computer}</strong></p>
    <h4>${resultText[result]}</h4>
  `;
}
CSS CODE
.rps-game {
    padding: 20px;
    background: #f8f9fa;
    border-radius: 8px;
    text-align: center;
}

.choices {
    display: flex;
    justify-content: space-around;
    margin: 20px 0;
}

.choice-btn {
    font-size: 2.5rem;
    background: none;
    border: none;
    cursor: pointer;
    transition: transform 0.2s;
}

.choice-btn:hover {
    transform: scale(1.2);
}

.scoreboard {
    display: flex;
    justify-content: space-around;
    margin-top: 20px;
    font-weight: bold;
}

.portfolio-image {
    width: 280px;
    transition: all 0.3s ease;
    border-radius: 16px;
}

.portfolio-image:hover {
    transform: scale(1.03);
    /* Slight zoom on hover */
    box-shadow: 0 6px 12px rgba(0, 0, 0, 0.15);
}
