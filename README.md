# 👨‍🍳 Smart Chef - Smart Recipe Management System

A C-based interactive recipe and inventory management application designed to organize recipes, track ingredients, handle dynamic memory allocation, and calculate nutrition facts.

Developed by **Shiran Chocavi** & **Shani Zahavi** as part of the Computer Science curriculum at **HIT - Holon Institute of Technology** (Spring 2026).

---

## 📸 Overview

**Smart Chef** is designed to streamline kitchen management and recipe organization[cite: 4, 13]. The system tracks available pantry items ("The Pantry") while managing a structured cookbook ("Book of Recipes") concurrently[cite: 6].

---

## ✨ Key Features

* **📦 Inventory Management (`ProgMemory`):** Simultaneously manages global pantry ingredients (`foods_in_prog`) and recipe collections (`BookRecipe`)[cite: 6].
* **🥗 Dynamic Recipe Construction:** Associates specific food products with custom quantities using a dedicated linking structure (`PairFoodAmount`)[cite: 6].
* **📊 Calorie Calculation Logic:** Automatically sums up total recipe calories using the formula:
  $$\text{Total Calories} = \sum_{i=0}^{n} (\text{Quantity}_i \times \text{CaloriesPerUnit}_i)$$
[cite: 12]
* **⚙️ Safe Dynamic Memory Allocation:** Built with rigorous `malloc` and `realloc` error handling, nested memory deallocation (`FreeBookMemory`), and deep copying (`_strdup`) to eliminate memory leaks[cite: 7, 8, 10].
* **🛡️ Buffer Overflow Protection:** Utilizes safe string inputs (`scanf("%99[^\n]", ...)`) and checks recipe name uniqueness before insertion[cite: 10].
* **💻 Interactive CLI Dashboard:** User-friendly menu loop with formatted table output (`%-15s`)[cite: 9].

---

## 🏗 System Architecture & Data Structures

* **`FoodProduct`:** Base structure holding a dynamically allocated product name (`char*`) and calorie content (`double`)[cite: 6].
* **`PairFoodAmount` / `Recipe`:** Couples food items with specific measurement quantities using dynamic arrays[cite: 6].
* **`ProgMemory`:** Core logical manager storing all active pantry items and recipes[cite: 6].

---

## 🛠 Tech Stack

* **Language:** C (C11 standard)[cite: 5, 11]
* **IDE / Compiler:** Visual Studio / GCC[cite: 8, 10]
* **Key Concepts:** Dynamic Arrays (`realloc`), Pointers, Deep Copying, Memory Leak Prevention, CLI Development[cite: 6, 7, 8, 11]

---

## 🚀 How to Run

### Prerequisites
* C Compiler (GCC or MSVC via Visual Studio).

### Compilation & Execution

1. **Clone the repository:**
   ```bash
   git clone [https://github.com/shiran-chocavi/Smart-Chef.git](https://github.com/shiran-chocavi/Smart-Chef.git)
   cd Smart-Chef
