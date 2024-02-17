# Manufacturing-Process-Optimization-TensorFlow
Create neural network using 3 years of lab and controller data to identify machine and process improvements

### System Description:
* A mixer processes media for use in production line. After use, the material comes back to be mixed again. 
* 3 control parameters are in the data, Process disruptions and other variations have a large effect on the system but are not controlled
*  

### Goal
* identify ideal set points for control parameters
* identify key measured values for high scrap rates - these will be plotted and analyzd real time
* identify equipment issues and associated cost for CAPEX planning

### Model Definition: 
Output Data (y value) = scrap %

Input data (X values) :


|                  |Temp F|Set Point 1|Measrued 1*|Water Set Point|Water Added|Sys Bias  |Strength*|Moisture*|Addition 2|Calculated|Batch Weight|Mixer Amps|
|----------------- |------|-----------|---------- |---------------|-----------|----------|-------- | ------- | -------- | -------  | ---------- | -------- |
|Range             |0-238 | 0-90      |0-100      |0-194          | 0-194     |-27 to 113| 0-438   | 0-650   | 0-422    | 0-1260   | 2500-3500  | 0-354    |
|Mean              |97.83 | 48.0      |48.2       |81.1           | 81.2      |15.6      | 197     | 316     | 179      | 620      | 2650       | 151      |
|St deviation      |16.63 | 3.78      |5.27       |14.93          | 15.0      |9.1       | 30.8    | 30      | 62.05    | 57.4     | 230        | 18       |
|Adjustable        |      | X         |           |X              |           |          |         |         | X        |          | X          |          |
|Exclude in model  |      |           |           |               |           |          |         |         |          |          |            |          |
