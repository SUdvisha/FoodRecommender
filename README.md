# FoodRecommender
🧠 Mood-Based Recipe Recommendation System: This project is a Natural Language Processing (NLP)-powered recipe recommendation system that personalizes meal suggestions based on the user's mood or craving. It leverages TextBlob, spaCy, and TF-IDF cosine similarity to analyze user input and match it with recipes from the Food.com Recipes and Reviews dataset.

📊 Dataset Overview: Source: Kaggle - Food.com Recipes and Reviews(https://www.kaggle.com/datasets/irkaal/foodcom-recipes-and-reviews?select=recipes.csv). Records: Over 226,000 recipes

#Key Features:

Name, AuthorId, Description, RecipeInstructions Time metrics: PrepTime, CookTime, TotalTime Nutritional info: Calories, FatContent, ProteinContent, CarbohydrateConten RecipeIngredientParts, AggregatedRating, ReviewCount, RecipeServings
🧪 Features
User Mood Detection:
Identifies user mood from free-text input using TextBlob sentiment polarity and keyword-based rules.
Moods: comfort, energizing, light, indulgent, refreshing, hearty, sweet, detox, neutral.

Recipe Text Processing:
Cleans and parses Description and RecipeIngredientParts.
Lemmatizes and filters non-alphabetic tokens using TextBlob and spaCy.

Feature Engineering:

Computes total cooking time (in minutes) from ISO 8601 durations.
Derives CaloriesPerServing, ProteinToFatRatio, and CarbToFatRatio.
Classifies recipes into Easy, Medium, or Hard complexity levels.
Mood Tagging:
Tags each recipe with a predefined MoodTag based on ingredients and description.

Recommendation Engine:

Filters recipes matching the detected mood.
Vectorizes processed recipe text using TF-IDF.
Computes cosine similarity to user input and returns top-N recipe matches.
Visualization:

Mood tag distribution plot (Seaborn)
Ingredient word cloud (WordCloud)
🛠️ Tech Stack
Programming Language: Python
Libraries/Frameworks:
Pandas
NumPy
Matplotlib
Seaborn
TextBlob
spaCy
scikit-learn
WordCloud
Tools:
Google Colab (for development)
Kaggle (for dataset)
Other:
TF-IDF Vectorization
Cosine Similarity
Sentiment Analysis (TextBlob)
