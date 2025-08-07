# Final-Project - Titanic
## 1. Exploratory Data Analysis (EDA)

The goal of this project is to predict which kinds of people were more likely to survive the Titanic disaster.

In this section, we will explore the dataset with this guiding question in mind, focusing on survival rates by gender, age, class, and other social or economic indicators.

### 1.1 Missing Value Treatment Strategy

- `Cabin`: The cabin code gives us the deck (first letter). We'll extract the deck and fill missing values with the most common one.
- `Age`: We'll fill missing ages with the median age, as it's less sensitive to outliers.
- `Embarked`: Only two missing values, so we'll fill them with the most common port (mode).
