# 2. Data

## Feature selection and engineering

**Selection**:
* Choose features that don't impact the model performance
    * person's name when predicting if they like tea
*  Makes model faster to train and more accurate
* Gaps in data. Remove? Keep? Infer?
> Use domain knowledge, drop features with little correlation target, low variance or lots of missing data

Feature engineering
* Compute new features from existing features
    * Time of day, from timestamp
    * Country from city
> Simplify features, remove irrelevant info, standardise ranges (0-10: 0-1 && -100-100: -1-1), transform data

## Principal component analysis
Unsupervised dimension reduction while retaining all or most of the information
* Example is taking a photograph of a 3d object. You lose one dimension of the data, but the info is still there
* Often used as a data pre-processing step
* Can be used to plot high-dimensional data as groups of features

## Missing and unbalanced data
Missing: 
* Few datapoints missing: Replace missing data with average
* Few rows missing: Remove row
* Column missing most data: Remove column

How to deal with Unbalanced: 
* Get more data (often overlooked)
* Oversample minority: Little variation
* Synthesize data: Take minority data, apply some variation to make new points
* Different algorithms 

## Label and 1-hot-encoding
* Label-Encoding: Replace strings with values (brazil:0, USA: 1, UK: 2)
* One-hot-encoding: New columns with binary values if they match (Brazil: (brazil:1, usa:0, uk: 0) )

## Splitting and Randomization
Train/test splits. ALways randomize data

## RecordIO format
Pipe mode instead of File mode. Faster start and better throughput. Streams the data to the model
* SageMaker works best with RecordIO, streams data directly from S3 without storing locally

