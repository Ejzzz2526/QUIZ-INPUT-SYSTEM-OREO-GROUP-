# Quiz Management System (Java OOP Project)

## 1. Project Title
**Quiz Management System**

---

## 2. Description / Overview
This project is a simple console-based Quiz Management System written in Java. It allows the user to create a quiz, add different types of questions (Multiple Choice, True/False, and Short Answer), delete questions, view the quiz, and take the quiz. The goal of the project is to apply Object-Oriented Programming concepts while building a functional tool that can be used for practice quizzes or small exercises.

---

## 3. OOP Concepts Applied

### a. Abstraction
The project uses an abstract class `QuizItem` which represents a general quiz question. It contains the common attributes and abstract methods that all question types must implement.

### b. Inheritance
`MultipleChoiceQuestion`, `TrueFalseQuestion`, and `ShortAnswerQuestion` all inherit from the `QuizItem` abstract class. Each subclass provides its own version of displaying and checking answers.

### c. Polymorphism
The `Quiz` and `QuizManager` classes work with the parent type `QuizItem`, allowing different question types to be handled through the same interface. Methods such as `displayQuestion()` and `checkAnswer()` behave differently depending on the actual object.

### d. Encapsulation
Attributes across classes are private, and getters/setters are used when needed. Inputs are handled safely (e.g., `safeIntInput`, `safeCharInput`) to avoid invalid data.

### e. Interface Implementation
The `Scorable` interface defines scoring-related behavior. The `Quiz` class implements this interface to calculate total points and possible points.

---

## 4. Program Structure

### Main Classes
- **QuizItem (abstract class)**  
  Base class for all question types.

- **MultipleChoiceQuestion**  
  Subclass for 4-option multiple-choice questions.

- **TrueFalseQuestion**  
  Handles True/False type questions.

- **ShortAnswerQuestion**  
  Accepts exact match and alternative textual answers.

- **Quiz**  
  Holds the quiz title, questions, and scoring.

- **QuizManager**  
  Handles the menu system, user input, and overall program flow.

- **QuizSystem (main class)**  
  Contains the method that starts the program.

### Simple Text-Based Diagram

