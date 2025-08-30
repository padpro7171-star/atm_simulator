# atm_simulator
 A simple Python-based billing system that collects seller and customer details,  takes purchased items and prices, and generates a formatted invoice.


 
 #ATM_SIMULATOR
print("====== WELCOME TO YES BANK ATM ======")

#choose option
balance = 5000
print("\nChoose an option: ")
print("1. Check Balance")
print("2. Deposit Money")
print("3. Withdraw Money")
print("4. Exit")

choice = input("Enter choice (1-4): ")

#Check balance
if choice == "1":
    pin = input("Enter PIN: ")   
    if pin == "9345":
        print("-----------------------------------")            
        print("Your balance is:", balance)
    else:
        print("Invalid PIN")
        
#Deposite money        
elif choice == "2":
    amount = float(input("Enter an deposite Amount: " ))
    pin = input("Enter PIN: ") 
    if pin == "9345":
       balance += amount
       print(f"₹ {amount} Deposited successfully" )
       print("-----------------------------------")
    
       print("Total balance:₹ ",balance)
    else:
        print("Invalid pin")

#Withraw money        
elif choice == "3":
        amount = float(input("Enter Withraw amount:₹"))
        pin = input("Enter pin: ")
        if pin == "9345":
            balance -= amount
            print(f"₹ {amount} Withraw sucessfully")
            print("-----------------------------------")
        
            print("Balance amount: ", balance)
        else:
            print("Invalid pin")
            
#Exit            
elif choice == "4":
    print("----------THANK YOU FOR USING YES BANK ATM-----------")
    
else:
   print("-----------------------------------")
   print("Invalid choice! please try again")
