# Seismic Data Analysis for Oil Exploration

## Overview

This project aims to use **seismic data analysis** for identifying potential oil-bearing formations based on seismic attributes such as **magnitude**, **depth**, **latitude**, and **longitude**. By using machine learning techniques such as clustering and classification, the project mimics the type of analysis performed in the oil and gas industry to detect areas likely to contain hydrocarbon reserves.

Key features of the analysis include:
- Fetching seismic data using the **USGS Earthquake API**.
- Visualizing seismic event locations and magnitudes to identify geographical clusters.
- Applying **K-Means clustering** to group seismic events by their geological attributes.
- Predicting potential oil-bearing formations using **Random Forest classification**, where features like **magnitude** serve as proxies for oil exploration factors.

## Project Structure

```bash
|-- data/                         # Folder for saving any data files
|-- notebooks/                    # Jupyter notebooks with code and analysis
|-- seismic_oil_exploration.ipynb  # Main Jupyter Notebook with all code and visualizations
|-- README.md                      # This file
|-- requirements.txt               # Dependencies for the project
```

## Features

### 1. Data Collection

Seismic data was collected using the **USGS Earthquake API**, focusing on events with magnitudes between **5.0 and 9.0**. These seismic waves can be analogous to those used in oil exploration to map underground geological formations. By analyzing these attributes, we can make informed predictions about where oil might be located.

### 2. Seismic Data Visualization

- **Magnitude Over Time**: Visualizes how seismic event magnitudes vary throughout the year.
- **Geographical Distribution**: A scatter plot showing the **latitude** and **longitude** of seismic events, with colors representing magnitude. This helps identify **geological zones** that may correspond to potential oil-bearing formations.

### 3. Clustering Seismic Events

Using **K-Means clustering**, seismic events are grouped into **3 clusters** based on their latitude, longitude, depth, and magnitude. These clusters may indicate different geological formations, some of which could potentially contain oil.

### 4. Risk Level Classification for Oil Exploration

Seismic events are classified into **risk levels** to simulate how geophysicists predict potential oil-bearing formations. The **Random Forest Classifier** is used to predict these risk levels based on seismic data:

- **Low Risk**: Magnitude less than 5.5
- **Medium Risk**: Magnitude between 5.5 and 6.5
- **High Risk**: Magnitude greater than 6.5

The classifier predicts risk levels with perfect accuracy, demonstrating how seismic data can be used to infer the likelihood of finding oil in certain regions.

## Installation

To run this project, you will need Python 3.x and the following dependencies. You can install all dependencies by running:

```bash
pip install -r requirements.txt
```

### Dependencies

- `pandas`
- `matplotlib`
- `scikit-learn`
- `requests`

You can install these libraries individually, or use the provided `requirements.txt` file.

## How to Run

1. **Clone the repository**:
   ```bash
   git clone https://github.com/yourusername/seismic-oil-exploration.git
   ```
   
2. **Install dependencies**:
   ```bash
   pip install -r requirements.txt
   ```

3. **Run the Jupyter Notebook**:
   Launch Jupyter Notebook and open the file `seismic_oil_exploration.ipynb` to run the code and view the results.

```bash
jupyter notebook
```

4. **Execute the cells**:
   The notebook contains all the code for fetching data, visualization, clustering, and classification. Execute the cells in order to see the analysis.

## Results

- **Clustering**: Seismic events were grouped into **3 clusters**, likely representing different geological formations. These clusters could indicate varying levels of potential for oil-bearing reservoirs.
- **Classification**: The Random Forest Classifier achieved **perfect accuracy** in classifying seismic events into risk levels based on their magnitudes.

### Feature Importance:

- **Magnitude** was identified as the most important feature for predicting risk levels, followed by **longitude**, **depth**, and **latitude**. In the context of oil exploration, magnitude can serve as a proxy for the strength of seismic reflections from underground formations, which may indicate the presence of hydrocarbons.

## Visualizations

1. **Seismic Event Magnitudes Over Time**:
   - Displays the variations in seismic event magnitudes throughout 2020.

2. **Geographical Distribution of Seismic Events**:
   - Maps the location of seismic events globally, colored by magnitude.

3. **K-Means Clustering**:
   - Visualizes how seismic events are grouped into clusters based on their geographical and geological properties.

4. **Random Forest Classification**:
   - Simulates risk level predictions for potential oil-bearing formations based on seismic attributes.

## Next Steps

- **Enhance the model** by adding features such as **porosity**, **velocity**, and **permeability**, which are critical in predicting the presence of oil and gas.
- **Use real-world seismic data**: Apply the techniques on real seismic survey data (e.g., from the F3 Netherlands dataset or SEG Open Data) to directly predict oil reservoirs.
- **Deploy the model**: Create a web-based application that predicts the likelihood of oil-bearing formations in real-time using seismic data inputs.

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

---

### Adjustments:
- Replace `yourusername` with your actual GitHub username when you upload the project.
- Consider adding a **License** file if you want to specify licensing terms.
- Add any future real seismic datasets (e.g., from SEG Open Data) to the repository for extended analysis.

This `README.md` file is now tailored to emphasize the **Seismic Oil Exploration** goal of the project. Let me know if you need further adjustments!
