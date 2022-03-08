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

Example:<br>

$ ./2-hellofile<br>
##<br>
# User Database<br>
#<br>
# Note that this file is consulted directly only when the system is running<br>
# in single-user mode. At other times this information is provided by<br>
# Open Directory.<br>
#<br>
# See the opendirectoryd(8) man page for additional information about<br>
# Open Directory.<br>
##<br>
nobody:*:-2:-2:Unprivileged User:/var/empty:/usr/bin/false<br>
root:*:0:0:System Administrator:/var/root:/bin/sh<br>
daemon:*:1:1:System Services:/var/root:/usr/bin/false<br>
_uucp:*:4:4:Unix to Unix Copy Protocol:/var/spool/uucp:/usr/sbin/uucico<br>
_taskgated:*:13:13:Task Gate Daemon:/var/empty:/usr/bin/false<br>
_networkd:*:24:24:Network Services:/var/networkd:/usr/bin/false<br>
_installassistant:*:25:25:Install Assistant:/var/empty:/usr/bin/false<br>
_lp:*:26:26:Printing Services:/var/spool/cups:/usr/bin/false<br>
_postfix:*:27:27:Postfix Mail Server:/var/spool/postfix:/usr/bin/false<br>
_scsd:*:31:31:Service Configuration Service:/var/empty:/usr/bin/false<br>
_ces:*:32:32:Certificate Enrollment Service:/var/empty:/usr/bin/false<br>
_mcxalr:*:54:54:MCX AppLaunch:/var/empty:/usr/bin/false<br>
_krbfast:*:246:-2:Kerberos FAST Account:/var/empty:/usr/bin/false<br>
$<br>

# 3. What about 2?
Display the content of /etc/passwd and /etc/hosts<br>

Example:<br>

$ ./3-twofiles<br>
##<br>
# User Database<br>
#<br>
# Note that this file is consulted directly only when the system is running<br>
# in single-user mode. At other times this information is provided by<br>
# Open Directory.<br>
#<br>
# See the opendirectoryd(8) man page for additional information about<br>
# Open Directory.<br>
##<br>
nobody:*:-2:-2:Unprivileged User:/var/empty:/usr/bin/false<br>
root:*:0:0:System Administrator:/var/root:/bin/sh<br>
daemon:*:1:1:System Services:/var/root:/usr/bin/false<br>
##<br>
# Host Database<br>
#<br>
# localhost is used to configure the loopback interface<br>
# when the system is booting. Do not change this entry.<br>
##<br>
127.0.0.1   localhost<br>
255.255.255.255 broadcasthost<br>
::1 localhost<br>
$<br>

# 4. Last lines of a file
Display the last 10 lines of /etc/passwd<br>

Example:<br>

$ ./4-lastlines<br>
_assetcache:*:235:235:Asset Cache Service:/var/empty:/usr/bin/false<br>
_coremediaiod:*:236:236:Core Media IO Daemon:/var/empty:/usr/bin/false<br>
_launchservicesd:*:239:239:_launchservicesd:/var/empty:/usr/bin/false<br>
_iconservices:*:240:240:IconServices:/var/empty:/usr/bin/false<br>
_distnote:*:241:241:DistNote:/var/empty:/usr/bin/false<br>
_nsurlsessiond:*:242:242:NSURLSession Daemon:/var/db/nsurlsessiond:/usr/bin/false<br>
_nsurlstoraged:*:243:243:NSURLStorage Daemon:/var/empty:/usr/bin/false<br>
_displaypolicyd:*:244:244:Display Policy Daemon:/var/empty:/usr/bin/false<br>
_astris:*:245:245:Astris Services:/var/db/astris:/usr/bin/false<br>
_krbfast:*:246:-2:Kerberos FAST Account:/var/empty:/usr/bin/false<br>

Tips: “Thinks of it as a cat, what is at the end of it?”<br>

# 5. I'd prefer the first ones actually
Display the first 10 lines of /etc/passwd<br>

Example:<br>

$ ./5-firstlines<br>
##<br>
# User Database<br>
#<br>
# Note that this file is consulted directly only when the system is running<br>
# in single-user mode. At other times this information is provided by<br>
# Open Directory.<br>
#<br>
# See the opendirectoryd(8) man page for additional information about<br>
# Open Directory.<br>
##<br>
$<br>

# 6. Line #2
Write a script that displays the third line of the file iacta.<br>

The file iacta will be in the working directory<br>

* You’re not allowed to use sed
* 
julien@ubuntu:/tmp/h$ cat iacta <br>
Alea iacta est<br>
<br>
Alea iacta est ("The die is cast") is a Latin phrase attributed by Suetonius<br>
(as iacta alea est) to Julius Caesar on January 10, 49 BC<br>
as he led his army across the Rubicon river in Northern Italy. With this step,<br>
he entered Italy at the head of his army in defiance of the Senate and began<br>
his long civil war against Pompey and the Optimates. The phrase has been<br>
adopted in Italian (Il dado è tratto), Romanian (Zarurile au fost aruncate),<br>
Spanish (La suerte está echada), French (Les dés sont jetés), Portuguese (A<br>
sorte está lançada), Dutch (De teerling is geworpen),<br>
German (Der Würfel ist gefallen), Hungarian (A kocka el van vetve) and many other languages to<br>
indicate that events have passed a point of no return.<br>
<br>
Read more: https://en.wikipedia.org/wiki/Alea_iacta_est<br>
julien@ubuntu:/tmp/h$ ./6-third_line <br>
Alea iacta est ("The die is cast") is a Latin phrase attributed by Suetonius<br>
julien@ubuntu:/tmp/h$ <br>

Note: The output will differ, depending on the content of the file iacta.<br>

# 7. It is a good file that cuts iron without making a noise
Write a shell script that creates a file named exactly \*\\'"Best School"\'\\*$\?\*\*\*\*\*:) containing the text Best School ending by a new line.<br>

julien@ubuntu:~/shell$ ls && ./7-file && ls -l && cat -e \\*<br>
0-mac_and_cheese 7-file 7-file~ Makefile<br>
total 20<br>
-rwxrw-r-- 1 julien julien 79 Jan 20 06:24 0-mac_and_cheese<br>
-rwxrw-r-- 1 julien julien 90 Jan 20 06:40 7-file<br>
-rwxrw-r-- 1 julien julien 69 Jan 20 06:37 7-file~<br>
-rw-rw-r-- 1 julien julien 14 Jan 20 06:38 Makefile<br>
-rw-rw-r-- 1 julien julien 17 Jan 20 06:40 '\*\\'"Best School"\'\\*$\?\*\*\*\*\*:)'<br>
Best School$<br>
julien@ubuntu:~/shell$<br>

# 8. Save current state of directory
Write a script that writes into the file ls_cwd_content the result of the command ls -la. If the file ls_cwd_content already exists, it should be overwritten. If the file ls_cwd_content does not exist, create it.<br>

julien@ubuntu:/tmp/h$ ls -la<br>
total 20<br>
drwxrwxr-x  2 julien julien 4096 Sep 20 18:18 .<br>
drwxrwxrwt 13 root   root   4096 Sep 20 18:18 ..<br>
-rwxrw-r--  1 julien julien   36 Sep 20 18:18 8-cwd_state<br>
-rw-rw-r--  1 betty  julien   23 Sep 20 14:25 hello<br>
-rw-rw-r--  1 julien julien  926 Sep 20 17:52 iacta<br>
julien@ubuntu:/tmp/h$ ./8-cwd_state <br>
julien@ubuntu:/tmp/h$ ls -la<br>
total 24<br>
drwxrwxr-x  2 julien julien 4096 Sep 20 18:18 .<br>
drwxrwxrwt 13 root   root   4096 Sep 20 18:18 ..<br>
-rwxrw-r--  1 julien julien   36 Sep 20 18:18 8-cwd_state<br>
-rw-rw-r--  1 betty  julien   23 Sep 20 14:25 hello<br>
-rw-rw-r--  1 julien julien  926 Sep 20 17:52 iacta<br>
-rw-rw-r--  1 julien julien  329 Sep 20 18:18 ls_cwd_content<br>
julien@ubuntu:/tmp/h$ cat ls_cwd_content <br>
total 20<br>
drwxrwxr-x  2 julien julien 4096 Sep 20 18:18 .<br>
drwxrwxrwt 13 root   root   4096 Sep 20 18:18 ..<br>
-rwxrw-r--  1 julien julien   36 Sep 20 18:18 8-cwd_state<br>
-rw-rw-r--  1 betty  julien   23 Sep 20 14:25 hello<br>
-rw-rw-r--  1 julien julien  926 Sep 20 17:52 iacta<br>
-rw-rw-r--  1 julien julien    0 Sep 20 18:18 ls_cwd_content<br>
julien@ubuntu:/tmp/h$ <br>

# 9. JDuplicate last line
Write a script that duplicates the last line of the file iacta

* The file iacta will be in the working directory

julien@ubuntu:/tmp/h$ cat iacta <br>
Alea iacta est<br>
<br>
Alea iacta est ("The die is cast") is a Latin phrase attributed by Suetonius<br>
(as iacta alea est) to Julius Caesar on January 10, 49 BC<br>
as he led his army across the Rubicon river in Northern Italy. With this step,<br>
he entered Italy at the head of his army in defiance of the Senate and began<br>
his long civil war against Pompey and the Optimates. The phrase has been<br>
adopted in Italian (Il dado è tratto), Romanian (Zarurile au fost aruncate),<br>
Spanish (La suerte está echada), French (Les dés sont jetés), Portuguese (A<br>
sorte está lançada), Dutch (De teerling is geworpen),<br>
German (Der Würfel ist gefallen), Hungarian (A kocka el van vetve) and many other languages to<br>
indicate that events have passed a point of no return.<br>
<br>
Read more: https://en.wikipedia.org/wiki/Alea_iacta_est<br>
julien@ubuntu:/tmp/h$ ./9-duplicate_last_line <br>
julien@ubuntu:/tmp/h$ cat iacta <br>
Alea iacta est<br>
<br>
Alea iacta est ("The die is cast") is a Latin phrase attributed by Suetonius<br>
(as iacta alea est) to Julius Caesar on January 10, 49 BC<br>
as he led his army across the Rubicon river in Northern Italy. With this step,<br>
he entered Italy at the head of his army in defiance of the Senate and began<br>
his long civil war against Pompey and the Optimates. The phrase has been<br>
adopted in Italian (Il dado è tratto), Romanian (Zarurile au fost aruncate),<br>
Spanish (La suerte está echada), French (Les dés sont jetés), Portuguese (A<br>
sorte está lançada), Dutch (De teerling is geworpen),<br>
German (Der Würfel ist gefallen), Hungarian (A kocka el van vetve) and many other languages to<br>
indicate that events have passed a point of no return.<br>
<br>
Read more: https://en.wikipedia.org/wiki/Alea_iacta_est<br>
Read more: https://en.wikipedia.org/wiki/Alea_iacta_est<br>
julien@ubuntu:/tmp/h$ <br>

# 10. No more javascript
Write a script that deletes all the regular files (not the directories) with a .js extension that are present in the current directory and all its subfolders.<br>
<br>
julien@ubuntu:/tmp/h$ ls -lR<br>
.:<br>
total 24<br>
-rwxrw-r-- 1 julien julien   49 Sep 20 18:29 10-no_more_js<br>
drwxrwxr-x 2 julien julien 4096 Sep 20 18:23 dir1<br>
drwxrwxr-x 2 julien julien 4096 Sep 20 18:24 dir.js<br>
-rw-rw-r-- 1 betty  julien   23 Sep 20 14:25 hello<br>
-rw-rw-r-- 1 julien julien  982 Sep 20 18:21 iacta<br>
-rw-rw-r-- 1 julien julien  329 Sep 20 18:18 ls_cwd_content<br>
-rw-rw-r-- 1 julien julien    0 Sep 20 18:23 main.js<br>
<br>
./dir1:<br>
total 0<br>
-rw-rw-r-- 1 julien julien 0 Sep 20 18:23 code.js<br>
<br>
./dir.js:<br>
total 0<br>
julien@ubuntu:/tmp/h$ ./10-no_more_js <br>
julien@ubuntu:/tmp/h$ ls -lR<br>
.:<br>
total 24<br>
-rwxrw-r-- 1 julien julien   49 Sep 20 18:29 10-no_more_js<br>
drwxrwxr-x 2 julien julien 4096 Sep 20 18:29 dir1<br>
drwxrwxr-x 2 julien julien 4096 Sep 20 18:24 dir.js<br>
-rw-rw-r-- 1 betty  julien   23 Sep 20 14:25 hello<br>
-rw-rw-r-- 1 julien julien  982 Sep 20 18:21 iacta<br>
-rw-rw-r-- 1 julien julien  329 Sep 20 18:18 ls_cwd_content<br>
<br>
./dir1:<br>
total 0<br>
<br>
./dir.js:<br>
total 0<br>
julien@ubuntu:/tmp/h$ <br>

# 11. Directories
Create a script that adds execute permission to all subdirectories of the current directory for the owner, the group owner and all other users. Regular files should not be changed.

# 12. More directories
Create a script that creates a directory called my_dir with permissions 751 in the working directory.

# 13. Change group
Write a script that changes the group owner to school for the file hello

* The file hello will be in the working directory

# 
