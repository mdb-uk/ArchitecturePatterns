10:53 | 2024-09-30
# Links

[[Architecture]] [[Architecture Patterns Index]]
# Content

This design pattern separates an application into three interconnected components, the Model, the View and the Controller.

Model:
- Represents the data and business model of the application 
- Manages the data, logic and rules of the application
- Acts as a data source for the View layer

View:
- Represents the user interface of the application
- Displays data from the Model to the User
- Sends user commands to the Controller

Controller
- Intermediary between the Model and the View
- Processer user input from the View
- Updates the Model based on user actions and refreshes the View

Advantages:
- Separation of concerns
- Maintainability
- Reusability
- Testability
Disadvantages:
- Complexity
- Learning Curve
- Overhead

This pattern is commonly used in web development and desktop applications.

![[Pasted image 20240930112153.png]]

### References

[MVC Architecture - System Design - GeeksforGeeks](https://www.geeksforgeeks.org/mvc-architecture-system-design/)