# Homework-2

Observer Pattern Implementation in C#

Overview

This project demonstrates the Observer Design Pattern in C#. The Observer Pattern is a behavioral pattern where an object (the Subject) maintains a list of its dependents (Observers) and notifies them of any state changes. This allows for a decoupled and event-driven architecture.

Project Structure

1. Subject (Observable) Interface

Defines methods for adding, removing, and notifying observers.

Implemented in ISubject interface.

2. Concrete Subject Class

Stores state and maintains a list of observers.

Notifies observers whenever the state changes.

Implemented in ConcreteSubject class.

3. Observer Interface

Defines an Update() method that observers must implement.

Implemented in IObserver interface.

4. Concrete Observer Classes

Implement the observer interface and respond to state changes.

Includes ConcreteObserverA and ConcreteObserverB.

5. Client Class (Program.cs)

Demonstrates the Observer Pattern in action.

Creates a subject, attaches observers, modifies the state, and observes the notifications.

Implementation Details

The ConcreteSubject class maintains a state and a list of observers.

When the state changes, Notify() is called to update all attached observers.

Observers receive updates and execute their respective Update() methods.

Observers can be dynamically added or removed from the subject.

How to Run the Program

# Clone the repository
$ git clone <repository-url>

# Navigate to the project directory
$ cd observer-pattern-csharp

# Build and run the application
$ dotnet run

Example Output

Changing state to 'Active'
Observer A1 received update: Active
Observer B received a state change: Active

Changing state to 'Inactive'
Observer A1 received update: Inactive
Observer B received a state change: Inactive

Changing state to 'Completed'
Observer B received a state change: Completed

Benefits of the Observer Pattern

Decoupling: Subjects and observers are loosely coupled.

Flexibility: Multiple observers can dynamically subscribe/unsubscribe.

Event-Driven Architecture: Enables reactive programming.

Conclusion

This implementation provides a clear understanding of the Observer Pattern and its benefits in building event-driven, maintainable, and scalable software.

Author

[Your Name]

License

This project is licensed under the MIT License.

