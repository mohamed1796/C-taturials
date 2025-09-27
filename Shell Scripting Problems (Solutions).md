## ✅ Solutions to 10 Shell Scripting Problems

---

### **1. Create and Redirect Output**

```bash
#!/bin/bash
# List files and append date

ls > file_list.txt
date >> file_list.txt
echo "Files listed and date appended to file_list.txt"
```

---

### **2. Check File Existence**

```bash
#!/bin/bash
# Check if file exists and readable

echo -n "Enter filename: "
read filename

if [ -f "$filename" ] && [ -r "$filename" ]; then
    cat "$filename"
else
    echo "Error: File does not exist or is not readable."
fi
```

---

### **3. Count Lines in a File**

```bash
#!/bin/bash
# Count lines and check size

echo -n "Enter filename: "
read filename

if [ -f "$filename" ]; then
    lines=$(wc -l < "$filename")
    echo "File has $lines lines"
    if [ "$lines" -gt 50 ]; then
        echo "File is large"
    else
        echo "File is small"
    fi
else
    echo "File not found"
fi
```

---

### **4. Backup Files**

```bash
#!/bin/bash
# Backup all .txt files

mkdir -p backup
cp *.txt backup/ 2>/dev/null
echo "All .txt files copied to backup/ directory"
```

---

### **5. Search for a Pattern**

```bash
#!/bin/bash
# Search keyword in file

echo -n "Enter filename: "
read file
echo -n "Enter keyword: "
read keyword

if grep -q "$keyword" "$file" 2>/dev/null; then
    echo "Keyword found"
else
    echo "Not found"
fi
```

---

### **6. Compare Two Files**

```bash
#!/bin/bash
# Compare two files

if [ $# -ne 2 ]; then
    echo "Usage: $0 file1 file2"
    exit 1
fi

if cmp -s "$1" "$2"; then
    echo "Files are identical"
else
    echo "Files differ"
fi
```

---

### **7. File Size Check**

```bash
#!/bin/bash
# Check if file is empty

echo -n "Enter filename: "
read file

if [ -z "$file" ]; then
    echo "No filename entered"
    exit 1
fi

if [ -f "$file" ]; then
    if [ -z "$file" ]; then
        echo "File is empty"
    else
        echo "File is not empty"
    fi
else
    echo "File does not exist"
fi
```

---

### **8. Loop Through Directory**

```bash
#!/bin/bash
# Loop until /etc/hosts

for f in /etc/*; do
    echo "$f"
    if [ "$f" = "/etc/hosts" ]; then
        echo "Reached /etc/hosts, stopping..."
        break
    fi
done
```

---

### **9. Redirection with Errors**

```bash
#!/bin/bash
# Redirect error message

sort non_existing_file.txt 2> error_log.txt
echo "Error log saved. Contents:"
cat error_log.txt
```

---

### **10. Menu-Driven File Manager**

```bash
#!/bin/bash
# Simple file manager

while true; do
    echo "------ File Manager ------"
    echo "1. View contents of a file"
    echo "2. Count words in a file"
    echo "3. Check if file exists"
    echo "4. Exit"
    echo -n "Choose option: "
    read choice

    case $choice in
        1) echo -n "Enter filename: "; read file
           [ -f "$file" ] && cat "$file" || echo "File not found"
           ;;
        2) echo -n "Enter filename: "; read file
           [ -f "$file" ] && wc -w < "$file" || echo "File not found"
           ;;
        3) echo -n "Enter filename: "; read file
           [ -e "$file" ] && echo "File exists" || echo "File does not exist"
           ;;
        4) echo "Exiting..."; exit 0 ;;
        *) echo "Invalid choice" ;;
    esac
done
```
* `ls`, `cat`, `wc`, `grep`, `cmp`, `sort`, `cp`, `mkdir`
* Redirection (`>`, `>>`, `2>`), Conditionals (`if`), and Loops (`for`, `while`).

---

Do you want me to also **bundle these scripts into a single PDF or `.zip` with `.sh` files** so you can run them directly?
