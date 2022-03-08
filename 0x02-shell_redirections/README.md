# General Requirements
* Allowed editors: vi, vim, emacs
* All your scripts will be tested on Ubuntu 20.04 LTS
* All your scripts should be exactly two lines long ($ wc -l file should print 2)
* All your files should end with a new line (why?)
* The first line of all your files should be exactly #!/bin/bash
* A README.md file, at the root of the folder of the project, describing what each script is doing
* You are not allowed to use backticks, &&, || or ;
* All your files must be executable
* You are not allowed to use sed or awk

# More Info
Read your /etc/passwd and /etc/shadow files.<br>
Note: You do not have to learn about fmt, pr, du, gzip, tar, lpr, sed and awk yet.<br>


# Tasks

# 0. Hello World
Write a script that prints “Hello, World”, followed by a new line to the standard output.<br>

julien@ubuntu:/tmp/h$ ./0-hello_world<br>
Hello, World<br>
julien@ubuntu:/tmp/h$ ./0-hello_world | cat -e<br>
Hello, World$<br>
julien@ubuntu:/tmp/h$<br>

# 1. Confused Smiley
Write a script that displays a confused smiley "(Ôo)'.<br>

julien@ubuntu:/tmp/h$ ./1-confused_smiley<br>
"(Ôo)'<br>
julien@ubuntu:/tmp/h$<br> 

# 2. Let's display file
Display the content of the /etc/passwd file.<br>


# 3. What about 2?
Display the content of /etc/passwd and /etc/hosts<br>


# 4. Last lines of a file
Display the last 10 lines of /etc/passwd<br>

Tips: “Thinks of it as a cat, what is at the end of it?”<br>

# 5. I'd prefer the first ones actually
Display the first 10 lines of /etc/passwd<br>


# 6. Line #2
Write a script that displays the third line of the file iacta.<br>

The file iacta will be in the working directory

* You’re not allowed to use sed

Note: The output will differ, depending on the content of the file iacta.<br>

# 7. It is a good file that cuts iron without making a noise
Write a shell script that creates a file named exactly \ * \ \ ' " Best School " \   ' \ \ * $ \ ? \ * \ * \ * \ * \ * : ) containing the text Best School ending by a new line.


# 8. Save current state of directory
Write a script that writes into the file ls_cwd_content the result of the command ls -la. If the file ls_cwd_content already exists, it should be overwritten. If the file ls_cwd_content does not exist, create it.


# 9. Duplicate last line
Write a script that duplicates the last line of the file iacta

* The file iacta will be in the working directory


# 10. No more javascript
Write a script that deletes all the regular files (not the directories) with a .js extension that are present in the current directory and all its subfolders.<br>


# 11. Don't just count your directories, make your directories count
Write a script that counts the number of directories and sub-directories in the current directory.

* The current and parent directories should not be taken into account
* Hidden directories should be counted


# 12. What’s new
Create a script that displays the 10 newest files in the current directory.<br>
<br>
Requirements:<br>
* One file per line
* Sorted from the newest to the oldest


# 13. Being unique is better than being perfect
Create a script that takes a list of words as input and prints only words that appear exactly once.<br>

* Input format: One line, one word
* Output format: One line, one word
* Words should be sorted


# 14. It must be in that file
Display lines containing the pattern “root” from the file /etc/passwd


# 15. Count that word
Display the number of lines that contain the pattern “bin” in the file /etc/passwd<br>

$ ./15-countthatword<br>
81<br>
$ <br>


# 16. What's next?
Display lines containing the pattern “root” and 3 lines after them in the file /etc/passwd.


# 17. I hate bins
Display all the lines in the file /etc/passwd that do not contain the pattern “bin”.

# 18.  Letters only please
Display all lines of the file /etc/ssh/sshd_config starting with a letter.
* include capital letters as well


# 19. A to Z
Replace all characters A and c from input to Z and e respectively.<br>

 julien@ubuntu:/tmp/0x02$ echo 'Replace all characters `A` and `c` from input to `Z` and `e`.' | ./19-AZ <br>
Replaee all eharaeters `Z` and `e` from input to `Z` and `e`.<br>
julien@ubuntu:/tmp/0x02$ <br>

# 20. Without C, you would live in hiago
Create a script that removes all letters c and C from input.<br>

julien@ubuntu:/tmp/0x02$ echo Chicago | ./20-hiago <br>
hiago<br>
julien@ubuntu:/tmp/0x02$ <br>


# 21. esreveR
Write a script that reverse its input.<br>

julien@ubuntu:/tmp/0x02$ echo "Reverse" | ./21-reverse <br>
esreveR<br>
julien@ubuntu:/tmp/0x02$ <br>

# 22. DJ Cut Killer
Write a script that displays all users and their home directories, sorted by users.
* Based on the the /etc/passwd file

# 23. Change group
Write a command that finds all empty files and directories in the current directory and all sub-directories.

* Only the names of the files and directories should be displayed (not the entire path)
* Hidden files should be listed
* One file name per line
* The listing should end with a new line
* You are not allowed to use basename, grep, egrep, fgrep or rgrep


# 24. A gif is worth ten thousand words
Write a script that lists all the files with a .gif extension in the current directory and all its sub-directories.

* Hidden files should be listed
* Only regular files (not directories) should be listed
* The names of the files should be displayed without their extensions
* The files should be sorted by byte values, but case-insensitive (file aaa should be listed before file bbb, file .b should be listed before file a, and file Rona should be listed after file jay)
* One file name per line
* The listing should end with a new line
* You are not allowed to use basename, grep, egrep, fgrep or rgrep


# 25. Acrostic
An acrostic is a poem (or other form of writing) in which the first letter (or syllable, or word) of each line (or paragraph, or other recurring feature in the text) spells out a word, message or the alphabet. The word comes from the French acrostiche from post-classical Latin acrostichis). As a form of constrained writing, an acrostic can be used as a mnemonic device to aid memory retrieval. Read more.<br>

Create a script that decodes acrostics that use the first letter of each line.<br>

* The ‘decoded’ message has to end with a new line
* You are not allowed to use grep, egrep, fgrep or rgrep

# 26. The biggest fan
Write a script that parses web servers logs in TSV format as input and displays the 11 hosts or IP addresses which did the most requests.

* Order by number of requests, most active host or IP at the top
* You are not allowed to use grep, egrep, fgrep or rgrep

# 
