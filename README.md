# 🔀 Multiple Inheritance in Java (Using Interfaces)

![Java](https://img.shields.io/badge/Java-21-orange?style=for-the-badge&logo=openjdk)
![OOP](https://img.shields.io/badge/OOP-Multiple%20Inheritance-blue?style=for-the-badge)
![IDE](https://img.shields.io/badge/IDE-Eclipse-purple?style=for-the-badge)
![Status](https://img.shields.io/badge/Status-Completed-brightgreen?style=for-the-badge)

---

# 📚 Project Overview

This project demonstrates **Multiple Inheritance in Java using Interfaces**.

Unlike some programming languages, Java **does not allow a class to inherit from multiple classes** because it can create ambiguity (known as the *Diamond Problem*). Instead, Java supports **Multiple Inheritance through Interfaces**.

In this project, **Child4** implements **Interface1** and **Interface2**, allowing it to inherit behaviors from both interfaces while providing its own implementation of their methods. :contentReference[oaicite:0]{index=0}

---

# 🧬 What is Multiple Inheritance?

Multiple Inheritance means a class receives behavior from **more than one parent**.

In Java:

❌ Multiple Classes → Not Allowed

✅ Multiple Interfaces → Allowed

---

# 🖼 Class Diagram

```text
                Interface1
          ┌──────────────────────┐
          │ commonTrait          │
          │ method1()            │
          └──────────┬───────────┘
                     │
                 implements
                     │
                     ▼
                  Child4
          ┌──────────────────────┐
          │ name                 │
          │ method1()            │
          │ method2()            │
          └──────────┬───────────┘
                     ▲
                 implements
                     │
          ┌──────────┴───────────┐
          │      Interface2      │
          │ uniqueSkill          │
          │ method2()            │
          └──────────────────────┘
```

---

# 🏗 Project Structure

```text
day8
│
├── Interface1
│      ├── commonTrait
│      └── method1()
│
├── Interface2
│      ├── uniqueSkill
│      └── method2()
│
├── Child4
│      ├── name
│      ├── method1()
│      └── method2()
│
└── MultipleInheritanceExample
```

---

# 🧠 Learning Objectives

After completing this project you will understand:

- ✅ What Multiple Inheritance is
- ✅ Why Java uses Interfaces instead of multiple classes
- ✅ The **implements** keyword
- ✅ Interface variables
- ✅ Interface methods
- ✅ Method implementation
- ✅ Object creation

---

# 💻 Java Concepts Used

- ☕ Java Interfaces
- 🔀 Multiple Inheritance
- 📦 Objects
- 🧩 Interface Implementation
- 📚 Variables
- ⚙ Methods
- 🖨 Console Output

---

# 🔍 Code Walkthrough

## Step 1

Create Interface1.

```java
interface Interface1
```

Interface1 contains:

- commonTrait
- method1()

Every class that implements Interface1 must provide an implementation for **method1()**. :contentReference[oaicite:1]{index=1}

---

## Step 2

Create Interface2.

```java
interface Interface2
```

Interface2 contains:

- uniqueSkill
- method2()

Any implementing class must define **method2()**. :contentReference[oaicite:2]{index=2}

---

## Step 3

Create Child4.

```java
class Child4 implements Interface1, Interface2
```

Notice the keyword:

```java
implements
```

Instead of **extends**, Java uses **implements** for interfaces.

Child4:

- Implements method1()
- Implements method2()
- Has its own variable (name)

while also accessing interface constants. :contentReference[oaicite:3]{index=3}

---

## Step 4

Create the Object

```java
Child4 obj = new Child4();
```

The object can now:

- Access its own variable
- Call method1()
- Call method2()
- Access Interface constants using the Interface name. :contentReference[oaicite:4]{index=4}

---

# 🔄 Program Flow

```text
Create Interface1
        │
        ▼
Create Interface2
        │
        ▼
Child4 implements both
        │
        ▼
Create Object
        │
        ▼
Access Child Variable
        │
        ▼
Call method1()
        │
        ▼
Call method2()
        │
        ▼
Access Interface Constants
```

---

# ▶ Sample Output

```text
Max
Method1 from Interface1
Method2 from Interface2
Dedicated
Problem Solving
Method1 from Interface1
Method2 from Interface2
```

---

# 🌎 Real-World Example

Imagine hiring an employee.

👨 **Employee (Child4)**

must satisfy two job requirements.

---

📋 **Interface1**

Requires:

- Good Work Ethic
- method1()

---

📋 **Interface2**

Requires:

- Problem Solving Skills
- method2()

---

👨‍💻 **Employee (Child4)**

Implements both requirements.

Result:

One employee can fulfill multiple roles by implementing multiple interfaces.

---

# 🖼 Visual Representation

```text
          📋 Interface1
         (Rules & Behavior)
                │
                │
                ▼
          👨‍💻 Child4
                ▲
                │
                │
          📋 Interface2
        (Additional Rules)
```

---

# ⚠ Why Java Doesn't Allow Multiple Class Inheritance

Suppose two parent classes both have:

```java
display();
```

If Child inherits from both,

Java wouldn't know which version to use.

This is called the **Diamond Problem**.

Interfaces solve this issue because they define **what must be done**, while the implementing class decides **how it is done**.

---

# 🎯 Key Takeaways

✅ Java does NOT support Multiple Inheritance with classes.

✅ Java DOES support Multiple Inheritance using interfaces.

✅ Interfaces define behavior.

✅ Classes implement behavior.

✅ Interfaces improve flexibility and code organization.

---

# 📖 OOP Vocabulary

| Term | Meaning |
|------|---------|
| Interface | A contract that defines methods a class must implement |
| implements | Allows a class to implement an interface |
| Class | Blueprint for creating objects |
| Object | Instance of a class |
| Variable | Stores data |
| Method | Performs an action |
| Multiple Inheritance | Receiving behavior from multiple interfaces |

---

# 🚀 Technologies Used

- ☕ Java 21
- 💻 Eclipse IDE
- 🧬 Object-Oriented Programming (OOP)
- 🔀 Multiple Inheritance
- 🧩 Java Interfaces

---

# 💡 Why This Project Matters

Understanding interfaces is essential for professional Java development. Interfaces promote **loose coupling**, **flexibility**, and **code reusability**, making them a core part of enterprise applications and automation frameworks like **Selenium**, **Spring Boot**, and **JUnit**.

Mastering interfaces prepares developers to build scalable, maintainable, and extensible Java applications.

---

## ⭐ Author

**Tracy Joseph**

*Cloudberry Java Bootcamp – Day 8*

*"Learning Java one interface at a time."* ☕🚀
