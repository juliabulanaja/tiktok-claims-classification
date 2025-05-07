**Claims Classification Model for TikTok: Predicting Claims vs. Opinions in User-Generated Content**

**Overview**

This project aimed to classify TikTok videos as factual claims or opinions using Random Forest and XGBoost models. 
Trained on features like view count, follower count, and author type, the final Random Forest model achieved an F1 
score of 0.81 and precision of 0.84. The most important features in distinguishing claims from opinions included 
video_view_count, video_like_count, video_download_count, share_count, andcomment_count.

**Business Understanding**

This project aims to support content moderation by classifying TikTok videos as factual claims or opinions, 
helping prioritize fact-checking and reduce misinformation.

**Data Understanding**

The dataset contains TikTok videos labeled as either “claims” (49.6%) or “opinions” (50.3%), indicating a balanced 
distribution ideal for classification modeling. Claim videos have much higher average view counts (501,029 vs. 4,956), 
likes per view (0.33 vs. 0.22), and shares per view than opinion videos, highlighting stronger audience engagement. 
Videos by banned authors show even greater engagement, with average views of 445,845 compared to 215,927 for active 
authors, and a median share count of 14,468 vs. 437. These trends suggest that both claim content and banned authors 
drive significantly more interaction, likely due to controversial or provocative material.

**Modeling and Evaluation**

Two models, Random Forest and XGBoost, were trained using a 60/20/20 data split. Random Forest was chosen for its 
slightly better performance. It was built on 10 engineered features related to video engagement and author attributes. 
With tuned parameters (e.g., n_estimators=20, max_depth=5), the final Random Forest model achieved outstanding 
results: 100% accuracy, 0.9995 precision, 0.9909 recall, and an F1-score above 0.99.


**Conclusion**

The Random Forest model accurately classified claim vs. opinion videos with over 99% precision and recall. 
Claim content and banned authors were key drivers of higher engagement, offering valuable insights for content 
and policy strategies.
