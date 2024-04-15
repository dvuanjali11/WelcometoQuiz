import java.util.Scanner;

public class Quiz {
    static Scanner scanner = new Scanner(System.in);

    static void displayQuestion(String question, String[] options) {
        System.out.println(question);
        for (int i = 0; i < options.length; i++) {
            System.out.println((char)('A' + i) + ". " + options[i]);
        }
    }

    static String getUserInput() {
        return scanner.nextLine().toUpperCase();
    }

    static boolean checkAnswer(String userAnswer, String correctAnswer) {
        return userAnswer.equalsIgnoreCase(correctAnswer);
    }

    public static void main(String[] args) {
        System.out.println("Let's go!");

        String[][] javaQuestions = {
                {"What is Java?", "A programming language", "A scripting language", "An operating system"},
                {"What is a class in Java?", "A blueprint for objects", "A data type", "A method"},
                {"What is JVM?", "Java Virtual Machine", "Java Version Manager", "Java Variable Manager"},
                {"What is inheritance in Java?", "A mechanism in which one class acquires the properties and behaviors of another class", "A way to define constants", "A way to iterate through a collection"},
                {"What is the purpose of the 'static' keyword in Java?", "It allows variables and methods to be accessed without creating an instance of the class", "It makes a variable constant", "It creates dynamic variables"}
        };

        String[][] dbmsQuestions = {
                {"What does DBMS stand for?", "Database Management System", "Data Management System", "Database Modeling System"},
                {"What is an entity in DBMS?", "A thing or object in the real world that is distinguishable from other objects", "A table", "A primary key"},
                {"What is normalization in DBMS?", "Organizing the attributes and tables of a relational database to minimize redundancy", "Creating complex queries", "Adding indexes to tables"},
                {"What is a primary key?", "A unique identifier for each record in a database table", "A foreign key", "A composite key"},
                {"What is SQL?", "Structured Query Language used for managing relational databases", "Simple Query Language", "Structured Query Logic"}
        };


        String[][] dsaQuestions = {
            {"What is DSA?", "Data Structures and Algorithms", "Database standard ad algo", "Datawise Structures and Algo"},
            {"What is a linked list?", "A linear data structure where elements are stored in a sequence", "A list of linked data", "None"},
            {"What is a stack?", "A linear data structure that follows the Last In, First Out (LIFO) principle", "Which follows FIFO", "A non linear data structure"},
            {"What is a queue?", "A linear data structure that follows the First In, First Out (FIFO) principle", "Which follows LIFO", "A no linear data structure"},
            {"What is a binary search tree?", "A binary tree in which each node has at most two children, and the left child is less than the parent and the right child is greater", "A tree which has infinite nodes", "A tree in whic searching is done linearly"}
    };

        System.out.println("Choose a category: Java, DBMS, DSA");
        String category = getUserInput();

        String[][] selectedQuestions;
        switch (category.toLowerCase()) {
            case "java":
                selectedQuestions = javaQuestions;
                break;
            case "dbms":
                selectedQuestions = dbmsQuestions;
                break;
            case "dsa":
                selectedQuestions= dsaQuestions;
                break;
            default:
                System.out.println("Invalid category selected. Exiting quiz.");
                return;
        }

        int score = 0;

        for (String[] q : selectedQuestions) {
            displayQuestion(q[0], new String[]{q[1], q[2], q[3]});
            String userAnswer = getUserInput();

            if (checkAnswer(userAnswer, "A")) {
                System.out.println("Correct!");
                score++;
            } else {
                System.out.println("Incorrect! Game Over.");
                break;
            }
        }

        if (score == selectedQuestions.length) {
            System.out.println("Well done!");
        }

        System.out.println("Your total score is: " + score);
    }
}
