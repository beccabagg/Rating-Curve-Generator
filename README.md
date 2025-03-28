## Rating Curve Generator ##
This Shiny application generates discharge rating curves from stage and discharge measurements. It provides a user-friendly interface for uploading data, configuring model parameters, and visualizing the results.

## Features ##
- Data Upload: Accepts .xlsx files exported from the Rating Review Tool (RRT).
- Segmented Power Law Model: Supports flexible modeling with user-defined breakpoints to handle different behaviors across the rating curve's range.

## Interactive Inputs: ##
- Stage at Zero Flow (datum correction).
- Maximum discharge for the rating curve.
- Number of breakpoints for the segmented model.

## Outputs: ##
- Rating curve plot with observed data points, predicted curve, and segment breakpoints.
- Table of predicted gage heights and discharges.
- Model fit statistics, including R-squared, adjusted R-squared, RMSE, and the number of observations.
- Error Handling: Provides notifications for missing or invalid data, segmentation errors, and fallback to linear models when necessary.
  
## How to Use ##
- Prepare Data: 
Export the field measurements table from RRT.
Ensure the .xlsx file contains the required columns: Gage height (ft), Discharge (ft^3/s), and optionally Use.
Do not edit the .xlsx file before uploading.

- Upload File:
Use the "Upload .xlsx File" input to upload your data.

- Configure Parameters:
Set the "Stage at Zero Flow" (datum correction).
Specify the "Maximum Discharge" for the rating curve.
Adjust the "Number of Breakpoints" for the segmented model.

- Process Data:
Click the "Process Data" button to generate the rating curve.

- View Results:
Rating Curve Plot: Displays observed data, predicted curve, and segment breakpoints.
Breakpoints Table: Lists segment breakpoints with corresponding stage and discharge values.
Rating Table: Provides a table of predicted gage heights and discharges.
Model Statistics: Displays R-squared, adjusted R-squared, RMSE, and the number of observations.
Notes
The segmented model provides flexibility to handle different behaviors across the rating curve's range.
The app is not configured to compute offset values.
For questions, contact Rebecca Baggott at rbaggott@usgs.gov.
Dependencies

The script requires the following R packages:

ggplot2
readxl
shiny
segmented
If any of these packages are missing, the app will attempt to install them automatically.

Running the App
To run the app, execute the following command in R:

Replace "path/to/app.R" with the actual path to the script.
