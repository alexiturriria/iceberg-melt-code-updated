# iceberg-melt-code
Code to estimate iceberg melt rates from repeat high-resolution digital elevation models of icebergs. This readme will be updated as the code is finalized.

Overview:
This code uses repeat pairs of ortho images and digital elevation models, produced by either the Polar Geospatial Center or in-house using the Ames Stereo Pipeline, from the WorldView constellation of satellites to estimate iceberg volume change and submarine melt rate. Ideally, data are filtered so that only repeat pairs that contain a subset of the same icebergs are run through the pipeline, since repeat observations are needed to estimate melt rates using an elevation-differencing approach. 

To run the pipeline, open Polar_iceberg_meltrate_estimation_pipeline.m and modify the paths and other variables in the top section. This should provide all the customization that you need to run the code on your computer! This wrapper coder will then call a number of other functions, depending on Matlab-prompted user inputs, to track icebergs, extract iceberg volume changes, and convert the volume change observations to melt rate estimates.


Dependencies:
1) RACMO or other SMB data are also needed to convert volume change to melt rate.
2) Each function called by the wrapper lists its dependent functions in the readme. If they are not found in this repository, please ask the code developer (ellynenderlin@boisestate.edu) for these files since they are provided by others and are archived in a separate repo.
