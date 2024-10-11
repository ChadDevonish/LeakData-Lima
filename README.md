# Life-Bear Data Processing Script

## Overview

This repository contains a Python script designed to process a large CSV dataset related to Protexxa/Life-Bear. It includes functionality for splitting large files, handling missing and invalid data, removing empty lines, and structuring the data for further analysis. The script operates on CSV files stored in Google Drive and processes them in chunks to avoid memory overload.

## Prerequisites
Before running the script, ensure that you have the following:

Google Colab or a local Python environment with access to Google Drive.
Required Python libraries:
pandas
numpy
os
csv
re
random
datetime
dateutil

## Setup Instructions
### Step 1: Mount Google Drive
Ensure you have access to the dataset in your Google Drive. The following command mounts Google Drive for access in Google Colab:

from google.colab import drive
drive.mount('/content/drive')

### Step 2: Define File Paths
Set the path to your CSV file and output folder in Google Drive:

### file_path = '/content/drive/My Drive/Protexxa/Life-Bear/Life-Bear-Data.csv'
output_folder = '/content/drive/My Drive/Protexxa/Life-Bear/output'
 
## Functions
### 1. Split Large Files into Chunks
This function splits large CSV files into smaller chunks based on a specified size (in MB).

def split_file(file_path, chunk_size, output_directory):
    # Splits large files into smaller chunks to avoid memory issues.
