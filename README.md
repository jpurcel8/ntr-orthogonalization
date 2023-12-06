# NTR Orthogonalization Library

## Overview

The NTR Orthogonalization Library is a specialized MATLAB toolkit designed to aid fMRI block-based studies in constructing word lists for their experiments. By ensuring minimal correlation between words, the library helps scientists optimize the construction of word lists, thereby enhancing the precision of fMRI studies.

## Features

- **Minimized Word Correlation**: Construct word lists with minimal inter-word correlations.
- **Adjustable Word List Length**: Tailor the length of word lists while maintaining minimal correlation.
- **User-Friendly Interface**: Designed for scientists with varying levels of coding experience.
- **Customizable**: Accommodates unique datasets and parameters to fit specific project needs.
- **Visualization Tools**: Visualize distance matrices and correlations to aid study design.
- **Extensibility**: Designed for ease of extension to cater to related projects.

## Algorithm

The core algorithm behind the NTR Orthogonalization Library focuses on minimizing the correlation between words in block-based fMRI studies. The algorithm achieves this by:

1. Calculating pairwise correlations between words based on their semantic vectors.
2. Creating a triangular distance matrix that represents the semantic distances between words.
3. Iteratively adjusting the word list to minimize the overall correlation while maintaining the desired length.

This approach ensures that the word lists generated are both short and minimally correlated, optimizing the precision of fMRI studies.

## Getting Started

### Prerequisites

- MATLAB (R2019a or later recommended).
- Data files (e.g., `wordinput_1.csv`) should be placed in the `data` directory.

### Setup

1. Clone or download the repository to your local machine.
2. Open MATLAB and open the root folder of this project. Immediately to the left of the text showing the current path, select the icon with the folder and green arrow and navigate to the root folder `ntr-orthogonalization`.
3. When running a script in this library for the first time, you may be asked by MATLAB to add the folder to the working path. When prompted, select "Add to Path."

## Usage

### NTR_Orthogonalization_v16_listinput.m

The primary script to run the library's functionality is `NTR_Orthogonalization_v16_listinput.m`. This script takes in a list of words and outputs distance matrices for those words. An example word list is provided in `data/wordinput_1.csv`.

If you want to use your own list of words, create a .csv file with each of the words in a different cell, in all lowercase, in a single row. Replace `data/wordinput_1.csv` with this file, or edit the `NTR_Orthogonalization_v16_listinput.m` script to accomodate the name and location of your file in the line reading

`wordlistinput = readtable("data/wordinput_1.csv", 'ReadVariableNames', false);`

### NTR_Orthogonalization_v16_random_iterations.m

The script `NTR_Orthogonalization_v16_random_iterations.m` generates distance matrices from a random list of words.

## Contribution and Support

Contributions to enhance the library are welcome. If you encounter any issues or have questions regarding its use, please raise an issue on the GitHub repository.

## License

This project is open-source. Please refer to the `LICENSE` file for more details.

## Acknowledgments

- The initial foundation of this library is based on the work done in the original fMRI block-based study script by Audrey Lyu.
