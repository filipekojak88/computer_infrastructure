# Computer Infrastructure

This repository presents the tasks and project completed for the module of Computer Infrastructure in ATU with the lecturer Ian McLoughlin. 
In order to complete the tasks and the project it was utilized skills in command-line navigation, file management, and Bash scripting to automate tasks like creating directories, timestamping files, and downloading weather data.  

This README has been written with [Github's documentation on README](https://docs.github.com/en/repositories/managing-your-repositorys-settings-and-features/customizing-your-repository/about-readmes) and Wenger's article on [Why having a Readme on your internal project is essential](https://wengerk.medium.com/why-having-a-readme-on-your-internal-project-is-essential-c85cb9dd8e65) in mind [[1]](#1) [[2]](#2).     
MarkDown was used in this README file and was based on [GitHub's Documentation](https://docs.github.com/en/get-started/writing-on-github/getting-started-with-writing-and-formatting-on-github/basic-writing-and-formatting-syntax) [[3]](#3).

## About This Project

The Weather Data Processing Report showcases acquired knowledge with Unix commands such as `mkdir`, `wget`, and `touch`, as well as the use of the `date` command for timestamp generation. It also highlights Python programming skills, particularly with the `pandas` library for reading, inspecting, and analyzing JSON data. The ability to troubleshoot and optimize processes, including debugging scripts and using resources like manual pages, is also evident. Overall, the report reflects a blend of command-line, automation techniques, and data analysis capabilities which reflects the content learned in the module of Computer Infrastructure.

The data used in this project was obtained from [Met Eireann - Irish Meteorological Service](https://www.met.ie) website which provides weather information and related services to the public and specialized sectors such as aviation and agriculture. Met Eireann monitors, analyzes, and predicts Ireland's weather and climate, utilizing the latest technological and scientific advances to improve the accuracy and effectiveness of its forecasts [4](4).

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
Trigger workflows via [.github/workflows/weather-data.yml](.github/workflows/weather-data.yml) by running [weather.sh](weather.sh). The `weather.sh` script downloads and saves Athenry's current weather data from the Met Éireann API with a timestamped filename.

3. Process Data 
   - Timestamp files: Stored in [data/timestamps/](data/timestamps/).  
   - Downloaded weather data: Check [data/weather/](data/weather/) for timestamped JSON files.

4. Analyze Weather Data  
Open [weather.ipynb](weather.ipynb) in Jupyter Notebook to explore and analyze the weather records.

The file weather.ipynb documents a comprehensive process for weather data collection and analysis using Bash scripting and Python. It begins by outlining tasks such as creating directory structures, generating and formatting timestamps, and automating data downloads from Met Éireann’s API. Each task is meticulously detailed with commands like mkdir, date, and wget, explaining how to dynamically name and save weather data files with timestamps.

The later sections cover creating and testing a Bash script (weather.sh) to automate data downloads, and a brief analysis of one of the collected weather data files. The analysis includes a short explanation of the dataset obtained from data.gov.ie, rounding out the report as a complete guide to data acquisition, management, and preliminary examination.

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

<a id="2">[2]</a> Basic writing and formatting syntax (no date) GitHub Docs. Available at: https://docs.github.com/en/get-started/writing-on-github/getting-started-with-writing-and-formatting-on-github/basic-writing-and-formatting-syntax (Accessed: 29 April 2024).       

<a id="3">[3]</a> Basic writing and formatting syntax (no date) GitHub Docs. Available at: https://docs.github.com/en/get-started/writing-on-github/getting-started-with-writing-and-formatting-on-github/basic-writing-and-formatting-syntax (Accessed: 29 April 2024).   

<a id="4">[4]</a> https://www.met.ie/about-us
