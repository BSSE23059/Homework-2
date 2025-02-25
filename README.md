# Homework-2

\documentclass{article}
\usepackage{hyperref}

\title{Observer Pattern Implementation in C\#}
\author{Your Name}
\date{\today}

\begin{document}

\maketitle

\section{Overview}
This project demonstrates the \textbf{Observer Design Pattern} in C\#. The Observer Pattern is a behavioral pattern where an object (the Subject) maintains a list of its dependents (Observers) and notifies them of any state changes. This allows for a decoupled and event-driven architecture.

\section{Project Structure}
\begin{itemize}
    \item \textbf{Subject (Observable) Interface}
    \begin{itemize}
        \item Defines methods for adding, removing, and notifying observers.
        \item Implemented in \texttt{ISubject} interface.
    \end{itemize}
    \item \textbf{Concrete Subject Class}
    \begin{itemize}
        \item Stores state and maintains a list of observers.
        \item Notifies observers whenever the state changes.
        \item Implemented in \texttt{ConcreteSubject} class.
    \end{itemize}
    \item \textbf{Observer Interface}
    \begin{itemize}
        \item Defines an \texttt{Update()} method that observers must implement.
        \item Implemented in \texttt{IObserver} interface.
    \end{itemize}
    \item \textbf{Concrete Observer Classes}
    \begin{itemize}
        \item Implement the observer interface and respond to state changes.
        \item Includes \texttt{ConcreteObserverA} and \texttt{ConcreteObserverB}.
    \end{itemize}
    \item \textbf{Client Class (Program.cs)}
    \begin{itemize}
        \item Demonstrates the Observer Pattern in action.
        \item Creates a subject, attaches observers, modifies the state, and observes the notifications.
    \end{itemize}
\end{itemize}

\section{Implementation Details}
\begin{itemize}
    \item The \textbf{ConcreteSubject} class maintains a state and a list of observers.
    \item When the state changes, \texttt{Notify()} is called to update all attached observers.
    \item \textbf{Observers} receive updates and execute their respective \texttt{Update()} methods.
    \item Observers can be dynamically added or removed from the subject.
\end{itemize}

\section{How to Run the Program}
\begin{verbatim}
# Clone the repository
git clone <repository-url>

# Navigate to the project directory
cd observer-pattern-csharp

# Build and run the application
dotnet run
\end{verbatim}

\section{Example Output}
\begin{verbatim}
Changing state to 'Active'
Observer A1 received update: Active
Observer B received a state change: Active

Changing state to 'Inactive'
Observer A1 received update: Inactive
Observer B received a state change: Inactive

Changing state to 'Completed'
Observer B received a state change: Completed
\end{verbatim}

\section{Benefits of the Observer Pattern}
\begin{itemize}
    \item \textbf{Decoupling:} Subjects and observers are loosely coupled.
    \item \textbf{Flexibility:} Multiple observers can dynamically subscribe/unsubscribe.
    \item \textbf{Event-Driven Architecture:} Enables reactive programming.
\end{itemize}

\section{Conclusion}
This implementation provides a clear understanding of the Observer Pattern and its benefits in building event-driven, maintainable, and scalable software.

\section{Author}
Your Name

\section{License}
This project is licensed under the MIT License.

\end{document}

