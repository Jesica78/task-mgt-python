# task-mgt-python
#def task():
    tasks = []#empty list
    print("WELCOME TO THE TASK MANAGEMENT")
    
    
    total_task = int(input("enter how many task to add"))
    
    for i in range(1, total_task+1):
        task_name = input(f"Enter task {i}: ")#enter  task i =
        tasks.append(task_name)
        
    print(f"\nToday's task are:\n{tasks}") 
    
    
    while True:
        operation = int(input("Enter 1-Add\n2-Update\n3-delete\n4-View\n5-Exit/Stop"))
        if operation ==1:
            add = input("enter task you want to add : ")
            tasks.append(add)
            print(f"Task {add} has been successfully added.") 
        
        elif operation ==2:
            Updated_val = input("Enter the task name you want to update : ")
            if Updated_val in tasks:
                new_task = input(" Enter the new task : ")
                index = tasks.index(Updated_val)
                tasks[index] = new_task
                print(f" task '{Updated_val}'has been successfuly updated")
            else:
               print(f"task '{updated_val}' not found.")
        elif operation ==3:
            del_val = input("Which task do you want to delete ? ")
            if del_val in tasks:
                    task.remove(del_val)
                    print(f" task '{del_val}' has been deleted...")
            else:(f"task'{del_val}' not found")
        elif operation ==4:
           print(f"\ntotal task = {tasks}")
       
        elif operation ==5:
            print("closing the program....")
            break
        
        else:
            print("Invalid Input")
    
