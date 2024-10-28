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


### Task 3: Formatting Timestamps

Run the date command again, but this time format the output using YYYYmmdd_HHMMSS (e.g., 20261114_130003 for 1:00:03 PM on November 14, 2016). Refer to the date man page (using man date) for more formatting options. (Press q to exit the man page). Append the formatted output to a file named formatted.txt.

Steps:

1 - I consulted the manual for the command date by typing 'date man' in Terminal and pressing enter. I was able to see from the examples that the date can be formatted to output in Terminal in the following way:
- Year: %Y
- Month: %m
- Day: %d
- Hour: %H
- Minute: %M
- Second: %S

Therefore, if I want to write YYYYmmdd_HHMMSS in terminal that would have to be written by using "%Y%m%d_%H%M%S". Note: Double quotes are used in the example before and after the wished format.

2 - I also found by looking into the manual of command date that the operand '+' sign specifies the format in which the date and time must be displayed.
In this case as I want the date to be displayed in a certain format, I had to add the plus before the new format. The command typed was like 'date +" %Y%m%d_%H%M%S"'.
I ran the date command by typing the following in Terminal 'date +" %Y%m%d_%H%M%S"' and pressing enter. This gave the current Date and Time in the format expected, i.e. 20241020_214025.

3 - I had to go from timestamps repository back one parent folder using '../' instead of 'cd ..', which I learned once I forgot the command 'cd ..' and when I tried it then it just worked well. I am taking that the file 'formatted.txt' is to be created in the directory 'data' once this was created in Task 1 and also used in Task 2, which indicates that in Task 3 the directory should also be used.

4 - Confirmed that I was in the repository 'data', then I typed in Terminal the command 'date +"%Y%m%d_%H%M%S" >> formatted.txt'. This command created the file 'formatted.txt'.

5 - To confirm the date within the file 'formatted.txt' I used the command 'cat formatted.txt' and I was able to see the date and time '20241020_223520'.

For this task, I also reviewed the information on https://phoenixnap.com/kb/linux-date-command#:~:text=To%20format%20the%20date%20command's,substituted%20by%20their%20current%20values.&text=To%20see%20all%20formatting%20options,or%20use%20the%20man%20command.

### Task 4: Create Timestamped Files

Use the touch command to create an empty file with a name in the YYYYmmdd_HHMMSS.txt format. You can achieve this by embedding your date command backticks ` into the touch command. You should no longer use redirection (>>) in this step.

I consulted the superuser website (https://superuser.com/questions/982156/quickest-way-to-give-file-name-the-current-date-on-linux) and found that I can use touch to create a file and backticks with the command date followed by space, the operand '+' and the date format and backtick again to be able to embed the date with the determined format as a name of the new file created by the command touch. The command used in Terminal would look like: touch `date +"%Y%m%d_%H%M%S.txt"`

I just had to make sure that '.txt' was presented after the format for second to ensure it creates a text file. I could confirm by typing the command 'ls' in my Terminal that the file '20241020_225246.txt' was created.

### Task 5: Download Today's Weather Data

Change to the 'data/weather' directory. Download the latest weather data for the Athenry weather station from Met Eireann using 'wget'. Use the '-O <filename>' options to save the file as 'weather.json'. The data can be found at this URL:
https://prodapi.metweb.ie/observations/athenry/today.

To complete this task, I first checked the manual for wget. I could not find it so I searched how to install wget in Terminal. I was able to install using the command 'brew install wget' that I learned from https://stackoverflow.com/questions/33886917/how-to-install-wget-in-macos.
Now that I had the program 'wget' installed in my machine I then went into 'man wget'. From week 06 video 02 of the class on wget_timestamps of Computer Infrastructure I was biased that the command was 'wget' followed by '-O' followed by the '<filename>' and the website. However, I wanted to understand a bit more on how the command 'wget' works with '-O' to output the file with the specified name. I got the understand that the -O (--output-document) option in wget is used to specify a single output file where all downloaded content will be written, rather than saving each document to its original filename as specified in the URL.
Furthermore, I exited from man wget with 'q', I accessed the directory '<weather>' under the directory '<data>'. I then typed in Terminal 'wget -O weather.json https://prodapi.metweb.ie/observations/athenry/today' and executed.
Though I could see that the file 'weather.json' was created within the folder '<weather>', I typed in Terminal 'ls' and it was output to me the file 'weather.json' within the folder '<weather>'.
I also used 'nano weather.json' to see the content within the file in my Terminal.

### Task 6: Timestamp the Data

Modify the command from Task 5 to save the downloaded file with a timestamped name in the format YYYYmmdd_HHMMSS.json.

This task was completed using the knowlodge from tasks 4 and 5. Just had to type in Terminal the command: wget -O `date +"%Y%m%d_%H%M%S.json"` https://prodapi.metweb.ie/observations/athenry/today
Then to confirm that the content of the file I checked using nano again.

