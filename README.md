# NDAV-Training : Event Filtering (Mantid)

## Neutron Events

I believe that everyone knows about this!

## Filter Events

FilterEvents (http://docs.mantidproject.org/nightly/algorithms/FilterEvents-v1.html)

### Mandatory Inputs
1. Input EventWorkspace for splitting from;
2. Splitters
  * SplittersWorkspace
  * MatrixWorkspace
  
  Each splitter is composed by
  * Start time;
  * Stop time;
  * Target workspace number
  
  Start and stop time can be either absolute time (epoch time) or relative time (to run start time or user defined time)

### Optional Inputs
1. Splitting information TableWorkspace
2. TOF correction from detector to sample
  * TOF correction MatrixWorkspace
  * from instrument geometry: elastic, direct and indirect

## Generate Events Filter Manually

Users can create an arbitrary SplittersWorkspace or MatrixWorkspace according to their request.
They are required to be familiar with Mantid and Python.

## Generate Events Filter By Mantid Algorithms

GenerateEventsFilter (http://docs.mantidproject.org/nightly/algorithms/GenerateEventsFilter-v1.html) can help to generate splitters workspace if user wants to filter events by constant time step or by constant log value step.

### Common Mandatory Inputs:
1. Input workspace which may only contain meta data;
2. start time and stop time of the data 

### Filter by constant time step:
1. Time step

### Filter by constant log value step:
1. Minimum log value
2. Maximum log value
3. Log value step
4. Changing direction of log value: both, up or down

### MantidPlot - Filter Events GUI
