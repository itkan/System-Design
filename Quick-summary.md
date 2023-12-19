# System Design

### A.S.P.E.C.T.S. [System]

- Availability: How consistently and reliably the system is available for use.
- Scalability: The ability of the system to handle increased load and growth.
- Performance: How well the system responds to user interactions and processes tasks.
- Efficiency: The system's ability to use resources optimally to achieve its goals.
- Configurability: The ease with which the system can be configured to meet different requirements.
- Testability: The ease with which the system can be tested for quality assurance.
- Security: The measures in place to protect the system from unauthorized access and data breaches.

### S.O.L.I.D. [Classes/Modules]

- Single Responsibility Principle: A class should have only one reason to change.
- Open/Closed Principle: Software entities (classes, modules, functions, etc.) should be open for extension but closed for modification.
- Liskov Substitution Principle: Subtypes must be substitutable for their base types without altering the correctness of the program.
- Interface Segregation Principle: No client should be forced to depend on methods it does not use.
- Dependency Inversion Principle: High-level modules should not depend on low-level modules; both should depend on abstractions.

### D.E.S.I.G.N. [Modules/Components]
- Decoupling: The degree to which components are independent and can be modified without affecting others.
- Expandability: The ease with which the system can accommodate additional features or functionalities.
- Scalability: The ability of the system to handle increased load and growth.
- Interoperability: How well the system can interact with other systems or components.
- Graceful degradation: The ability of the system to maintain partial functionality in case of failures.
- Naming conventions: Consistent and meaningful naming conventions for elements in the system.

## Database

### C.A.P. Theorem

- Consistency: In a distributed system, all nodes see the same data at the same time. Every read receives the most recent write or an error.
- Availability: Every request to a non-failing node in the system receives a response, without the guarantee that it contains the most recent version of the information.
- Partition Tolerance: The system continues to operate despite network partitions that may cause communication failures between nodes.

### BASE

- Basically Available: The system remains operational even in the presence of faults or partial failures.
- Soft state: The system's state may not be consistent at all times, allowing for temporary inconsistencies between nodes.
- Eventual consistency: The system will become consistent over time, given that it is not experiencing input and that no new updates are made to the system.

### ACID

- Atomicity: A transaction is atomic, meaning that it is treated as a single, indivisible unit of work. Either all its operations are executed, or none of them is. If any part of the transaction fails, the entire transaction is rolled back to its previous state.
- Consistency: A transaction brings the database from one consistent state to another. It ensures that the integrity constraints and business rules defined in the database schema are not violated.
- Isolation: The execution of a transaction is isolated from other transactions. Even though multiple transactions may be executing concurrently, the result should be as if they were executed serially. This property prevents interference between transactions.
- Durability: Once a transaction is committed, its effects (changes to the database) are permanent and survive any subsequent failures. The system guarantees that the committed transaction will persist, even in the event of a power outage, crash, or other failures.
