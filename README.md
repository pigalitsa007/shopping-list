# shopping-list
def display_menu():
    print("\nShopping List Menu:")
    print("1. Add item")
    print("2. Remove item")
    print("3. View list")
    print("4. Exit")

def add_item(shopping_list):
    item = input("Enter the item to add: ")
    shopping_list.append(item)
    print(f'Added "{item}" to the list.')

def remove_item(shopping_list):
    item = input("Enter the item to remove: ")
    if item in shopping_list:
        shopping_list.remove(item)
        print(f'Removed "{item}" from the list.')
    else:
        print(f'"{item}" is not in the list.')

def view_list(shopping_list):
    if shopping_list:
        print("\nCurrent Shopping List:")
        for item in shopping_list:
            print(f'- {item}')
    else:
        print("The shopping list is empty.")

def main():
    shopping_list = []
    while True:
        display_menu()
        choice = input("Choose an option (1-4): ")
        if choice == '1':
            add_item(shopping_list)
        elif choice == '2':
            remove_item(shopping_list)
        elif choice == '3':
            view_list(shopping_list)
        elif choice == '4':
            print("Exiting the program.")
            break
        else:
            print("Invalid option. Please choose again.")

if __name__ == "__main__":
    main()
