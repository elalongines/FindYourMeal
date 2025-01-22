# NoSQL Project: Find Your Meal

"Find Your Meal" is a NoSQL-based project designed to simplify meal planning for individuals following keto or vegan diets. Meal planning can be a complex task, especially with diverse dietary needs, and this project aims to make the process faster, easier, and more enjoyable.

## Features and Highlights

1. **Efficient Meal Search**: 
   - Powered by MongoDB's aggregation pipelines for lightning-fast, customizable meal searches.
   - Supports detailed filtering options to help users find meals tailored to their preferences.

2. **Comprehensive Recipe Database**: 
   - Data sourced from the "low-carb-recipes" API via RapidAPI, featuring a wide variety of keto recipes with detailed nutritional information.
   - Recipes are enriched with metadata, including tags, preparation steps, ingredient details, and nutritional profiles.

3. **Seamless System Architecture**:
   - Backend built with Python for data processing and integration.
   - MongoDB Atlas for cloud-based database storage and management.
   - Jupyter Notebooks for data analysis and transformation workflows.

4. **User-Centric Approach**:
   - Designed with multiple personas in mind to meet varying user needs, ensuring accessibility and relevance for different dietary lifestyles.

## Data Model Overview

The data model is structured to maximize flexibility, scalability, and ease of use, featuring the following core collections:

### **Recipe Collection**:
- Houses primary recipe data, including:
  - **Name**: Recipe title (e.g., "Keto Corn Dog Bites").
  - **Tags**: Array of dietary or descriptive labels.
  - **Ingredients**: Array of objects with name and serving size details.
  - **Steps**: Array of ordered instructions for preparation.
  - **Nutrients**: Reference to a detailed nutritional profile object.
  - **Images**: URL or reference to the images collection.
  - **PrepareTime** and **CookTime**: Integers representing time in minutes.

### **Tags, Ingredients, and Steps Collections**:
- Each collection isolates recipe attributes for efficient querying and reusability:
  - **Tags**: Unique labels for filtering recipes.
  - **Ingredients**: Detailed entries with names and serving size information.
  - **Steps**: Sequential instructions with descriptions.

### **Nutrients Collection**:
- Captures a recipe's complete nutritional profile, including:
  - Carbohydrates, proteins, fats, vitamins, and minerals.

### **Images Collection**:
- Stores image metadata, such as:
  - URLs, dimensions, photographer credit, and annotations.

## Data Integration and Transformation
- Data was standardized, cleansed, and transformed to enhance usability:
  - Arrays retained for multi-valued fields like tags and ingredients.
  - Complex strings parsed into query-friendly formats.
  - Duplicate entries identified and removed to ensure consistency.

## Technical Constraints
- Operating within a free API plan with a limit of 300 requests per month (1 request/second rate limit).

## Future Directions
- Expand to include vegan recipes and other dietary preferences.
- Introduce advanced filtering and personalization features.
- Enhance the UI for an interactive and user-friendly experience.

"Find Your Meal" is an ongoing effort to take the stress out of meal planning while providing a robust and scalable NoSQL solution tailored for diverse dietary needs.
