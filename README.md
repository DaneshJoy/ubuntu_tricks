# UbuntuTricks

Ub-untu Tips and Tricks

----------------------------

### Table of Contents

> - [User Management](#user-management)
> - [Work with Files](#work-with-files)

----------------------------

### User Management

* Enter SuperUser mode
  ```bash
  sudo su -
  ```
* Change password
  ```bash
  passwd
  # To be abale to use weak passwords, run it after $ sudo su -
  ```

----------------------------

### Work with Files

* Type of a file
  ```bash
  file <filename>
  ```

* Read text file
  ```bash
  vi <fn>
  cat <fn>
  nano <fn>
  gedit <fn>
  ```

* Page by page reading
  ```bash
  cat <fn> | less
  # or
  less <fn>
  # (press 'q' to quit the less mode)
  ```

* Count number of lines in a file
  ```bash
  wc -l <filename>
  ```

* Search a text in all files of a directory
  ```bash
  grep -iRl "your-text"
  # -i - ignore text case
  # -R - recursively search files in subdirectories
  # -l - show file names instead of file contents portions
  # -n - show the line number
  # -w - match the whole word
  ```
