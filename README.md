Rate model network with ring connection architecture and short-term synaptic depression. Represents a cortical hypercolumn in visual coretex V1.

Was used to perform calculations for the paper https://www.frontiersin.org/articles/10.3389/fncom.2017.00021/full

ring.py is the main script which by default calculates a single trace and plots it

Variable CalcMode on 16th line defines calculation mode:
* for value 0 single realisation with amplitude of visual stimuli C = 10 is calculated and then printed.
* for value 1 realisations for different U, I0 is calculated and saved into files. Parameters of simulations are reflected in saved file names.
* for value 2 U is set from argv and then single realisation is calculated (can be used for parallel calculation with GNU parallel)
* for value 3 I0 vs U curve is calculated and saved into file by bisection method. To do this variable C on 42th line shoud be nulled.

resultsPlot.py plots the results calculated by ring.py when CalcModel was 1 or 2 (parallel calculation)
For proper work variables SimTime, C, freq, N etc. should be same as in ring.py
