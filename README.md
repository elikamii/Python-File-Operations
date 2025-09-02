# main.py

def create_and_write_file(filename, content):
    """Creates a new file and writes content to it."""
    try:
        with open(filename, 'w') as file:
            file.write(content)
    except IOError as e:
        print(f"An error occurred: {e}")

def read_file(filename):
    """Reads and prints the content of a file."""
    try:
        with open(filename, 'r') as file:leNotFoundError:
        print(f"Error: The file '{filename}' was not found.")
    except IOError as e:
        print(f"An error occurred: {e}")

def append_to_file(filename, new_content):
    """Appends new content to an existing file."""
    try:
        with open(filename, 'a') as file:
            file.write("\n" + new_content)
        print(f"\nContent appended to '{filename}' successfully.")
    except IOError as e:
        print(f"An error occurred: {e}")

if __name__ == "__main__":
    file_name = "example.txt"
    file_content = "This is the first line.\nThis is the second line."
    
    create_and_write_file(file_name, file_content)
    read_file(file_name)
    
    new_text_to_add = "This is a new line appended to the file."
    append_to_file(file_name, new_text_to_add)
    read_file(file_name)
