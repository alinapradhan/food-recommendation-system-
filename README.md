
# Food Recommendation System

A content-based recommendation system that suggests food recipes based on ingredient similarity using **TF-IDF vectorization** and **cosine similarity**.  
Built with Python and Jupyter Notebook.

---

## Overview

This project analyzes food or recipe data and recommends similar dishes based on text similarity between ingredient lists or descriptions.  
It leverages **NLP** techniques from scikit-learn to convert recipe ingredients into feature vectors and compute similarity scores.

The system can:
- Recommend similar recipes based on an input dish.
- Load and clean raw food datasets.
- Build or load pre-trained TF-IDF models.
- Provide quick search functionality for food names.

---

## Core Features

- **Text Preprocessing:** Cleaning and tokenizing food descriptions.
- **TF-IDF Vectorization:** Transforming text into numerical feature vectors.
- **Cosine Similarity:** Measuring similarity between recipes.
- **Persistent Model Loading:** Save and reload trained models for faster inference.
- **Custom Recommendation Function:** Retrieve top-N most similar foods.

---

##  Project Structure

```

├── foodipynb.ipynb         # Main notebook containing code and analysis
├── data/                   # (Optional) Folder for input CSV data
├── models/                 # Saved TF-IDF and similarity model files
├── README.md               # Project documentation
└── requirements.txt        # Python dependencies

````

---

##  Requirements

Install the required dependencies:

```bash
pip install -r requirements.txt
````

Key libraries used:

* `pandas`
* `numpy`
* `scikit-learn`
* `re`
* `pickle`
* `typing`

---

##  How It Works

1. **Data Loading**

   ```python
   df = load_data_from_csv("recipes.csv")
   ```
2. **Text Cleaning**

   ```python
   df['cleaned'] = df['ingredients'].apply(clean_text)
   ```
3. **Model Building or Loading**

   ```python
   tfidf_matrix, tfidf = build_or_load_model(df)
   ```
4. **Generate Recommendations**

   ```python
   get_recommendations("chicken curry", tfidf_matrix, df)
   ```

---

## Example Output

**Input:** `chicken biryani`
**Top 3 Recommendations:**

1. Chicken fried rice
2. Mutton biryani
3. Vegetable pulao

*(Results vary depending on dataset)*

---

##  Results and Visualization

The notebook includes sections for:

* Data exploration and cleaning
* Model performance inspection
* Visualizing similarity relationships between foods

---

## Future Improvements

* Add user-based collaborative filtering
* Deploy via Streamlit web app
* Integrate with an external recipe API (e.g., Spoonacular)
* Support multilingual recipe names

---

##  How to Run

1. Clone this repository:

   ```bash
   git clone https://github.com/alinapradhan/food-recommendation-system.git
   cd food-recommendation-system
   ```

2. Install dependencies:

   ```bash
   pip install -r requirements.txt
   ```

3. Launch Jupyter Notebook:

   ```bash
   jupyter notebook foodipynb.ipynb
   ```

4. Run all cells to reproduce the results.

---

##  License

This project is licensed under the [MIT License](LICENSE).

---


