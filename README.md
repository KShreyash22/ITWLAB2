# ITWLAB2
#!/bin/bash

# A simple shell script that displays system info and does basic operations.

# 1. Display the current date and time
echo "Current Date and Time: $(date)"

# 2. Display the system's uptime
echo "System Uptime: $(uptime -p)"

# 3. Ask the user for their name
echo "Please enter your name: "
read name
echo "Hello, $name!"

# 4. Perform a simple arithmetic operation
echo "Enter two numbers to add:"
read num1
read num2
sum=$((num1 + num2))
echo "The sum of $num1 and $num2 is $sum"

# 5. List files in the current directory
echo "Files in the current directory:"
ls -l

# 6. Check if a directory exists
echo "Enter a directory name to check if it exists:"
read dir
if [ -d "$dir" ]; then
    echo "Directory '$dir' exists."
else
    echo "Directory '$dir' does not exist."
fi

# 7. Create a simple log file and append data
echo "Logging system info to 'log.txt'..."
echo "Logged at: $(date)" >> log.txt
echo "Uptime: $(uptime -p)" >> log.txt

# 8. Display the contents of the log file
echo "Contents of 'log.txt':"
cat log.txt

# End of script
echo "Script execution completed."
