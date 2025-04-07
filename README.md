# python-week-4-assignment

def modify_file(filename):
    try:
        with open(filename, 'r') as file:
            content = file.read()
            modified_content = content.upper()
            
        with open('modified_' + filename, 'w') as new_file:
            new_file.write(modified_content)
        print("Modified file created successfully.")
    except FileNotFoundError:
        print(f"File {filename} not found.")
    except Exception as e:
        print(f"An error occurred: {e}")
filename = input("Enter the filename: ")
modify_file(filename)
