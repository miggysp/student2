---
toc: True
comments: True
layout: post
title: Correcting Errors
courses: {'compsci': {'week': 4}}
type: hacks
---

```python
menu = {
    "burger": 3.99,
    "fries": 1.99,
    "drink": 0.99
}
total = 0

while True:
    print("Menu")
    for item, price in menu.items():
        print(f"{item.capitalize()}: ${price:.2f}")

    choice = input("Please select an item from the menu (or 'done' to finish): ").lower()

    if choice == 'done':
        break

    if choice in menu:
        total += menu[choice]
        print(f"Added {choice} to your order. Total: ${total:.2f}")
    else:
        print("Invalid item. Please choose from the menu.")

print(f"Your total bill is: ${total:.2f}")


```

    Menu
    Burger: $3.99
    Fries: $1.99
    Drink: $0.99
    Added fries to your order. Total: $1.99
    Menu
    Burger: $3.99
    Fries: $1.99
    Drink: $0.99
    Added drink to your order. Total: $2.98
    Menu
    Burger: $3.99
    Fries: $1.99
    Drink: $0.99
    Your total bill is: $2.98

