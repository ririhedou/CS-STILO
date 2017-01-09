# CS-STILO
The implementation of STILO (STatically InitiaLized markOv) and its extension CMarkov (Context-sensitive Markov )

## Step 1: Extract CFG from a program

Folder: parse-program:

- input: executable program
- output: the control flow graph 

parse the program to generate the control flow graph (cfg.dot) and extract all the functions in the program (all_functions)


## Step 2: Initialize Transitive Probabilities for HMM

Folder: process_graph:

- inpput: the control flow graph 
- output: transition probabilities matrix   


## Step 3: Train the HMM with collected traces
We use syscall as the example.

Folder: syscall -> used by STILO (context insensitive traces)

Folder: syscall-context -> used by CMarkov (context sensitive traces)

For how to collect traces using strace/ltrace based on the SIR project, please refer to 
[traceCollect](https://github.com/yaoGroupAnomaly/traceCollect)

 
- input: traces and the initialized model 
- output: the trained model


# Dependencies:

Dyninst-8.0

jahmm-0.6.1.jar
