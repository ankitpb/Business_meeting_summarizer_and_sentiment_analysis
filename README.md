# Business_meeting_summarizer_and_sentiment_analysis
# Audio to summarised text using GCP 

Convert audio to sumarised text by using Google Cloud Platform tools (fully automated)

This project utilizes the following tools -
Google Cloud Storage (Bucket)
Google Speech to Text API 
Vertex AI (AutoML)

Basic workflow :
  speech_to_text.py 
-> Audio frame rate and channels are determined
-> creates a bucket in GCP and uploads the locally stored audio file. 
-> The Google speech to text API is used to find the transcript, which is then stored in the bucket. 
-> Repeats for all the audio files in the folder.
-> Transcripts are downloaded and the bucket is deleted.



  sentiment_prediction.py
-> Bucket is created in GCP and locally stored transcript is uploaded. 
-> AutoML's Sentiment Analysis model was trained on multiple appropriate datsets resulting in a accuracy of 92.6%
-> Utilizing the endpoints, we use the model to convert the text to a summarized version.


Note : 
Things you would need :
- JSON key from your GCP account 
- Endpoint ID from your AutoML model
- Project ID from your current project under your GCP account
