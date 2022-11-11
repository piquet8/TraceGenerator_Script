# TraceGenerator_Script
This script provides a tool that can be used to create Boolean traces and trace samples from the log files of different executions. 
- Define **log file** as a set of information (in the form of messages exchanged by the components of a system) representing the change in certain parameters during the execution of that system. 
- Define **trace** as a sequence of t-uples containing Boolean values that can change from one t-uple to the next.
- Define **sample** as the set of all positive and negative traces (first all positive then all negative traces)  

The algorithm offers three modes of operation:
- **LOG FILE ⟶ TRACE**\
takes a log file in .txt format and returns its trace in a .json file (the new file ends with _s.json if the log file is related to a successful execution, with _f.json if the execution failed)
- **LOG FILES FOLDER ⟶ TRACES FOLDER**\
takes a folder containing multiple log files and returns a folder containing all the related traces
- **TRACES FOLDER ⟶ SAMPLE**\
takes a folder containing all traces and returns a sample

## How to launch
Download the folder or clone it wherever you want:
```
https://github.com/piquet8/TraceGenerator_Script.git
```
To launch the file from the terminal move to the folder that contains the script and type
```
python3 traceGenerator.py 
```
*N.B. if the file might be to be made executable, to do so use:* `chmod +x traceGenerator.py` 

## How to use
A folder containing log files has been provided as an example in this repository: [log_files_example](https://github.com/piquet8/TraceGenerator_Script/tree/main/log_files_example)\
In the next screens we see how the algorithm works by referring to the file given as an example.