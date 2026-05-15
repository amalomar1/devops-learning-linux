## Changing File Permissions
I used the `chmod` command to change the permissions of the file.

Command used:
chmod 644 hello.sh

The permission `644` means:
- Owner can read and write
- Group can only read
- Others can only read

---

## Viewing File Permissions
I used the `ls -l` command to display the file permissions and file details.

Command used:
ls -l hello.sh

Output:
-rw-r--r-- 1 amalomar staff 32 May 13 14:04 hello.sh

Permission breakdown:
- rw- = owner permissions (read and write)
- r-- = group permissions (read only)
- r-- = others permissions (read only)

This completed the challenge requirement to create a file that only I can read/write while others can only read.
