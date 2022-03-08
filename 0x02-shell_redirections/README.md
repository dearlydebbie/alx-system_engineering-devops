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
\#\#<br>
\#User Database<br>
\#<br>
\# Note that this file is consulted directly only when the system is running<br>
\# in single-user mode. At other times this information is provided by<br>
\# Open Directory.<br>
\#<br>
\# See the opendirectoryd(8) man page for additional information about<br>
\# Open Directory.<br>
\#\#<br>
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
\#\#<br>
\# User Database<br>
\#<br>
\# Note that this file is consulted directly only when the system is running<br>
\# in single-user mode. At other times this information is provided by<br>
\# Open Directory.<br>
\#<br>
\# See the opendirectoryd(8) man page for additional information about<br>
\# Open Directory.<br>
\#\#<br>
nobody:*:-2:-2:Unprivileged User:/var/empty:/usr/bin/false<br>
root:*:0:0:System Administrator:/var/root:/bin/sh<br>
daemon:*:1:1:System Services:/var/root:/usr/bin/false<br>
\#\#<br>
\# Host Database<br>
\#<br>
\# localhost is used to configure the loopback interface<br>
\# when the system is booting. Do not change this entry.<br>
\#\#<br>
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
\#\#<br>
\# User Database<br>
\#<br>
\# Note that this file is consulted directly only when the system is running<br>
\# in single-user mode. At other times this information is provided by<br>
\# Open Directory.<br>
\#<br>
\# See the opendirectoryd(8) man page for additional information about<br>
\# Open Directory.<br>
\#\#<br>
$<br>

# 6. Line #2
Write a script that displays the third line of the file iacta.<br>

The file iacta will be in the working directory<br>

* You’re not allowed to use sed

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

# 9. Duplicate last line
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

# 11. Don't just count your directories, make your directories count
Write a script that counts the number of directories and sub-directories in the current directory.

* The current and parent directories should not be taken into account
* Hidden directories should be counted

julien@production-503e7013:~/shell/fun_with_the_shell$ ls -lRa<br>
.:<br>
total 32<br>
drwxrwxr-x 3 julien julien 4096 Jan 20 03:53 .<br>
drwxrwxr-x 3 julien julien 4096 Jan 20 02:58 ..<br>
-rwxr--r-- 1 julien julien 43 Jan 20 02:59 0-commas<br>
-rwxr--r-- 1 julien julien 47 Jan 20 02:50 1-empty_casks<br>
-rwxrw-r-- 1 julien julien 68 Jan 20 03:35 2-gifs<br>
-rwxrw-r-- 1 julien julien 47 Jan 20 03:53 3-directories<br>
-rw-rw-r-- 1 julien julien 14 Jan 20 03:35 Makefile<br>
drwxrwxr-x 4 julien julien 4096 Jan 20 03:42 test_dir<br>
<br>
./test_dir:<br>
total 16<br>
drwxrwxr-x 4 julien julien 4096 Jan 20 03:42 .<br>
drwxrwxr-x 3 julien julien 4096 Jan 20 03:53 ..<br>
-rw-rw-r-- 1 julien julien 0 Jan 20 03:40 .horrible_selfie.gif<br>
-rw-rw-r-- 1 julien julien 0 Jan 20 03:23 README.md<br>
-rw-rw-r-- 1 julien julien 0 Jan 20 03:17 docker.gif<br>
-rw-rw-r-- 1 julien julien 0 Jan 20 03:17 file.sh<br>
drwxrwxr-x 2 julien julien 4096 Jan 20 03:23 photos<br>
drwxrwxr-x 2 julien julien 4096 Jan 20 03:23 rep.gif<br>
<br>
./test_dir/photos:<br>
total 8<br>
drwxrwxr-x 2 julien julien 4096 Jan 20 03:23 .<br>
drwxrwxr-x 4 julien julien 4096 Jan 20 03:42 ..<br>
-rw-rw-r-- 1 julien julien 0 Jan 20 03:23 cat.gif<br>
-rw-rw-r-- 1 julien julien 0 Jan 20 03:22 index.html<br>
-rw-rw-r-- 1 julien julien 0 Jan 20 03:23 main.gif<br>
-rw-rw-r-- 1 julien julien 0 Jan 20 03:23 rudy_rigot.gif<br>
<br>
./test_dir/rep.gif:<br>
total 8<br>
drwxrwxr-x 2 julien julien 4096 Jan 20 03:23 .<br>
drwxrwxr-x 4 julien julien 4096 Jan 20 03:42 ..<br>
julien@production-503e7013:~/shell/fun_with_the_shell$ ./11-directories<br>
3<br>
julien@production-503e7013:~/shell/fun_with_the_shell$<br>

# 12. What’s new
Create a script that displays the 10 newest files in the current directory.<br>
<br>
Requirements:<br>
* One file per line
* Sorted from the newest to the oldest
<br>
alex@ubuntu:/tmp$ ls -l<br>
total 7<br>
-rwxr-xr-x 1 501 dialout  32 Sep 27 23:51 0-hello_world<br>
-rwxr-xr-x 1 501 dialout  46 Sep 28 11:09 10-no_more_js<br>
-rwxr-xr-x 1 501 dialout  43 Sep 28 11:19 11-directories
-rwxr-xr-x 1 501 dialout  30 Sep 29 13:43 12-newest_files<br>
-rwxr-xr-x 1 501 dialout  28 Sep 27 23:54 1-confused_smiley<br>
-rwxr-xr-x 1 501 dialout  28 Sep 27 23:58 2-hellofile<br>
-rwxr-xr-x 1 501 dialout  39 Sep 27 23:58 3-twofiles<br>
-rwxr-xr-x 1 501 dialout  33 Sep 27 23:59 4-lastlines<br>
-rwxr-xr-x 1 501 dialout  33 Sep 28 00:00 5-firstlines
-rwxr-xr-x 1 501 dialout  28 Sep 28 00:25 6-third_line<br>
-rwxr-xr-x 1 501 dialout 110 Sep 28 00:34 7-file<br>
-rwxr-xr-x 1 501 dialout  36 Sep 28 00:34 8-cwd_state<br>
-rwxr-xr-x 1 501 dialout  35 Sep 28 00:35 9-duplicate_last_line<br>
-rw-r--r-- 1 501 dialout  19 Sep 27 23:51 README.md<br>
alex@ubuntu:/tmp$ ./12-newest_files <br>
12-newest_files<br>
11-directories<br>
10-no_more_js<br>
9-duplicate_last_line<br>
7-file<br>
8-cwd_state<br>
6-third_line<br>
5-firstlines<br>
4-lastlines<br>
3-twofiles<br>
alex@ubuntu:/tmp$<br>

# 13. Being unique is better than being perfect
Create a script that takes a list of words as input and prints only words that appear exactly once.<br>

* Input format: One line, one word
* Output format: One line, one word
* Words should be sorted

julien@ubuntu:/tmp/0x02$ cat list <br>
C#<br>
C<br>
Javascript<br>
Perl<br>
PHP<br>
PHP<br>
ASP<br>
R<br>
Go<br>
C#<br>
C++<br>
R<br>
Perl<br>
Javascript<br>
Javascript<br>
Python<br>
Javascript<br>
Javascript<br>
Javascript<br>
Java<br>
Java<br>
Python<br>
Javascript<br>
Javascript<br>
Javascript<br>
ASP<br>
julien@ubuntu:/tmp/0x02$ cat list | ./13-unique <br>
C<br>
C++<br>
Go<br>
julien@ubuntu:/tmp/0x02$<br>


# 14. It must be in that file
Display lines containing the pattern “root” from the file /etc/passwd<br>

$ ./14-findthatword<br>
root:*:0:0:System Administrator:/var/root:/bin/sh<br>
daemon:*:1:1:System Services:/var/root:/usr/bin/false<br>
_cvmsroot:*:212:212:CVMS Root:/var/empty:/usr/bin/false<br>
$<br>


# 15. Count that word
Display the number of lines that contain the pattern “bin” in the file /etc/passwd<br>

$ ./15-countthatword<br>
81<br>
$ <br>


# 16. What's next?
Display lines containing the pattern “root” and 3 lines after them in the file /etc/passwd.<br>

$ ./16-whatsnext<br>
root:*:0:0:System Administrator:/var/root:/bin/sh<br>
daemon:*:1:1:System Services:/var/root:/usr/bin/false<br>
_uucp:*:4:4:Unix to Unix Copy Protocol:/var/spool/uucp:/usr/sbin/uucico<br>
_taskgated:*:13:13:Task Gate Daemon:/var/empty:/usr/bin/false<br>
_networkd:*:24:24:Network Services:/var/networkd:/usr/bin/false<br>
--<br>
_cvmsroot:*:212:212:CVMS Root:/var/empty:/usr/bin/false<br>
_usbmuxd:*:213:213:iPhone OS Device Helper:/var/db/lockdown:/usr/bin/false<br>
_dovecot:*:214:6:Dovecot Administrator:/var/empty:/usr/bin/false<br>
_dpaudio:*:215:215:DP Audio:/var/empty:/usr/bin/false<br>
$<br>

# 17. I hate bins
Display all the lines in the file /etc/passwd that do not contain the pattern “bin”.<br>

 $ ./17-hidethisword<br>
\#\#<br>
\# User Database<br>
\#<br>
\# Note that this file is consulted directly only when the system is running<br>
\# in single-user mode. At other times this information is provided by<br>
\# Open Directory.<br>
\#<br>
\# See the opendirectoryd(8) man page for additional information about<br>
\# Open Directory.<br>
\#\#<br>
$<br>

# 18.  Letters only please
Display all lines of the file /etc/ssh/sshd_config starting with a letter.
* include capital letters as well

 $ ./18-letteronly<br>
SyslogFacility AUTHPRIV<br>
AuthorizedKeysFile  .ssh/authorized_keys<br>
UsePrivilegeSeparation sandbox # Default for new installations.<br>
AcceptEnv LANG LC_*<br>
Subsystem   sftp    /usr/libexec/sftp-server<br>
$<br>

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

julien@ubuntu:/tmp/0x02$ cat /etc/passwd<br>
root:x:0:0:root:/root:/bin/bash<br>
daemon:x:1:1:daemon:/usr/sbin:/usr/sbin/nologin<br>
bin:x:2:2:bin:/bin:/usr/sbin/nologin<br>
sys:x:3:3:sys:/dev:/usr/sbin/nologin<br>
sync:x:4:65534:sync:/bin:/bin/sync<br>
games:x:5:60:games:/usr/games:/usr/sbin/nologin<br>
man:x:6:12:man:/var/cache/man:/usr/sbin/nologin
lp:x:7:7:lp:/var/spool/lpd:/usr/sbin/nologin<br>
mail:x:8:8:mail:/var/mail:/usr/sbin/nologin<br>
news:x:9:9:news:/var/spool/news:/usr/sbin/nologin<br>
uucp:x:10:10:uucp:/var/spool/uucp:/usr/sbin/nologin<br>
proxy:x:13:13:proxy:/bin:/usr/sbin/nologin<br>
www-data:x:33:33:www-data:/var/www:/usr/sbin/nologin<br>
backup:x:34:34:backup:/var/backups:/usr/sbin/nologin<br>
list:x:38:38:Mailing List Manager:/var/list:/usr/sbin/nologin<br>
irc:x:39:39:ircd:/var/run/ircd:/usr/sbin/nologin<br>
gnats:x:41:41:Gnats Bug-Reporting System (admin):/var/lib/gnats:/usr/sbin/nologin<br>
nobody:x:65534:65534:nobody:/nonexistent:/usr/sbin/nologin<br>
systemd-timesync:x:100:102:systemd Time Synchronization,,,:/run/systemd:/bin/false<br>
systemd-network:x:101:103:systemd Network Management,,,:/run/systemd/netif:/bin/false<br>
systemd-resolve:x:102:104:systemd Resolver,,,:/run/systemd/resolve:/bin/false<br>
systemd-bus-proxy:x:103:105:systemd Bus Proxy,,,:/run/systemd:/bin/false<br>
syslog:x:104:108::/home/syslog:/bin/false<br>
_apt:x:105:65534::/nonexistent:/bin/false<br>
messagebus:x:106:110::/var/run/dbus:/bin/false<br>
uuidd:x:107:111::/run/uuidd:/bin/false<br>
lightdm:x:108:114:Light Display Manager:/var/lib/lightdm:/bin/false<br>
whoopsie:x:109:116::/nonexistent:/bin/false<br>
avahi-autoipd:x:110:119:Avahi autoip daemon,,,:/var/lib/avahi-autoipd:/bin/false<br>
avahi:x:111:120:Avahi mDNS daemon,,,:/var/run/avahi-daemon:/bin/false<br>
dnsmasq:x:112:65534:dnsmasq,,,:/var/lib/misc:/bin/false<br>
colord:x:113:123:colord colour management daemon,,,:/var/lib/colord:/bin/false<br>
speech-dispatcher:x:114:29:Speech Dispatcher,,,:/var/run/speech-dispatcher:/bin/false<br>
hplip:x:115:7:HPLIP system user,,,:/var/run/hplip:/bin/false<br>
kernoops:x:116:65534:Kernel Oops Tracking Daemon,,,:/:/bin/false<br>
pulse:x:117:124:PulseAudio daemon,,,:/var/run/pulse:/bin/false<br>
rtkit:x:118:126:RealtimeKit,,,:/proc:/bin/false<br>
saned:x:119:127::/var/lib/saned:/bin/false<br>
usbmux:x:120:46:usbmux daemon,,,:/var/lib/usbmux:/bin/false<br>
julien:x:1000:1000:Julien Barbier,,,:/home/julien:/bin/bash
guillaume:x:1001:1001:,,,:/home/guillaume:/bin/bash<br>
betty:x:1002:1002::/home/betty:<br>
julien@ubuntu:/tmp/0x02$<br>
julien@ubuntu:/tmp/0x02$ ./22-users_and_homes <br>
_apt:/nonexistent<br>
avahi-autoipd:/var/lib/avahi-autoipd<br>
avahi:/var/run/avahi-daemon<br>
backup:/var/backups<br>
betty:/home/betty<br>
bin:/bin<br>
colord:/var/lib/colord<br>
daemon:/usr/sbin<br>
dnsmasq:/var/lib/misc<br>
games:/usr/games<br>
gnats:/var/lib/gnats<br>
guillaume:/home/guillaume<br>
hplip:/var/run/hplip<br>
irc:/var/run/ircd<br>
julien:/home/julien<br>
kernoops:/<br>
lightdm:/var/lib/lightdm<br>
list:/var/list<br>
lp:/var/spool/lpd<br>
mail:/var/mail<br>
man:/var/cache/man<br>
messagebus:/var/run/dbus<br>
news:/var/spool/news<br>
nobody:/nonexistent<br>
proxy:/bin<br>
pulse:/var/run/pulse<br>
root:/root<br>
rtkit:/proc<br>
saned:/var/lib/saned<br>
speech-dispatcher:/var/run/speech-dispatcher<br>
sync:/bin<br>
sys:/dev<br>
syslog:/home/syslog<br>
systemd-bus-proxy:/run/systemd<br>
systemd-network:/run/systemd/netif<br>
systemd-resolve:/run/systemd/resolve<br>
systemd-timesync:/run/systemd<br>
usbmux:/var/lib/usbmux<br>
uucp:/var/spool/uucp<br>
uuidd:/run/uuidd<br>
whoopsie:/nonexistent<br>
www-data:/var/www<br>
julien@ubuntu:/tmp/0x02$ <br>


# 23. Change group
Write a script that changes the group owner to school for the file hello

* The file hello will be in the working directory


# 24. Change group
Write a script that changes the group owner to school for the file hello

* The file hello will be in the working directory


# 25. Change group
Write a script that changes the group owner to school for the file hello

* The file hello will be in the working directory

# 26. Change group
Write a script that changes the group owner to school for the file hello

* The file hello will be in the working directory

# 
