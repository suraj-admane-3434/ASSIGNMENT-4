# Assignment 4: Files, Exceptions, and Errors in Python
# Task 1: Read a File and Handle Errors

def read_file():
    try:
        with open("sample.txt", "r") as file:
            print("Reading 'sample.txt' content:\n")
            for line in file:
                print(line.strip())
    except FileNotFoundError:
        print("Error: 'sample.txt' file not found. Please make sure the file exists in the same directory.")

# Main execution
if __name__ == "__main__":
    read_file()

# Task 2: Write and Append Data to a File
def write_and_append_file():
    # Step 1: Write user input to output.txt
    user_input = input("Enter something to write to 'output.txt': ")
    with open("output.txt", "w") as file:
        file.write(user_input + "\n")

    # Step 2: Append additional data
    additional_data = input("Enter additional data to append: ")
    with open("output.txt", "a") as file:
        file.write(additional_data + "\n")

    # Step 3: Read and display final content
    print("\nFinal content of 'output.txt':")
    with open("output.txt", "r") as file:
        for line in file:
            print(line.strip())

# Main Program Execution
if __name__ == "__main__":
    print("=== Task 1: Read File ===")
    read_file()

    print("\n=== Task 2: Write and Append to File ===")
    write_and_append_file()
