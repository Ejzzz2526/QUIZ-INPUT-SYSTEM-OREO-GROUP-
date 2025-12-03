# Quiz Management System

## 1. Project Title

**Quiz Management System (Java OOP Console App)**

## 2. Description / Overview

The **Quiz Management System** is a Java console-based application that
allows users to create, manage, and take quizzes. It supports multiple
question types (Multiple Choice, True/False, and Short Answer) and
awards points for correct answers. The program demonstrates
Object-Oriented Programming principles and provides an interactive menu
for creating quizzes, adding/removing questions, viewing quiz content,
and taking the full quiz.

## 3. OOP Concepts Applied

### a. Abstraction

-   The `QuizItem` abstract class defines a general structure for all
    quiz questions.
-   Subclasses (**MultipleChoiceQuestion**, **TrueFalseQuestion**,
    **ShortAnswerQuestion**) provide concrete implementations.

### b. Inheritance

-   All question types inherit from the abstract `QuizItem`.
-   Common properties (question text, points) and methods
    (getters/setters) are reused.

### c. Polymorphism

-   `displayQuestion()`, `checkAnswer()`, and `getCorrectAnswer()` are
    overridden in each subclass.
-   The program treats all question types as `QuizItem` objects during
    quiz operations.

### d. Encapsulation

-   Private attributes (`questionText`, `points`, `choices`, etc.)
    protect data.
-   Access is controlled through public getters, setters, and
    constructors.

### e. Interface Implementation

-   The `Scorable` interface defines scoring requirements.
-   `Quiz` implements `Scorable` to calculate earned and total points.

## 4. Program Structure

### Main Classes and Their Roles

  ---------------------------------------------------------------------------
  Class                        Description
  ---------------------------- ----------------------------------------------
  **QuizItem (abstract)**      Base class for all question types. Defines
                               shared fields and abstract methods.

  **MultipleChoiceQuestion**   Represents a question with 4 choices (a--d).

  **TrueFalseQuestion**        Represents a question with True/False choices.

  **ShortAnswerQuestion**      Accepts one or many correct acceptable
                               answers.

  **Quiz**                     Stores quiz title, list of questions, scoring
                               functions, and question management.

  **QuizManager**              Handles user input, menu navigation, quiz
                               creation, and quiz-taking workflow.

  **QuizSystem (main)**        Runs the program using `QuizManager.run()`.
  ---------------------------------------------------------------------------

### Text-Based Diagram

                   QuizItem (abstract)
              /              |              \
    MultipleChoice      TrueFalse        ShortAnswer
           \                 |                /
                        Quiz  <--- implements Scorable
                           |
                     QuizManager
                           |
                      QuizSystem (main)

## 5. How to Run the Program

### A. Compile

Open terminal or command prompt inside the folder where the `.java`
files are located:

    javac QuizSystem.java

### B. Run

    java QuizSystem

## 6. Sample Output

### Example (Taking a Quiz)

    Question 1:
    What is the capital of France?
    a: Paris
    b: Rome
    c: Berlin
    d: Madrid
    Your answer (a/b/c/d): a
    Correct! +5 points

### Example (Main Menu)

    === QUIZ MANAGEMENT SYSTEM ===
    1. Create New Quiz
    2. Add Questions
    3. Delete Question
    4. View Quiz
    5. Take Quiz
    6. Clear Quiz
    0. Exit
    Choose option:

## 7. Author and Acknowledgement

**Author:** Nino Cabrera\
**Acknowledgement:** Special thanks to our instructor for guiding us
through OOP concepts and implementation.

## 8. Other Sections

### a. Future Enhancements

-   Save and load quizzes from a file\
-   Randomize question order\
-   Timer functionality\
-   GUI version using JavaFX\
-   Export results to text/CSV

### b. References

-   Oracle Java Documentation\
-   OOP course materials\
-   StackOverflow
