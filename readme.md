# Global Bank Data Extraction by Country

## Overview

This project is aimed at providing an accurate and up-to-date source of bank data for countries around the world. The data includes **bank names**, **SWIFT codes**, and **country codes**, extracted from multiple reliable sources. All data is stored in JSON files, organized by the country’s ISO 3166-1 alpha-2 country code (e.g., `US.json` for the United States, `DE.json` for Germany).

The purpose of this repository is to share the bank data extracted from a variety of financial databases, such as central banks, SWIFT directories, and major banking associations. The data was challenging to obtain and verify, and I'm open to any contributions to help improve its accuracy and completeness.

## Project Structure

The repository contains two main components:

1. **Data Folder**: The `/data` folder contains the extracted bank data in JSON format, organized by country code. Each file contains a list of banks in the respective country, including the bank's name, SWIFT code, and country code.

2. **Notebook**: The Jupyter notebook (`bank_data_extraction_notebook.ipynb`) contains the code used to extract, process, and save the bank data. It uses OpenAI's GPT-4 model to fetch the bank details for each country, processes the data into a valid JSON format, and saves the output into individual JSON files per country code.

### Files in this repository:

- `/data`: Folder containing the extracted bank data for all countries.
- `bank_data_extraction_notebook.ipynb`: Jupyter notebook used for extracting and saving bank data.
- `README.md`: This file.

### Example of Data Format

Each country’s bank data is saved as a JSON file in the `/data` folder. For example, `US.json` contains the following data:

```json
[
    {
        "bank_name": "Bank of America",
        "swift_code": "BOFAUS3N",
        "country_code": "US"
    },
    {
        "bank_name": "Chase Bank",
        "swift_code": "CHASUS33",
        "country_code": "US"
    }
]
```

## Getting Started

### Prerequisites

- Python 3.x
- Necessary Python libraries (e.g., `openai`, `json`, `re`, etc.)

### Installation

1. Clone the repository to your local machine:
   ```bash
   git clone https://github.com/AbYT101/Global-bank-data.git
   cd bank-data-extraction
   ```

2. Install required dependencies:
   ```bash
   pip install -r requirements.txt
   ```

### Running the Notebook

To extract bank data for all countries, run the provided Jupyter notebook `bank_data_extraction_notebook.ipynb`. 

1. Open the notebook in Jupyter or your preferred IDE.
2. Make sure to replace the OpenAI API key in the notebook:
   ```python
   client = OpenAI(api_key='YOUR_API_KEY_HERE')
   ```
3. Execute the cells in sequence to extract and save the data.

The notebook will loop through all ISO 3166-1 alpha-2 country codes, fetch bank details for each country, and save the results as individual JSON files in the `/data` folder.

### Contributing

This project is open for contributions. If you have access to better or more accurate bank data, please consider contributing. You can help by:

- Adding missing data for any country.
- Correcting inaccurate or outdated data.
- Submitting pull requests with improvements to the extraction logic or data formatting.

To contribute, please fork the repository, make your changes, and submit a pull request.

### Issues

If you encounter any issues with the data or the extraction process, feel free to open an issue, and I will do my best to address it.

### License

This project is open-source and available under the [MIT License](LICENSE).
