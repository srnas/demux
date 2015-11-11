# demux
Perl script to demux gromacs trajectories, with a fix that allows long trajectories to be processed correctly.

The script solves an issue in the original demux.pl that makes the demuxed trajectories when the following conditions are simultaneously true:
- Trajectories are longer than 100 ns
- Exchange stride is not a multiple of 1 ps

At variance with the original script, this script asks interactively the timestep and compute the time from the timestep and the number of the step.

The script is based on the official one found in the gromacs distribution. The modification has been implemented and tested by Andrea Perez-Villa and Sandro Bottaro.
