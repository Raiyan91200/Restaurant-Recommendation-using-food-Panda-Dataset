# Restaurant Recommendation System using Food Panda Dataset

A machine learning-based restaurant recommendation system that analyzes customer reviews and ratings from Bangladesh's food delivery data to provide personalized restaurant suggestions.

## 🎯 Project Overview

This project implements a content-based recommendation system that suggests restaurants based on:
- Customer review text similarity (using TF-IDF and cosine similarity)
- Restaurant ratings and sentiment analysis
- Location-based filtering
- Mean rating calculations

## 🚀 Features

- **Content-Based Filtering**: Recommends restaurants based on review text similarity
- **Sentiment Analysis**: Analyzes customer review sentiments using pre-trained transformers
- **Location-Based Recommendations**: Suggests restaurants within the same city
- **Rating Analysis**: Calculates and visualizes mean ratings for restaurants
- **Data Visualization**: Comprehensive charts showing rating distributions, top restaurants, and sentiment analysis

## 📊 Dataset

The project uses the "Food Review Dataset of Bangladesh" which contains:
- Restaurant names and locations
- Customer reviews and ratings
- Preprocessed text data
- Reviewer information
- Timestamps

**Dataset file**: `Dataset.zip` (6.2MB)

## 🛠️ Technologies Used

- **Python**: Core programming language
- **Pandas & NumPy**: Data manipulation and analysis
- **Scikit-learn**: Machine learning algorithms and metrics
- **TensorFlow/Keras**: Deep learning framework
- **Transformers**: Pre-trained sentiment analysis models
- **NLTK**: Natural language processing
- **Matplotlib & Seaborn**: Data visualization
- **TF-IDF Vectorization**: Text feature extraction
- **Cosine Similarity**: Content-based filtering

## 📋 Requirements

```
numpy
pandas
matplotlib
seaborn
scikit-learn
tensorflow
transformers
nltk
tqdm
scipy
```

## 🔧 Installation

1. Clone or download this repository
2. Install required packages:
   ```bash
   pip install numpy pandas matplotlib seaborn scikit-learn tensorflow transformers nltk tqdm scipy
   ```
3. Extract the dataset from `Dataset.zip`
4. Run the Jupyter notebook `Resturent_Recomendation_FoodpandaDataset.ipynb`

## 📈 How It Works

### 1. Data Preprocessing
- Loads restaurant review data from Excel file
- Removes unwanted columns (reviewer_name, scraper, etc.)
- Samples 8,300 records for processing
- Removes null values and duplicates

### 2. Sentiment Analysis
- Uses pre-trained transformer models to analyze review sentiments
- Categorizes reviews as Positive/Negative
- Adds sentiment scores to the dataset

### 3. Rating Calculation
- Calculates mean ratings for each restaurant
- Scales ratings to 1-5 range using MinMaxScaler
- Provides normalized rating comparison

### 4. Recommendation Engine
- **TF-IDF Vectorization**: Converts review text to numerical features
- **Cosine Similarity**: Measures similarity between restaurants
- **Content-Based Filtering**: Recommends similar restaurants based on review content

### 5. Recommendation Functions

#### `recommend(restaurant_name)`
Returns top 5 restaurants with similar reviews regardless of location.

#### `recommend_by_location(restaurant_name)`
Returns top 5 restaurants with similar reviews within the same city.

## 📊 Visualizations

The project includes several data visualizations:
- **Rating Distribution**: Histogram showing restaurant rating spread
- **Top 10 Restaurants**: Bar chart of highest-rated establishments
- **Sentiment Distribution**: Pie chart of review sentiments
- **Popular Restaurant Chains**: Bar chart showing most reviewed restaurants
- **Word Frequency Analysis**: Common word pairs in reviews

## 🎯 Usage Example

```python
# Get general recommendations
recommend('Kacchi Bhai - Dhanmondi')

# Get location-specific recommendations
recommend_by_location('Barcode Cafe_Chittagong')
```

## 📁 Project Structure

```
Restaurant-Recommendation-using-food-Panda-Dataset/
├── Dataset.zip                                    # Raw dataset
├── Resturent_Recomendation_FoodpandaDataset.ipynb # Main notebook
└── README.md                                      # Project documentation
```

## 🔍 Key Insights

- Analyzes restaurant performance across different cities in Bangladesh
- Identifies trending restaurants and customer preferences
- Provides data-driven restaurant recommendations
- Helps users discover new restaurants with similar characteristics to their preferences

## 🚀 Future Enhancements

- **Collaborative Filtering**: Add user-based recommendations
- **Deep Learning**: Implement neural networks for better text understanding
- **Real-time Data**: Integrate with live food delivery APIs
- **Geographic Filtering**: Add distance-based recommendations
- **Multi-language Support**: Support for Bengali and other local languages
- **Cuisine-based Filtering**: Recommendations based on food categories

## 📝 Notes

- The dataset is specifically focused on Bangladesh restaurants
- Sentiment analysis uses English language models
- Recommendations are based on text similarity and may require fine-tuning for better accuracy
- The project was originally designed to run on Google Colab

## 🤝 Contributing

Feel free to fork this project and submit pull requests for improvements. Areas for contribution:
- Model performance optimization
- Additional recommendation algorithms
- Better data visualization
- Enhanced preprocessing techniques

## 📄 License

This project is for educational and research purposes. Please respect the original dataset licensing terms.

---

*This recommendation system helps food enthusiasts discover new restaurants based on similar customer experiences and preferences.*
