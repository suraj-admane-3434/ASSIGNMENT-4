
# Task 1: Read a File and Handle Errors

try:
    with open("sample.txt", "r") as file:
        for line in file:
            print(line.strip())  # .strip() removes the newline character
except FileNotFoundError:
    print("Error: The file 'sample.txt' does not exist.")
except Exception as e:
    print("An unexpected error occurred:", e)

# Task 2: Write and Append Data to a File

# Step 1: Take user input and write to output.txt
user_input = input("Enter some text to write to the file: ")

with open("output.txt", "w") as file:
    file.write(user_input + "\n")

# Step 2: Append additional data to the same file
additional_input = input("Enter some text to append to the file: ")

with open("output.txt", "a") as file:
    file.write(additional_input + "\n")

# Step 3: Read and display the final content of the file
print("\nFinal content of 'output.txt':")
with open("output.txt", "r") as file:
    for line in file:
        print(line.strip())
        
