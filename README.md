# Restaurant Recommendation System using Food Panda Dataset

A machine learning-based restaurant recommendation system that analyzes customer reviews from Bangladesh's online food delivery platforms to provide personalized restaurant suggestions.

## 📋 Overview

This project implements a content-based filtering recommendation system that leverages customer reviews and ratings to suggest similar restaurants. The system uses Natural Language Processing (NLP) for sentiment analysis and machine learning techniques to calculate restaurant similarities based on review content.

## ✨ Key Features

- **Sentiment Analysis**: Automatic classification of customer reviews as positive or negative using transformer models
- **Content-Based Recommendations**: Restaurant suggestions based on review text similarity using TF-IDF and cosine similarity
- **Location-Based Filtering**: Get restaurant recommendations within the same city
- **Rating Analysis**: Mean rating calculations and distribution analysis
- **Data Visualization**: Interactive charts showing sentiment distribution, rating patterns, and popular restaurants

## 🗂️ Dataset

The project uses two primary datasets from Bangladesh's online food delivery platforms:
- `Bangladesh Online Food Portals Customer Reviews Dataset.xlsx`
- `Food Review Dataset of Bangladesh.xlsx`

**Dataset Features:**
- Restaurant names and locations
- Customer reviews and ratings
- City information
- Review text for sentiment analysis

## 🛠️ Technologies Used

- **Python**: Core programming language
- **Data Processing**: pandas, numpy
- **Machine Learning**: scikit-learn
- **Natural Language Processing**: 
  - NLTK for text preprocessing
  - Transformers (Hugging Face) for sentiment analysis
- **Visualization**: matplotlib, seaborn
- **Text Analysis**: TF-IDF vectorization, cosine similarity
- **Development Environment**: Jupyter Notebook, Google Colab

## 📦 Installation

### Prerequisites
- Python 3.7 or higher
- Google Colab (recommended) or Jupyter Notebook

### Required Libraries
```bash
pip install numpy pandas matplotlib seaborn nltk scikit-learn transformers tensorflow tqdm scipy
```

### Setup Instructions
1. Clone the repository:
```bash
git clone https://github.com/Raiyan91200/Restaurant-Recommendation-using-food-Panda-Dataset.git
cd Restaurant-Recommendation-using-food-Panda-Dataset
```

2. Extract the dataset:
```bash
unzip Dataset.zip
```

3. Open the Jupyter notebook:
```bash
jupyter notebook Resturent_Recomendation_FoodpandaDataset.ipynb
```

## 🚀 Usage

### Basic Restaurant Recommendation
```python
# Get general recommendations for a restaurant
recommend('Restaurant_Name')
```

### Location-Based Recommendations
```python
# Get recommendations within the same city
recommend_by_location('Restaurant_Name')
```

### Example Usage
```python
# Example 1: General recommendations
result = recommend('Barcode Cafe_Chittagong')
print(result)

# Example 2: Location-specific recommendations
result = recommend_by_location('Kacchi Bhai - Dhanmondi')
print(result)
```

## 📊 Project Workflow

1. **Data Loading & Preprocessing**
   - Load Excel datasets
   - Clean and preprocess text data
   - Remove unwanted columns

2. **Sentiment Analysis**
   - Apply transformer-based sentiment analysis
   - Classify reviews as positive or negative
   - Add sentiment labels to dataset

3. **Feature Engineering**
   - Calculate mean ratings per restaurant
   - Create TF-IDF matrix from preprocessed reviews
   - Generate cosine similarity matrix

4. **Recommendation System**
   - Implement content-based filtering
   - Find similar restaurants using cosine similarity
   - Filter results by location when needed

5. **Visualization & Analysis**
   - Plot rating distributions
   - Show sentiment analysis results
   - Display top restaurants and recommendations

## 📈 Results

The system provides:
- **Top 5-10 similar restaurants** based on review content
- **Sentiment analysis** with percentage distribution
- **Mean ratings** for quality assessment
- **Location-specific filtering** for practical recommendations
- **Visual insights** through charts and graphs

## 🏗️ Project Structure

```
Restaurant-Recommendation-using-food-Panda-Dataset/
├── Resturent_Recomendation_FoodpandaDataset.ipynb  # Main notebook
├── Dataset.zip                                      # Compressed datasets
├── README.md                                        # Project documentation
└── .git/                                           # Git repository files
```

## 🔧 Key Functions

### `recommend(restaurant_name)`
Returns top restaurants similar to the input restaurant based on review content similarity.

**Parameters:**
- `restaurant_name`: Name of the restaurant to find recommendations for

**Returns:**
- DataFrame with columns: city, mean_rating, sentiment

### `recommend_by_location(restaurant_name)`
Returns restaurants similar to the input restaurant within the same city.

**Parameters:**
- `restaurant_name`: Name of the restaurant to find recommendations for

**Returns:**
- DataFrame with similar restaurants in the same city

## 📊 Sample Output

```
TOP 5 RESTAURANTS SIMILAR TO 'Barcode Cafe_Chittagong':
                    city  mean_rating sentiment
Restaurant_A      Dhaka         3.62  Positive
Restaurant_B   Rajshahi         3.61   Negative
Restaurant_C     Sylhet         3.55  Positive
```

## 🤝 Contributing

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

## 📝 License

This project is available for educational and research purposes. Please check the dataset sources for specific licensing information.

## 👥 Authors

- **Syed Raiyan Nasim** - Initial work and development

## 🙏 Acknowledgments

- Food delivery platforms in Bangladesh for providing the dataset
- Hugging Face for transformer models
- The open-source community for the wonderful libraries used in this project

## 📞 Contact

For questions or suggestions, please feel free to reach out or create an issue in the repository.

---

**Note**: This project was developed for educational purposes to demonstrate machine learning applications in recommendation systems and natural language processing.