# Homework-2

# Observer Pattern Implementation in C#

## Overview
This project demonstrates the **Observer Design Pattern** in C#. The Observer Pattern is a behavioral pattern where an object (the Subject) maintains a list of its dependents (Observers) and notifies them of any state changes. This allows for a decoupled and event-driven architecture.

## Table of Contents
- [Project Structure](#project-structure)
- [Implementation Details](#implementation-details)
- [How to Run the Program](#how-to-run-the-program)
- [Example Output](#example-output)
- [Benefits of the Observer Pattern](#benefits-of-the-observer-pattern)
- [Conclusion](#conclusion)
- [Author](#author)
- [License](#license)

## Project Structure

### 1. Subject (Observable) Interface
- Defines methods for adding, removing, and notifying observers.
- Implemented in the `ISubject` interface.

### 2. Concrete Subject Class
- Stores state and maintains a list of observers.
- Notifies observers whenever the state changes.
- Implemented in the `ConcreteSubject` class.

### 3. Observer Interface
- Defines an `Update()` method that observers must implement.
- Implemented in the `IObserver` interface.

### 4. Concrete Observer Classes
- Implement the observer interface and respond to state changes.
- Includes `ConcreteObserverA` and `ConcreteObserverB`.

### 5. Client Class (`Program.cs`)
- Demonstrates the Observer Pattern in action.
- Creates a subject, attaches observers, modifies the state, and observes the notifications.

## Implementation Details
- The **`ConcreteSubject`** class maintains a state and a list of observers.
- When the state changes, `Notify()` is called to update all attached observers.
- **Observers** receive updates and execute their respective `Update()` methods.
- Observers can be dynamically added or removed from the subject.

## How to Run the Program
```sh
# Clone the repository
git clone <repository-url>

# Navigate to the project directory
cd observer-pattern-csharp

# Build and run the application
dotnet run


