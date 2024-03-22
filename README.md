# Prediction of Basic pKa Values in Nitrogen Compounds
This GitHub repository provides a user-friendly guide for Windows users to predict basic pKa values in nitrogen compounds, utilizing ORCA and Multiwfn. It includes simple instructions for setup, structure preparation, and calculations, with additional steps for large structures on Linux systems.

NOTE: This script is supported in the following article https://doi.org/10.1186/s13321-023-00763-3. If this tool is used, please cite article.

## Getting Started

Download and decompress all required files to your preferred location, referred to as the "main folder." The folder includes instructions for installing necessary programs like ORCA, Multiwfn, and Python. You will also need a molecular structure creator and editor, as outlined in the "Molecular visualization software" document.

## Step-by-Step Guide

1. **Structure Preparation:**
   - Draw the structure of the base and conjugate acid in xyz format.
   - Ensure:
     a) The base has a net charge of zero, and the conjugate acid has a net charge of +1. Add Cl<sup>-</sup> or Na<sup>+</sup> ions if needed.
     b) The target nitrogen atom should be the first atom in the xyz file's coordinate matrix. Edit using any text reader.

2. **File Naming:**
   - Name the xyz files "Base.xyz" for the non-protonated compound and "Conjugate_acid.xyz" for the protonated one, using capital letters.

3. **File Replacement:**
   - Replace old inputs with these new files in the "main folder."

4. **Running the Calculation:**
   - Double-click the `RUN.bat` file. The pKa value will display after calculations.

## Additional Steps for Large Structures

If structures are too large for a regular computer, optimize them using ORCA on Linux on a high-performance computer. Follow these steps:

1. **Optimization with ORCA:**
   - Use ORCA on Linux to optimize structures. Inputs in `.inp` format are in the "main folder."
   - After optimization, copy the out and gbw files to the "main folder."

2. **Running Alternate Batch Files:**
   - For optimized structures, run `RUN2.bat` (not `RUN.bat`) to get the pKa value.

3. **Calculating Required Single Points:**
   - If pKa calculations are still lengthy, use ORCA on Linux for single-point calculations.
   - Run `N_generate.bat` to create inputs `N.inp`, `N+1.inp`, and `N-1.inp`.
   - Copy the outputs to the "main folder" and run `RUN3.bat` to get the pKa value.

## Conclusion

These steps enable Windows users unfamiliar with computational chemistry to predict basic pKa values in nitrogen compounds. For any issues, refer to the detailed documents in the main folder.
