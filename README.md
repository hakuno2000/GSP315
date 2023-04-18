# [Perform Foundational Infrastructure Tasks in Google Cloud: Challenge Lab](https://www.cloudskillsboost.google/focuses/10379?parent=catalog)

## Task 1. Create a bucket
```
gsutil mb -l us-central1 gs://memories-bucket-37979
```

## Task 2. Create a Pub/Sub topic
```
gcloud pubsub topics create memories-topic-261
```

## Task 3. Create the thumbnail Cloud Function
```
gcloud functions deploy memories-thumbnail-creator --region=us-central1 \
--runtime nodejs14 --entry-point=thumbnail \
--trigger-event=google.storage.object.finalize \
--trigger-resource=memories-bucket-37979
```

## Task 4. Remove the previous cloud engineer
Remove using console
