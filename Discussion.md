# Log_Retrieval_solution

##Approach to Solve the Problem:

Understand the Input Format:

The input is a ZIP file containing a large log file (~1TB).
The log file has entries with timestamps (assumed to be YYYY-MM-DD at the start of each line).
Decomposing the Task:

Extract the log file from the ZIP archive.
Read the log file efficiently (line-by-line) to avoid memory overflow.
Group logs by date and write them into separate files.
Optimizing for Performance:

Use streaming read to handle large files.
Maintain file handles dynamically using a dictionary (defaultdict).
Close file handles after processing to prevent resource exhaustion.

##Final Solution Summary:
The solution efficiently extracts logs from a ZIP file and processes them without loading everything into memory.
Logs are split into separate files based on the date appearing in each log entry.
The implementation ensures scalability by handling large datasets and using optimized file handling.

##Steps to Run:
Prepare the Environment:

Install Python if not already installed.
Place the ZIP file (e.g., your_zip_file.zip) in the same directory as the script.
Run the Script:

Open a terminal or command prompt.
Navigate to the script directory.
Execute:
bash
Copy
Edit
python process_logs.py
Check Output:

The extracted log file will be stored in the logs/ directory.
Processed logs will be stored in the output/ directory as files named output_YYYY-MM-DD.txt.
