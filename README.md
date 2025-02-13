# AUTOMATED-REPORT-GENERATION-

COMPANY:CODTECH IT SOLUTIONS
NAME:AKSHAY.M
INTERN ID:CT08NEP
DOMAIN:PYTHON
BATCH DURATION:January 15th/2025 to February 15th/2025

### Description of the Script

This Python script is a versatile tool designed for analyzing CSV data and generating a professional PDF report summarizing the data. It combines the power of `pandas` for data manipulation and analysis with the `FPDF` library for creating formatted PDF documents. The script is ideal for professionals, data analysts, and developers who need to quickly analyze datasets and present their findings in a readable format.

---

### Script Breakdown

#### 1. **Importing Required Libraries**
The script imports two primary libraries:
- `pandas`: Used for reading the CSV file and generating descriptive statistics of the data.
- `fpdf`: Facilitates the creation of a PDF report, allowing for customized formatting and layout.

---

#### 2. **Functions**

##### a) `analyze_data(file_path)`
- **Purpose**: Reads the data from a CSV file and generates descriptive statistics.
- **Input**: Path to the CSV file (`file_path`).
- **Output**:
  - `df`: The DataFrame containing the dataset.
  - `summary`: A DataFrame containing the summary statistics (e.g., count, mean, standard deviation, min, max).
- **Process**: 
  - Reads the CSV file using `pandas.read_csv()`.
  - Computes descriptive statistics using `DataFrame.describe(include="all")`, which includes both numerical and categorical data.

##### b) `generate_pdf_report(summary, output_file)`
- **Purpose**: Generates a PDF report summarizing the data analysis.
- **Input**:
  - `summary`: The summary statistics DataFrame.
  - `output_file`: Name of the PDF file to save the report.
- **Output**: A PDF file containing a formatted table of the summary statistics.
- **Process**:
  - Initializes an `FPDF` object and sets up the page layout.
  - Adds a title to the report and includes a table to display the summary statistics.
  - Iterates over the summary DataFrame to dynamically populate the PDF with headers and content.
  - Saves the PDF file to the specified path.

---

#### 3. **Execution**
The script can be executed as a standalone program. Upon execution:
- The user specifies the CSV file (`data.csv` by default) and the desired output PDF file name (`report.pdf` by default).
- The script attempts to:
  1. Analyze the CSV data using `analyze_data()`.
  2. Generate a PDF report with the analysis using `generate_pdf_report()`.
- If any errors occur (e.g., file not found, incorrect file format), they are caught and displayed with an appropriate error message.

---

### Key Features
- **Data Analysis**: Computes comprehensive statistics such as count, mean, standard deviation, minimum, and maximum for numerical data, and unique values and frequency for categorical data.
- **Dynamic PDF Report**: Creates a well-structured PDF report with a title and a tabular format, automatically adjusting to the input data's structure.
- **Error Handling**: Ensures the script gracefully handles errors, making it robust for various use cases.

---

### How to Use
1. Place the script in a directory with the required CSV file (`data.csv` by default).
2. Update the `input_file` variable if the file name differs.
3. Run the script in a Python environment.
4. Locate the generated PDF report in the specified output path.

---

### Applications
This script is suitable for:
- Automating data reporting tasks.
- Providing quick summaries of datasets for business insights.
- Converting raw CSV data into presentable PDF reports.

By integrating the functionalities of `pandas` and `FPDF`, this script serves as a practical solution for data analysis and reporting workflows.


