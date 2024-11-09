<<<<<<< HEAD
# AI-Powered-Skincare-Recommendations-For-Melanin-Skin

![2d248f5507752726ddc2198b39071e4e](https://github.com/user-attachments/assets/9c7a2247-b758-4aee-8bc7-50fa0bf76f2d


### Table of Contents

- [Business Overview](#business-overview)
- [Business Understanding](#business-understanding)
- [Data Understanding](#data-understanding)
- [Modeling and Evaluation](#modeling-and-evaluation)
- [Conclusion](#conclusion)
- [Repository Navigation](#repository-navigation)

## Business Overview

Our AI-powered recommendation system addresses the lack of tailored skincare solutions for individuals with melanin-rich skin. By leveraging two datasets on skin care products and products reviews by different users , our model delivers personalized skincare recommendations, achieving an accuracy of over 90% in predicting optimal products for various skin needs and on different budgets.

## Business Understanding

This project aims to develop a recommendation system using advanced AI techniques to cater specifically to Black women’s skincare needs. By integrating machine learning, content- based filtering, collaborative filtering, and sentiment analysis, the system will offer personalized skincare recommendations. Leveraging skin_tone (Author's skin tone (e.g. fair, tan, etc.) as a classification feature, we aim to distinguish and target products that align with melanin-rich skin concerns.

## Data Understanding

The dataset was collected via a Python scraper and contains:
- Product Information: Over 8,000 beauty products from the Sephora online store, including product and brand names, prices, ingredients, ratings, and various features. 
- User Reviews: Approximately 1 million reviews across over 2,000 products in the skincare category. These reviews include user appearances, skin types, and review ratings.

The key features include:
- Product Features: `product_id`, `product_name`, `brand_name`, `ingredients`, `rating`, `price_ksh`, `new`, `out_of_stock`, `highlights`. 
- Review Features: `author_id`, `rating`, `review_text`, `skin_type`, `skin_tone`, and
`helpfulness`.


### EDA

#### Count of Products by Skin Type
![download](https://github.com/user-attachments/assets/afdbd9db-19a8-44db-803a-5741efe0c067)
The distribution shows that products labeled for combination skin are the most common, followed by those for dry, normal, and then oily skin. This insight can guide product selection based on prevalent skin types and consumer demand within the Black women demographic.

#### Top 20 Recommended Products for Melanin Skin

![download](https://github.com/user-attachments/assets/8946f8fa-8448-4107-a84e-03e661bd4b6c)
The chart highlights skincare products tailored to the specific needs of melanated skin, focusing on hydration, hyperpigmentation, and sun protection. **Signature Moisturizer** leads with the highest recommendation count, emphasizing a strong demand for deep hydration. Products targeting dark spots, such as **Blue Algae Vitamin C Dark Spot Correcting Peel**, show the importance of tone-evening solutions, while sunscreens like **Mineral MatteSunscreen SPF 40 PA+++** address the need for effective sun protection without a white cast. This selection showcases a commitment to skincare that respects and meets the unique requirements of darker skin tones.

#### Out of stock Products and Recommendations based on skin tone

![download](https://github.com/user-attachments/assets/292c819f-04f0-44fa-b1c2-851bdb099e33)

Lighter skin tones show a higher count of both in-stock and out-of-stock products. This contrasts with deep skin tones which have fewer options overall and lower in-stock counts. This discrepancy might indicate a supply gap for these deeper skin tones, which are more likely to face limited product availability.

Products targeting melanated skin tones receive fewer recommendations, suggesting that product options may not fully address the needs or preferences of these individuals.

#### Heatmap of Product Count by Skin Tone Category and Skin Type
![download](https://github.com/user-attachments/assets/85e65e5a-60de-4f85-8d36-bbc1aa258743)

The heatmap analysis of `skin_type` and `skin_tone_category` highlights important insights that align closely with our objective of providing tailored skincare recommendations for Black women. Our data reveals a concentration of products available for combination and dry skin types, particularly within lighter skin tones. However, there is a notable scarcity of options for deeper skin tones, suggesting that Black women may have fewer product options specifically suited to their needs. This gap underscores the limited market focus on skincare for melanin-rich skin concerns, such as hyperpigmentation, dryness, and sensitivity, which are often more pronounced in deeper skin tones.

These findings directly support our business problem: many existing recommendation systems fail to provide targeted solutions for Black women. The evident lack of specialized options for drier skin in deeper tones emphasizes an opportunity to develop and recommend products that address this unique need. By prioritizing these underserved areas, our recommendation system can significantly enhance satisfaction and efficacy for Black women seeking products that work for their melanin-rich skin.

## Modeling and Evaluation


## Conclusion

## Repository Navigation

=======
# PERSONALIZED BEAUTY PRODUCT RECOMMENDATIONS FOR MELANIN RICH SKIN
![product](https://github.com/user-attachments/assets/d370cd58-a84b-472c-afa3-ea13a3424085)


## Project Overview
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


## Objectives
- **Develop** a recommendation system that covers multiple beauty product categories using AI and ML techniques.
- **Incorporate** content-based filtering, collaborative filtering, and sentiment analysis for accurate, varied recommendations.
- **Deploy** the system through a user-friendly Streamlit application for accessible, personalized product discovery.

---

## Stakeholders
- **End Users**: Individuals seeking personalized beauty product recommendations across diverse categories.
- **Beauty Brands**: Companies interested in offering curated recommendations to their customers.
- **Retailers**: Platforms looking to enhance the shopping experience with targeted product suggestions.

---

## Data Description
The dataset used in this project was gathered via a Python-based web scraper, including a wide array of beauty products and user reviews.

1. **Product Data**:
   - **Beauty Products**: Data covering various beauty products from brands, with details on type, ingredients, ratings, and price.
   - **Main Features**: `product_id`, `product_name`, `category` (skincare, haircare, makeup, etc.), `brand_name`, `ingredients`, `rating`, `price`, `stock_status`.

2. **User Reviews**:
   - **Customer Feedback**: Reviews with insights into product effectiveness for various skin types, hair textures, and personal preferences.
   - **Main Features**: `author_id`, `rating`, `review_text`, `skin_type`, `hair_type`, `review_preferences`, `helpfulness`.

---

### Exploratory Data Analysis

#### 1. Count of Products by Skin Type
![skintype](https://github.com/user-attachments/assets/af072621-bc6b-48d9-9be2-b5ce11dea9eb)

* The distribution shows that products labeled for combination skin are the most common, followed by those for dry, normal, and then oily skin. This insight can guide product selection based on prevalent skin types and consumer demand within the Black women demographic.

#### 2. Top 20 Recommended Products for Melanin Skin
![Top 20 Recommended Products for Melanin Skin](https://github.com/ECCHERUIYOT/AI-Powered-Skincare-Recommendations-For-Melanin-Skin/blob/Echeruiyot/images/image2.png)
* For melanated skin tones, there's a strong emphasis on gentle yet effective skincare products, with the top three recommendations focusing on hydration and sun protection.
* The Dew Dream Cleansing Balm leads the pack with about 55 recommendations, suggesting that gentle makeup removal is a priority for this skin type. The second most recommended product being the Signature Moisturizer, followed by the NA°39 Facial Sunscreen Mist with SPF 39, indicates that maintaining skin hydration and sun protection are crucial concerns for melanated skin. The prevalence of brightening, revitalizing, and gentle products in the top 10 (such as Absolue Soft Cream and Evercalm Gentle Cleansing Gel) suggests that users with melanated skin often seek products that address hyperpigmentation and sensitivity while maintaining skin barrier health.

* The list also includes several treatment-focused products like glycolic serums and exfoliators in the middle to lower rankings, indicating that while these are important, they're secondary to basic skin protection and hydration needs.

#### 3. Out of stock Products and Recommendations based on skin tone
![Out of stock Products and Recommendations based on skin tone](https://github.com/ECCHERUIYOT/AI-Powered-Skincare-Recommendations-For-Melanin-Skin/blob/Echeruiyot/images/image3.png)
* The Recommended pie chart illustrates the percentage of products recommended versus those that are not. A significant portion (85%) of products are not marked as recommended, indicating a possible quality or suitability gap. This could help identify where product performance might fall short or suggest a need for more tailored product options.

* The Products pie chart shows the balance between new and existing products. The larger percentage of existing products (91%) suggests that the platform maintains a consistent range of products, with newer items being introduced selectively. This distribution can provide insights into the inventory management and refresh rates of the catalog over time.

#### 4. Skin Tone Distribution by Price Tier
![skintone](https://github.com/user-attachments/assets/6e1279f0-3247-479c-adef-3549870ebdab)
* There is a noticeable price difference across skin tones. Products for melanated skin tend to have lower average prices, than non-melanated skin tones, highlighting more affordable options specifically formulated or suited for melanated skin. 

#### 5. Heatmap of Product Count by Skin Tone Category and Skin Type
![Heatmap of Product Count by Skin Tone Category and Skin Type](https://github.com/ECCHERUIYOT/AI-Powered-Skincare-Recommendations-For-Melanin-Skin/blob/Echeruiyot/images/image5.png)
* The heatmap analysis of skin_type and skin_tone_category highlights important insights that align closely with our objective of providing tailored skincare recommendations for women of color. Our data reveals a concentration of products available for combination and dry skin types, particularly within lighter skin tones. However, there is a notable scarcity of options for deeper skin tones, suggesting that women of color may have fewer product options specifically suited to their needs. This gap underscores the limited market focus on skincare for melanin-rich skin concerns, such as hyperpigmentation, dryness, and sensitivity, which are often more pronounced in deeper skin tones.

* These findings directly support our business problem: many existing recommendation systems fail to provide targeted solutions for melanated women. The evident lack of specialized options for drier skin in deeper tones emphasizes an opportunity to develop and recommend products that address this unique need. By prioritizing these underserved areas, our recommendation system can significantly enhance satisfaction and efficacy for women of color seeking products that work for their melanin-rich skin.

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
The Streamlit application enables users to select product categories and highlights for personalized recommendations, covering the full beauty spectrum:
- **Recommendation Pages**: An intuitive interface where users can select options based on preferences (e.g., skincare, makeup, fragrance).
![Home Page 1](https://github.com/user-attachments/assets/395f3d3f-a4fd-4b30-af33-3ad5a2865914)
![Home Page 2](https://github.com/user-attachments/assets/0937d7c3-367a-43ee-a93f-60c591faa849)
- **Product Highlights-Based Recommendations**: Users can select specific highlights (e.g., "hydrating," "vegan," or "good for dry scalp") and receive products that meet these needs.
![Highlights](https://github.com/user-attachments/assets/66557dd3-55d7-4a59-a8a4-3f8445554fe6)
- **Recommendation Options**: Users receive product recommendations tailored to specific beauty needs or similar to products they already enjoy.
![Content-Based](https://github.com/user-attachments/assets/0e8ca50d-1371-48f9-9b0e-109d9245be16)

---

## CONCLUSION
- This project successfully developed a skincare recommendation system specifically tailored for individuals with melanin-rich skin, addressing a significant gap in personalized skincare recommendations. 
- By using content-based filtering on ingredient similarities, collaborative filtering through SVD, and sentiment analysis, the system delivers customized product suggestions that align with users’ unique skin concerns and preferences. The Streamlit interface enhances user experience, providing an intuitive way for users to access their personalized recommendations easily.
- Our approach demonstrates the potential of AI-driven solutions to meet niche market needs and make the skincare industry more inclusive. The system’s design aims not only to recommend relevant products but also to boost user satisfaction by prioritizing highly rated products based on sentiment analysis.

## CHALLENGES
Throughout the project, some notable challenges included:
- **Data Limitations**: The dataset was limited in brand and product diversity, which restricted the range of recommendations.
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
    streamlit run cosmeticsApp.py
   ```

---

## Repository Navigation
- **`data/`**: Contains raw and processed data supporting the recommendation system.
- **`images/`**: Saved images.
- **`models/`**: Saved machine learning models.
- **`index.ipynb/`**: Jupyter notebook for data preprocessing, EDA and model training.
- **`skincareApp.py`**: Main Streamlit application file.


# THANK YOU!
---

>>>>>>> a637dc5cac006b760c31fbe960ccd42ec7eb7c5b
