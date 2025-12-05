# Assignment 6 Part 2 - Writeup

---

## Question 1: Feature Importance

Based on your house price model, rank the four features from most important to least important. Explain how you determined this ranking.

**YOUR ANSWER:**
1. Most Important: Bedrooms
2. Bathrooms
3. Age
4. Least Important: SquareFeet

**Explanation:**

I determined this ranking by looking at the absolute value of each coefficient from the model. The coefficient tells us how much the price changes when that feature goes up by 1. Bedrooms had the highest coefficient at about $6,649, meaning each bedroom adds a lot of value. Bathrooms came second at around $3,859. Age was third with -$950 (negative because older houses lose value). SquareFeet was last at only $121 per square foot, which seems small but makes sense since you're adding many square feet at a time, not just one.

---

## Question 2: Interpreting Coefficients

Choose TWO features from your model and explain what their coefficients mean in plain English. For example: "Each additional bedroom increases the price by $___"

**Feature 1:** Bedrooms

Each additional bedroom increases the house price by about $6,649. So if you compare two identical houses but one has 3 bedrooms and the other has 4, the 4-bedroom house would be predicted to cost around $6,649 more.

**Feature 2:** Age

Each additional year of age decreases the house price by about $950. This makes sense because older houses usually need more repairs and updates. A house that's 10 years old would be predicted to cost about $9,500 less than a brand new house with the same other features.

---

## Question 3: Model Performance

What was your model's R-squared score? What does this tell you about how well your model predicts house prices? Is there room for improvement?

**YOUR ANSWER:**

My model got an R-squared score of 0.9936, which means it explains about 99.36% of the variation in house prices. This is a really strong score. The model is doing an excellent job at predicting prices based on the four features we gave it. The RMSE was around $4,478, so on average predictions are off by less than $5,000, which is pretty good for houses that cost $200,000-$425,000.

---

## Question 4: Adding Features

If you could add TWO more features to improve your house price predictions, what would they be and why?

**Feature 1:** Location/Neighborhood

**Why it would help:** Location is probably the biggest factor in real house prices. A small house in a nice neighborhood can cost way more than a big house in a less desirable area. Adding zip code or neighborhood ratings would definitely help the model make better predictions.

**Feature 2:** Garage Size (number of car spaces)

**Why it would help:** Having a garage, especially a 2 or 3 car garage, adds a lot of value to a home. Many buyers specifically look for homes with garages for storage and to protect their cars. This would give the model more info about the property's features.

---

## Question 5: Model Trust

Would you trust this model to predict the price of a house with 6 bedrooms, 4 bathrooms, 3000 sq ft, and 5 years old? Why or why not? (Hint: Think about the range of your training data)

**YOUR ANSWER:**

I would be cautious about trusting this prediction. Looking at the training data, the maximum values were 5 bedrooms, 3 bathrooms, and 2500 square feet. The house in this question has 6 bedrooms, 4 bathrooms, and 3000 sq ft. All of these are outside the range of data the model was trained on.

When you ask a model to predict for values it's never seen before, that's called extrapolation, and it can be unreliable. The model learned the relationships between features and price based on smaller houses, so it might not accurately capture how those relationships work for much larger homes. The prediction might still be in the right ballpark, but I wouldn't fully trust it without more data on similar high-end houses.
