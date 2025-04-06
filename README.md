[![Review Assignment Due Date](https://classroom.github.com/assets/deadline-readme-button-22041afd0340ce965d47ae6ef1cefeee28c7c493a6346c4f15d667ab976d596c.svg)](https://classroom.github.com/a/MMj2nZMu)

# Rsearch and Reflection Journal

Research and Reflection Journal for DGL 104 course

# WEEK 8:

### CLASS NOTE:

- Developers must understand user needs to create useful apps, but they are often not the target end-users. To bridge this gap, design-based methods like user stories help identify project requirements and develop functional user requirements. A user story is a short statement from the user’s perspective, typically starting with “As a user…,” describing expected software behavior in a specific context. These stories enhance developer empathy, clarify feature specifications, and can be refined through user consultation, such as focus groups.

# Week 8 - Activity Checklist #7

##OBJECTIVE
To provide you with a tool to track your progress in completing required activities throughout the semester.

##WHAT YOU'RE GOING TO DO:

- Every time you do activity work (i.e. Google CodeLabs) for this class:
- Open up your Activity Checklist.
- Record the time you start the activity.
- Write down any questions you have along the way.
- Record the time you finish the activity.
- Fill in other cells as appropriate.

## SUGGESTIONS AND STRATEGIES:

> Do this every time you do assigned work - it's going to be waaaay easier keeping up that way.
> Be honest! Filling this out honestly will give you a meaningful record for your self-evaluation.
> If you ever have unanswered questions left over after finishing an activity, or a unit, post them on Slack so that we can discuss about it in the following class - there is a good chance someone has found an answer, or would be willing to help you find it.

## SUBMISSION GUIDELINES:

- Use the following GitHub Classroom repo to write your code and push it in the repository: [Link](https://classroom.github.com/a/zL18pvUo)
- In the GitHub README.md file, write down what you have learned in this week and write down the accomplishments and some challenges that you faced in the process of doing the weekly activity. If you don't know how to write in markdown language in GitHub, please refer to this [link](https://docs.github.com/en/get-started/writing-on-github/getting-started-with-writing-and-formatting-on-github/basic-writing-and-formatting-syntax).
- Use the following template as an example to create your own activity checklist: [Activity Checklist Template](https://docs.google.com/spreadsheets/d/1jTBIJfgDkYe-HZrR8PKGQ__ljNAOs3v73gf003IY3y0/edit?usp=sharing)
- You need to upload this template as an excel or PDF by filling out with your information in the Brightspace assignment submission.

# Week 8 - App Development and Programming Languages

## Table of Contents
- [Key Concepts from Class](#key-concepts-from-class)
- [Activities for Week 8](#activities-for-week-8)
  - [Research a New Language: Haskell](#research-a-new-language-haskell)
  - [Write a User Story for Spotify's Offline Mode](#write-a-user-story-for-spotifys-offline-mode)
  - [Choose a Language for App Development](#choose-a-language-for-app-development)
- [Reflections and Questions](#reflections-and-questions)

---

## Key Concepts from Class

### Multiple Activities and Intents
- **Explicit Intent**: Used to navigate to a specific activity in your app or another app.
- **Implicit Intent**: Used for general actions (e.g., sending an email) where any matching app can handle the request.

```java
// Create an explicit intent to navigate to AnotherActivity
Intent intent = new Intent(CurrentActivity.this, AnotherActivity.class);
startActivity(intent);
```

### App Bar, Navigation Drawer, and Menus
- **App Bar**: Displays navigation options and controls.
- **Navigation Drawer**: A slide-out menu for navigation.
- **Menus**: Defined in XML, allowing users to interact with different features.
```<!-- activity_main.xml: App Bar Layout -->
<androidx.appcompat.widget.Toolbar
    android:id="@+id/toolbar"
    android:layout_width="match_parent"
    android:layout_height="?attr/actionBarSize"
    android:background="?attr/colorPrimary"
    android:elevation="4dp"/>RA_TEXT, "Message Body");
startActivity(intent);
```
```// MainActivity.java: Set up the App Bar
Toolbar toolbar = findViewById(R.id.toolbar);
setSupportActionBar(toolbar);
getSupportActionBar().setTitle("My App");
```

### Navigation in an App
- **Navigation Component**: A framework for managing navigation in Android apps.
  - **Key Parts**:
    - **Navigation Graph**: Defines app navigation paths.
    - **NavHost**: Hosts fragments for navigation.
    - **NavController**: Manages navigation actions.

```// MainActivity.java: Setting up Navigation Drawer
DrawerLayout drawerLayout = findViewById(R.id.drawer_layout);
NavigationView navigationView = findViewById(R.id.nav_view);

ActionBarDrawerToggle toggle = new ActionBarDrawerToggle(
    this, drawerLayout, toolbar, R.string.navigation_drawer_open, R.string.navigation_drawer_close);
drawerLayout.addDrawerListener(toggle);
toggle.syncState();

// Handle menu item clicks
navigationView.setNavigationItemSelectedListener(menuItem -> {
    switch (menuItem.getItemId()) {
        case R.id.nav_home:
            // Handle home click
            return true;
        case R.id.nav_settings:
            // Handle settings click
            return true;
    }
    return false;
});
```

### Navigation UI
- **Menus**: Can be linked with NavController for navigation.
- **Navigation Drawer & Bottom Navigation**: Used for structuring app navigation.
- **Back Stack Management**: Maintains navigation history for proper back navigation.

---

## Activities for Week 8

### Research a New Language: Haskell

#### Overview of Haskell
Haskell is a purely functional programming language known for its strong static typing and lazy evaluation. It emphasizes immutability, making it ideal for writing concise, reliable, and mathematically precise code (Peyton-Jones, 2003). Haskell’s type system helps detect errors at compile time, improving application safety and reducing runtime exceptions.

#### Applications of Haskell
- **Academic Research**: Haskell is widely used in universities to teach functional programming principles and explore theoretical computer science (Peyton-Jones, 2003).
- **Finance and Banking**: Haskell is employed in the financial industry for developing robust systems, such as those used by Standard Chartered for complex financial calculations (Gonzalez, 2012).
- **Web Development**: Frameworks like Yesod and Servant leverage Haskell’s type system to create scalable and secure web applications (Jaskelioff et al., 2015).
- **Data Analysis**: Libraries like Data.Vector and Data.Text provide efficient data processing capabilities, making Haskell suitable for large datasets (Bird, 2012).
- **Compiler Development**: Haskell is used to build compilers and language tools due to its strong support for pattern matching and abstract syntax trees (Gonzalez, 2012).

#### Helpful Resources
- **[Learn You a Haskell for Great Good!](http://learnyouahaskell.com)**: A beginner-friendly book introducing Haskell concepts in an engaging way.
- **[Haskell.org](https://www.haskell.org)**: Official documentation and tutorials for all levels.
- **[Hackage](https://hackage.haskell.org)**: A collection of Haskell libraries and packages.

---

### Write a User Story for Spotify's Offline Mode

#### General User Story:
"As a Spotify user, I want to be able to download songs so that I can listen to them offline without using mobile data, ensuring uninterrupted playback when I have no internet connection."

#### Specific User Stories:
1. **Downloading Songs for Offline Playback**  
   - **Single Song Download**: "As a user, I can download an individual song by tapping a download button next to it so that I can listen to it offline."
   - **Playlist and Album Download**: "As a user, I can download an entire playlist or album with a single tap."
   - **Download Progress**: "As a user, I can see a progress indicator for each song, playlist, or album while it is downloading."

2. **Managing Offline Downloads**  
   - **Viewing Downloaded Songs**: "As a user, I can access a dedicated ‘Downloaded’ section in my library."
   - **Removing Downloads**: "As a user, I can remove a downloaded song by tapping an option in the menu."
   - **Automatic Download Options**: "As a user, I can enable automatic downloads for my liked songs or playlists."

3. **Offline Mode and Playback**  
   - **Enabling Offline Mode**: "As a user, I can enable 'Offline Mode' to prevent Spotify from using mobile data."
   - **Error Handling**: "As a user, I am notified when I try to play a song that isn’t downloaded."
   - **Playback Features in Offline Mode**: "As a user, I can use shuffle, repeat, and queue features while listening offline."

---

### Choose a Language for Our App Development Project

#### Chosen Language: PHP

For this coding project, I have chosen **PHP** as the primary programming language. PHP is widely used in web development, especially for server-side scripting, making it an excellent choice for building a web-based task management system.

#### Why PHP?
- **Web-Focused Development**: PHP integrates seamlessly with front-end technologies like HTML, JavaScript, and CSS, which is ideal for building an interactive task management system.
- **Open-Source Ecosystem**: PHP has a rich ecosystem of frameworks (Laravel, Symfony, CodeIgniter), enabling rapid development and contributing to open-source communities.
- **Database Connectivity**: PHP works well with MySQL for efficient data storage and retrieval in web applications.
- **Security and Scalability**: PHP provides built-in security features like authentication and session management, which are essential for multi-user systems.

#### Aligning with Open Source Contributions
I plan to contribute to PHP-based open-source projects by:
- Developing features for task management frameworks like Laravel.
- Contributing plugins or integrations for existing PHP projects.
- Sharing improvements through my task manager project (e.g., reusable components).

#### Learning Opportunities
Through this project, I aim to:
- Improve my backend development skills in PHP.
- Gain experience in MySQL database management.
- Learn about RESTful API development.
- Enhance web app security practices.

---

## Reflections and Questions

1. **What is one interesting thing you've learned from researching programming languages?**
   The most interesting takeaway was how specific languages are optimized for certain tasks. For example, PHP excels in web development, while TypeScript is preferred for scalable frontend applications, and Kotlin is highly suitable for Android development (Brady, 2021).

2. **What other languages might you consider for DGL 104?**
   - **JavaScript (Node.js)**: For backend development and real-time features.
   - **Python**: For simplicity and integration with AI-driven features.
   - **TypeScript**: For enhancing maintainability in large-scale frontend applications.

3. **What did you find most interesting on GitHub?**
   I was surprised by the number of PHP projects using **Docker** and **microservices** for better scalability, and the level of community involvement and best practices (e.g., CI/CD pipelines).

4. **What similarities across repositories did you observe?**
   - Most projects follow **MVC architecture**.
   - **RESTful API development** is prevalent.
   - Repositories are well-documented and emphasize **security practices** like JWT and SQL injection prevention.

---

## Citations
- Bird, R. (2012). *Introduction to Haskell*. Cambridge University Press.
- Brady, E. (2021). *Programming Languages in Web Development*. Pearson Education.
- Gonzalez, L. (2012). *Haskell for Financial Systems*. Springer.
- Jaskelioff, M., et al. (2015). *Building Scalable Web Apps with Haskell*. Wiley.
- Peyton-Jones, S. (2003). *Haskell 98 Language and Libraries*. Cambridge University Press.

---

# Week 9 - Design Patterns in Software Development

## Overview
Design patterns are reusable coding solutions to common software design problems, designed to improve maintainability, readability, and overall software architecture. These patterns act as flexible frameworks or blueprints that can be tailored to specific programming languages and project needs. While design patterns are not rigid rules, they provide recognizable structures that make collaboration and long-term code maintenance easier (Gamma et al., 1994).

### Design Patterns
Design patterns can be categorized into three main classifications based on their purpose:

1. **Creational Patterns**: These patterns focus on object creation mechanisms, trying to create objects in a way that enhances flexibility and reuse. Examples include the Singleton, Factory, and Abstract Factory patterns.
   
2. **Structural Patterns**: These patterns deal with object composition, helping to design large structures more effectively. The Adapter and Composite patterns are key examples.
   
3. **Behavioral Patterns**: These patterns focus on how objects interact and communicate with each other. The Observer and Strategy patterns are among the most commonly used in this category.

## Inheritance vs. Composition

In object-oriented programming (OOP), inheritance allows one class to inherit the behavior and data of another. However, over-relying on inheritance chains can lead to brittle code and hinder maintainability, making the system more difficult to extend and modify. This is a classic example of the **fragile base class problem**, where changes in a parent class may unintentionally break subclasses (Meyer, 1997).

### Problems with Inheritance Chains:
- **Tight Coupling**: Inheritance chains introduce tight coupling, making it difficult to alter or extend parts of the system without affecting others.
- **Brittleness**: Since subclasses depend on the parent class, changes in the parent class may inadvertently break the behavior of subclasses.
- **Rigidity**: The structure of inheritance chains can make it harder to adapt to new requirements without modifying the hierarchy, leading to over-engineered solutions.

### Object Composition: A More Flexible Alternative
Object composition offers a more flexible and maintainable approach compared to inheritance chains. With composition, objects can delegate behavior and data to other objects, creating complex structures that better suit the system's needs. Composition is commonly associated with **functional programming** and **higher-order functions**, where smaller, reusable functions are combined to form more complex operations (Mann, 2019).

### Example: Using Composition Over Inheritance
```java
// Example of Object Composition in Java

// Car class using composition to delegate responsibilities to other objects
public class Car {
    private Engine engine;
    private Transmission transmission;

    public Car(Engine engine, Transmission transmission) {
        this.engine = engine;
        this.transmission = transmission;
    }

    public void drive() {
        engine.start();
        transmission.shift();
    }
}

class Engine {
    public void start() {
        System.out.println("Engine started");
    }
}

class Transmission {
    public void shift() {
        System.out.println("Transmission shifted");
    }
}
```

## Design Pattern Focus: The Observer Pattern
The Observer pattern is a behavioral design pattern that defines a one-to-many dependency between objects, where one object (subject) maintains a list of dependents (observers) that need to be notified of changes to the subject’s state. It’s often used to implement distributed event-handling systems, in which one object (subject) notifies other objects (observers) when a change occurs.

**Key Responsibilities of the Observer Pattern:**

- Subject: Maintains a list of observers and notifies them when its state changes.

- Observer: Registers with the subject and reacts to state changes.

**Characteristics:**
- One-to-many notifications: A single subject can notify multiple observers about a state change.

- Loose coupling: The subject does not need to know the specifics of the observers, allowing for greater flexibility and extensibility.

```import java.util.ArrayList;
import java.util.List;

// Subject
class NewsAgency {
    private List<Observer> observers = new ArrayList<>();
    private String news;

    public void addObserver(Observer observer) {
        observers.add(observer);
    }

    public void removeObserver(Observer observer) {
        observers.remove(observer);
    }

    public void setNews(String news) {
        this.news = news;
        notifyObservers();
    }

    private void notifyObservers() {
        for (Observer observer : observers) {
            observer.update(news);
        }
    }
}

// Observer
interface Observer {
    void update(String news);
}

class NewsChannel implements Observer {
    private String news;

    @Override
    public void update(String news) {
        this.news = news;
        System.out.println("News Channel updated: " + news);
    }
}

public class ObserverPatternExample {
    public static void main(String[] args) {
        NewsAgency agency = new NewsAgency();
        NewsChannel channel1 = new NewsChannel();
        NewsChannel channel2 = new NewsChannel();

        agency.addObserver(channel1);
        agency.addObserver(channel2);

        agency.setNews("Breaking News: Observer pattern in action!");
    }
}

```
## In this example:

- NewsAgency is the subject that notifies observers about the news.

- NewsChannel is the observer that reacts when it receives an update.

**Benefits of the Observer Pattern:**

- Loose Coupling: Subjects and observers are decoupled; the subject does not need to know the details of its observers.

- Scalability: Adding or removing observers is easy and does not require changes to the subject.




# WEEK 10:

# MV\* Architectural Patterns

MV\* (Model-View-Star) architectural patterns are fundamental to designing clean and maintainable user interfaces. These patterns focus on separating UI components from data models, enhancing code organization, testability, and overall reliability.

## 📌 What is MV\*?

**MV\*** refers to a family of UI architecture patterns that center around two main components:

- **Model**: Manages application data and business logic.
- **View**: Handles the user interface and presentation layer.

The asterisk (\*) represents the varying components used to handle interactions and logic, such as **Controllers** or **ViewModels**.

---

## Common MV\* Patterns

### Model-View-Controller (MVC)

- **Origin**: Introduced in the 1970s with Smalltalk.
- **Popularized by**: iOS development.
- **Structure**:
  - **Model** – Manages data and business rules.
  - **View** – Displays UI components.
  - **Controller** – Acts as the bridge between model and view.
- **Advantages**:
  - Clear separation of concerns.
  - Simplified maintenance and scaling.

---

### Model-View-ViewModel (MVVM)

- **Used in**: Modern frameworks like **SwiftUI** and **Jetpack Compose**.
- **Structure**:
  - **Model** – Represents application data.
  - **View** – Displays UI and listens for updates.
  - **ViewModel** – Prepares and transforms data for the view, manages UI logic.
- **Advantages**:
  - Reactive programming support.
  - Encourages testable and modular code.

---

## Benefits of MV\* Architecture

- **Separation of Concerns**: Cleanly separates data, UI, and logic layers.
- **Improved Testability**: Business logic can be unit tested independently.
- **Scalability**: Encourages modular codebases that are easier to scale.
- **Better Maintainability**: Organized project structure improves readability and ease of updates.

---

MV\* patterns are a powerful intersection of software architecture and design, especially suited for modern UI development. They help build reliable, maintainable, and scalable applications by clearly defining responsibilities across components.

### Components

- **Model**  
  Represents the data and business logic of the application.

  - Data should be stored in a compatible format (local or remote).
  - Proper modeling using OOP (Object-Oriented Programming) classes improves accessibility and application functionality.

- **View**  
  The UI component that presents data to the user.

  - Reflects the current state of the model.
  - Does **not** store data itself or maintain state — it simply mirrors the model.

- **Controller**  
  Acts as the intermediary between the Model and the View.
  - Handles user input and updates the model or view accordingly.
  - Central to the MVC architecture, ensuring each component interacts without being tightly coupled.

### What is Forking?

- **Forking** a repository creates a personal copy of someone else’s repository on your GitHub account.
- It allows you to:
  - Develop features or fix bugs independently.
  - Experiment without affecting the original (upstream) project.
  - Submit **pull requests** to propose changes to the original repository.
- Your fork remains connected to the original, enabling you to **sync changes** as updates occur upstream.

---

### What is Cloning?

- **Cloning** is the process of downloading a repository (your fork or the original) to your local machine.
- This allows you to:
  - Work offline.
  - Use local development tools and editors.
  - Manage code using Git and GitHub Desktop (or command-line Git).

---

### How to Contribute Effectively

1. **Fork the Repository**

   - Navigate to the original repository on GitHub.
   - Click the **"Fork"** button to create a copy under your GitHub account.

2. **Clone the Fork**

   - Open GitHub Desktop or use the Git CLI.
   - Clone your fork to work on it locally:
     ```bash
     git clone https://github.com/your-username/forked-repo.git
     ```

3. **Keep Your Branch Up to Date**

   - Sync your fork with the original repository to avoid conflicts.
   - Fetch and merge changes from the upstream repository regularly.

4. **Create a New Branch for Each Feature**

   - Avoid working directly on the `main` or `master` branch.
   - Example:
     ```bash
     git checkout -b feature/my-new-feature
     ```

5. **Push and Create a Pull Request**
   - After committing your changes, push to your fork and create a pull request to the original repository.

---

By following this workflow, you can collaborate efficiently, manage your code effectively, and contribute to shared projects with confidence.
# Week 11 - Object-Oriented Programming (OOP) and SOLID Principles

## Overview
Object-Oriented Programming (OOP) is a programming paradigm based on the concept of **objects**, which encapsulate both **data** and **code**. Data is stored in fields (attributes), and the code is stored as procedures (methods) that manipulate that data. This approach promotes modularity, reusability, and maintainability in software development.

### Key OOP Terms:
- **Classes**: Templates or blueprints for creating objects, defining initial attributes and methods.
- **Encapsulation**: The practice of keeping fields (attributes) private and providing access to them via public methods, ensuring data integrity.
- **Inheritance**: The mechanism by which one class can inherit the attributes and methods of another class, promoting code reuse.
- **Polymorphism**: The ability of different classes to provide a method with the same name but different implementations.

### Well-Known Programming Paradigms:
1. **Imperative Programming (OOP)**: Focuses on statements that describe the step-by-step process of how a program should accomplish tasks.
2. **Declarative Programming (Functional)**: Focuses on what a program should accomplish without detailing how it should be executed. Functions are first-class citizens, and side effects are minimized.
3. **Prototypal Programming (part of Imperative and related to OOP)**: Uses prototype objects instead of classes. Shared behavior is delegated through the prototype chain rather than inheritance.

## SOLID Principles in OOP

The **SOLID** principles are a set of five design principles that aim to improve the structure and maintainability of object-oriented software. Initially proposed in 2000, they have evolved over time to address contemporary software design concerns (Martin, 2000).

### 1. **Single Responsibility Principle (SRP)**
- **Definition**: A class should have only one reason to change, meaning it should have only one job or responsibility.
- **Example**: In a company, think of each role (e.g., HR, Finance, IT). Each role should have narrowly defined responsibilities, and those responsibilities should not overlap.

**Example Code** (Violating SRP):
```java
// This class violates the SRP because it manages both user data and logging.
class User {
    public void saveUser() {
        // Code to save user data
    }

    public void logUserAction() {
        // Code to log user actions
    }
}
```

### 2. Open-Closed Principle (OCP)
- Definition: Software entities (classes, modules, functions) should be open for extension but closed for modification. This means you should be able to add new functionality without modifying existing code.

- Example Consideration: If the code you’ve inherited is modified, your extension might be impacted, leading to potential issues.

**Example Code (Violating OCP):**
```
// This violates OCP as adding a new shape type requires modifying the existing class.
class AreaCalculator {
    public double calculateArea(Rectangle rectangle) {
        return rectangle.getWidth() * rectangle.getHeight();
    }

    public double calculateArea(Circle circle) {
        return Math.PI * circle.getRadius() * circle.getRadius();
    }
}
```

**Refactored Code (Adhering to OCP):**
```
interface Shape {
    double calculateArea();
}

class Rectangle implements Shape {
    private double width, height;

    @Override
    public double calculateArea() {
        return width * height;
    }
}

class Circle implements Shape {
    private double radius;

    @Override
    public double calculateArea() {
        return Math.PI * radius * radius;
    }
}

class AreaCalculator {
    public double calculateArea(Shape shape) {
        return shape.calculateArea();
    }
}
```
### 3. Liskov Substitution Principle (LSP)

- Definition: Objects of a superclass should be replaceable with objects of a subclass without affecting the correctness of the program.

- Example: If a subclass does not fulfill the contract of the superclass (e.g., by modifying behavior unexpectedly), it violates LSP.

### 4. Interface Segregation Principle (ISP)

- Definition: Clients should not be forced to depend on interfaces they do not use. Rather than one large interface, you should break it down into smaller, more specific ones.

**Example Code:**

```// Violating ISP: A large interface that forces implementations to use methods they don't need
interface Worker {
    void work();
    void eat();
}

class HumanWorker implements Worker {
    public void work() {
        // Working
    }

    public void eat() {
        // Eating
    }
}

class RobotWorker implements Worker {
    public void work() {
        // Working
    }

    // Robot doesn't eat, violating ISP
    public void eat() {
        throw new UnsupportedOperationException();
    }
}
```

**Refactored Code (Adhering to ISP):**

```interface Workable {
    void work();
}

interface Eatable {
    void eat();
}

class HumanWorker implements Workable, Eatable {
    public void work() {
        // Working
    }

    public void eat() {
        // Eating
    }
}

class RobotWorker implements Workable {
    public void work() {
        // Working
    }
}
```

### 5. Dependency Inversion Principle (DIP)

- Definition: High-level modules should not depend on low-level modules; both should depend on abstractions. Furthermore, abstractions should not depend on details; details should depend on abstractions.

**Example Code:**

```// Violating DIP: The high-level class directly depends on the low-level implementation
class LightBulb {
    public void turnOn() {
        System.out.println("Light Bulb turned on");
    }
    public void turnOff() {
        System.out.println("Light Bulb turned off");
    }
}

class Switch {
    private LightBulb bulb;

    public Switch(LightBulb bulb) {
        this.bulb = bulb;
    }

    public void operate() {
        // Direct dependency on LightBulb, violates DIP
        bulb.turnOn();
    }
}
```
**Refactored Code (Adhering to DIP):**

```
interface Switchable {
    void turnOn();
    void turnOff();
}

class LightBulb implements Switchable {
    public void turnOn() {
        System.out.println("Light Bulb turned on");
    }
    public void turnOff() {
        System.out.println("Light Bulb turned off");
    }
}

class Switch {
    private Switchable device;

    public Switch(Switchable device) {
        this.device = device;
    }

    public void operate() {
        device.turnOn();
    }
}
```

### Conclusion
The SOLID principles offer a robust foundation for writing maintainable, scalable, and flexible object-oriented software. By adhering to these principles, developers can ensure that their code remains extensible, loosely coupled, and easy to modify without introducing bugs or breaking functionality.

**Further Reading:**
- Martin, R. C. (2000). Design Principles and Design Patterns.
- Meyer, B. (1997). Object-Oriented Software Construction. Prentice Hall.

# Week 12 - Declarative & Functional Programming in Kotlin

## Overview

The **declarative programming paradigm** is based on expressing *what* a program should accomplish rather than *how* to accomplish it. This approach contrasts with **imperative programming**, where the programmer explicitly defines the control flow of computation.

> 🧠 “Declarative programming is like describing the desired outcome, while imperative programming is like giving step-by-step instructions.”  
> — [Elliotte Rusty Harold, "Effective Java"](https://www.oreilly.com/library/view/effective-java/9780134686097/)

Functional programming is a **subset of the declarative paradigm**. It treats computation as the evaluation of mathematical functions and avoids changing state or mutable data.

---

## Functional Programming in Kotlin

Languages like **Kotlin** (and **Swift**) support multiple paradigms, including functional programming. Kotlin is statically typed and features **type inference**, making it well-suited for functional constructs such as higher-order functions and immutability.

###  Key Benefit: Reduced Side Effects

**Side effects** refer to any application state changes that occur outside the intended return value of a function (e.g., modifying a global variable, I/O operations, etc.).

###  Imperative Example (with Side Effects)

```kotlin
var listOfInts = listOf(1, 2, 3, 4, 5, 6)
var count = 0

fun filterOnEven(list: List<Int>): MutableList<Int> {
    val newList = mutableListOf<Int>()
    while (count < list.count()) {
        if (list[count] % 2 == 0) {
            newList.add(list[count])
        }
        count++
    }
    return newList
}

# Recursion in Functional Languages

## Functions in functional languages can also call themselves as part of their definition!

- **Recursion** is essentially using (or calling) a function in its own definition.
- For this to work, the function definition must have an **edge case** – or a natural end condition.

### Kotlin Example

```kotlin
fun fibonacci(n: Int): Int {
    if (n < 2) {
        return n
    } else {
        return fibonacci(n - 1) + fibonacci(n - 2)
    }
}
```
**Functional Style: Pure Functions**

In purely functional languages, functions return the same output for the same input and avoid side effects. Kotlin supports functional constructs that promote this style.

**Kotlin Functional Example (Using filter)**

```val listOfInts = listOf(1, 2, 3, 4, 5, 6)
val evenInts = listOfInts.filter { it % 2 == 0 }
```

 This example is concise, has no side effects, and is easier to test and maintain.

 **Higher-Order Functions:**

 A higher-order function is a function that takes other functions as parameters or returns them. This is a key feature in functional programming and widely supported in Kotlin.

 **Kotlin Example:**

 ```
 fun calculate(x: Int, y: Int, operation: (Int, Int) -> Int): Int {
    return operation(x, y)
}

fun sum(x: Int, y: Int) = x + y

val sumResult = calculate(x = 4, y = 5, ::sum)
val mulResult = calculate(x = 4, y = 5) { a, b -> a * b }

println(sumResult) // 9
println(mulResult) // 20
```

**Recursion in Functional Programming**

Recursion is when a function calls itself to solve a problem. It's a common pattern in functional programming where traditional loops are avoided.

**Kotlin Example: Fibonacci Sequence**

```
fun fibonacci(n: Int): Int {
    return if (n < 2) {
        n
    } else {
        fibonacci(n - 1) + fibonacci(n - 2)
    }
}
```
