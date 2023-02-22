## Laravel Environment Setup

### Mac

#### 1. Install [XAMPP](https://www.apachefriends.org/download.html) version ^8.1 or ^8.2 for Mac, if you haven't already.

#### 2. Make PHP executable from any folder by following these steps:

##### Update `~/.bash_profile`
1. Open the Terminal app on your Mac.
2. Type the following command to open your shell configuration file in the nano editor:
    ```shell
    nano ~/.bash_profile
    ```
   This will open the .bash_profile file in the nano editor.
3. Scroll to the end of the file and add the following line:
    ```shell
    export PATH="/Applications/XAMPP/xamppfiles/bin:$PATH"
    ```
    This line adds the path to the PHP binary file in XAMPP to your system's PATH environment variable.
4. On your keyboard, press `Control + O` to save the file, then `Control + X` to exit nano.
5. To make the changes take effect, type the following command:
    ```shell
    source ~/.bash_profile
    ```
   This command reloads your shell configuration file.


##### Update `~/.bashrc`
1. Open the Terminal app on your Mac.
2. Type the following command to open your `.bashrc` file in the nano editor:
    ```shell
   nano ~/.bashrc
    ```
   If the file does not exist, create it by running `touch ~/.bashrc` first.
3. Scroll to the end of the file and add the following line:
   ```shell
   export PATH="/Applications/XAMPP/xamppfiles/bin:$PATH"
   ```
   This line adds the path to the PHP binary file in XAMPP to your system's PATH environment variable.
4. On your keyboard, press `Control + O` to save the file, then `Control + X` to exit nano.
5. To make the changes take effect, close and reopen the Terminal app.


#### 3. Install composer by following these steps:
1. Open the Terminal app on your Mac.
2. Navigate to your home directory by typing the following command:
   ```shell
   cd ~
   ```
3. Download the latest version of Composer by typing the following command:
   ```shell
   php -r "copy('https://getcomposer.org/installer', 'composer-setup.php');"
   ```
4. Verify the downloaded installer by running the following command:
   ```shell
   php -r "if (hash_file('sha384', 'composer-setup.php') === '55ce33d7678c5a611085589f1f3ddf8b3c52d662cd01d4ba75c0ee0459970c2200a51f492d557530c71c15d8dba01eae') { echo 'Installer verified'; } else { echo 'Installer corrupt'; unlink('composer-setup.php'); } echo PHP_EOL;"
   ```
   This command checks if the downloaded installer matches the expected hash and prints "Installer verified" if it does.
5. Run the installer by typing the following command:
   ```shell
   php composer-setup.php --install-dir=/usr/local/bin --filename=composer
   ```
   This command installs Composer globally in your system's `/usr/local/bin` directory and creates a symlink named `composer` that points to the Composer binary.
6. Verify that Composer is installed correctly by typing the following command:
   ```shell
   composer --version
   ```
   This command should output the version of Composer installed.

#### 4. Make `composer` executable global.
1. Open the Terminal app on your Mac.
2. Navigate to your home directory by typing the following command:
   ```shell
   cd ~
   ```
3. Open the `.bash_profile` file in a text editor by typing the following command:
   ```shell
   nano .bash_profile
   ```
4. Scroll to the end of the file and add the following line:
   ```shell
   export PATH="$PATH:$HOME/.composer/vendor/bin"
   ```
   This line adds the Composer binary directory to your system's `PATH` environment variable. The `~/.composer/vendor/bin` directory is where Composer installs global packages and creates symlinks to executable files.
5. Press `Control + O` to save the file, then `Control + X` to exit nano.
6. To make the changes take effect, either open a new Terminal window or run the following command:
   ```shell
   source ~/.bash_profile
   ```
   This command reloads the `.bash_profile` file and updates the `PATH` environment variable.
   
   
