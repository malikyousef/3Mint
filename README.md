# 3Mint

The 3Mint analysis treats the data types of microRNA (miRNA), methylation (CpG) and gene expresssion (mRNA) in terms of 3-way relationships, giving different levels of impact of each towards understanding the cellular behavior of
defined groups of BRCA.

# Data Preparation
The 3 different data sheets consist of rows and columns representing same sample IDs in an order and features, respectively. The workflow created in KNIME analytics platform takes the data sheets as ‘.table’ extension files. The last column represents the class information for control and case (tumor) samples or subtypes of the disease. The binary class information should be defined as string. 

  -The link for downloading KNIME: https://www.knime.com/downloads
  -For more information about the Knime platform, please visit https://www.knime.com/software-overview

# 3Mint Main Workflow
 
 
 
# Set up Parameters

3Mint default parameters are given below. The SetParameters node allows the users to change the parameters. 
  - Positive Correlation Threshold (Default: 0.6)
  - Negative Correlation Threshold (Default: -0.6)
  - Number of iteration (Default: 100)
  - Number of Group (Default: 10)
  -	Number of iterations for Internal Rank (Default: 10)
  -	Performance metric (Accuracy, Precision, Sensitivity, etc.) weight (Default for accuracy: 1.0)

The 3Mint metanode in the main workflow contains Filter Genes, Highly correlated miRNAs (microRNAs) and CpGs (methylation data), Grouping and Group ranking metanodes. These metanodes constitute the framework of the Grouping-Scoring-Modelling Approach.
 
 
 
 
# The Environment Settings of 3Mint
After installing KNIME Analytics platform, 3Mint workflow is downloaded and imported into the KNIME. The workflow contains R scripts therefore the following commands should be followed to prevent errors.
Before initiation of the workflow process in KNIME, R / RStudio is required to be run with following commands:
  - library(Rserve);
  - Rserve(args = "--vanilla") 
  -	library(tidyr)

Execution of R / RStudio and the workflow simultaneously enables the 3Mint analysis without retrieving any error. 
