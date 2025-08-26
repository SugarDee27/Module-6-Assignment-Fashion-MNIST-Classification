
# Module 6 Assignment: Fashion MNIST Classification

This package includes **Python (Keras/TensorFlow)** and **R (keras)** implementations of a **6-layer CNN** for Fashion MNIST, plus prediction on at least two images.

## Files
- `fashion_cnn.py` — Python script to train and predict
- `Fashion_MNIST_CNN.ipynb` — Python notebook (run cell-by-cell)
- `fashion_cnn.R` — R keras script
- `outputs/` — models and images saved here at runtime
- `requirements.txt` — Python deps

## Python (quick start)
```bash
python -m venv .venv
# Windows: .venv\Scripts\activate
# macOS/Linux: source .venv/bin/activate
pip install -r requirements.txt
python fashion_cnn.py
```

## R (quick start)
```r
install.packages("keras")
library(keras)
install_keras()  # one-time setup
source("fashion_cnn.R")
```

## Architecture (6 layers)
1) Conv2D(32, 3x3, relu, same)  
2) Conv2D(64, 3x3, relu, same)  
3) MaxPooling2D(2x2)  
4) Flatten  
5) Dense(128, relu)  
6) Dense(10, softmax)

The implicit Input layer is not counted toward the six.

## Notes
- Default training is 5 epochs for speed. Increase for better accuracy.
- Script saves: `outputs/fashion_cnn.h5`, `outputs/training_history.png`, `outputs/sample_predictions.png`.
