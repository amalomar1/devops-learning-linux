# Task 5: Text Processing in Linux

## grep - searching text

Used to find patterns in files.

Commands:
grep "error" /var/log/syslog
grep -r "TODO" ~/projects/
grep -i "failed" /var/log/auth.log | wc -l

---

## awk - column-based processing

Used to extract specific columns from text.

Commands:
ps aux | awk '{print $1, $11}'
cat /etc/passwd | awk -F: '{print $1, $6}'

---

## sed - stream editor

Used to modify text.

Commands:
sed 's/old/new/g' file.txt
sed -n '10,20p' file.txt

---

## Pipes - chaining commands

Used to combine multiple commands together.

Command:
cat /var/log/syslog | grep "error" | awk '{print $1, $2, $3}' | sort | uniq

---

## Challenge: users with /bin/bash shell

Command:
awk -F: '$7 == "/bin/bash" {print $1}' /etc/passwd

---

## What I learned

- grep is used for filtering text
- awk is useful for structured data (columns)
- sed edits text streams
- pipes combine commands into workflows
- /etc/passwd contains system user information
