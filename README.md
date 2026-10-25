# Expense--Tracker
You are required to build a simple personal finance management The program should allow the user to:
expence = [] # list of expences in from of dictionary

expenceslist = []

while True:
    print("\n==== KHARCHA SYSTEM ====")
    print("1. Add kharcha")
    print("2. View kharcha")
    print("3. Total kharcha")
    print("4. Exit")

    choice = int(input("Enter Choice: "))

    if choice == 1:
        date = input("kis date kharcha kiya tha?: ")
        category = input("kis type ka kharcha kiya? (food, travle, makeup, book): ")
        description = input("aur detals dedo: ")
        amount = float(input("enter your amount: "))

        Expenses = {
            "date": date,
            "category": category,
            "description": description,
            "amount": amount,
        }
        expenceslist.append(Expenses)
        print("\n DONE bor. expences is add succesfully")

    elif choice == 2:
        if len(expenceslist) == 0:
            print(" no expences added. jou pehle kharcha karo.")
        else:
            print("====ye y apka sara expences====")
            count = 1
            for eachkharcha in expenceslist:
                print(f"kharcha numbar {count} -> {eachkharcha['date']}, {eachkharcha['category']}, {eachkharcha['description']}, {eachkharcha['amount']}")
                count += 1

    elif choice == 3:
        total = 0
        for eachkharcha in expenceslist:
            total = total + eachkharcha["amount"]
        print("\n TOTAL KHARCHA =", total)

    elif choice == 4:
        print("dhanyawad appbe humara system use kiya")
        break

    else:
        print("INVALTED CHOICE. TRY AGANE")
