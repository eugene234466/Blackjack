# 🎰 Blackjack Game

A fully interactive, browser-based Blackjack game with visual playing cards, betting system, and casino-style interface. Built with vanilla JavaScript, HTML5, and CSS3.

![Blackjack Game](https://img.shields.io/badge/Game-Blackjack-gold)
![JavaScript](https://img.shields.io/badge/JavaScript-ES6-yellow)
![HTML5](https://img.shields.io/badge/HTML-5-orange)
![CSS3](https://img.shields.io/badge/CSS-3-blue)

## 🎮 Features

- **🎴 Visual Playing Cards** - Animated card dealing with proper suits (♠ ♥ ♦ ♣)
- **💰 Betting System** - Place bets ranging from $10 to ALL IN
- **🎲 Classic Blackjack Rules** - Hit, Stand, and aim for 21
- **💎 Casino-Style UI** - Professional gradient design with glowing buttons
- **📊 Chip Management** - Track your winnings and losses in real-time
- **🎯 Win Conditions** - Blackjack pays 2:1, bust detection, and smart stand logic
- **♻️ Reset Function** - Start new rounds and restore chips when broke

## 🚀 Demo

[Live Demo](#) <!-- Add your GitHub Pages link here -->

## 📸 Screenshots

```
[Add screenshots of your game here]
```

## 🎯 How to Play

1. **Place Your Bet**: Choose from $10, $25, $50, $100, or go ALL IN
2. **Start Game**: Click "START GAME" to receive your initial two cards
3. **Make Your Move**:
   - **HIT**: Draw another card (risky if close to 21)
   - **STAND**: Keep your current hand (best when you have 17-20)
4. **Win or Lose**:
   - Get exactly **21 = BLACKJACK!** 🎉
   - Go over **21 = BUST** 💥
   - Stand on **17-20 = WIN** ✅
   - Stand on **<17 = LOSE** ❌

## 🛠️ Installation & Setup

### Clone the Repository
```bash
git clone https://github.com/eugene234466/blackjack-game.git
cd blackjack-game
```

### Run Locally
Simply open `index.html` in your web browser:
```bash
open index.html
# or
double-click index.html
```

No build tools or dependencies required! Pure vanilla JavaScript.

## 📁 Project Structure

```
blackjack-game/
│
├── index.html          # Main HTML file with embedded CSS and JavaScript
├── README.md           # This file
└── screenshots/        # Game screenshots (optional)
```

## 🎲 Game Logic

### Card Values
- **Number cards (2-10)**: Face value
- **Face cards (J, Q, K)**: Worth 10
- **Ace (A)**: Worth 11

### Betting System
- Starting chips: **$145**
- Bet before each round
- Winnings: **2x your bet**
- Lose your bet if you bust or stand too low

### Win Conditions
1. **Blackjack (21)**: Instant win with 2x payout
2. **Stand (17-20)**: Beat the dealer and win 2x
3. **Bust (>21)**: Automatic loss

## 💻 Technologies Used

- **HTML5** - Structure and layout
- **CSS3** - Styling, animations, and responsive design
- **JavaScript (ES6)** - Game logic and interactivity

## 🎨 Key Features Implementation

### Animated Card Dealing
```javascript
@keyframes dealCard {
    from {
        transform: translateY(-100px) rotate(10deg);
        opacity: 0;
    }
    to {
        transform: translateY(0) rotate(0);
        opacity: 1;
    }
}
```

### Random Card Generation
```javascript
function getRandomCard() {
    let random = Math.floor(Math.random() * 13) + 1
    let suit = suits[Math.floor(Math.random() * suits.length)]
    // Returns card with value, display, and suit
}
```

### Betting Validation
```javascript
function placeBet(amount) {
    if (amount > player.chips) {
        // Not enough chips!
        return
    }
    bet = amount
    player.chips -= bet
}
```

## 🎯 Future Enhancements

- [ ] Add dealer's hand and proper Blackjack rules
- [ ] Implement card splitting
- [ ] Add double down option
- [ ] Create leaderboard system
- [ ] Add sound effects
- [ ] Mobile responsive improvements
- [ ] Multiple deck simulation
- [ ] Insurance betting option

## 🤝 Contributing

Contributions are welcome! Feel free to submit issues and pull requests.

1. Fork the repository
2. Create your feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

## 📝 License

This project is open source and available under the [MIT License](LICENSE).

## 👨‍💻 Author

**Eugene Yarney**
- GitHub: [@eugene234466](https://github.com/eugene234466)
- Email: eugeneyarney5@gmail.com
- Phone: 0506798129

## 🙏 Acknowledgments

- Card suit symbols (♠ ♥ ♦ ♣) from Unicode
- Inspired by classic casino Blackjack
- Built as a learning project to master JavaScript fundamentals

## 📊 Game Statistics

- **Lines of Code**: ~400+
- **Game States**: 5 (Betting, Playing, Won, Lost, Reset)
- **Card Combinations**: 52 possible cards
- **Betting Options**: 5 quick-bet buttons

---

### ⭐ If you enjoyed this project, please give it a star!

**Made with ❤️ and JavaScript**