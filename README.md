# task mgt 
def task():
    tasks = []  # empty list
    print("WELCOME TO THE TASK MANAGEMENT")

    total_task = int(input("Enter how many tasks to add: "))

    for i in range(1, total_task + 1):
        task_name = input(f"Enter task {i}: ")
        tasks.append(task_name)

    print(f"\nToday's tasks are:\n{tasks}")

    while True:
        print("\nOperations Menu:")
        print("1 - Add Task")
        print("2 - Update Task")
        print("3 - Delete Task")
        print("4 - View Tasks")
        print("5 - Exit/Stop")

        operation = int(input("Enter operation number: "))

        if operation == 1:
            add = input("Enter task you want to add: ")
            tasks.append(add)
            print(f"Task '{add}' has been successfully added.")

        elif operation == 2:
            Updated_val = input("Enter the task name you want to update: ")
            if Updated_val in tasks:
                new_task = input("Enter the new task: ")
                index = tasks.index(Updated_val)
                tasks[index] = new_task
                print(f"Task '{Updated_val}' has been successfully updated.")
            else:
                print(f"Task '{Updated_val}' not found.")

        elif operation == 3:
            del_val = input("Which task do you want to delete? ")
            if del_val in tasks:
                tasks.remove(del_val)
                print(f"Task '{del_val}' has been deleted.")
            else:
                print(f"Task '{del_val}' not found.")

        elif operation == 4:
            print(f"\nTotal tasks: {tasks}")

        elif operation == 5:
            print("Closing the program...")
            break

        else:
            print("Invalid Input. Please enter a number between 1-5.")
