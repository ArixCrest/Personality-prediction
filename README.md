# Personality Prediciton on Social Media posts
## Introduction
The Myers-Briggs Type Indicator(MBTI) is the name of a personality test designed to assess personality type of a person. It was Developed by Katherine Briggs and her daughter Isabel Myers during the World War II . The MTBI is popular with recruiters and managers because studies showing this assessment show clusters of different personality types in different professions. <br />
I have used different models to predict what MBTI type a person belongs to depending on the social media posts of the person. The models are based on how certain words appear more often in certain personality types and using this the model tries to assign a personality type.
## Methodology
1. The posts column had a lot of noise like links to websites, three bars separating sentences special characters and so on. These were removed because they are not relevant. We also try to do lexicon normalisation on the data as well as object standardisation. o help us get the data in the desired format. I used ‘NLTK' module for removing the noise.
2. Here after the noise removal we convert the textual data into features Term Frequency - Inverse Document Frequency(TF- IDF). This method converts the text directly into numbers.
3. Testing on different Classifiers like SVM, XGBoost etc.
## Conclusion
From the above observed results we can see that SVM does better than most of the models whether we use linear kernel or an RBF kernel. XGBoost comes close to linear SVM but it is far more computationally heavier than it taking nearly 10-15 minutes to complete whereas linear SVM took less than a minute. <br /> 
Random forest classifier experiences a loss in accuracy was the max depth was changed from None to 36 whereas the opposite happened for decision tree when setting the limit for max depth the accuracy increased this might be because Random forest uses more than one decision trees and averages the final prediction, where for the latter we only have one single tree. <br />
Similarly adaboost also does bad considering it is similar to random forest but employs a slightly different algorithm. <br/>
Multinomial Naive bayes does the worst here which might be due to the assumption that textual data follows a multinomial Distribution.<br />
Overall SVM is the preferred model.
