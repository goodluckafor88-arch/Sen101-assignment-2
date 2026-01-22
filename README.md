voters = []

def register_voter():
    name = input("Enter voter name: ")
    voter_id = input("Enter voter ID: ")
    voters.append({"name": name, "voter_id": voter_id})
    print("Voter registered successfully")

def view_voters():
    if not voters:
        print("No voters registered")
    else:
        for v in voters:
            print("Name:", v["name"], "| Voter ID:", v["voter_id"])

def main():
    while True:
        print("1. Register Voter")
        print("2. View Voters")
        print("3. Exit")

        choice = input("Choose option: ")

        if choice == "1":
            register_voter()
        elif choice == "2":
            view_voters()
        elif choice == "3":
            break
        else:
            print("Invalid option")

main()
