# AI Powered Google-Lens
# Image Similarity Engine (Google Lens Recreation with ResNet)

## Overview
This project is an Image Similarity Search Engine that recreates Google Lens functionalities using a **ResNet model**. It allows users to find similar images based on a query image by performing feature extraction and similarity search.

## Project Structure
```
.
├── Simmilarity_Search_Model.ipynb   # Jupyter Notebook for Image Similarity Search
├── Weights/                         # Pretrained ResNet Weights
├── Saved_Vector_database/           # Precomputed feature vectors for images
│   ├── filenames-caltech101.pickle  # Stores dataset image names
│   └── class_ids-caltech101.pickle  # Stores class names
├── requirements.txt                 # List of dependencies
└── Dataset/                         # Dataset containing image classes
    ├── Class1/
    ├── Class2/
    └── ...
```

## Dataset: Caltech-101
The dataset consists of images of objects belonging to 101 categories, plus a background class. Each image is labeled with a single object. Details:
- **101 object categories** + 1 background clutter class
- **Images per category:** 40 to 800
- **Total images:** ~9,000
- **Image size:** ~200-300 pixels per edge

## Implementation Steps

### 1. Install Dependencies
Ensure you have Python 3.10 installed. Then, install required packages:
```bash
pip install -r requirements.txt
```

### 2. Setting Up the Dataset
- Organize the dataset as mentioned in the structure above.
- If the dataset is not present, it will be downloaded automatically.

### 3. Running the Similarity Search Model
Run the Jupyter Notebook to start the image search engine:
```bash
jupyter notebook Simmilarity_Search_Model.ipynb
```

### 4. How It Works
- **Feature Extraction:** The ResNet model extracts image features.
- **Dimensionality Reduction:** PCA reduces feature dimensions from 2048 to 150.
- **Similarity Search:** KNN finds the most similar images based on extracted features.
- **Query Execution:** A query image is compared against the dataset to retrieve similar images.

## Google Lens Recreation: Key Features
- Accepts an image as input and finds similar images.
- Uses **ResNet** for feature extraction.
- Employs **PCA** to reduce dimensionality for better performance.
- Uses **K-Nearest Neighbors (KNN)** for fast retrieval of nearest neighbors.
- Efficient for large-scale image search applications.

## Future Enhancements
- Optimize search time using **faiss** or **Annoy**.
- Improve accuracy by fine-tuning ResNet.
- Extend the system to work with real-time image uploads.

## Contributing
Contributions are welcome! Feel free to raise issues or submit pull requests.

## License
This project is open-source and available under the MIT License.

