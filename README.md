# PERSONALIZED SEPHORA BEAUTY PRODUCT RECOMMENDER SYSTEM FOR MELANIN-RICH SKIN
![product](https://github.com/user-attachments/assets/a99f82c1-111e-4b1d-a447-518fac92dedd)


# Project Overview
This project addresses a significant gap in the beauty industry: **the lack of tailored product recommendations for people of color**, who often have unique beauty and skincare needs such as hyperpigmentation, dryness, sensitivity, and specific haircare requirements. Current recommendation systems often generalize recommendations, resulting in lower customer satisfaction and less effective beauty routines for individuals with melanin-rich skin tones.
To bridge this gap, we developed an **AI-Powered Cosmetics Recommendation System** that caters to the diverse beauty needs of people of color, offering personalized suggestions across various product categories including skincare, haircare, makeup, fragrances, and supplements. Leveraging a combination of advanced machine learning models, such as content-based filtering (using cosine similarity for ingredient-based matching), collaborative filtering (employing SVD), and sentiment analysis (utilizing an LSTM model and Sentiment Intensity Analyzer), the system provides precise, personalized recommendations.

Key elements include:
- **Sentiment classification** to assess customer reviews, helping refine recommendations based on product feedback.
- **Ingredient similarity analysis** to suggest products with similar compositions, especially beneficial for skincare and haircare products.
- **Hybrid recommendation approach** to integrate user preferences with product characteristics, enhancing the relevance of suggestions.
The model can deliver recommendations based on product similarity, collaborative filtering for user-product interaction, and user-specified needs across a wide range of beauty products. A user-friendly **Streamlit interface** enables users to input a product name or specify preferences to receive tailored product suggestions across different beauty categories.
By addressing the specific beauty needs of people of color, **this project aims to increase accessibility to effective beauty solutions, improve customer satisfaction, and support underrepresented demographics in finding products that best suit their unique requirements**. 
This AI-powered recommendation system extends beyond traditional recommendations by considering a holistic view of beauty needs, making it a comprehensive tool for diverse beauty routines.

---

## Problem Statement
People of color face limited access to beauty products tailored to their unique needs, such as hyperpigmentation, dryness, and sensitivity in skincare, as well as specific haircare and makeup preferences. Current recommendation systems often overlook these factors, offering general suggestions that may not meet the specific needs of those with melanin-rich skin tones.
This project develops an AI-powered recommendation system designed to deliver personalized product suggestions across multiple beauty categories, including skincare, haircare, makeup, and fragrances. Using skin tone classification and advanced AI techniques like content-based filtering, collaborative filtering, and sentiment analysis, the system provides targeted recommendations that cater to diverse beauty routines.
By addressing this gap, **the project aims to improve accessibility and satisfaction, empowering people of color to find products that support their unique beauty goals.**


### Objectives
1. Develop a recommendation system covering multiple beauty product categories, tailored to the unique needs of people of color.
2. Use content-based filtering, collaborative filtering, and sentiment analysis to deliver accurate, personalized recommendations.
3. Deploy the system via a user-friendly Streamlit app for accessible and personalized product discovery.

### Stakeholders
1. *End Users*: Individuals seeking tailored beauty product recommendations across various categories.
2. *Beauty Brands*: Companies aiming to provide curated, inclusive product suggestions.
3. *Retailers*: Platforms looking to enhance the shopping experience with targeted beauty recommendations.

---

## Data Understanding:
The dataset was collected via a Python scraper and contains:
- Product Information: Over 8,000 beauty products from the Sephora online store, including product and brand names, prices, ingredients, ratings, and various features. 
- User Reviews: Approximately 1 million reviews across over 2,000 products in the skincare category. These reviews include user appearances, skin types, and review ratings.

The key features include:
- Product Features: `product_id`, `product_name`, `brand_name`, `ingredients`, `rating`, `price_ksh`, `new`, `out_of_stock`, `highlights`. 
- Review Features: `author_id`, `rating`, `review_text`, `skin_type`, `skin_tone`, and
`helpfulness`.

---

### Exploratory Data Analysis

#### 1. Count of Products by Skin Type
![skintype](https://github.com/user-attachments/assets/af072621-bc6b-48d9-9be2-b5ce11dea9eb)

* The distribution shows that products labeled for combination skin are the most common, followed by those for dry, normal, and then oily skin. 

#### 2. Top 20 Recommended Products
![Top20](https://github.com/user-attachments/assets/e1d047c2-6be9-45f0-90f0-67d51bf3f368)

The visualization displays the top 20 recommended products for melanated skin tone, with the Trinity + Eye and Lip Enhancer Attachment Bundle leading at approximately 200 recommendations. Moisturizing products dominate the top rankings, with The Moisturizing Soft Cream Moisturizer and Rose Quartz Facial Roller in second and third place. Universal facial oils, including Mini Algae + Moringa variants, are prominently featured in the top positions. 
The recommendations show a balanced mix of daily care products like moisturizers and sun protection, alongside treatment products such as serums and concentrates. The recommendation counts gradually decrease from around 200 at the top to about 75 for the lowest-ranked product, the Skin Perfecting 25% AHA + 2% BHA Exfoliant Peel, demonstrating a clear hierarchy in product popularity among users with melanated skin.

#### 3. Out of stock Products and Recommendations based on skin tone
![Out of stock Products and Recommendations based on skin tone](https://github.com/ECCHERUIYOT/AI-Powered-Skincare-Recommendations-For-Melanin-Skin/blob/Echeruiyot/images/image3.png)
* The Recommended pie chart illustrates the percentage of products recommended versus those that are not. A significant portion (85%) of products are not marked as recommended, indicating a possible quality or suitability gap. This could help identify where product performance might fall short or suggest a need for more tailored product options.

* The Products pie chart shows the balance between new and existing products. The larger percentage of existing products (91%) suggests that the platform maintains a consistent range of products, with newer items being introduced selectively. This distribution can provide insights into the inventory management and refresh rates of the catalogue over time.

#### 4. Skin Tone Distribution by Price Tier
![skintone](https://github.com/user-attachments/assets/6e1279f0-3247-479c-adef-3549870ebdab)
* There is a noticeable price difference across skin tones. Products for melanated skin tend to have lower average prices, than non-melanated skin tones, highlighting more affordable options specifically formulated or suited for melanated skin. 

#### 5. Heatmap of Product Count by Skin Tone Category and Skin Type
![Heatmap of Product Count by Skin Tone Category and Skin Type](https://github.com/ECCHERUIYOT/AI-Powered-Skincare-Recommendations-For-Melanin-Skin/blob/Echeruiyot/images/image5.png)
* The heatmap analysis of skin_type and skin_tone_category highlights important insights that align closely with our objectives. Our data reveals a concentration of products available for combination and dry skin types, particularly within lighter skin tones. However, there is a notable scarcity of options for deeper skin tones.This gap underscores the limited market focus on skincare for melanin-rich skin concerns, such as hyperpigmentation, dryness, and sensitivity, which are often more pronounced in deeper skin tones.

* These findings directly support our business problem: many existing recommendation systems fail to provide targeted solutions for specific skin tones. The evident lack of specialized options for drier skin in deeper tones emphasizes an opportunity to develop and recommend products that address this unique need. By prioritizing these underserved areas, our recommendation system can significantly enhance satisfaction and efficacy for women of color seeking products that work for their melanin-rich skin.

---

## Modeling Approach
The recommendation system integrates multiple models:
1. **Customer Feature-Based Recommender**: Recommends products based solely on customer characteristics.
2. **Highlight-Based Recommender**: Recommends products based on selected highlights, catering to specific product features.
3. **Content-Based Filtering Model**: Recommends similar products based on ingredients and features using cosine similarity.
4. **Collaborative Filtering with SVD**: Leverages user-product interactions to recommend products based on user preferences.
5. **Hybrid Model**: Combines content-based and collaborative filtering to provide robust, varied recommendations.

### Evaluation Metrics
- **Precision@k**: Measures the relevance of the top K-recommended products.
- **Recall@k**: Evaluates the system's effectiveness in covering user preferences in the top K recommendations.
- **F1-Score**: Ensures a balance between precision and recall.
- **Hit Rate@k**: Determines if users find a relevant product in the top 5.
- **Normalized Discounted Cumulative Gain (NDCG)**:Considers the position of relevant items, rewarding relevant items appearing earlier in the recommendations list.

---
### Model Performance
1. **High Precision and Recall at *K*=1:**
- **Precision@1** of 0.99 and Recall@1 of 0.91 indicate that the model is very accurate when recommending a single top item. Users are very likely to find a relevant item in the top 1 recommendation.
2. **Performance Drops as *𝐾* Increases:**
- Precision drops significantly as **𝐾** increases (e.g., **Precision@5** of 0.24 and **Precision@20** of 0.06). This suggests that as more items are recommended, fewer of them are relevant.
3. **Hit Rate@k == 0.99**
- With a Hit Rate of 0.99 across all values of **𝐾**,the model is consistently recommending at least one relevant item within the top **𝐾** recommendations for almost every user.
4.  The **NDCG@10:** 0.99 result is excellent, indicating that the ranking provided by your recommendation model closely matches the ideal order, where the most relevant items appear at the top.
---

## System Interface
The Streamlit [App](https://melanin-centered-skincare-recommendation-system.streamlit.app/) enables users to select product categories and highlights for personalized recommendations, covering the full skincare spectrum:
- **Recommendation Pages**: An intuitive interface where users can select options based on preferences (e.g., skincare, makeup, fragrance).
 ![Home Page 1](https://github.com/user-attachments/assets/367f5794-5e65-4718-b342-5f8ef4e0e6d0)
![Home Page 2](https://github.com/user-attachments/assets/78d7db20-b1e5-4d96-8bdb-7031629aafea)
- **Product Highlights-Based Recommendations**: Users can select specific highlights (e.g., "hydrating," "anti-aging," ) and receive products that meet these needs.
![Highlights](https://github.com/user-attachments/assets/d5d19dc2-b7df-420a-9f38-b7c0121c4784)
- **Recommendation Options**: Users receive product recommendations tailored to specific beauty needs or similar to products they already enjoy.
![Content-Based](https://github.com/user-attachments/assets/86e48078-39c1-428e-8a8d-cf3e34ce3e30)

---

## CONCLUSION
- This project successfully developed a skincare recommendation system specifically tailored for individuals with melanin-rich skin, addressing a significant gap in personalized skincare recommendations. 
- By using content-based filtering on ingredient similarities, collaborative filtering through SVD, and sentiment analysis, the system delivers customized product suggestions that align with users’ unique skin concerns and preferences. The Streamlit interface enhances user experience, providing an intuitive way for users to access their personalized recommendations easily.
- Our approach demonstrates the potential of AI-driven solutions to meet niche market needs and make the skincare industry more inclusive. The system’s design aims not only to recommend relevant products but also to boost user satisfaction by prioritizing highly rated products based on sentiment analysis.

## CHALLENGES
Throughout the project, some notable challenges included:
- **Data Limitations**: The dataset was limited in brand, categories and product diversity, which restricted the range of recommendations.
- **Model Optimization**: Balancing the hybrid model’s performance was challenging, as both content-based and collaborative methods required fine-tuning to avoid biases.
- **Sentiment Analysis Accuracy**: Ensuring accurate sentiment analysis was critical for prioritizing products, but limitations in natural language processing led to occasional inaccuracies in sentiment scoring.

## RECOMMENDATIONS
To enhance the functionality and user engagement of this skincare recommendation system, several improvements are recommended:
- **Enhance User Engagement**: Implement feedback mechanisms to allow users to rate and provide input on recommended products. This feedback loop would help refine the recommendations and improve overall user satisfaction.
- **Expand Dataset Diversity**: Increase the dataset size and diversity to include more skincare brands, product varieties, and user profiles. This would ensure a broader range of personalized recommendations and allow the system to cater to a wider audience.
- **Implement Educational Resources**: Include educational content about skincare for melanin-rich skin, helping users better understand product ingredients, skincare routines, and how to address specific skin concerns.
- **Improve User Interface**: Enhance the user interface for greater ease of use, enabling users to quickly and seamlessly find tailored product recommendations.

## NEXT STEPS:
To further enhance the system and expand its impact, the following steps are recommended:
- **Partner with Skincare Experts and Dermatologists**: Collaborate with skincare specialists to review and validate product recommendations, ensuring that suggestions meet the specific needs of melanin-rich skin.
- **Expand Dataset Coverage**: Increase the dataset size and diversity to cover a broader range of brands, products, and user profiles. This will improve recommendation accuracy and offer users more choices.
- **Integrate Educational Resources**: Include guides and educational content about skincare ingredients and routines for melanin-rich skin, empowering users to make informed decisions.
- **Implement Feedback Loops**: Add mechanisms for users to rate and provide feedback on recommendations, allowing the system to learn and improve continuously.
- **Collaborate with Brands**: Partner with major skincare brands like Garnier and other beauty companies to integrate this recommendation system directly into their platforms, making it accessible to a wider audience.
This project serves as a foundation for creating an inclusive and personalized skincare experience, supporting users with tailored product recommendations that address their unique skincare needs.
---

## Getting Started
To run this project locally, follow these steps:

### Prerequisites
- Python 3.8 or higher
- Required Libraries: `pandas`, `numpy`, `scikit-learn`, `nltk`, `tensorflow`, `streamlit`

### Installation
1. Clone this repository:
   ```bash
   git clone https://github.com/Divinegrace05/Personalized-Beauty-Product-Recommendations-For-Melanin-Rich-Skin.git
   cd Personalized-Beauty-Product-Recommendations-For-Melanin-Rich-Skin
   ```
2. Install required packages:
    ```bash
    pip install -r requirements.txt
    ```

### Usage
To start the Streamlit application:
   ```bash
    streamlit run skincareApp.py
   ```

---

## Repository Navigation
- **`data/`**: Contains raw and processed data supporting the recommendation system.
- **`images/`**: Saved images.
- **`models/`**: Saved machine learning models.
- **`index.ipynb/`**: Jupyter notebook for data preprocessing, EDA and model training.
- **`cosmeticsApp.py`**: Main Streamlit application file.

# THANK YOU!!
---
