Programming languages are all about asking big questions. PureScript asks, “What is purity?” ClojureScript asks, “What is simplicity?” And JavaScript asks, “Wat?”

Here's what I'm looking for in my dream programming language. Is there some genius or madman out there cooking this up?

Language

1. Customizable Reader: Lets me change the syntax.
1. First-Class Functions: Functions can be passed around.
1. Impurity: Lets me mix pure and impure code.
1. S-Expressions: Enables structural editing.
1. Immutable Data Structures
1. Type Classes: Type class instances are resolved statically when possible, with a fallback to dynamic dispatch.
1. Forward Reference: Lets me use constants and functions before they are defined.
1. Automatic Promise Handling: If a function returns a promise, the runtime system automatically treats it as a dataflow variable and schedules a continuation, effectively awaiting its resolution, without any special syntax.
1. Tail Recursion: Optimizes both self-recursive and mutually recursive functions seamlessly, without any special syntax.
1. Flexible Standard Library: Allows the standard library to be replaced or customized.
1. Null Key Absence in Maps: Enforces that keys associated with `null` values are not present in the map, ensuring that there's only one way to represent the absence of a value.
1. Clear Error Messages: Lets me know what went wrong and how to fix it.
1. Gradual Typing: If the system stumbles upon code where it can't infer the type, it doesn't demand annotations.
1. Contract System
1. Flexible Evaluation Strategy: Supports both strict and lazy evaluation.

IDE

1. Syntax Highlighting
1. Code Formatting
    - Indentation
    - Sorting: Automatically alphabetizes imports and dictionary keys.
    - Call-Graph Ordering: Automatically sorts definitions by traversing the call graph depth-first from the entry point.
1. Auto Complete
    - Type-Aware: Offers suggestions that are type-compatible.
    - Automatic Import: Imports the things I select automatically, if they are not already imported.
    - Alias Management: Suggests the common aliases for the modules I import.
1. Commenting and Uncommenting
1. Static Analysis
    - Type Inference: Infers the types of everything as much as possible.
    - Contract Inference: Automatically deduces preconditions, postconditions, and invariants.
    - Duplicate Detection: Identifies duplicate definitions, keys, etc.
    - Unused Entity Detection: Finds unused definitions, imports, etc.
    - Consistency: Ensures consistent aliasing, naming conventions, etc.
    - Idiomatic Code Suggestions
1. Generative Testing: Identifies pure function composition and conducts generative testing automatically.
1. Structural Editing: Manipulates S-expressions.
1. REPL
    - Contextual Code Evaluation: Supports evaluating the current form where the cursor is located.
    - Namespace Respect: Lets me evaluate the code in the namespace I want, without switching to it.
    - Library Integration:
    - Interactive Navigation: Lets me explore nested data in a tree-like view, and copy or use any part of it.
1. Definition Navigation: Allows for quick navigation to definitions.
1. Refactoring: Supports renaming namespaces, definitions, function parameters, macro parameters, etc.
1. Hot Reloading

Interoperability

1. Backend Targets:
    - JavaScript: Compiles to JavaScript for front-end development and desktop applications using Electron, etc.
    - Python: Compiles to Python to meet the ecosystem's expectation of having Python for model training.
    - VM:
        - Synchronous Execution: Makes synchronous operations the default to avoid callback hell or async/await.
        - Multithreading
        - Cross-Platform
        - Polyglot: The VM should support JavaScript and Python, allowing direct library calls to avoid IPC.
        - Fast Startup: Startup time is 100 ms or less for a responsive CLI.
1. Seamless Interoperability: No need for a separate file to do FFI.
1. Execution Speed: Execution speed shouldn't be an order of magnitude slower in each target environment.
1. Compilation Speed: Initial compilation might take a while, but any subsequent ones should be done fast, like 100 ms or less.
1. Code Conversion: A handy utility to translate Python or JavaScript code to my language.
1. Code Reusability: Conditional execution where a specific code segment is compiled using a specific backend target.

Package Management

1. Version Set: A package management system that curates a set of library versions known to play nice together.
1. Dependency Lock File: Automatically records the exact version.
1. Type Repository: A place where developers can contribute, share, and retrieve type definitions.
1. Contract Repository

Documentation

1. Searchable: A search function that covers not just built-in but also third-party libraries.
1. Interlinked Content: Hyperlinks for function names, type definitions, contracts, and more.
1. Type Information
1. Contract Information
1. Interactive Example: Incorporating runnable code examples directly into the documentation.
