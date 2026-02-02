# Technical Core

**Duration**: 6 weeks

**Learning Objective**: Transition from writing code to engineering robust, efficient software components.

## Object-Oriented Programming & Systems Programming

This module focuses on mastering **Object-Oriented Programming (OOP)** principles and systems programming concepts. You will learn how to design and implement software using **encapsulation**, **inheritance**, **polymorphism**, and **abstraction**. Additionally, you will explore low-level programming concepts such as **memory management**, **pointers**, and **concurrency**.

### Object-Oriented Programming (OOP)

OOP is the dominant praradigm for enterprise software. For an architect, the goal isn't just "creating classes," but creating *boundaries* that allow systems to evolve.

#### Encapsulation & Information Hiding
* **Concept**: Bundling data with methods that operate on that data and restricting direct access to some of the object's components.
* **Architectural View**: This is the basis of **Microservices** and **Modules**. If internal state is exposed, other parts of the system will couple to it, making refactoring difficult.

```ts
// TypeScript Example of Encapsulation
class BankAccount {
    private balance: number;

    constructor(initialBalance: number) {
        this.balance = initialBalance;
    };

    deposit(amount: number): void {
        if (amount > 0)
            this.balance += amount;
    };

    getBalance(): number {
        return this.balance;
    };
};

const account = new BankAccount(100);
account.deposit(50);
console.log(account.getBalance()); // 150
console.log(account.balance); // Error: Property 'balance' is private
```

#### Inheritance vs. Composition
* **Concept**: Deriving new classes from existing ones (inheritance) vs. building complex types by combining objects (composition).
   * **Inheritance** creates an "is-a" relationship.
   * **Composition** creates a "has-a" relationship.
* **Architectural View**: **Favor composition over inheritance**. Deep inheritance hierarchies create brittle systems where a change in a parent class breaks all children. Composition enables flexible designs.

```ts
// TypeScript Example of Inheritance
class Human {
    speak(): void {
        console.log('Hello!');
    };
};

class Employee extends Human {
    work(): void {
        console.log('Working...');
    };
};

const emp = new Employee();
emp.speak(); // Hello!
emp.work(); // Working...
```

```ts
// TypeScript Example of Composition
class Employee {
    work(): void {
        console.log('Working...');
    };
};

class Company {
    private employees: Employee[] = [];

    addEmployee(emp: Employee): void {
        this.employees.push(emp);
    };

    getEmployees(): Employee[] {
        return this.employees;
    };
};

const company = new Company();
const emp = new Employee();
company.addEmployee(emp);
console.log(company.getEmployees()); // [Employee]
```
#### Polymorphism & Interfaces
* **Concept**: The ability to present the same interface for different underlying forms (data types).
* **Architectural View**: This is critical for **Dependency Injection**. By coding to an *Interface* rather than an *Implementation*, you can swap a database driver (e.g., switch from MySQL to PostgreSQL) without changing business logic.

```ts
// TypeScript Example of Polymorphism via Interfaces
interface PaymentProcessor {
    processPayment(amount: number): void;
};

class PayPalProcessor implements PaymentProcessor {
    processPayment(amount: number): void {
        console.log(`Processing PayPal payment of $${amount}`);
    };
};

class StripeProcessor implements PaymentProcessor {
    processPayment(amount: number): void {
        console.log(`Processing Stripe payment of $${amount}`);
    };
};

const executePayment = (processor: PaymentProcessor, amount: number): void => {
    processor.processPayment(amount);
};

const paypal = new PayPalProcessor();
const stripe = new StripeProcessor();
executePayment(paypal, 100); // Processing PayPal payment of $100
executePayment(stripe, 200); // Processing Stripe payment of $200
```

#### Abstraction
* **Concept**: Hiding complex reality while exposing only the necessary parts.
* **Architectural View**: API Design is essentially an exercise in abstraction. You must hide the "how" (complexity) and expose the "what" (functionality).

```ts
// TypeScript Example of Abstraction
abstract class Vehicle {
    abstract startEngine(): void;
    abstract stopEngine(): void;
};

class Car extends Vehicle {
    startEngine(): void {
        console.log('Car engine started');
    };
    stopEngine(): void {
        console.log('Car engine stopped');
    };
};

const myCar = new Car();
myCar.startEngine(); // Car engine started
myCar.stopEngine(); // Car engine stopped
```

### Systems Programming Concepts

Understanding how software interacts with hardware is what separates "coder" from a "systems engineer." This knowledge is crucial for architects who need to design high-performance, reliable systems.

#### Memory Management (Stack vs. Heap)
* **Stack**: Fast, temporary storage for function variables.
* **Heap**: Dynamic storage for objects that live longer than a function call.
* **Architectural Relevance**: Poor heap management leads to **Memory Leaks** and **Garbage Collection pauses**, which kill system latency.
* Example: In languages like C/C++, you must manually allocate and free memory. In managed languages (Java, C#), understanding how the garbage collector works is essential.

```c
// C Example of Manual Memory Management
#include <stdio.h>
#include <stdlib.h>

int main() {
    int *arr = (int *)malloc(10 * sizeof(int)); // Allocate memory on the heap

    for (int i = 0; i < 10; i++)
        arr[i] = i;

    free(arr); // Free allocated memory
    return 0;
};
```

#### Pointers & References
* **Concept**: Direct access to memory addresses vs. safe handling of objects.
* **Architectural Relevance**: Understanding "Pass by Value" vs. "Pass by Reference" is critical when designing high-performance systems or processing large data structures (to avoid unnecessary copying).

```c
// C Example of Pointers
#include <stdio.h>
void increment(int *num) {
    (*num)++;
};
int main() {
    int value = 5;
    increment(&value); // Pass address of value
    printf("%d\n", value); // 6
    return 0;
};
```
#### Concurrency & Parallelism
* **Threads vs. Processes**: A thread is a lightweight unit of execution within a process. Processes are isolated and have their own memory space.
* **Synchronization**: Using Locks, Mutexes, and Semaphores to prevent **Race Conditions**.
* **Deadlocks**: A situation where two processes are waiting for each other to release resources.
* **Architectural Relevance**: Modern cloud systems are highly concurrent. If you don't understand thread safety, your "scalable" web server will crash under load.

```c
// C Example of Thread Creation using pthreads
#include <stdio.h>
#include <pthread.h>

void* printMessage(void* arg) {
    char* message = (char*)arg;
    printf("%s\n", message);
    return NULL;
};

int main() {
    pthread_t thread1, thread2;
    char* msg1 = "Hello from Thread 1";
    char* msg2 = "Hello from Thread 2";

    pthread_create(&thread1, NULL, printMessage, (void*)msg1); // Create first thread
    pthread_create(&thread2, NULL, printMessage, (void*)msg2); // Create second thread

    pthread_join(thread1, NULL); // Wait for first thread to finish
    pthread_join(thread2, NULL); // Wait for second thread to finish
    return 0;
};
```

## Summary

Object-Oriented Programming and Systems Programming are foundational skills for any aspiring system architect. Mastery of these concepts enables you to design software that is modular, maintainable, and efficient. As you progress, always remember to evaluate trade-offs in your architectural decisions, balancing complexity, performance, and scalability.

## Practical Output

Build a small payment processing system that supports multiple payment gateways (e.g., PayPal, Stripe) using OOP principles. Implement concurrency to handle multiple payment requests simultaneously, ensuring thread safety and efficient memory management.

## Reading & Resources
* **Bloch, J.** (2018). *Effective Java* (3rd ed.). Addison-Wesley Professional.
* **Bryant, R. E., & O'Hallaron, D. R.** (2015). *Computer Systems: A Programmer's Perspective* (3rd ed.). Pearson.
* **Gamma, E., Helm, R., Johnson, R., & Vlissides, J.** (1994). *Design Patterns: Elements of Reusable Object-Oriented Software*. Addison-Wesley.
* **Goetz, B., Peierls, T., Bloch, J., Bowbeer, J., Holmes, D., & Lea, D.** (2006). *Java Concurrency in Practice*. Addison-Wesley Professional.
* **Martin, R. C.** (2017). *Clean Architecture: A Craftsman's Guide to Software Structure and Design*. Prentice Hall.
* **Tanenbaum, A. S., & Bos, H.** (2014). *Modern Operating Systems* (4th ed.). Pearson.