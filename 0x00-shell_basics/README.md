# 0x00-shell_basics project

0-current_working_directory
: Write a script that prints the absolute path name of the current working directory.

1-listit
: Display the contents list of your current directory.

2-bring_me_home
: Write a script that changes the working directory to the user’s home directory.

3-listfiles
: Display current directory contents in a long format

4-listmorefiles
: Display current directory contents, including hidden files (starting with .). Use the long format.

5-listfilesdigitonly
: Display current directory contents.
  > * Long format
  
  > * with user and group IDs displayed numerically

  > * And hidden files (starting with .)

6-firstdirectory
: Create a script that creates a directory named my_first_directory in the /tmp/ directory.

7-movethatfile
: Move the file betty from /tmp/ to /tmp/my_first_directory.

8-firstdelete
: Delete the file betty.
  > * The file betty is in /tmp/my_first_directory

9-firstdirdeletion
: Delete the directory my_first_directory that is in the /tmp directory.

10-back
: Write a script that changes the working directory to the previous one.

11-lists
: Write a script that lists all files (even ones with names beginning with a period character, which are normally hidden) in the current directory and the parent of the working directory and the /boot directory (in this order), in long format.

12-file_type
: Write a script that prints the type of the file named iamafile. The file iamafile will be in the /tmp directory when we will run your script.

13-symbolic_link
: Create a symbolic link to /bin/ls, named __ls__. The symbolic link should be created in the current working directory.

14-copy_html
: Create a script that copies all the HTML files from the current working directory to the parent of the working directory, but only copy files that did not exist in the parent of the working directory or were newer than the versions in the parent of the working directory.

You can consider that all HTML files have the extension .html

100-lets_move
: Create a script that moves all files beginning with an uppercase letter to the directory /tmp/u.
You can assume that the directory /tmp/u will exist when we will run your script

101-clean_emacs
: Create a script that deletes all files in the current working directory that end with the character ~.

102-tree
: Create a script that creates the directories welcome/, welcome/to/ and welcome/to/school in the current directory.

103-commas
: Write a command that lists all the files and directories of the current directory, separated by commas (,).
  > * Directory names should end with a slash (/)
  > * Files and directories starting with a dot (.) should be listed
  > * The listing should be alpha ordered, except for the directories . and .. which should be listed at the very beginning.
  > * Only digits and letters are used to sort; Digits should come first
  > * You can assume that all the files we will test with will have at least one letter or one digit
  > * The listing should end with a new line

school.mgc
: Create a magic file school.mgc that can be used with the command file to detect School data files. School data files always contain the string SCHOOL at offset 0.

### Format of the magic source file

The most important thing to remember is that each line in the file specifies a test. Each test is made up of 4 items, which are separated by one or more whitespace characters (usually tabs, but spaces appear to work as well):

  > * offset – specifies the offset, in bytes, into the file of the data which is to be tested.
  > * type – the type of the data to be tested (see here for a list of all possible values) .
  > * test – the value to be compared with the value from the file.
  > * message – the message to be printed if the comparison succeeds.

Here’s an example (actually this is the JPEG 2000 magic that is currently used in File 5.11):

offset type 	  test 	   message

0	     string 	bonjour  politesse

### How to create a .mgc file
1- create a file school
  ```
  0	 string 	bonjour  politesse
  ```

2- put the example above inside the file school

3- compile it to generate the .mgc file by using the following command:
  ```
  file -C -m school
  ```
  It will compile and generate a file called school.mgc
  
4- test it
   ```
   file -i -m school.mgc *
   ```

  [follow this link for more info](https://openpreservation.org/blogs/magic-editing-and-creation-primer/ "Title").

  [pdf](https://drive.google.com/file/d/1Auz54eSR4KYwLF-ct8wAhg13VXZqvd_U/view?usp=sharing "Title"). 
