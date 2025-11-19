# Natural Language Processing with Disaster Tweets

## Setup Instructions

### Python Version Requirement

**Important**: TensorFlow does not currently support Python 3.13. Please use Python 3.11 or 3.12 for this project.

### Virtual Environment Setup

1. Create a virtual environment:
   ```bash
   python3.11 -m venv venv
   # or
   python3.12 -m venv venv
   ```

2. Activate the virtual environment:
   ```bash
   source venv/bin/activate  # On macOS/Linux
   # or
   venv\Scripts\activate  # On Windows
   ```

3. Install required packages:
   ```bash
   pip install --upgrade pip
   pip install -r requirements.txt
   ```

### Alternative: Using PyTorch

If you prefer to use PyTorch instead of TensorFlow, you can modify the code to use PyTorch. PyTorch supports Python 3.13.

To install PyTorch:
```bash
pip install torch torchvision torchaudio
```

### Project Structure

```
Deep_Learning_W4/
├── data/
│   ├── train.csv
│   ├── test.csv
│   └── sample_submission.csv
├── notebook/
│   └── project.ipynb
├── venv/
├── requirements.txt
└── README.md
```

### Running the Notebook

1. Activate the virtual environment
2. Start Jupyter Notebook:
   ```bash
   jupyter notebook
   ```
3. Open `notebook/project.ipynb`

### Notes

- If you're using Python 3.13, TensorFlow installation will fail. Consider using Python 3.11 or 3.12, or switch to PyTorch.
- Make sure to download NLTK data on first run:
  ```python
  import nltk
  nltk.download('punkt')
  nltk.download('stopwords')
  ```

