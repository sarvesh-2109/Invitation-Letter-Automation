# Invitation-Letter-Automation
This Python project automates the process of generating personalized invitation letters for multiple recipients. It's a great example of how Python can be used to streamline repetitive tasks, making your life easier.

## Key Concepts and Learnings

### File Handling
The project utilizes Python's file handling capabilities to read the list of recipient names from one file and the template letter from another.

```python
with open("./Input/Names/invited_names.txt") as names_file:
    names = names_file.readlines()
```

```python
with open("./Input/Letters/starting_letter.txt") as letter_file:
    letter_content = letter_file.read()
```

### String Manipulation
Through string manipulation, each recipient's name is dynamically replaced in the letter template using Python's `.replace()` method.

```python
new_letter = letter_content.replace(PLACEHOLDER, stripped_name)
```

### File Output
Python is used to create individual invitation letters for each recipient and save them in separate files.

```python
with open(f"./Output/ReadyToSend/letter_for_{stripped_name}.txt", mode="w") as completed_letter:
    completed_letter.write(new_letter)
```

### Automation
This project demonstrates how Python can automate repetitive tasks, especially when dealing with a large number of documents. It's modular, easy to understand, and can be adapted for various applications.

## Usage

1. Prepare your list of recipient names in `invited_names.txt`.
2. Customize your letter template in `starting_letter.txt`, using `[name]` as a placeholder for the recipient's name.
3. Run the Python script, and personalized invitation letters will be generated and saved in the `./Output/ReadyToSend/` directory.

Feel free to explore, use, and adapt this project for your own automation needs. Automation with Python opens up endless possibilities and simplifies your work.

If you find this project helpful, please consider giving it a star on GitHub.
