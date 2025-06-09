# ASSIGNMENT-4

# Task 1: Read a File and Handle Errors
try:
    with open("sample.txt", "r") as file:
        print("Contents of sample.txt:")
        for line in file:
            print(line.strip())
except FileNotFoundError:
    print("Error: sample.txt file does not exist.")

# Task 2: Write and Append Data to a File
try:
    user_input = input("\nEnter some text to write into output.txt: ")
    with open("output.txt", "w") as file:
        file.write(user_input + "\n")

    additional_input = input("Enter additional text to append: ")
    with open("output.txt", "a") as file:
        file.write(additional_input + "\n")

    print("\nFinal content of output.txt:")
    with open("output.txt", "r") as file:
        for line in file:
            print(line.strip())
except Exception as e:
    print(f"An unexpected error occurred: {e}")

######################################################################################################################################################################
