
# 🎲 Dice Game

This is a simple Dice Game built using **HTML**, **CSS**, and **JavaScript**. It simulates the rolling of two dice and announces the winner.

## 📁 Project Structure

```
DiceGameTAsk/
├── index.html          # Game layout and structure
├── styles.css          # Styling for the game
├── script.js           # Dice logic and DOM manipulation
└── images/             # Dice face images and rolling animation
```

## 📄 File Descriptions

### `index.html`
- The main structure of the web page.
- Uses semantic HTML and includes references to the stylesheet and script.
- Elements:
  - Two player dice images.
  - Heading to show the winner or draw message.

### `styles.css`
- Custom styling for the dice game page.
- Key styles:
  - Centered layout using `flexbox`.
  - Styling for dice images with shadows.
  - Font styling for headings.

### `script.js`
- JavaScript logic for random dice rolling.
- Main functionalities:

```javascript
// Generates a random number from 1 to 6
var randomNumber1 = Math.floor(Math.random() * 6) + 1;

// Updates dice image based on the random number
var randomDiceImage = "images/dice" + randomNumber1 + ".png";

// Selects the image tag and changes the src attribute
document.querySelectorAll("img")[0].setAttribute("src", randomDiceImage);
```

- Compares the two dice values to declare a winner:

```javascript
if (randomNumber1 > randomNumber2) {
  document.querySelector("h1").innerHTML = "🚩 Player 1 Wins!";
} else if (randomNumber2 > randomNumber1) {
  document.querySelector("h1").innerHTML = "Player 2 Wins! 🚩";
} else {
  document.querySelector("h1").innerHTML = "Draw!";
}
```

### `images/`
- `dice1.png` to `dice6.png`: Represent each side of a standard die.
- `diceroll.gif`: Animated gif to visually represent dice rolling (optional for animation effects).

## ✅ Features

- 🎲 Random dice outcome on page load.
- 🏁 Winner is calculated based on dice numbers.
- 💻 Fully responsive and visually clean UI.

## 🚀 How to Run Locally

1. Download or clone the repository:
   ```bash
   git clone https://github.com/yourusername/DiceGameTAsk.git
   ```
2. Open `index.html` in your preferred web browser.

> No additional setup required.

## 📸 Preview

![Rolling Dice](./images/diceroll.gif)

## 🛠 Technologies Used

- HTML5
- CSS3
- JavaScript (ES6)

## 📬 Contact

For feedback or contributions, reach out at [your.email@example.com](mailto:your.email@example.com)

## 🪪 License

Licensed under the [MIT License](LICENSE).
