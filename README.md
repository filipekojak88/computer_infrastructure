# My Assessment Repository

Author: Filipe Carvalho

This repository contains my assessment submission for the module of Computer Infrastructure.

## Getting Started

1 - Clone this repository...

2 - Run the code...

## Tasks

### Task 1:

Using the command line, create a directory (that is, a folder) named 'data' at the root of your repository. Inside 'data', create two subdirectories: timestamps and weather.

Steps: 
1 - I first ensured that I was in the repository 'computer_infrastructure' by reading the file location showing in my Terminal '-> computer_infrastructure git:(main)', then I typed 'ls' and saw that there was only the file README.md.

2 - I googled 'create a folder named data using terminal', scrolled down a bit and found https://simpledev.io/lesson/create-folder-terminal-1/

3 - I found that to create a folder under the repository (root) 'computer_infrastructure' I have to use the command 'mkdir' followed by the name of the folder.

4 - After creating the folder with the name 'data', I confirmed with the command 'ls' that the repository 'data' was within the repository 'computer_infrastructure'.

5 - I learned from <Simple Dev> website how to create multiple folders using the command mkdir followed by the first folder name, space, the second folder name, space, and continue adding names to add directories under the current directory on Terminal as much as I need. They will all be added at the same time under the current directory once I press enter in my keyboard. I also learned that by using the command 'mkdir' followed by '-p' and adding the subdirectory name followed by forward slash and the name of the subdirectory I want to create under it will create that subdirectory for me. For instance, in my case if I want to create the repository 'timestamps' and 'weather' under the repository data I first have to write 'mkdir -p data/timestamps' then execute and then repeat the same for 'weather'. I decided to use both knowledge to create two subdirectories under the directory 'data' at the same time. I used: 'mkdir -p data/timestamps data/weather'. 

Note: At the end I noticed that I named one of the subdirectories with the name timestamp instead of timestamps. So to rename it to the correct name, I found on https://hpc.nmsu.edu/onboarding/linux/commands/mv/ that I can use 'mv' followed by current directory name, space, and the new directory name. As this file was in the subdirectory 'data' and I wanted to use it in the current root directory 'computer_infrastructure', I first tried the command 'mv -p data/timestamp data/timestamps' which show that '-p' is an illegal option for 'mv'. Then I used the command 'man mv' and found that I can use 'mv -h' followed by 'data/timestamp' + space + 'data/timestamps' to change the name of the repository  timestamp to timestamps.
