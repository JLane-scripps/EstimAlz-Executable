EstimAlz

This tool processes quantitative mass spectrometry data for Aβ40 peptide isoforms and calculates the relative abundances of Alzheimer's subtypes (Type I and II). The script uses experimental signal ratios and blank thresholding to identify the dominant subtype per sample.  
Formulae and data gathered by Casimir Bamberger, code implemented by Jeff Lane.

# Alzheimer's Subtype Classifier
The EstimAlz executable will access each of the other three files, perform calculations, and create intermediary dataframes. Each action is logged. These intermediary dataframes are saved as their own excel files for the purpose of debugging and traceability, and can be found in the Output subfolder.
The final dataframe includes the conversion of detected labeled ratios into a percentage and probability score of Alzheimer's subtypes. This can be found as "Conversion_Matrix.xlsx" in Output. 
All actions are logged in the text file "pipeline_debug_{timestamp}.log", which will not be overwritten by subsequent runs. 
Currently, only Ab40_z4 is included; in the future, Ab42 and z5 will both be integrated. 

## How to Use
1. Ensure `Ab40_Transitions.xlsx`, `Ab40_z4.xlsx`, and `Ab40_PrecInt.xlsx` remain in the root folder.
2. Run the executable (or script).
3. Output is saved in the `/Output` directory.

## Included Files
1. `EstimAlz.exe`.
2. Three input files: `Ab40_Transitions.xlsx`, `Ab40_z4.xlsx`, and `Ab40_PrecInt.xlsx`.
3. `Expected Output`: a folder containing the results of our run of the executable.
4. `Output`: an empty folder to store the results of your run of the executable.

## Requirements
- Python 3.10+
- pandas, numpy, openpyxl

## License
MIT

