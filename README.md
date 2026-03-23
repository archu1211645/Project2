# Project2
#This is my First Project
#Define the menu of Resturant
menu ={
    'Momos':40,
    'Chawmin':50,
    'Burger':30,
    'Dosa':50,
    'Pizza':99,
    'Cold drink':60,
}
#Greet
print("Welcome to PYTHON Resturant")
print("Momos: Rs40\n Chawmin:50\n Burger:30\n Dosa:50\n Pizza:99\n Cold drink:60")

order_total = 0
item_1 = input("Enter the name of item you want to order: ")
if item_1 in menu:
    order_total += menu[item_1]
    print(f"Your item {item_1} has been added to your order")
    another_order = input("Do you want to add another item? (yes/no): ")
    if another_order.strip().lower() == "yes":
        item_2 = input("Enter the name of second item: ")
        if item_2 in menu:
            order_total += menu[item_2]
            print(f"Item {item_2} has been added to the order")
        else:
            print(f"Ordered item {item_2} is not available!")
else:
    print(f"This item {item_1} is currently not available; please order something shown in the menu")
    another_order = input("Do you want to add another item? (yes/no): ")
    if another_order.strip().lower() == "yes":
        item_2 = input("Enter the name of second item: ")
        if item_2 in menu:
            order_total += menu[item_2]
            print(f"Item {item_2} has been added to the order")
            item_2 = input("Enter the name of second item: ")
        if item_2 in menu:
            order_total += menu[item_2]
            print(f"Item {item_2} has been added to the order")
        else:
            print(f"Ordered item {item_2} is not available!")
print(f"The total amount to pay is Rs {order_total}")
print(f"Thank you for ordering from PYTHON Resturent, please visit again!")
