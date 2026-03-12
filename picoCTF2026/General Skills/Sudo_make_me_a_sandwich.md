# [SUDO MAKE ME A SANDWICH]
**Category:** General Skills
**Points:** 50

### 1. Challenge Description
The challenge tasks you with reading the flag.txt file on a linux machine.

### 2. My Approach
*   **Initial Thought:** I tried `sudo cat flag.txt` but I didn't have the correct permissions.
*   **Research:** I searched for "how to check user permissions in Linux" and found the `sudo -l` command.
*   **Execution:** I discovered that I had access to one specific command, /bin/emacs. Upon using this I discovered that it was a text editor, and used it to open the flag.txt file, and read the flag in plaintext.

### 3. Commands Used
```bash
sudo cat flag.txt
sudo -l
sudo emacs flag.txt
