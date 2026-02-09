# Quiz CLI

🎓 **Quiz CLI** is an interactive command-line quiz game aimed at testing and improving programming knowledge. It supports JavaScript, Node.js fundamentals, and general programming categories, making it a fun and educational tool for developers of all levels.

## Features

💡 **Quiz CLI** is designed to deliver a tailored and interactive learning experience for all developers. Below are its standout features:

### 🕹️ Interactive Experience
- An engaging **Command-Line Interface** designed for smooth interaction.
- Easy navigation with clear prompts and user-friendly controls.

### 📚 Diverse Quiz Categories
- Choose from a variety of categories:
  - **JavaScript Basics**: For foundational understanding of JavaScript.
  - **Node.js Fundamentals**: Covering backend essentials with Node.
  - **General Programming Concepts**: Ideal for developers of any domain.

### ⚙️ Customizable Quiz Sessions
- Select the number of questions:
  - **All available questions**
  - Quick quizzes of **3 or 5 questions**
- Experience randomized question sequences for dynamic learning.

### 🧠 Insightful Feedback
- Real-time explanations for both **correct and incorrect answers**, ensuring clear understanding.
- Final scores with a detailed review of your performance.

### 📊 Performance Visualization
- A **progress bar** tracks your quiz completion in real-time.

### 🔄 Unique and Ever-Fresh
- Randomized questions ensure a different learning experience in every session.
- An excellent tool for preparing for job interviews or expanding programming proficiency.

### 🚀 Core Programming Concepts in Action
- Demonstrates modern JavaScript/Node.js practices:
  - **ES6 Modules** (import/export patterns).
  - Utilizing **async/await** and managing Promises.
  - **File system operations** for external data management.
  - Effective **user input handling** via Node's `readline` module.
  - Implements object-oriented design using **classes and objects**.
  - Showcases advanced **array and string manipulation techniques**.
  - Incorporates best practices for **error handling in Node.js applications**.

---

## Installation

1. Make sure you have [Node.js](https://nodejs.org/) (v18.0.0 or later) installed.
2. Clone this repository:
    ```bash
    git clone https://github.com/SiarheiSkrabneuski/test-app.git
    ```
3. Navigate to the project directory:
    ```bash
    cd test-app
    ```
4. Install the dependencies:
    ```bash
    npm install
    ```

---

## How to Play

1. Start the quiz by running:
    ```bash
    npm start
    ```
2. You will be greeted with a welcome banner.
3. Choose a category from the given options.
4. Decide the number of questions you'd like to answer:
   - All questions
   - 3 questions
   - 5 questions
5. Answer each question by selecting the correct option number.
6. Get feedback for each answer, including explanations for incorrect choices.
7. At the end of the quiz, review your results including any incorrect answers.

---

## Architecture and Codebase Overview

### `index.js`
- The entry point of the application.
- Handles the main application workflow, including loading questions, user interaction, and quiz execution.
- Imports and utilizes modules for user input (`src/input.js`), quiz logic (`src/quiz.js`), and terminal colors (`src/colors.js`).

### `src/colors.js`
- Provides terminal color and styling utilities using ANSI escape codes.
- Includes functions like `success`, `error`, `info`, and `highlight` for enhanced user interaction.

### `src/input.js`
- Implements user input handling using Node.js's `readline` module.
- Functions:
  - `createInterface()`: Creates a readline interface.
  - `prompt()`: Asks for user input.
  - `select()`: Offers a list of options for the user to choose from.
  - `confirm()`: Prompts a yes/no question.
  - `pressEnter()`: Waits for the user to press `Enter`.

### `src/quiz.js`
- Contains the core quiz logic and game flow in the `Quiz` class.
- Key methods:
  - `askQuestion()`: Displays questions and evaluates answers.
  - `showResults()`: Presents the final score and detailed feedback.
  - `renderProgressBar()`: Visualizes the quiz progress.

### `data/questions.json`
- Stores the categorized questions and answers in JSON format.
- Example structure:
    ```json
    {
      "categories": {
        "javascript": {
          "name": "JavaScript Basics",
          "questions": [
            {
              "question": "What keyword is used to declare a constant in JavaScript?",
              "options": ["var", "let", "const", "define"],
              "answer": 2,
              "explanation": "The 'const' keyword declares a block-scoped constant that cannot be reassigned."
            }
          ]
        }
      }
    }
    ```

---

## Key Dependencies

- **Node.js**:
  - `readline`: For user input handling.
  - `node:fs/promises`: To load questions from the JSON file.
- The project doesn't require any external dependencies.

---

## Running Tests

Execute the following command to run tests:
```bash
npm test
```
(*Note:* Implement test cases in the project's structure as needed.)

---

## Contribution Guidelines

We welcome contributions to enhance the Quiz CLI!

1. Fork this repository.
2. Create a new branch for your feature or bug fix:
    ```bash
    git checkout -b feature-name
    ```
3. Make your changes and test them.
4. Commit your changes with meaningful commit messages:
    ```bash
    git commit -m "Feature: Add new category for advanced programming concepts"
    ```
5. Push to your fork and create a pull request:
    ```bash
    git push origin feature-name
    ```

---

## License

This project is licensed under the **MIT License**. See the `LICENSE` file for details.

---

## Acknowledgments

💡 Inspired by coding quiz games to create a fun educational tool for developers!