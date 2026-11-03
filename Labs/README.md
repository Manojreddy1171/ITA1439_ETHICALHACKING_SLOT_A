# ITA1439 - Ethical Hacking Laboratory

This directory contains the laboratory exercises and command demonstrations conducted in Kali Linux.

---

## List of Experiments

| Exp No. | Target Commands | Aim / Objective |
|:-------:|:----------------|:----------------|
| **1** | `rm`, `users`, `tree` | File deletion, viewing logged-in users, and displaying directory structures |
| **2** | `less`, `more`, `vi` | Viewing and editing text files interactively in terminal |
| **3** | `tree`, `head`, `tail` | Directory hierarchy display and viewing top/bottom lines of files |
| **4** | `ls`, `cat`, `mkdir` | Listing directory contents, reading file text, and creating folders |
| **5** | `uptime`, `date`, `mv` | Checking system uptime, inspecting date/time, and renaming/moving files |
| **6** | `touch`, `pwd`, `wget` | Creating blank files, printing working directory, and web downloading |
| **7** | `cd`, `cp`, `ls` | Directory navigation, copying files, and listing files |

---

### Experiment 1: File Deletion, User Enumeration & Directory Tree
- **Commands:** `rm`, `users`, `tree`
- **AIM:** To execute and understand the `rm`, `users`, and `tree` commands in Kali Linux.
- **Procedure:**
  ```bash
  # 1. rm - Remove a file
  touch test.txt
  ls
  rm test.txt
  ls

  # 2. users - Display logged-in users
  users

  # 3. tree - Display directory structure
  mkdir -p lab/docs
  touch lab/file1.txt lab/docs/file2.txt
  tree lab
  ```
- **Result:** The `rm`, `users`, and `tree` commands were executed to delete files, display logged-in users, and view the directory structure.

---

### Experiment 2: File Viewing and Terminal Text Editing
- **Commands:** `less`, `more`, `vi`
- **AIM:** To execute the `less`, `more`, and `vi` commands to view and edit text files in Kali Linux.
- **Procedure:**
  ```bash
  # Step 1: Create a sample file
  printf "Line 1\nLine 2\nLine 3\nLine 4\nLine 5\n" > sample.txt

  # 1. less - View file contents (Press 'q' to exit)
  less sample.txt

  # 2. more - View file page by page (Press 'q' to exit)
  more sample.txt

  # 3. vi - Edit a file
  cd ~
  vi myfile.txt
  # Inside editor:
  # Press 'i' to enter insert mode
  # Type: Hello Kali Linux
  # Press 'Esc'
  # Type ':wq' and press Enter

  # Verify file content:
  cat myfile.txt
  ```
- **Result:** The `less`, `more`, and `vi` commands were executed to view, edit, and save text files.

---

### Experiment 3: Tree Inspection, File Headers and Footers
- **Commands:** `tree`, `head`, `tail`
- **AIM:** To execute the `tree`, `head`, and `tail` commands to display directory structures and file contents in Kali Linux.
- **Procedure:**
  ```bash
  # 1. tree - Display directory hierarchy
  mkdir -p lab/docs
  touch lab/file1.txt lab/docs/file2.txt
  tree lab

  # 2. head - Display the first three lines
  printf "Line 1\nLine 2\nLine 3\nLine 4\nLine 5\n" > sample.txt
  head -n 3 sample.txt

  # 3. tail - Display the last three lines
  tail -n 3 sample.txt
  ```
- **Result:** The `tree`, `head`, and `tail` commands were executed to display directory hierarchy and beginning/ending lines of files.

---

### Experiment 4: Directory Listing, Concatenation & Folder Creation
- **Commands:** `ls`, `cat`, `mkdir`
- **AIM:** To execute the `ls`, `cat`, and `mkdir` commands to list files, display file contents, and create directories in Kali Linux.
- **Procedure:**
  ```bash
  # 1. ls - List files and directories
  ls
  ls -l
  ls -a

  # 2. cat - Display file contents
  echo "Welcome to Kali Linux" > file.txt
  cat file.txt

  # 3. mkdir - Create a directory
  mkdir -p hacking_lab
  ls
  ```
- **Result:** The `ls`, `cat`, and `mkdir` commands were executed to list files, display file contents, and create a new directory.

---

### Experiment 5: System Uptime, Date & Renaming Files
- **Commands:** `uptime`, `date`, `mv`
- **AIM:** To execute the `uptime`, `date`, and `mv` commands to display system information and rename files in Kali Linux.
- **Procedure:**
  ```bash
  # 1. uptime - Display system uptime
  uptime

  # 2. date - Display current date and time
  date
  date "+%d-%m-%Y"

  # 3. mv - Rename a file
  touch old.txt
  mv old.txt new.txt
  ls
  ```
- **Result:** The `uptime`, `date`, and `mv` commands were executed to display system uptime, check date/time, and rename files.

---

### Experiment 6: Creating Files, Printing Working Directory & Remote Fetch
- **Commands:** `touch`, `pwd`, `wget`
- **AIM:** To execute the `touch`, `pwd`, and `wget` commands to create files, display current directory, and download files in Kali Linux.
- **Procedure:**
  ```bash
  # 1. touch - Create an empty file
  touch report.txt
  ls

  # 2. pwd - Display current working directory
  pwd

  # 3. wget - Download a webpage (requires network connection)
  wget -O test.html https://example.com/
  ls
  ```
- **Result:** The `touch`, `pwd`, and `wget` commands were executed to create an empty file, display current directory, and download a webpage.

---

### Experiment 7: Directory Navigation, Copying & Verification
- **Commands:** `cd`, `cp`, `ls`
- **AIM:** To execute the `cd`, `cp`, and `ls` commands to navigate directories, copy files, and list directory contents in Kali Linux.
- **Procedure:**
  ```bash
  # 1. cd - Change directory
  cd ~
  mkdir -p test_folder
  cd test_folder
  pwd

  # 2. cp - Copy a file
  echo "Hello Kali Linux" > sample.txt
  cp sample.txt backup.txt
  ls

  # 3. ls - List files and directories
  ls
  ls -l
  ```
- **Result:** The `cd`, `cp`, and `ls` commands were executed to navigate directories, copy files, and display directory contents.

