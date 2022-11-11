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
*WARNING*: the following script was tested with python version 3.10.6 other python versions may give errors or may not work.
To check your version of python from the terminal, type:* `python3 --version`
\
\
To launch the file from the terminal move to the folder that contains the script and type:
```
python3 traceGenerator.py 
```
*N.B. if the file might be to be made executable, to do so use:* `chmod +x traceGenerator.py` 

## How to use
A folder containing log files has been provided as an example in this repository: [log_files_example](https://github.com/piquet8/TraceGenerator_Script/tree/main/log_files_example)\
In the next screens we see how the algorithm works by referring to the file given as an example.
When the script is launched you are asked which of the 3 functions you want to use:\
\
![figure1](https://github.com/piquet8/TraceGenerator_Script/blob/main/media/figure1.png)\
\
By selecting the first option we choose to convert a log file to the corresponding track. Before doing this we are prompted to set the coordinates related to the
extremes of the map where the execution takes place. \
\
![figure2](https://github.com/piquet8/TraceGenerator_Script/blob/main/media/figure2.png)\
\
After assigning the coordinates, you are prompted for the name of the file to convert (note, the file must be in the current folder of this script)\
\
![figure3](https://github.com/piquet8/TraceGenerator_Script/blob/main/media/figure3.png)\
\
What we receive as output is the sequence of t-uples that make up the trace and the outcome of the execution.\
\
![figure4](https://github.com/piquet8/TraceGenerator_Script/blob/main/media/figure4.png)\
\
By selecting the second function instead we convert a folder of log files to a folder of tracks. Again, it is necessary initially to provide the coordinates of the extremes of the map used in the executions.\
\
![figure5](https://github.com/piquet8/TraceGenerator_Script/blob/main/media/figure5.png)\
\
Once the coordinates are set, we need to provide the path to the folders we want to convert.\
\
![figure6](https://github.com/piquet8/TraceGenerator_Script/blob/main/media/figure6.png)\
\
Finally with the third function we give as input a folder containing the traces and get as output a sample containing all positive traces followed by all negative traces. \
\
![figure7](https://github.com/piquet8/TraceGenerator_Script/blob/main/media/figure7.png)
