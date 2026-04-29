# patient_system.py
patient-system
patients = []

while True:
    print("\n=== PATIENT RECORD SYSTEM ===")
    print("1. Add Patient")
    print("2. View Patients")
    print("3. Exit")

    choice = input("Choose an option: ")

    if choice == "1":
        name = input("Enter patient name: ")
        age = input("Enter patient age: ")

        patient = {
            "name": name,
            "age": age
        }

        patients.append(patient)
        print("✅ Patient added successfully!")

    elif choice == "2":
        if len(patients) == 0:
            print("No patients found.")
        else:
            print("\nPatient List:")
            for p in patients:
                print(f"Name: {p['name']}, Age: {p['age']}")

    elif choice == "3":
        print("Goodbye 👋")
        break

    else:
        print("❌ Invalid option. Try again.")
