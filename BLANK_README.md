# ADVANCE ENERGY INSIGHTS
<!-- PROJECT SHIELDS -->
<!--
*** I'm using markdown "reference style" links for readability.
*** Reference links are enclosed in brackets [ ] instead of parentheses ( ).
*** See the bottom of this document for the declaration of the reference variables
*** for contributors-url, forks-url, etc. This is an optional, concise syntax you may use.
*** https://www.markdownguide.org/basic-syntax/#reference-style-links
-->

<!-- TABLE OF CONTENTS -->
<details open="open">
  <summary><h2 style="display: inline-block">Table of Contents</h2></summary>
  <ol>
    <li>
      <a href="#about-the-project">About The Project</a>
      <ul>
        <li><a href="#features">Features</a></li>
      </ul>
    </li>
    <li>
      <a href="#getting-started">Getting Started</a>
      <ul>
        <li><a href="#prerequisites">Prerequisites</a></li>
        <li><a href="#project-dependencies">Project Dependencies</a></li>
        <li><a href="#installation">Installation</a></li>
        <li><a href="#additional-documentation">Additional Documentation</a></li>
      </ul>
    </li>
    <li><a href="#contributing">Contributing</a></li>
    <li><a href="#contact">Contact</a></li>
  </ol>
</details>



<!-- ABOUT THE PROJECT -->
## About The Project
This repository is part of the project for **Advance Energy Insights** where we are aiming to provide with regression tools for energy forecasting, baselining and benchmarking. 

The project can be divided in two categories:

**1. Forecasting Regression Tool:** This tool provides with a forecast of energy consumption in a frequency of hours and days.

**2. Benchmarking:** This set of numerical calculations, calculate the CDD (Cooling Degree Day) according to the desired threshold for energy benchmarking purposes.


### Features
The repository is divided into the following files:
* **Main_Script_H & Main_Script_D:** These are the main scripts that will call the ones below. The one ending in "H" will forecast for hourly values whereas the one ending in "D" will forecast daily values.
* **Preprocess_resample:** This function takes care of the NaNs, performs interpolation and resamples to the desired frequency.
* **feature_selection:** This function performs feature selection by variance threshold, and by an ANOVA test where it will return a ranking of the most influencial parameters on energy.
* **Polynomial_regression:** This function performs a univariate third order polynomial regression in the same manner as DES tool would do.
* **knn_regression:** This function performs a multivariate knn regression with the features selected from the "feature_selection" script.
* **plots:** Plots function graphically shows the results of the forecast regression tools.
* **TO_POWERBI:** This script is the only one not called by the "Main_Script". In here, the daily and hourly results are combined and arranged to be suitable for the POWERBI dashboard.



<!-- GETTING STARTED -->
## Getting Started

To get a copy up and running follow these simple steps.

### Prerequisites

To run this project, you need a conda installation with Python 3.8 or higher. follow the tutorial on [activestate](https://www.activestate.com/resources/quick-reads/how-to-manage-python-dependencies-with-conda/) to install the
needed packages in the requirements.txt file included.

### Project Dependencies
Access to Azure machine learning is also needed to run and monitor the training of the Ml algorithm as well as viewing results. please login to [Azure](https://portal.azure.com)

### Installation

1. Clone the repo
   ```sh
   git clone https://danfoss.visualstudio.com/ECSServiceSandbox/_git/Energy
   ```
2. Install txt depencencies


<!-- USAGE EXAMPLES -->
## Additional Documentation

_For more detailed explanations, please refer to the [Documentation](https://danfoss.visualstudio.com/ECSServiceSandbox/_wiki/wikis/ECSServiceSandbox.wiki/8868/Advanced-Energy-Services)_



<!-- CONTRIBUTING -->
## Contributing

Contributions are what make the open source community such an amazing place to be learn, inspire, and create. Any contributions you make are **greatly appreciated**.

1. Fork the Project
2. Create your Feature Branch (`git checkout -b feature/AmazingFeature`)
3. Commit your Changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the Branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request



<!-- CONTACT -->
## Contact

Leire Chavarri - leire.chavarri@danfoss.com

Project Link: [https://danfoss.visualstudio.com/ECSServiceSandbox/_git/Energy](https://danfoss.visualstudio.com/ECSServiceSandbox/_git/Energy)

