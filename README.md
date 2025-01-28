# echr_foe

## This is the Github Repository of the ECHR Freedom of Expression Project

read_dataset.ipynb reads the dataset from the unstructured json file, extracts relevant sections into markdown format, gets the full text of the case, uses regular expressions to split the dataset into "violation of article 10" , "non - violation of article 10" and "other" subsets, picks a subset of the subsets, shuffles it and creates a dataset for manual validation.

calculate_agreement.ipynb extracts the annotation data from the excel file and calculates the kappa cohen score for inter-annotator agreement.

preprocess_foe.ipynb preprocesses the text to clean it up, remove stopwords, detect and remove named entities, generates bigrams and saves the files.

lda_foe.ipynb gets the preprocessed text and performs LDA using grid search optimisation to get the best possible combination of topic coherence (CV) and topic diversity. 