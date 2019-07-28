# UbuntuTricks

Ub-untu Tips and Tricks

----------------------------

### Table of Contents

> - [User Management](#user-management)
> - [Work with Files](#work-with-files)
> - [Terminal](#terminal)

----------------------------

### User Management

* #### Enter SuperUser mode
  ```bash
  sudo su -
  ```
* #### Change password
  ```bash
  passwd
  # To be abale to use weak passwords, run it after $ sudo su -
  ```

----------------------------

### Terminal

* #### Change bash title (prompt)
  * Temporary test: Put your title after ''PS1='' in terminal
    ```bash
	PS1='test > '
    ```
  * Permanent: Change this line in ~/.bashrc
    ```bash
	PS1='${debian_chroot:+($debian_chroot)}\u@\h:\w\$ '
	# \u -> username
	# \h -> hostname
	# \w -> curr dir
    ```

* #### Replace bash with zsh
  * Install
    ```bash
    sudo apt install zsh
    ```
  * install oh-my-zsh
    ```bash
    sh -c "$(curl -fsSL https://raw.githubusercontent.com/robbyrussell/oh-my-zsh/master/tools/install.sh)"
    ```
  * Customize or enable/disable plugins in .zshrc file, in  your home directory

  * Set zsh as the default shell
  	```bash
      chsh -s /bin/zsh
    ```
  * Set bash as the default shell
  	```bash
      chsh -s /bin/bash
    ```

* #### Change default terminal
  ```bash
  sudo update-alternatives --config x-terminal-emulator
  ```

----------------------------

### Work with Files

* #### Get the type of a file
  ```bash
  file <filename>
  ```

* #### Read text files
  ```bash
  vi <fn>
  cat <fn>
  nano <fn>
  gedit <fn>
  ```

* #### Page by page reading
  ```bash
  cat <fn> | less
  # or
  less <fn>
  # (press 'q' to quit the less mode)
  ```

* #### Count number of lines in a text file
  ```bash
  wc -l <filename>
  ```

* #### Search a text in all text files of a directory
  ```bash
  grep -iRl "your-text"
  # -i - ignore text case
  # -R - recursively search files in subdirectories
  # -l - show file names instead of file contents portions
  # -n - show the line number
  # -w - match the whole word
  ```
