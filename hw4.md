## Homework: 4 The Linux Filesystem
Watch the video **“Linux Filesystem Explained”** and read the presentation **“How to navigate the filesystem”** then answer the questions below.

**1. Explain the difference between absolute path and relative path:** The difference between the two paths are absolute path states the full path name from the root directory. Where as relative path specifies the path name from the current directory.

**2. Why Linux uses / instead of \ for its directory paths?** 
* Linux follows UNIX traditions which is why it uses the forward slash instead of the back slash like windows.

**3. In Windows, these files are all the same: File FILE file and FiLE. But in Linux this is not the case, Why?**
* In Linux, they care about capitalization which is why linux will allow this because they're technically not named exactly the same.

**4. What is the Filesystem Hierarchy Standard (FHS) and who maintains it?**
* It defines the structure and layout for file/directory placement and is maintained by the Linux Foundation.

**5. Explain what type of files are stored in the following directories:**

Directory | What is it used for?
----------|---------------------
/bin | : Contains binary commands such has ls, cat and can be accessed in single user mode.
/dev | : This is where your devices are located such as your webcam or keyboard.
/etc | : This folder is where all your configurations are stored such as apt.
/home | : Each user has it's own folder in the home directory. Contains many different directories which stores your application settings. 
/lib | : This is where shared libraries are stored.
/opt | : Usually contains manually installed software from vendors and software packages such as virtualbox.
/tmp | : This is where files are temporarily stored by applications that can be used during a session. This folder is usually empty when you reboot the system.
/var | : Variable directory that contains files and directories that are expected to grow in size. EX. var crash
/proc | : It is where you'll find pseudo files that contain information about system processing and resources
/usr | : This is where applications are installed that are used by the user. Contains shareable, read-only applications and files.

**6. How does a period at the beginning of a file name means (example .bashrc)?** 
* It means that the file is a hidden file because it starts with a "."

**7. Which command would you use to list all the files inside the /usr/share/ directory?**
* cd / | ls usr/share

**8. If you are working in the /usr/share/icons directory and want to move to your home directory, which command would you use?**
* cd

**9. Explain what these commands do:**

cd .config/.htop; cd ../; ls -lX

* **cd .config/.htop** - This command will change your directory from the current to .htop.

* **cd ../** - This command will make you go back one directory.

* **ls -lX** - This command will long list the current directory by extension.

**10. John has a lot of files in the directory /var/www/html/webapp. He wants to long list all the files, including hidden files, by modification time (newest first), and with human-readable file sizes. Which command should he use conjuring that his current working directory is:**

/home/john/.git/

* ls -ath /var/www/html/webapp