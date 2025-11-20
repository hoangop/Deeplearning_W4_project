# Natural Language Processing with Disaster Tweets

## Project Overview
This project is a solution for the Kaggle competition "Natural Language Processing with Disaster Tweets". The goal is to build a machine learning model that predicts which Tweets are about real disasters and which one’s aren’t.

**Kaggle Score**: 0.79773 (Rank ~402)

## Model Architecture
- **Type**: Bidirectional LSTM (Bi-LSTM)
- **Embedding**: Keras Embedding Layer (100 dimensions)
- **Structure**:
  - Embedding Layer
  - Bidirectional LSTM (64 units)
  - Global Max Pooling 1D
  - Dense Layer (64 units, ReLU, L2 Regularization)
  - Dropout (0.5)
  - Output Layer (Sigmoid)

## Setup Instructions

### Python Version Requirement
**Important**: TensorFlow does not currently support Python 3.13. Please use Python 3.11 or 3.12 for this project.

### Installation

1. Clone the repository:
   ```bash
   git clone https://github.com/hoangop/Deeplearning_W4_project.git
   cd Deeplearning_W4_project
   ```

2. Create and activate a virtual environment (Python 3.11 recommended):
   ```bash
   python3.11 -m venv venv
   source venv/bin/activate  # macOS/Linux
   # venv\Scripts\activate  # Windows
   ```

3. Install dependencies:
   ```bash
   pip install --upgrade pip
   pip install -r requirements.txt
   ```

### Running the Project

1. Start Jupyter Notebook:
   ```bash
   jupyter notebook
   ```
2. Open `notebook/project.ipynb` and run all cells.

### NLTK Data
The first time you run the code, you might need to download NLTK data:
```python
import nltk
nltk.download('punkt')
nltk.download('punkt_tab')
nltk.download('stopwords')
```

## Project Structure
```
Deep_Learning_W4/
├── data/                  # Data files (not included in repo, download from Kaggle)
│   ├── train.csv
│   ├── test.csv
│   └── sample_submission.csv
├── notebook/
│   └── project.ipynb      # Main analysis and modeling notebook
├── requirements.txt       # Python dependencies
└── README.md              # Project documentation
```

## Results
The final optimized model achieved an F1-score of ~0.87 on the local validation set and ~0.80 on the Kaggle public leaderboard. The key to success was balancing model complexity with regularization (Dropout + L2) to prevent overfitting on the small dataset.
