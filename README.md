# iTBG-Net: Enhancing Short-Term Renewable Energy Forecasting with Incremental Deep Learning

**One-click reproducibility: Clone, update paths, and run the notebook on Kaggle or Google Colab.**

## Overview
This repository implements an incremental deep learning framework for short-term renewable energy forecasting. The project was originally developed as a Kaggle Jupyter Notebook using **Python 3.10.12**. It leverages online incremental learning techniques along with a hybrid deep learning architecture that combines TCN, GRU, and LSTM layers. Additionally, several models including CNN, non-incremental LSTM, and xLSTM are implemented.

## Dataset

Download the dataset from the CSV file in the **"Dataset Folder"** or access it directly on Kaggle:  
[Integrated Energy Management and Forecasting Dataset](https://www.kaggle.com/datasets/aftabhussaincui/integrated-energy-management-and-forecasting)


> **Important:**  
> After downloading the dataset from the provided Google link, update the dataset path in the code.  
> For example, change the following line in the first proposed model:
> ```python
> data = pd.read_csv('/kaggle/input/integrated-energy-management-and-forecasting/Integrated Energy Management and Forecasting Dataset.csv')
> ```
>** Replace it with your local dataset path.**

## How to Reproduce
1. **Download the Dataset:**  
   Download the dataset from the Google link provided in the project documentation.

2. **Download the Jupyter Notebook:**  
   Download the Python Jupyter Notebook from this repository.

3. **Upload to Kaggle or Google Colab:**  
   Upload the notebook to Kaggle or Google Colab. Both platforms provide GPU support, which is especially beneficial for models such as xLSTM.

4. **Update Dataset Paths:**  
   - **First Proposed Model:**  
     Locate the dataset loading code in the notebook and update the path:
     ```python
     data = pd.read_csv('/kaggle/input/integrated-energy-management-and-forecasting/Integrated Energy Management and Forecasting Dataset.csv')
     ```
     Change it to point to your dataset location.
   - **Other Models:**  
     Similarly, update the dataset path in the code cells for the CNN model, non-incremental LSTM, and xLSTM models.

5. **Run the Notebook:**  
   Hit the run button to execute the code cells and reproduce the results.

## Methodology
- **Incremental Updates & Data Streaming:**  
  The dataset is partitioned into small streams to simulate online incremental learning. The model is retrained over **26 incremental updates**, with **100 epochs per update**.
  
- **Replay Buffer:**  
  A replay buffer mechanism is used to mix past data with new incoming data, ensuring continuous learning from both historical and current information.

- **Hybrid Model Architecture:**  
  The main model combines Temporal Convolutional Networks (TCN) with Bidirectional GRU and LSTM layers to capture both short-term and long-term temporal dependencies.

- **Global Epoch Tracking:**  
  Global epochs are tracked to compare performance with traditional batch-based learning models that train over an identical number of epochs.

## Comparison Mode
A comparison modeling section is included (details to be updated) to show performance differences between the incremental learning approach and conventional batch-based models, including CNN, LSTM (non-incremental), and xLSTM.

## Publication
**Title:** *iTBG-Net: Enhancing Short-Term Renewable Energy Forecasting with Incremental Deep Learning*

## Repository
The complete source code and project configuration are available on GitHub:  
[GitHub Repo](https://github.com/Aftab-Hussain302/iTGB-Net-online-learning.git)

## License
This work is licensed under the [MIT License](LICENSE).

## Acknowledgments
Thank you for exploring the iTBG-Net project. Contributions and feedback are highly appreciated!
