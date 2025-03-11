# A Novel Method to Determine Total Oxidant Concentration Produced by Non-Thermal Plasma: Image Processing-Based Machine Learning
This repository contains the code and data for machine learning-assisted total oxidant concentration estimation using image processing.

## Project Description
This study presents an innovative approach for determining total oxidant concentration ([Ox]ₜₒₜ) in water samples by integrating advanced image processing and machine learning (ML). A non-thermal plasma (NTP) system was used to generate reactive oxidizing species, inducing observable color changes in a potassium iodide (KI) solution. These changes were captured using a Raspberry Pi-based camera system within a custom-designed sampling chamber.

A comprehensive image processing pipeline incorporating YOLOv8 segmentation, HSV thresholding, inpainting, CLAHE enhancement, and adaptive thresholding was applied to extract colorimetric features across RGB, HSV, and LAB color spaces. These features were correlated with [Ox]ₜₒₜ values obtained via the standard KI method, revealing strong predictive relationships, particularly in the G (RGB), S (HSV), and L and A (LAB) channels.

Multiple ML models (Linear Regression, Ridge Regression, Lasso Regression, Random Forest Regression, and Neural Networks) were evaluated using R², MSE, and MAE metrics. Lasso Regression (LaR) achieved the highest performance (R² = 0.9966, MSE = 0.0946, MAE = 0.3038), highlighting the effectiveness of L1 regularization. This methodology offers a cost-effective, scalable alternative to traditional spectrophotometric techniques, enhancing precision, reproducibility, and accessibility for applications in environmental monitoring, diagnostics, and industrial analysis.

## Repository Structure
notebook/ - Full code implementation.
data/ - Contains Excel files and image data.

## Installation Instructions
Clone this repository:
git clone https://github.com/yourusername/repository-name.git
cd repository-name

Install the required dependencies:
pip install -r requirements.txt

## Follow the steps in the Jupyter Notebook to reproduce the results.

## Usage Instructions
- Run the provided Jupyter Notebook to process images and extract colorimetric features.
- Train ML models using the extracted features.
- Evaluate model performance using R², MSE, and MAE metrics.
- Compare results with standard KI method data.

## Dataset Information
Users can either utilize the dataset included in the repository or create their own using the same methodology.

## Results & Performance
- YOLOv8 segmentation demonstrated high accuracy (confidence scores: 0.9648 to 0.9938).
- LaR exhibited the best performance with R² = 0.9966, MSE = 0.0946, and MAE = 0.3038.
- Correlation analysis identified G (RGB), S (HSV), and L and A (LAB) channels as the most predictive features.
- Feature selection improved ML model accuracy, with Lasso Regression performing the best.

## License
This repository is licensed under the MIT License.

## Contributors

- Mirkan Emir Sancak (Department of Environmental Engineering, Gebze Technical University) - (mailto:mrkn.sancak@gmail.com)
- Unal Sen (Department of Environmental Engineering, Gebze Technical University)
- Ulker Diler Keris-Sen (Institute of Earth and Marine Sciences, Gebze Technical University)

## Future Work & Contributions
This study demonstrates the potential of ML-assisted image processing for colorimetric analysis. Future research will focus on:
- Reducing computational costs for real-time applications.
- Expanding the methodology to analyze other chemical parameters (e.g., pH, H₂O₂, total hardness).
- Optimizing ML models for improved generalization.
