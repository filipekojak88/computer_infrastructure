# Computer Infrastructure

This repository presents the tasks and project completed for the module of Computer Infrastructure in ATU with the lecturer Ian McLoughlin. 
In order to complete the tasks and the project it was utilized skills in command-line navigation, file management, and Bash scripting to automate tasks like creating directories, timestamping files, and downloading weather data.  

This README has been written with [Github's documentation on README](https://docs.github.com/en/repositories/managing-your-repositorys-settings-and-features/customizing-your-repository/about-readmes) and [Wenger's article on 'Why having a Readme on your internal project is essential'](https://wengerk.medium.com/why-having-a-readme-on-your-internal-project-is-essential-c85cb9dd8e65) in mind [[1]](#1) [[2]](#2).     
MarkDown was used in this README file and was based on [GitHub's Documentation](https://docs.github.com/en/get-started/writing-on-github/getting-started-with-writing-and-formatting-on-github/basic-writing-and-formatting-syntax) [[3]](#3).

## About This Project

The Weather Data Processing Report showcases acquired knowledge with Linux/Unix commands such as `mkdir`, `wget`, and `touch`, as well as the use of the `date` command for timestamp generation. It also highlights Python programming skills, particularly with the `pandas` library for reading, inspecting, and analyzing JSON data. The ability to troubleshoot and optimize processes, including debugging scripts and using resources like manual pages, is also evident. Overall, the report reflects a blend of command-line, automation techniques, and data analysis capabilities which reflects the content learned in the module of Computer Infrastructure.

The data used in this project was obtained from [Met Eireann - Irish Meteorological Service](https://www.met.ie) website which provides weather information and related services to the public and specialized sectors such as aviation and agriculture. Met Eireann monitors, analyzes, and predicts Ireland's weather and climate, utilizing the latest technological and scientific advances to improve the accuracy and effectiveness of its forecasts [[4]](#4).

## Use of this project

This project serves as an example of how to automate data collection and analysis tasks using a combination of command-line tools, Bash scripting, Python, and GitHub Actions. In this project, users can learn practical skills for automating data pipelines, working with timestamps, and analyzing weather data programmatically.

Some suggested applications:

- Educational Value: It demonstrates how to structure a repository, use Linux commands, and create automated workflows with GitHub Actions. Students can adapt this project as a template for other automation tasks involving data collection and processing.
- Real-World Insights: By integrating weather data from Met Éireann, the project provides an example of how publicly available datasets can be used for meaningful analysis.

## Getting Started

This project processes and stores weather data using automation and scripting tools. Below is a guide to navigate the structure and use the files:

1. Navigate the Project  
Use [Computer Infrastructure](https://github.com/filipekojak88/computer_infrastructure/tree/main) to enter the project folder.

2. Run Automation  
Trigger workflows via [.github/workflows/weather-data.yml](.github/workflows/weather-data.yml) which runs [weather.sh](weather.sh). The `weather.sh` script downloads and saves Athenry's current weather data from the Met Éireann API with a timestamped filename.

Some background on `weather-data.yml` workflow:
- To automate the daily execution of the `weather.sh` script and push weather data to a GitHub repository, a GitHub Actions workflow was created. This involved adding a workflow file (`weather-data.yml`) to the `.github/workflows/` directory of the repository. The workflow is scheduled to run daily at 10 a.m. using the `cron` event and includes a `workflow_dispatch` event to allow manual testing. It uses a Linux-based Ubuntu virtual machine as the environment for running the actions.   
- The workflow clones the repository, executes the `weather.sh` script to fetch and save the weather data, and then commits and pushes the updated data back to the repository.    
- After creating and pushing the workflow file, the automation was tested by reviewing the logs in GitHub Actions to confirm the script executed correctly and new weather data was successfully committed to the repository. This was verified with the creation of [20241201_225405.json](data/weather/20241201_225405.json) and Commit message on GitHub [Update weather dta for 2024-12-01 22:54:07](https://github.com/filipekojak88/computer_infrastructure/commit/48b479227817f1ad66c57fcfbee927cea4b8365f).

3. Process Data 
- Timestamp files: Stored in [data/timestamps/](data/timestamps/).  
- Downloaded weather data: Check [data/weather/](data/weather/) for timestamped JSON files.

4. Analyze Weather Data  
Open [weather.ipynb](weather.ipynb) in Jupyter Notebook to explore and analyze the weather records.

Some background on `weather.ipynb` file:
- The file `weather.ipynb` documents a comprehensive process for weather data collection and analysis using Bash scripting and Python. It begins by outlining tasks such as creating directory structures, generating and formatting timestamps, and automating data downloads from Met Éireann’s API. Each task is meticulously detailed with commands like `mkdir`, `date`, and `wget`, explaining how to dynamically name and save weather data files with timestamps.
- The later sections cover creating and testing a Bash script (weather.sh) to automate data downloads, and a brief analysis of one of the collected weather data files. The analysis includes a short explanation of the dataset obtained from data.gov.ie, rounding out the report as a complete guide to data acquisition, management, and preliminary examination.

## Get Help

If questions are raised while checking this project, you can contact me via github, and I will be happy to provide more information. Full list of references is available at the end of this README file and the numbers provided across this README.md and the weather.ipynb files are direct links to their respective references in the reference section, which can provide further insights into the structure and fundamentals used to build this project.

## Contribute

This project reflects the author's understanding of data automation and analysis using Python and Bash scripting. Contributions and suggestions to improve the project are highly encouraged, as they can lead to more robust solutions and innovative features.
Additionally, the step-by-step nature of this project enables others to replicate the process or customize it to analyze datasets from different sources. The automation of daily data collection ensures consistency and demonstrates the practical use of continuous integration tools.

Contributions are welcome, especially those that improve functionality, enhance the readability of scripts, or add new features for analyzing weather data.

I used [openincolab.com](https://openincolab.com) to generate the following clickable link.      
It opens the [weather.ipynb](weather.ipynb) notebook in [Google Colab](https://colab.research.google.com)

<a target="_blank" href="https://colab.research.google.com/github/filipekojak88/computer_infrastructure/blob/main/weather.ipynb">
  <img src="https://colab.research.google.com/assets/colab-badge.svg" alt="Open In Colab"/>
</a>

## Author

I am currently a Quality Engineer with a Production Engineering & Management background. Though I have had around 12 years of experience swinging between the medical device and car assembly industry, I am currently chasing a change in my career through this course of Data Analytics in ATU. My long term goal is to move into Artificial Intelligence. If you want to know more about me, please add me on LinkedIn: [Filipe Carvalho](https://www.linkedin.com/in/filipe-carvalho-8146232a/) 

## References:      

<a id="1">[1]</a> About readmes (no date) GitHub Docs. Available at: https://docs.github.com/en/repositories/managing-your-repositorys-settings-and-features/customizing-your-repository/about-readmes (Accessed: 29 April 2024).   

<a id="2">[2]</a> Wenger, K. (2023) Why having a readme on your internal project is essential, Medium. Available at: https://wengerk.medium.com/why-having-a-readme-on-your-internal-project-is-essential-c85cb9dd8e65 (Accessed: 08 December 2024).       

<a id="3">[3]</a> Basic writing and formatting syntax (no date) GitHub Docs. Available at: https://docs.github.com/en/get-started/writing-on-github/getting-started-with-writing-and-formatting-on-github/basic-writing-and-formatting-syntax (Accessed: 29 April 2024).   

<a id="4">[4]</a> About Us (no date) Met Éireann - The Irish Meteorological Service. Available at: https://www.met.ie/about-us (Accessed: 08 December 2024). 

<a id="5">[5]</a> Create a folder - terminal (2022) Simple Dev. Available at: https://simpledev.io/lesson/create-folder-terminal-1/ (Accessed: 08 December 2024).

<a id="6">[6]</a> McElhearn, K. (2022) Master the macos command line: How to navigate files and folders in terminal, Macworld. Available at: https://www.macworld.com/article/221277/command-line-navigating-files-folders-mac-terminal.html (Accessed: 08 December 2024). 

<a id="7">[7]</a> Write current date/time to a file using shell script (1962) Stack Overflow. Available at: https://stackoverflow.com/questions/43221469/write-current-date-time-to-a-file-using-shell-script (Accessed: 08 December 2024). 

<a id="8">[8]</a> LS command in linux: Listing files & directories (2023) Linode Guides & Tutorials. Available at: https://www.linode.com/docs/guides/ls-command-in-linux/ (Accessed: 08 December 2024). 

<a id="9">[9]</a> Zivanov, S. (2024) Linux Cat Command (with examples): Phoenixnap KB, Knowledge Base by phoenixNAP. Available at: https://phoenixnap.com/kb/linux-cat-command#:~:text=The%20cat%20(concatenate)%20command%20in,files%2C%20and%20create%20new%20files (Accessed: 08 December 2024).

<a id="10">[10]</a> Whats the difference between ‘cat’ ‘more’ and ‘less’ in linux? (no date) Quora. Available at: https://www.quora.com/Whats-the-difference-between-cat-more-and-less-in-Linux#:~:text=The%20cat%20command%20displays%20the,scroll%20up%20the%20next%20page (Accessed: 08 December 2024).

<a id="11">[11]</a> Marijan, B. (2024) Linux date command: Set, change, format and display date, Knowledge Base by phoenixNAP. Available at: https://phoenixnap.com/kb/linux-date-command#:~:text=To%20format%20the%20date%20command’s,substituted%20by%20their%20current%20values.&text=To%20see%20all%20formatting%20options,or%20use%20the%20man%20command (Accessed: 08 December 2024).  

<a id="12">[12]</a> Quickest way to give file name the current date on linux (no date) Super User. Available at: https://superuser.com/questions/982156/quickest-way-to-give-file-name-the-current-date-on-linux (Accessed: 08 December 2024). 

<a id="13">[13]</a> Met Eireann (No date) Prodapi.metweb.ie. Available at: https://prodapi.metweb.ie/observations/athenry/today (Accessed: 08 December 2024).

<a id="14">[14]</a> How to install WGET in macos? (no date) Stack Overflow. Available at: https://stackoverflow.com/questions/33886917/how-to-install-wget-in-macos (Accessed: 08 December 2024).

<a id="15">[15]</a> Manage files in terminal on Mac (no date) Apple Support. Available at: https://support.apple.com/en-ie/guide/terminal/apddfb31307-3e90-432f-8aa7-7cbc05db27f7/mac#:~:text=Go%20to%20the%20Terminal%20app,it%20in%20the%20new%20location (Accessed: 08 December 2024). 

<a id="16">[16]</a> Mishra, S. (2020) (#!/bin/bash ) what exactly is this ?, Medium. Available at: https://medium.com/@codingmaths/bin-bash-what-exactly-is-this-95fc8db817bf (Accessed: 08 December 2024). 

<a id="17">[17]</a> Understanding the linux file system and file permissions (2023) Digital Cloud Training. Available at: https://digitalcloud.training/understanding-the-linux-file-system-and-file-permissions/#:~:text=Default%20permissions%20for%20the%20root,and%20execute%20but%20not%20write (Accessed: 08 December 2024). 

<a id="18">[18]</a> (No date) Chatgpt. Available at: https://openai.com/chatgpt/ (Accessed: 08 December 2024).

<a id="19">[19]</a> Pandas.read_json# (no date) pandas.read_json - pandas 2.2.3 documentation. Available at: https://pandas.pydata.org/docs/reference/api/pandas.read_json.html (Accessed: 08 December 2024). 

<a id="20">[20]</a> Pandas dataframe.head() - javatpoint (no date) www.javatpoint.com. Available at: https://www.javatpoint.com/pandas-dataframe-head (Accessed: 08 December 2024). 

<a id="21">[21]</a> Python: Pandas dataframe.info() (2023) GeeksforGeeks. Available at: https://www.geeksforgeeks.org/python-pandas-dataframe-info/ (Accessed: 08 December 2024). 

<a id="22">[22]</a> Llego, M.A. (2023) A comprehensive guide to pandas df.describe() for descriptive statistics on numeric columns, Unconventional Musings from an Extraordinary Mind. Available at: https://llego.dev/posts/pandas-df-describe-statistics-numeric-columns/ (Accessed: 08 December 2024). 

<a id="23">[23]</a> How to read wind direction. even if it sounds too simple (no date) WINDY.APP. Available at: https://windy.app/blog/what-is-wind-direction.html#:~:text=Because%20the%20wind%20direction%20is,north%2Dnortheast%20wind%20(NNE) (Accessed: 08 December 2024). 

<a id="24">[24]</a> Dry cold, damp cold... is winter weather colder when humidity is higher? (2023) Montreal Science Centre. Available at: https://www.montrealsciencecentre.com/blog/dry-cold-damp-cold-winter-weather-colder-when-humidity-higher (Accessed: 08 December 2024). 

<a id="25">[25]</a> Today’s Weather Athenry (no date) Data.Gov.IE. Available at: https://data.gov.ie/dataset/todays-weather-athenry (Accessed: 08 December 2024). 
