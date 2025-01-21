# Identification-of-Toxic-Comments-and-analysis-for-model-bias
The dataset used in this project was curated by the Conversation AI team, a research initiative established by Jigsaw and Google. It featured in the 2019 Kaggle competition, [Jigsaw Unintended Bias in Toxicity Classification](https://www.kaggle.com/c/jigsaw-unintended-bias-in-toxicity-classification/overview/description), and was sourced from the Civil Comments platform between 2015 and 2017.

File descriptions

    train.csv - the training set, which includes toxicity labels and subgroups
    test.csv - the test set, which does not include toxicity labels or subgroups
    sample_submission.csv - a sample submission file in the correct format

The following files were added post-competition close, to use for additional research. Learn more here.

    test_public_expanded.csv - The public leaderboard test set, including toxicity labels and subgroups. The competition target was a binarized version of the toxicity column, which can be easily reconstructed using a >=0.5 threshold.
    test_private_expanded.csv - The private leaderboard test set, including toxicity labels and subgroups. The competition target was a binarized version of the toxicity column, which can be easily reconstructed using a >=0.5 threshold.
    toxicity_individual_annotations.csv - The individual rater decisions for toxicity questions. Columns are:
        id - The comment id. Corresponds to id field in train.csv, test_public_labeled.csv, or test_private_labeled.csv.
        worker - The id of the individual annotator. These worker ids are shared between toxicity_individual_annotations.csv and identity_individual_annotations.csv.
        toxic - 1 if the worker said the comment was toxic, 0 otherwise.
        severe_toxic - 1 if the worker said the comment was severely toxic, 0 otherwise. Note that any comment that was considered severely toxic was also considered toxic.
        identity_attack, insult, obscene, sexual_explicit, threat - Toxicity subtype attributes. 1 if the worker said the comment exhibited each of these traits, 0 otherwise.
    identity_individual_annoations.csv - The individual rater decisions for identity questions. Columns are:
        id - The comment id. Corresponds to id field in train.csv, test_public_labeled.csv, or test_private_labeled.csv.
        worker - The id of the individual annotator. These worker ids are shared between toxicity_individual_annotations.csv and toxicity_individual_annotations.csv.
        disability, gender, race_or_ethnicity, religion, sexual_orientation - The list of identities within this category that the rater noticed in the comment. Formatted a space-separated strings
