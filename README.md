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
CSS CODE
.age-calculator {
    padding: 20px;
    background: #f8f9fa;
    border-radius: 8px;
    text-align: center;
}

.date-input {
    padding: 12px;
    width: 100%;
    margin: 15px 0;
    border: 2px solid #ddd;
    border-radius: 5px;
    font-size: 1rem;
}

.result-box {
    margin-top: 20px;
    padding: 15px;
    background: white;
    border-radius: 5px;
    box-shadow: 0 2px 5px rgba(0, 0, 0, 0.1);
}
JS SCRIPT
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
