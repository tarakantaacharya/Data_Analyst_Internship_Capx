# Reddit Stock Prediction Scraper and Model

This project involves scraping data from Reddit related to stock discussions, performing data preprocessing, and building a machine learning model to predict stock price movements based on Reddit sentiment analysis.

## **Table of Contents**
- [Overview](#overview)
- [Installation](#installation)
- [Usage](#usage)
- [Demonstration](#demonstration)
- [Model Evaluation](#model-evaluation)
- [License](#license)

## **Overview**
The project uses the **PRAW** library to scrape Reddit data, particularly related to stock discussions. The scraped data is then preprocessed to extract meaningful features and used to train a machine learning model for predicting stock price movements based on sentiment analysis of Reddit posts.

### **Key Components:**
1. **Data Scraping**: Scrapes Reddit posts from specific subreddits related to stock discussions.
2. **Data Preprocessing**: Cleans the text data, performs sentiment analysis, and generates numerical features for model training.
3. **Model Training**: Uses features from the text data and stock data to train a machine learning model (Logistic Regression) to predict stock price changes.
4. **Model Evaluation**: Evaluates the model's performance using metrics like accuracy, precision, recall, and F1 score.

## **Installation**

### **Clone the repository:**

To get started, first clone the repository to your local machine:

```bash
git clone https://github.com/yourusername/reddit_scraper_project.git
cd reddit_scraper_project
```

### **Install dependencies:**

Ensure you have Python 3.7+ installed. Then, install the required dependencies using the following command:

```bash
pip install -r requirements.txt
```

### **Set up environment variables:**

Make sure to create a `.env` file with your **Reddit API credentials** (client ID, secret, and user agent). This file is required to interact with Reddit via PRAW.

Example of `.env` file:

```plaintext
REDDIT_CLIENT_ID=your_client_id
REDDIT_SECRET=your_secret
REDDIT_USER_AGENT=your_user_agent
```

## **Usage**

### **Step 1: Data Scraping**

Run the **data_scraping_py.ipynb** script to scrape data from Reddit. This script fetches posts from specific stock-related subreddits and saves the data to a CSV file.

```bash
python data_scraping_py.ipynb
```

### **Step 2: Data Preprocessing**

After scraping the data, use the **data_preprocessing_py.ipynb** script to preprocess and clean the text data. The script performs tasks such as tokenization, stopword removal, and sentiment analysis.

```bash
python data_preprocessing_py.ipynb
```

This will save the cleaned and preprocessed data to a file named `reddit_stock_data_posts_cleaned.csv`.

### **Step 3: Model Training**

To train the machine learning model, run the **model_training_py.ipynb** script. This script will split the preprocessed data into training and testing sets, train a **Logistic Regression** model, and evaluate its performance.

```bash
python model_training_py.ipynb
```

### **Step 4: Model Evaluation**

After training the model, the script will output the performance metrics, including accuracy, precision, recall, and F1 score.

```bash
python model_training.py
```

## **Demonstration**

To run the demonstration steps, follow these instructions:

1. **Clone the Repository**: First, clone the repository and navigate to the project directory.
2. **Install Dependencies**: Install the required libraries using the `pip install -r requirements.txt` command.
3. **Run Data Scraping**: Use `python scraper.py` to scrape Reddit data.
4. **Preprocess the Data**: After scraping, run `python data_preprocessing.py` to clean and preprocess the data.
5. **Train the Model**: Run `python model_training.py` to train the machine learning model.
6. **Evaluate the Model**: The evaluation metrics will be printed to the console.

For example:
```bash
Accuracy: 0.85
Precision: 0.84
Recall: 0.82
F1-score: 0.83
```

## **Model Evaluation**

The model's performance is evaluated using several metrics:

- **Accuracy**: Measures how many predictions are correct.
- **Precision**: The proportion of true positives among all positive predictions.
- **Recall**: The proportion of true positives among all actual positives.
- **F1-score**: A balanced metric that combines precision and recall.

These metrics help assess how well the model can predict stock price movements based on Reddit discussions.

---

### **Final Steps**

1. **Run the code** as outlined in the instructions to scrape data, preprocess it, and train the model.
2. **Evaluate** the model’s performance and see the results in the terminal.
3. **Future Enhancements**: You can enhance the model by incorporating more complex algorithms or using a larger dataset.


