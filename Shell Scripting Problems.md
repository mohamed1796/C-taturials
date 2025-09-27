## 🔹 10 Shell Scripting Problems (File Manipulation & Command Practice)

1. **Create and Redirect Output**
   Write a script that lists all files in the current directory and redirects the output to a file named `file_list.txt`. Then append the current date to the same file.

2. **Check File Existence**
   Write a script that prompts the user to enter a filename. If the file exists and is readable, display its contents with `cat`. If it does not exist, display an error message.

3. **Count Lines in a File**
   Write a script that asks the user for a file name and counts the number of lines in the file using `wc -l`. If the line count is greater than 50, display a message `"File is large"`, otherwise `"File is small"`.

4. **Backup Files**
   Write a script that creates a backup of all `.txt` files in the current directory into a folder called `backup/`. If the folder does not exist, create it.

5. **Search for a Pattern**
   Write a script that asks the user for a search keyword and a file name, then uses `grep` to check if the keyword exists inside the file. If found, print `"Keyword found"`; otherwise, print `"Not found"`.

6. **Compare Two Files**
   Write a script that takes two filenames as arguments and compares them. If they are the same, print `"Files are identical"`, otherwise `"Files differ"`.

7. **File Size Check**
   Write a script that checks whether a given file is empty (`-z`) or not empty (`-s`). Print an appropriate message for each case.

8. **Loop Through Directory**
   Write a script that loops through all files in `/etc` and prints their names until it reaches the file `/etc/hosts`, then stops.

9. **Redirection with Errors**
   Write a script that tries to sort a non-existing file and redirects the error message to `error_log.txt`. Display the contents of `error_log.txt` after execution.

10. **Create a Menu-Driven File Manager**
    Write a script that displays a simple menu with options:

* `1. View contents of a file`
* `2. Count words in a file`
* `3. Check if file exists`
* `4. Exit`
  The script should execute the chosen option using appropriate commands.

---

⚡ Each of these problems uses **file manipulation commands** (`cat`, `wc`, `grep`, `sort`, `ls`, `cp`, `mkdir`) and integrates **redirection, conditionals, and loops** as covered in your Lab4 material.
