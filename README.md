# My Assessment Repository

Author: Filipe Carvalho

This repository contains my assessment submission for the module of Computer Infrastructure.

## Getting Started

1 - Clone this repository...

2 - Run the code...

## Tasks

### Task 1: Create Directory Structure

Using the command line, create a directory (that is, a folder) named 'data' at the root of your repository. Inside 'data', create two subdirectories: timestamps and weather.

Steps: 
1 - I first ensured that I was in the repository 'computer_infrastructure' by reading the file location showing in my Terminal '-> computer_infrastructure git:(main)', then I typed 'ls' and saw that there was only the file README.md.

2 - I googled 'create a folder named data using terminal', scrolled down a bit and found https://simpledev.io/lesson/create-folder-terminal-1/

3 - I found that to create a folder under the repository (root) 'computer_infrastructure' I have to use the command 'mkdir' followed by the name of the folder.

4 - After creating the folder with the name 'data', I confirmed with the command 'ls' that the repository 'data' was within the repository 'computer_infrastructure'.

5 - I learned from <Simple Dev> website how to create multiple folders using the command mkdir followed by the first folder name, space, the second folder name, space, and continue adding names to add directories under the current directory on Terminal as much as I need. They will all be added at the same time under the current directory once I press enter in my keyboard. I also learned that by using the command 'mkdir' followed by '-p' and adding the subdirectory name followed by forward slash and the name of the subdirectory I want to create under it will create that subdirectory for me. For instance, in my case if I want to create the repository 'timestamps' and 'weather' under the repository data I first have to write 'mkdir -p data/timestamps' then execute and then repeat the same for 'weather'. I decided to use both knowledge to create two subdirectories under the directory 'data' at the same time. I used: 'mkdir -p data/timestamps data/weather'. 

Note: At the end I noticed that I named one of the subdirectories with the name timestamp instead of timestamps. So to rename it to the correct name, I found on https://hpc.nmsu.edu/onboarding/linux/commands/mv/ that I can use 'mv' followed by current directory name, space, and the new directory name. As this file was in the subdirectory 'data' and I wanted to use it in the current root directory 'computer_infrastructure', I first tried the command 'mv -p data/timestamp data/timestamps' which show that '-p' is an illegal option for 'mv'. Then I used the command 'man mv' and found that I can use 'mv -h' followed by 'data/timestamp' + space + 'data/timestamps' to change the name of the repository  timestamp to timestamps.


### Task 2: Timestamps

Navigate to the data/timestamps directory. Use the date command to output the current date and time, appending the output to a file named now.txt. Make sure to use the  >> operator to append (not overwrite) the file. Repeat this step ten times, then use the more command to verify that now.txt has the expected content.

Steps:

1 - To navigate to the data.timestamps directory from computer_infrastructure I just had to type in cd followed by data/timestamps in Terminal and press enter as per https://www.macworld.com/article/221277/command-line-navigating-files-folders-mac-terminal.html.

2 - Looking into https://stackoverflow.com/questions/43221469/write-current-date-time-to-a-file-using-shell-script, I found that I can just type 'date' followed by:
'>' if I want to create the new file, or
'>>' if I want to append the new file.
In this case as it was appending I used '>>'.

3 - For the time, I use the recommendation of Video 2 from week 05 of the class of Computer Infrastructure which is to use the format 'date +" %Y%m%d%H%M%S"'.

4 - Then, I added the file name 'now.txt' to be added tothe current repository (/Users/filipecarvalho/Desktop/computer_infrastructure/data/timestamps) and pressed enter.

5 - This created the file 'now.txt'. I entered ls in Terminal to see the files within the repository timestamps (https://www.linode.com/docs/guides/ls-command-in-linux/) and found 'now.txt', then I used the command 'cat now.txt' to confirm the data within the file (https://phoenixnap.com/kb/linux-cat-command#:~:text=The%20cat%20(concatenate)%20command%20in,files%2C%20and%20create%20new%20files.).

6 - I executed 9 more times the command 'date +" %Y%m%d%H%M%S" >> now.txt' in Terminal and then checked again the data within the file 'now.txt', but this time I used the command 'more' to see the data. Note: I found this discussion in Quora explaining the difference between 'cat' and 'more' (https://www.quora.com/Whats-the-difference-between-cat-more-and-less-in-Linux#:~:text=The%20cat%20command%20displays%20the,scroll%20up%20the%20next%20page).


