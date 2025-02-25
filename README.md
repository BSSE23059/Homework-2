# Homework-2

# Observer Pattern in C#

## Overview
This project demonstrates the **Observer Design Pattern** in C#. The pattern enables an object (Subject) to notify multiple dependent objects (Observers) about state changes, promoting a **loosely coupled, event-driven architecture**.

## Table of Contents
- [Project Structure](#project-structure)
- [Implementation](#implementation)
- [Running the Program](#running-the-program)
- [Example Output](#example-output)
- [Key Benefits](#key-benefits)
- [Conclusion](#conclusion)
- [Author](#author)
- [License](#license)

## Project Structure
1. **Subject (`ISubject`)** – Interface defining methods to manage observers.  
2. **Concrete Subject (`ConcreteSubject`)** – Maintains state and notifies observers when it changes.  
3. **Observer (`IObserver`)** – Interface requiring an `Update()` method for notifications.  
4. **Concrete Observers (`ConcreteObserverA`, `ConcreteObserverB`)** – Implement `IObserver` and react to state changes.  
5. **Client (`Program.cs`)** – Demonstrates the pattern by attaching observers, modifying state, and displaying notifications.  

## Implementation
- `ConcreteSubject` maintains a list of observers and calls `Notify()` when its state changes.  
- Observers dynamically **subscribe/unsubscribe** and react to updates.  
- Ensures **decoupling** between components, improving maintainability.  

## Running the Program
```sh
# Clone the repository
git clone <repository-url>

# Navigate to the project directory
cd observer-pattern-csharp

# Build and run the application
dotnet run
