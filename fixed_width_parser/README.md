# Fixed Width Parser

## Overview

`fixed_width_parser` is a Python library designed to parse fixed-width formatted files. Fixed-width files are plain text files where each column has a fixed width, and this library helps in extracting and processing the data efficiently.

## Features

- Parse fixed-width formatted files
- Define custom column widths
- Handle large files efficiently
- Convert parsed data to CSV format

## Points to be noted

- The fixed width file was generated manually using the spec.json file provided and it is stored in the input_files/fixed-width-file.txt.
- The output is a CSV file for the given fixed-width-file.txt file stored in output_files/csv_file.csv.
- Empty rows in fixed width file are retained in CSV file as well.
- Special operators like '(single quotes), "(double quotes), ,(comma) etc are preserved in CSV file.
- There is already a sample_output.csv file placed manually in the output_files. Exact same file (csv_file.csv) will be generated after executing the program.

## Instructions

### Installation

1. Ensure you have Python 3 installed. You can download it from [python.org](https://www.python.org/).

### Running the Parser

1. Navigate to the project directory:
    ```sh
    cd Demyst/fixed_width_parser
    ```

2. Run the parser using the following command:
    ```sh
    python -m src.main
    ```

### Running the Tests

1. Navigate to the project directory:
    ```sh
    cd Demyst/
    ```

2. Run the parser using the following command:
    ```sh
    python -m unittest fixed_width_parser.tests.test_parser
    ```

### Use Docker Image

1. Navigate to the parser directory with Dockerfile:
    ```sh
    cd Demyst/fixed_width_parser
    ```

2. Build docker container:
    ```sh
    docker build -t fixed-width-parser .
    ```
3. Run docker container (The output CSV file will be stored in docker_output in your current directory):
    ```sh
    docker run -v $(pwd)/docker_output:/app/Demyst/output_files --workdir /app/Demyst fixed-width-parser
    ```

    For Power Shell

    ```sh
    docker run -v ${pwd}/docker_output:/app/Demyst/output_files --workdir /app/Demyst fixed-width-parser
    ```
