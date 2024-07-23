# Phone Number Formatting Script

This repository contains a Python script for formatting phone numbers with country codes. It processes non-standard phone numbers from Google Sheets, formats them correctly, and allows you to paste the results back into your Google Sheets for consistent formatting.

## Root Problem

The script addresses the issue where phone numbers entered in a spreadsheet are not in a standard format. Common issues include missing country codes, inconsistent international prefixes, or non-numeric characters. This script helps in standardizing phone numbers by adding the correct international dialing codes.

## Installation

To use the phone number formatting script, follow these steps:

### Prerequisites

- Python 3.x installed on your system.
- An IDE or text editor for running Python scripts (e.g., VSCode, PyCharm, Vim).

### Installation Steps

1. **Clone the Repository:**

   ```bash
   git clone https://github.com/grbade/phone_number_formatter.git
   cd phone-number-formatting
   ```

2. **Install Required Libraries:**

   The script uses the `re` library, which is included in Python's standard library, so no additional installations are required for dependencies.

## Usage

Follow these steps to format phone numbers using the script:

### 1. Prepare Your Data

1. **Copy Phone Numbers and Countries from Google Sheets:**
   - Open your existing Google Sheet that contains the phone numbers and countries.
   - Copy the entire column of phone numbers.
   - Copy the corresponding column of country names.

### 2. Update the Script

1. **Paste the Data into the Script:**
   - Open the `phone_number_formatting.py` file in your text editor.
   - Replace the `phone_numbers` and `countries` lists in the script with the copied data.

   Example:
   ```python
   # List of phone numbers from the input sheet
   phone_numbers = """355699823345
   614323322342
   43660112355""".split('\n')

   # List of countries corresponding to the phone numbers from the input sheet
   countries = """Albania
   Australia
   Austria""".split('\n')
   ```

2. **Run the Script:**

   Open a terminal and navigate to the directory containing the script. Run the script with:

   ```bash
   python3 phone_number_formatting.py
   ```

3. **Copy the Results:**
   - The script will output the formatted phone numbers in the terminal.

### 3. Paste Results Back into Google Sheets

1. **Open Your Google Sheet:**
   - Go to the Google Sheet where you want to paste the formatted phone numbers.

2. **Paste the Formatted Numbers:**
   - Copy the output from the terminal and paste it into the appropriate column in your Google Sheet.

### 4. Format Cells in Google Sheets

To ensure that phone numbers are displayed correctly:

1. **Select the Column with Formatted Phone Numbers:**
   - Click on the column header.

2. **Apply Custom Number Formatting:**
   - Go to `Format` > `Number` > `More Formats` > `Custom number format`.
   - Enter the format `"+"0` and click `Apply`.

This format will display the phone numbers with a `+` sign and the correct number of digits.

## Example

**Input Data:**

| Phone Number | Country      |
|--------------|--------------|
| 355699823345 | Albania      |
| 614323322342 | Australia    |
| 43660112355  | Austria      |

**Output Data:**

| Formatted Phone Number |
|------------------------|
| +355699823345          |
| +614323322342          |
| +434660112355          |

## Troubleshooting

- **Error Handling:** Ensure that the country names are spelled correctly and match the entries in the `country_to_code` dictionary in the script.
- **Formatting Issues:** Verify that custom number formatting is correctly applied in Google Sheets.

## Contributing

Feel free to fork the repository and submit pull requests if you have improvements or bug fixes.

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.
