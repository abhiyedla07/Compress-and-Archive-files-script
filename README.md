# Compress-and-Archive-files-script
compressing larger files and archiving

This Bash script automates the process of compressing and archiving files larger than 20MB within a specified directory. Here's what it does:

Variables Setup:

The script defines several variables:
$BASE: Specifies the directory where files are located.
$DAYS: Determines the number of days since the last modification of files to consider.
$DEPTH: Sets the maximum depth of subdirectories to search for files.
$RUN: A flag to control whether the compression and archiving should be performed.

Directory Existence Check:
It checks if the base directory specified by $BASE exists. If not, it prints an error message and exits.

Archive Directory Creation:
If an 'archive' directory does not exist within the base directory, the script creates one.

Finding Large Files:
Using the find command, the script searches for files larger than 20MB in the specified directory ($BASE).

Compression and Archiving:
For each large file found, if the $RUN flag is set to 0, the file is compressed using gzip.
The compressed file is then moved to the 'archive' directory.
