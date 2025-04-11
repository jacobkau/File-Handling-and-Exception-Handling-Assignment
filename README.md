# File-Handling-and-Exception-Handling-Assignment
Week 4 assignment

# File Read & Write Challenge
# Write to a file
with open("original.txt", "w") as file:
    file.write("This is the original content.\nIt will be modified.")

# Read the file and write a modified version
with open("original.txt", "r") as file:
    content = file.read()

modified_content = content.replace("original", "modified")

with open("modified.txt", "w") as new_file:
    new_file.write(modified_content)

# Error Handling Lab
filename = input("Enter a filename to read: ")

try:
    with open(filename, "r") as user_file:
        print("\nFile content:")
        print(user_file.read())
except FileNotFoundError:
    print("Error: File not found.")
except IOError:
    print("Error: File cannot be read.")
