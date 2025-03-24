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



# WEEK 8

## Note from class:

**Multiple Activities and Intents**
- Explicit Intent: Used to navigate to a specific activity in your app or another app.
- Implicit Intent: Used for general actions (e.g., sending an email) where any matching app can handle the request.

**App Bar, Navigation Drawer, and Menus**
App Bar: Displays navigation options and controls. 
Navigation Drawer: A slide-out menu for navigation.
Menus: Defined in XML, allowing users to interact with different features.

**Navigation in an App**
Navigation Component: A framework for managing navigation in Android apps.

**Key Parts:**
- Navigation Graph: Defines app navigation paths.
- NavHost: Hosts fragments for navigation.
- NavController: Manages navigation actions.

**Navigation UI**
Menus: Can be linked with NavController for navigation.
Navigation Drawer & Bottom Navigation: Used for structuring app navigation.
Back Stack Management: Maintains navigation history for proper back navigation.


## Activities Week 8:

### Research a new language
Exploring a New Programming Language: Haskell
Haskell is a purely functional programming language known for its strong static typing and lazy evaluation. It emphasizes immutability, allowing developers to write concise, reliable, and mathematically precise code. Haskell’s expressive syntax and powerful type system help detect errors at compile time, making applications safer and reducing runtime exceptions.

Applications of Haskell
Academic Research – Haskell is widely used in universities to teach functional programming principles. Its strong mathematical foundations make it an excellent tool for exploring theoretical computer science and programming paradigms.
Finance and Banking – Haskell is used in the financial industry, particularly for developing robust and maintainable financial systems. Institutions like Standard Chartered rely on Haskell for its type safety and immutability, which help prevent costly errors in complex calculations.
Web Development – Frameworks such as Yesod and Servant leverage Haskell’s type system to create scalable and secure web applications. These tools allow developers to build structured and efficient web services with minimal risk of type-related bugs.
Data Analysis – Haskell provides efficient data processing capabilities through libraries like Data.Vector and Data.Text, making it a suitable choice for handling large datasets and performing advanced computations.
Compiler and Language Development – Many programming languages and compilers are developed using Haskell due to its strong support for pattern matching and abstract syntax trees, simplifying language design and implementation.
Who Uses Haskell?
University Professors and Researchers – for teaching and exploring functional programming.
Finance and Banking Software Developers – for building reliable financial applications.
Web Developers – for creating type-safe and scalable web applications.
Data Scientists and Analysts – for handling large datasets and performing complex computations.
Compiler and Tooling Engineers – for designing new programming languages and compilers.
Helpful Resources for Learning Haskell
Learn You a Haskell for Great Good! – A beginner-friendly book that introduces Haskell in a fun and engaging way, making complex concepts easier to grasp. Read here
Haskell.org – The official website provides documentation, tutorials, and community links, making it a great starting point for learners at all levels. Visit site
Hackage – A massive collection of Haskell libraries and packages, essential for discovering tools that enhance Haskell projects. Explore Hackage
Stack Overflow – A valuable resource where developers discuss common challenges, share solutions, and learn best practices. Browse Haskell questions


###  Write a user story
User Story for Spotify’s Offline Mode Feature
General User Story:
“As a Spotify user, I want to be able to download songs so that I can listen to them offline without using mobile data, ensuring uninterrupted playback when I have no internet connection.”

Specific User Stories:
1. Downloading Songs for Offline Playback
Single Song Download:
“As a user, I can download an individual song by tapping a download button next to it so that I can listen to it offline.”
Playlist and Album Download:
“As a user, I can download an entire playlist or album with a single tap, making it easier to save multiple songs for offline listening.”
Download Progress & Status:
“As a user, I can see a progress indicator for each song, playlist, or album while it is downloading, so I know when my songs are ready to play.”
“As a user, I can see a confirmation or notification once a song, playlist, or album has been successfully downloaded.”
2. Managing Offline Downloads
Viewing Downloaded Songs:
“As a user, I can access a dedicated ‘Downloaded’ section in my library to quickly find all my offline songs in one place.”
Removing Downloads:
“As a user, I can remove a downloaded song, playlist, or album by tapping an option in the menu, freeing up storage space on my device.”
“As a user, I can see the amount of storage used by my downloaded songs in the app settings to help manage my phone’s available space.”
Automatic Download Options:
“As a user, I can enable automatic downloads for my liked songs or favorite playlists so that I always have fresh offline music available.”
“As a user, I can set a limit on the number of songs that can be downloaded automatically to prevent excessive storage usage.”
3. Offline Mode and Playback
Enabling Offline Mode:
“As a user, I can enable ‘Offline Mode’ in settings to prevent Spotify from using mobile data when I have limited or no internet access.”
Error Handling for Unavailable Songs:
“As a user, I am notified when I try to play a song that is not downloaded and unavailable offline, so I understand why it can’t be played.”
“As a user, I can see which songs in my playlists are unavailable in Offline Mode to avoid confusion.”
Playback Features in Offline Mode:
“As a user, I can still use shuffle, repeat, and queue features while listening to my downloaded music.”
“As a user, I can sort and filter my downloaded songs by artist, album, or playlist for easy navigation.”

### Choose a language for our app develop project

**Chosen Language: PHP**
For this coding project, I have chosen PHP as the primary programming language. PHP is widely used in web development, particularly for server-side scripting, making it an excellent choice for building a web-based task management system. Given that PHP powers a significant portion of the web (including CMS platforms like WordPress and Laravel), it has a strong and active open-source community, making it an ideal language to contribute to and learn from.

**Why PHP?**
Web-Focused Development – Since PHP is designed for dynamic web applications, it seamlessly integrates with front-end technologies like HTML, JavaScript, and CSS. This makes it suitable for building an interactive task management system that allows users to create, assign, and track tasks in real time.

Open-Source Ecosystem – PHP has a rich ecosystem of open-source frameworks (Laravel, CodeIgniter, Symfony) and community-driven projects. Contributing to PHP-based open-source projects will allow me to collaborate with developers worldwide and enhance my coding skills.

Database Connectivity – PHP works well with MySQL, which is commonly used in task management systems to store and retrieve data efficiently.

Scalability & Security – PHP provides built-in security features and supports authentication, session management, and API integration, which are essential for multi-user task management systems.

How This Aligns with Open Source Contributions
I plan to contribute to PHP-based open-source projects by:

Developing or improving features in PHP frameworks used for task management (e.g., Laravel task scheduler).
Creating PHP-based plugins or integrations for existing open-source projects.
Contributing to open-source PHP projects that align with my web development goals.
Sharing improvements in my own project (e.g., making components of my task manager reusable for the community).
Learning Opportunities
Through this project, I aim to:

✔ Improve my backend development skills in PHP.

✔ Gain experience in database management with MySQL.

✔ Learn about RESTful API development in PHP.

✔ Enhance security practices for web apps.

✔ Collaborate with an open-source community by contributing to PHP projects.


**Follow-Up Questions and Reflections**
1. What is one interesting thing that you’ve learned from researching about programming languages and from reading other students’ posts?
One interesting takeaway from researching programming languages and reading other students' responses is how different languages are optimized for specific tasks. While PHP remains a strong contender for web development and backend services, languages like TypeScript have gained popularity for scalable frontend applications, and Kotlin is preferred for Android development. Additionally, I learned that many modern PHP projects integrate with JavaScript frameworks (like React or Vue.js) for full-stack development, making PHP a flexible and evolving language.

2. What other programming languages might you consider working with for DGL 104? What are your second choices, and why?
While PHP is my primary choice, my second choices would be:

✅ JavaScript (Node.js) – Because of its versatility in both frontend and backend development. It would allow me to create real-time features like live updates in my task manager app.
✅ Python – Known for its simplicity and wide adoption in data handling, automation, and AI integrations. It could be useful if I wanted to introduce AI-driven task prioritization in my project.
✅ TypeScript – A strongly typed version of JavaScript that could be beneficial if I wanted to enhance the maintainability of my project, particularly for frontend development.

3. What did you find most interesting when examining repositories on GitHub? Is there anything that surprised you, or that you didn’t expect?
One of the most interesting things I noticed while exploring GitHub repositories was the variety of open-source PHP projects that go beyond just content management systems. I found repositories dedicated to task automation, API authentication, and microservices in PHP, which I hadn't considered before.

Surprises:

The number of PHP projects using Docker and microservices for better scalability.
The level of community involvement—many repositories have detailed discussions, issue tracking, and feature requests, showing how active open-source collaboration can be.
The importance of testing—many projects emphasize unit testing and CI/CD pipelines, reinforcing best practices for modern PHP development.
4. What similarities are there across some of the repositories you’ve starred?
Some key similarities I noticed:
🔹 Most projects follow MVC architecture, which is common in modern PHP frameworks.
🔹 API-driven development—many PHP projects involve RESTful APIs, GraphQL, or headless CMS structures.
🔹 Use of Laravel and Symfony frameworks—these frameworks dominate modern PHP development.
🔹 Well-documented repositories—the best projects include clear installation guides, contribution guidelines, and API documentation.
🔹 Strong security practices—projects related to authentication and database management emphasize data encryption, token-based authentication (JWT/OAuth2), and SQL injection prevention.


# Week 9:

## Note from class:

- Design patterns are reusable coding solutions for common software design problems, improving maintainability and readability. They act as flexible recipes rather than rigid rules, allowing variations based on language and project needs. While they don't function independently, they provide recognizable structures that make collaboration and long-term code maintenance easier. Different programming languages may have unique implementations of the same pattern, but the core principles remain consistent. Resources like Refactoring.guru and Learning JavaScript Design Patterns offer examples of these patterns across various languages.

- In Opp we rely on the inheritance chain to share data and behavior

- Relying Solely on Inheritance Chains for Behavior Can Be Limiting

Inheritance chains can lead to brittle code and over-engineering, making the system difficult to maintain and extend.
Object composition offers a more flexible approach by allowing data and behavior from multiple objects to be combined into complex structures that better match behavior requirements.
This concept is closely related to function composition and higher-order functions in functional programming, where smaller functions are combined to create more powerful operations.

Design patterns are typically categorized into three solution-based classifications:

- Creational patterns are used for creating objects (sometimes many objects) in a predictable way.

- Structural patterns are used for composing classes into larger structures with more complex behaviour.

- Behavioural patterns are used to support common communication patterns between distinct objects.

The Observer pattern notifies observers of state changes so that they can update correctly:

- Responsibility: Subjects keep a list of observers; observers subscribe and unsubscribe to subjects.

- A behavioural pattern.

- Notifications are one-to-many.

- Subjects don’t care how many observers they have.

- Ideally, subjects and observers are loosely coupled.









# WEEK 11:

* Terms in OPP:
- classes
- encapsulation
- inheritance
- polymorphism
