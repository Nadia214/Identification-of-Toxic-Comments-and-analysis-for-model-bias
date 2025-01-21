# Identification-of-Toxic-Comments-and-analysis-for-model-bias
The dataset used in this project was curated by the Conversation AI team, a research initiative established by Jigsaw and Google. It featured in the 2019 Kaggle competition, [Jigsaw Unintended Bias in Toxicity Classification](https://www.kaggle.com/c/jigsaw-unintended-bias-in-toxicity-classification/overview/description), and was sourced from the Civil Comments platform between 2015 and 2017.

**File Descriptions**  

1. **Training and Test Files:**  
   - **train.csv**: The training dataset, containing toxicity labels and subgroup information for the comments.  
   - **test.csv**: The test dataset, which excludes toxicity labels and subgroup information.  
   - **sample_submission.csv**: A sample submission file formatted correctly for the competition.  

2. **Post-Competition Additions for Further Research:**  
   - **test_public_expanded.csv**: The public leaderboard test set, now including toxicity labels and subgroup details. The competition target is a binary version of the toxicity column, which can be reconstructed using a threshold of `>= 0.5`.  
   - **test_private_expanded.csv**: The private leaderboard test set, also containing toxicity labels and subgroup details. Similar to the public set, the binary toxicity target can be derived using a `>= 0.5` threshold.  

3. **Annotation Files:**  
   - **toxicity_individual_annotations.csv**: Includes individual rater decisions for toxicity questions.  
     - **Columns:**  
       - `id`: The comment ID, corresponding to `id` in `train.csv`, `test_public_labeled.csv`, or `test_private_labeled.csv`.  
       - `worker`: The ID of the annotator, shared with `identity_individual_annotations.csv`.  
       - `toxic`: Indicates if the annotator flagged the comment as toxic (`1`) or not (`0`).  
       - `severe_toxic`: Indicates severe toxicity (`1` if flagged, `0` otherwise). Any comment flagged as severely toxic is also considered toxic.  
       - `identity_attack`, `insult`, `obscene`, `sexual_explicit`, `threat`: Subtype attributes of toxicity. Each is flagged as `1` if present or `0` otherwise.  

   - **identity_individual_annotations.csv**: Contains individual rater decisions for identity-related questions.  
     - **Columns:**  
       - `id`: The comment ID, corresponding to `id` in `train.csv`, `test_public_labeled.csv`, or `test_private_labeled.csv`.  
       - `worker`: The ID of the annotator, shared with `toxicity_individual_annotations.csv`.  
       - `disability`, `gender`, `race_or_ethnicity`, `religion`, `sexual_orientation`: Space-separated strings listing identities noticed by the annotator within each category.  
