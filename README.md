# navigatingNYCjobmarket
data: https://catalog.data.gov/dataset/nyc-jobs

Research Questions:
What are the most common job titles and industries represented in job postings in New York City?
What are the most commonly required Technical skill and qualifications in job postings in New York City?
What soft skills are preferred?

Methodology:
For preprocessing, text data was converted into lowercase. Numbers, special/junk characters, and NLTK defined stop words were deleted, and the text was lemmatized.
To identify the necessary skills from our data, we use classification. 
The data is clustered based on job title 
We opt for multilabel classification as there may be multiple job titles with similar characteristics. 
XGBoost Classifier was used to combine the outputs from individual decision trees to perform regression or classification.This model helps prevent overfitting by combining many decision trees. 
The data is split 80-20 for train/test data. For feature extraction, CountVectorizer is used in a format supported by machine learning algorithms from text datasets.
To figure out what the minimum requirements were for most jobs, we summed up the amount of listings a requirement appeared in a listing as the lowest accepted qualification
For finding the specific soft skills employers were seeking, we performed feature extraction on our classified data.
Technical skills were extracted by matching predefined sets of technical skills to the words in each class. 
To extract soft skills, we leverage the TextBlob library, which uses POS-tags to identify adjectives that describe a person's skills or traits.
The most significant characteristics of each class were determined by computing the probabilities of each feature 

Technical skills:
<img width="985" alt="image" src="https://github.com/Harshi293/navigatingNYCjobmarket/assets/144385477/eacfd278-587c-40d5-b0bd-42c5477fffd5">
<img width="985" alt="image" src="https://github.com/Harshi293/navigatingNYCjobmarket/assets/144385477/5877dbee-417f-4210-8cbb-739c9894d7f0">
<img width="985" alt="image" src="https://github.com/Harshi293/navigatingNYCjobmarket/assets/144385477/69e9ffe9-e35e-4100-86be-57c8c8ec17cf">
<img width="985" alt="image" src="https://github.com/Harshi293/navigatingNYCjobmarket/assets/144385477/3f5436b0-43f0-45f3-a85a-72a78ae191f7">

Soft skills:
<img width="985" alt="image" src="https://github.com/Harshi293/navigatingNYCjobmarket/assets/144385477/25c321cb-82a5-428f-84b3-4bc52715c86e">
<img width="985" alt="image" src="https://github.com/Harshi293/navigatingNYCjobmarket/assets/144385477/f7cbfcd4-060b-4264-9730-8319b634b06e">




