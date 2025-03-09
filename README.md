# High Throughput Screening Analysis for Calcium-Activated Chloride Channels

## Overview
This project analyzes high-throughput screening (HTS) data to identify compounds that activate TMEM16A calcium-activated chloride channels. These channels play a critical role in various physiological processes, and their activation could serve as a potential therapeutic approach for diseases such as cystic fibrosis and asthma. In the context of this study, the authors are looking for a compound to use in in-vitro studies.

Using data from PubChem Bioassay AID 623877, we apply statistical and visualization techniques to identify hit compounds similar to what the authors originally found.

## Data Source
- **National Center for Biotechnology Information (2025).**  
  - **PubChem Bioassay Record for AID 623877**  
  - Source: Johns Hopkins Ion Channel Center  
  - Retrieved: March 4, 2025  
  - [PubChem Bioassay Link](https://pubchem.ncbi.nlm.nih.gov/bioassay/623877)

## Assay for Compound Screening
Each compound was evaluated using **YFP fluorescence ratios**, which were normalized against negative controls. Compounds were classified as **active potentiators** of TMEM16A if their activity score was below **three standard deviations** from the mean B-score of all screened compounds.

## Methods & Analysis Pipeline
1. **Data Preprocessing**
   - Imported PubChem data
   - Removed NA values.
   - Assigned numerical values to active and inactive compounds.
   - Removed columns and rows with no values to streamline analysis.

2. **Hit Identification**
   - Used a strict statistical threshold to define active hits.

3. **Statistical & Graphical Analysis**
   - **Scatter plots**: Showed activity scores of all compounds.
   - **Violin plots**: Displayed distribution of activity scores.
   - **ROC curve analysis**: Assessed classification performance.

4. **Top Hit Compounds**
   - Identified **82 hit compounds** with significant activity.
   - Top 10 hits were ranked based on activity score.
  
## Results
Identified 82 active compounds, with the top 10 ranked by activity score. The results align with the original study’s findings, supporting the validity of our analysis.

## Lesons Learned
- How to analyze high-throughput screening data.
- What the data analysis workflow looks like.
- How to implement statistical analysis to ensure the correct identification of hits.
- How to confirm normalization was done correctly to a data set.

## How to Run This Analysis
This project is implemented in Python using Google Colab.

### **Requirements**
- Python libraries: `pandas`, `numpy`, `matplotlib`, `seaborn`, `scipy`
- Download the dataset or load it directly from PubChem.

### **Instructions**
1. Clone this repository and load in google colab.
2. Install raw data file from the pubchem link listed earlier and upload it to the google colab document.

### **Future Directions**
Further investigation should focus on dose-response curves for the top 10 compounds to confirm potency and efficacy.
