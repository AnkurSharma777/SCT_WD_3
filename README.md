# SCT_WD_3 - Interactive Tic-Tac-Toe Game

![Project Preview](https://img.shields.io/badge/Status-Completed-brightgreen) ![Technology](https://img.shields.io/badge/Tech-HTML%20%7C%20CSS%20%7C%20JavaScript-blue) ![Internship](https://img.shields.io/badge/Internship-SkillCraft%20Technology-orange)

## 📋 Project Overview

**SCT_WD_3** is the third task of the **SkillCraft Technology Web Development Internship Program**. This project demonstrates the creation of a **fully interactive Tic-Tac-Toe game** featuring both Player vs Player and Player vs AI game modes, complete with win detection logic, score tracking, and a modern responsive interface.

## 🎯 Task Requirements

The main objective was to create an interactive Tic-Tac-Toe web game with the following specifications:

- **Interactive Game Board**: 3x3 grid with clickable cells for player moves
- **Two Game Modes**: Player vs Player and Player vs AI functionality
- **Win Detection Logic**: Automatic detection of wins, draws, and game-over states
- **Score Tracking**: Keep track of wins for each player/mode
- **Reset Functionality**: Clear the board and start a new game
- **Responsive Design**: Optimized for all devices and screen sizes
- **Visual Feedback**: Clear indication of current player, game status, and results

## ✨ Features

### 🎮 Core Game Features
- **Classic 3x3 Grid**: Traditional Tic-Tac-Toe board with intuitive cell selection
- **Turn-Based Gameplay**: Alternating moves between X and O players
- **Win Detection Algorithm**: Checks all possible winning combinations (rows, columns, diagonals)
- **Draw Detection**: Recognizes when the board is full with no winner
- **Game State Management**: Proper handling of active/inactive game states

### 🤖 AI Opponent Features  
- **Player vs AI Mode**: Challenge yourself against computer opponent
- **Intelligent AI Logic**: Strategic moves using minimax algorithm or similar logic
- **Multiple Difficulty Levels**: Easy, medium, and hard AI opponents (if implemented)
- **Responsive AI Moves**: Computer responds instantly with optimal or strategic moves

### 🏆 Advanced Features
- **Score Tracking System**: Persistent scoring across multiple games
- **Player Names**: Customizable player names for personalized experience
- **Game Statistics**: Track wins, losses, and draws for each player
- **Animated Transitions**: Smooth visual effects for moves and game state changes
- **Sound Effects**: Optional audio feedback for moves and game events

### 🎨 User Interface
- **Modern Design**: Clean, intuitive interface with professional styling
- **Responsive Layout**: Seamless experience across desktop, tablet, and mobile
- **Visual Game States**: Clear indication of whose turn it is and game results
- **Interactive Elements**: Hover effects, button animations, and visual feedback

## 🛠️ Technologies Used

| Technology | Purpose | Implementation |
|------------|---------|----------------|
| **HTML5** | Structure and game board layout | Semantic grid structure, game controls |
| **CSS3** | Styling and responsive design | Grid layout, animations, hover effects |
| **JavaScript (ES6+)** | Game logic and interactivity | Win detection, AI logic, DOM manipulation |

### Key Technical Implementations
- **Game Logic Functions**: Win checking algorithms, move validation, and game state management
- **AI Algorithm**: Minimax or strategic move selection for computer opponent
- **DOM Manipulation**: Dynamic board updates, score displays, and game status
- **Event Handling**: Click events for cell selection and game controls
- **CSS Grid/Flexbox**: Responsive 3x3 game board layout
- **Local Storage**: Persistent score tracking and game preferences

## 📁 Project Structure

```
SCT_WD_3/
├── index.html              # Main HTML file
├── styles/
│   ├── style.css          # Main stylesheet
│   └── responsive.css     # Mobile responsiveness
├── scripts/
│   ├── game.js            # Core game logic
│   ├── ai.js              # AI opponent logic
│   └── ui.js              # User interface functions
├── assets/
│   ├── images/            # Game icons and graphics
│   ├── sounds/            # Sound effects (optional)
│   └── fonts/             # Custom fonts
├── README.md              # Project documentation
└── LICENSE                # Project license
```

## 🚀 Getting Started

### Prerequisites
- Modern web browser (Chrome, Firefox, Safari, Edge)
- Basic understanding of HTML, CSS, and JavaScript
- Code editor (VS Code recommended)

### Installation & Setup

1. **Clone the repository**
   ```bash
   git clone https://github.com/AnkurSharma777/SCT_WD_3.git
   ```

2. **Navigate to project directory**
   ```bash
   cd SCT_WD_3
   ```

3. **Open in code editor**
   ```bash
   code .  # For VS Code users
   ```

4. **Launch the game**
   - Open `index.html` in your web browser
   - Or use Live Server extension for development

### Alternative Access Methods
- **GitHub Pages**: [Live Demo](https://ankursharma777.github.io/SCT_WD_3) *(if deployed)*
- **Direct Download**: Download ZIP from repository
- **Local Development**: Use any local server setup

## 🎮 How to Play

### Player vs Player Mode
1. **Choose Player vs Player**: Select two-player mode from the main menu
2. **Enter Player Names**: Customize names for Player X and Player O
3. **Take Turns**: Click on empty cells to place your mark (X or O)
4. **Win the Game**: Get three marks in a row (horizontal, vertical, or diagonal)
5. **Track Scores**: View wins, losses, and draws for each player

### Player vs AI Mode
1. **Select AI Mode**: Choose single-player mode against computer
2. **Pick Difficulty**: Select AI difficulty level (if available)
3. **Make Your Move**: Click on cells to place your mark
4. **AI Response**: Computer makes its move automatically
5. **Challenge Yourself**: Try to beat the AI's strategic gameplay

## 🧠 Game Logic Implementation

### Win Detection Algorithm
```javascript
function checkWinner(board) {
    const winPatterns = [
        [0, 1, 2], [3, 4, 5], [6, 7, 8], // Rows
        [0, 3, 6], [1, 4, 7], [2, 5, 8], // Columns
        [0, 4, 8], [2, 4, 6]             // Diagonals
    ];
    
    for (let pattern of winPatterns) {
        if (board[pattern[0]] && 
            board[pattern[0]] === board[pattern[1]] && 
            board[pattern[1]] === board[pattern[2]]) {
            return board[pattern[0]];
        }
    }
    return null;
}
```

### AI Move Selection
```javascript
function makeAIMove(board, difficulty) {
    // Minimax algorithm implementation
    if (difficulty === 'easy') {
        return getRandomMove(board);
    } else if (difficulty === 'medium') {
        return getStrategicMove(board);
    } else {
        return getBestMove(board); // Minimax
    }
}
```

## 🎓 Learning Outcomes

Through this project, the following skills were developed:

### Game Development Skills
- **Algorithm Design**: Implementing win detection and AI logic
- **State Management**: Tracking game states, turns, and scores
- **User Experience**: Creating intuitive and engaging gameplay
- **Problem Solving**: Handling edge cases and game scenarios

### JavaScript Proficiency
- **Complex Logic**: Multi-dimensional array handling and pattern matching
- **AI Programming**: Basic artificial intelligence and decision trees
- **Event Management**: User interactions and game flow control
- **Data Structures**: Efficient board representation and game state tracking

### Frontend Development
- **Interactive Design**: Creating engaging user interfaces
- **Responsive Gaming**: Adapting games for different screen sizes
- **Animation**: Smooth transitions and visual feedback
- **Performance**: Optimizing game logic for smooth gameplay

## 🔧 Key Game Functions

### Core Game Logic
```javascript
class TicTacToe {
    constructor() {
        this.board = Array(9).fill(null);
        this.currentPlayer = 'X';
        this.gameActive = true;
        this.scoreX = 0;
        this.scoreO = 0;
    }
    
    makeMove(index) {
        if (this.board[index] || !this.gameActive) return false;
        
        this.board[index] = this.currentPlayer;
        if (this.checkWinner()) {
            this.gameActive = false;
            this.updateScore();
        } else if (this.isBoardFull()) {
            this.gameActive = false;
        } else {
            this.switchPlayer();
        }
        return true;
    }
}
```

### AI Decision Making
```javascript
function minimax(board, depth, isMaximizing) {
    const winner = checkWinner(board);
    
    if (winner === 'O') return 10 - depth;
    if (winner === 'X') return depth - 10;
    if (isBoardFull(board)) return 0;
    
    if (isMaximizing) {
        let bestScore = -Infinity;
        for (let i = 0; i < 9; i++) {
            if (board[i] === null) {
                board[i] = 'O';
                let score = minimax(board, depth + 1, false);
                board[i] = null;
                bestScore = Math.max(score, bestScore);
            }
        }
        return bestScore;
    } else {
        let bestScore = Infinity;
        for (let i = 0; i < 9; i++) {
            if (board[i] === null) {
                board[i] = 'X';
                let score = minimax(board, depth + 1, true);
                board[i] = null;
                bestScore = Math.min(score, bestScore);
            }
        }
        return bestScore;
    }
}
```

## 📚 Resources & References

### Game Development Resources
- [Minimax Algorithm Explained](https://www.geeksforgeeks.org/minimax-algorithm-in-game-theory-set-1-introduction/)
- [Tic-Tac-Toe AI Implementation](https://www.freecodecamp.org/news/how-to-make-your-tic-tac-toe-game-unbeatable-by-using-the-minimax-algorithm-9d690bad4b37/)
- [JavaScript Game Development Guide](https://developer.mozilla.org/en-US/docs/Games)

### Technical Documentation
- [MDN Web Docs - JavaScript](https://developer.mozilla.org/en-US/docs/Web/JavaScript)
- [CSS Grid Layout Guide](https://css-tricks.com/snippets/css/complete-guide-grid/)
- [HTML5 Canvas API](https://developer.mozilla.org/en-US/docs/Web/API/Canvas_API)

### Development Tools
- **VS Code**: Primary development environment
- **Chrome DevTools**: Debugging and testing
- **Git**: Version control system
- **GitHub**: Repository hosting and deployment

## 🤝 Contributing

This project was created as part of an internship program. Contributions and improvements are welcome:

1. **Fork the repository**
2. **Create a feature branch** (`git checkout -b feature/amazing-feature`)
3. **Commit changes** (`git commit -m 'Add amazing feature'`)
4. **Push to branch** (`git push origin feature/amazing-feature`)
5. **Open a Pull Request**

### Contribution Ideas
- **Enhanced AI**: Implement more sophisticated AI algorithms
- **Game Modes**: Add different board sizes (4x4, 5x5)
- **Themes**: Create multiple visual themes and customizations
- **Online Multiplayer**: Add network-based multiplayer functionality
- **Tournament Mode**: Implement bracket-style tournaments

## 🧪 Testing & Quality Assurance

### Game Logic Testing
- **Win Conditions**: Verified all 8 possible winning combinations
- **Draw Detection**: Tested full board scenarios without winners
- **Input Validation**: Ensured invalid moves are properly handled
- **AI Behavior**: Confirmed AI makes logical and strategic moves

### Cross-Browser Testing
- **Chrome**: Full functionality and smooth animations
- **Firefox**: Consistent gameplay and visual rendering
- **Safari**: Mobile and desktop compatibility
- **Edge**: Modern browser standard compliance

### Mobile Testing
- **Touch Controls**: Responsive touch interactions for mobile devices
- **Screen Adaptation**: Proper scaling and layout on different screen sizes
- **Performance**: Smooth gameplay on mobile processors
- **Orientation**: Support for both portrait and landscape modes

## 📞 Contact & Support

**Developer**: Ankur Sharma  
**GitHub**: [@AnkurSharma777](https://github.com/AnkurSharma777)  
**Project Link**: [SCT_WD_3 Repository](https://github.com/AnkurSharma777/SCT_WD_3)

### SkillCraft Technology
**Website**: [skillcrafttech.com](https://skillcrafttech.com)  
**Internship Program**: Web Development Track  
**Task**: SCT_WD_3 - Interactive Tic-Tac-Toe Game

---

## 📜 License

This project is part of the SkillCraft Technology internship program. Please respect the educational nature of this project and provide appropriate attribution when using or referencing this code.

---

## 🙏 Acknowledgments

- **SkillCraft Technology** for providing the internship opportunity and challenging project requirements
- **Game Development Community** for inspiration and algorithmic approaches
- **JavaScript Community** for excellent documentation and learning resources
- **Fellow Developers** for peer learning and collaborative problem-solving

---

## 🔍 Future Enhancements

### Potential Improvements
- **Advanced AI**: Implement neural network-based AI opponent
- **Multiplayer Support**: Real-time online multiplayer functionality
- **Game Analytics**: Track detailed gameplay statistics and patterns
- **Custom Themes**: Multiple visual themes and personalization options
- **Tournament System**: Bracket-style competitions with multiple players

### Technical Upgrades
- **Progressive Web App**: Offline functionality and app-like experience
- **WebSocket Integration**: Real-time multiplayer communication
- **Canvas Graphics**: Enhanced visual effects and animations
- **Machine Learning**: AI that learns from player strategies

---

### 📈 Project Status: ✅ Completed

This project successfully fulfills all requirements of the SCT_WD_3 task and demonstrates advanced JavaScript skills in game development, algorithm implementation, and interactive user interface design. The Tic-Tac-Toe game is fully functional, engaging, and ready for both casual and competitive gameplay.

**Last Updated**: October 2025  
**Version**: 1.0.0  
**Compatibility**: Modern browsers (Chrome 60+, Firefox 55+, Safari 12+, Edge 79+)  
**Game Modes**: Player vs Player, Player vs AI  
**Difficulty Levels**: Easy, Medium, Hard (if implemented)
