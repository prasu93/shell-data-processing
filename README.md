# shell-data-processing

## Retrieving text from a URL
* We use curl command to extract the data from a particular URL. For storing the extracted data into a file, we will use -O option. The command will be like: ```curl "http://shakespeare.mit.edu/romeo_juliet/full.html" -O data.txt```

## Processing text data
* ```tr ' ' '\12' < data.txt``` -> Command for transforming each line into individual words.
* ```tr ' ' '\12' < data.txt | sort``` -> Command for sorting the data in the text file.

Note: We use pipe symbol for giving output of one command as input to another command.

* ```tr ' ' '\12' < data.txt | sort | uniq -c``` -> Command for piping the sorted output to uniq -c to count.
* ```tr ' ' '\12' < data.txt | sort | uniq -c | sort -nr``` -> Command for piping the reduced output to sort with -nr flag. 'n' is for numerical comparision and 'r' is for reverse order.
* ```tr ' ' '\12' < data.txt | sort | uniq -c | sort -nr > result.txt``` -> Command for storing the total output after processing all the preceding commands to result.txt file.
* In bash shell, up arrow will be used to display the previosuly executed commands.
* Even the flag is single letter or more than one letter, only one dash will be used. 