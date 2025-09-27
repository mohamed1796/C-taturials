## 📌 What are Structures in C?

In **C language**, a **structure (`struct`)** is a user-defined data type that allows grouping of variables of **different data types** under a single name.

Think of it like a **container** that can hold related information (like a record in a database).

For example: if you want to store information about a student (name, roll number, and marks), instead of creating separate variables, you can put them in a **structure**.

---

## 📖 Syntax of a Structure

```c
struct StructureName {
    data_type member1;
    data_type member2;
    ...
    data_type memberN;
};
```

* `struct` → keyword
* `StructureName` → name of the structure
* `member1, member2, ...` → variables inside the structure (can be of different types)

---

## 🔹 Example 1: Basic Structure

```c
#include <stdio.h>

// Define structure
struct Student {
    int roll;
    char name[50];
    float marks;
};

int main() {
    // Create a variable of struct Student
    struct Student s1 = {1, "Mohamed", 88.5};

    // Access members using dot (.)
    printf("Roll: %d\n", s1.roll);
    printf("Name: %s\n", s1.name);
    printf("Marks: %.2f\n", s1.marks);

    return 0;
}
```

**Output:**

```
Roll: 1
Name: Mohamed
Marks: 88.50
```

---

## 🔹 Example 2: Array of Structures

You can store multiple records (like a list of students).

```c
#include <stdio.h>

struct Student {
    int roll;
    char name[50];
    float marks;
};

int main() {
    struct Student students[3] = {
        {1, "Ali", 90.5},
        {2, "Sara", 85.0},
        {3, "John", 78.5}
    };

    for (int i = 0; i < 3; i++) {
        printf("\nRoll: %d\n", students[i].roll);
        printf("Name: %s\n", students[i].name);
        printf("Marks: %.2f\n", students[i].marks);
    }

    return 0;
}
```

---

## 🔹 Example 3: Structures with Pointers

```c
#include <stdio.h>

struct Student {
    int roll;
    char name[50];
    float marks;
};

int main() {
    struct Student s1 = {10, "Ahmed", 92.0};

    // Pointer to structure
    struct Student *ptr = &s1;

    // Access with arrow (->)
    printf("Roll: %d\n", ptr->roll);
    printf("Name: %s\n", ptr->name);
    printf("Marks: %.2f\n", ptr->marks);

    return 0;
}
```

---

## 🔹 Example 4: Nested Structures

Structures can be placed inside another structure.

```c
#include <stdio.h>

struct Address {
    char city[50];
    int zip;
};

struct Student {
    int roll;
    char name[50];
    struct Address addr;  // Nested structure
};

int main() {
    struct Student s1 = {1, "Mohamed", {"Doha", 12345}};

    printf("Name: %s\n", s1.name);
    printf("City: %s\n", s1.addr.city);
    printf("ZIP: %d\n", s1.addr.zip);

    return 0;
}
```

---

## 📌 Why Do We Need Structures?

* To group **related data** of different types together.
* Useful in representing **real-world entities** (students, employees, books, etc.).
* Makes **code cleaner and manageable** instead of using separate variables.
* Forms the basis for more advanced concepts like **linked lists, trees, and file handling**.

---
