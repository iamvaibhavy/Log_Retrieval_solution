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
