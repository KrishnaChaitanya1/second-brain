# Data and Data Models

## Data

 Data is a collection of attributes (features or variables or columns) and objects (sample or instance or rows). **Attributes** are characteristcs of **objects** and objects are collection of attributes.  

Data is broadly classified as **Quantitative** (Interval and Ratio) **Qualitative or Categorical** (Nominal and Ordinal)

### Attribute Types

There are 4 different attribute types:

1. Nominal
2. Ordinal
3. Interval
4. Ratio

All of the above possess all the properties and operations like *Distinctiveness*, *Order*, *Addition*, *Multiplication*.

> Refer T3 - Page 26, Table 2.2 for more info

Attributes can be further divided based on the number of values they take:

1. Discrete - Finite or countable infinte set of values
    - Binary Attributes - Special case of discrete
2. Continuous - Real Numbers, Temperature, Height etc.,
3. Assymentric - Only non-zero attribute value is considered

### Types of Datasets

Datasets generally have the following characteristics:

1. Dimensionality
    - The number of attributes that the objects in dataset possess.
2. Sparsity
    - Datasets with more 0 values.
3. Resolution
    - Picture resolution etc.,

Below are the Data Formats:

- Record Data - Usually stored in flat files or Relational Databases.
  - Transaction or Market Basket Data
  - Data Matrix
    - If data objects in a dataset have fixed set of numeric attributes then they can be represented as vectors in a multidimensional space, where each dimension is an attribute.
    - A set of such objects can be interpreted as $m$ by $n$ matrix where $m$ are rows and $n$ are columns.
  - Sparse Data Matrix
  - Document Term Matrix

- Graph Data
  - Relationships among data objects - Webpages, etc.,
  - Data objects themselves as graphs - Chemical Compounds etc.,

- Ordered Data
  - Sequential Data or Temporal Data - Records have time associated with them.
  - Sequence Data - Genome Sequence etc.,
  - Time Series
    - It is important to consider **Temporal Autocorrelation**, which means if two objects are close in time then value of those two will be same.
  - Spatial
    - Important to consider **Spatial Autocorrelation**, which means if two objects are physically close, they tend to be similar.

## Data Quality

*Issues*:

1. Noise and Outliers
2. Measurement and Data Collection Errors
3. Missing Data
4. Duplicate Data
5. Inconsistent Data
6. Biased Data
7. Data that is unrepresentative of population

## Preprocessing Data

*Concepts*:

1. Aggregation
    - Combining two or more objects into a single object.
    - Smaller datasets resulting from aggregation requires less memory and processing time, therefore more expensive algorithms can be used.
    - Aggregation can provide a high-level view.
2. Sampling
    - Selecting a subset of data objects to be analyzed.
    - Key Principle: **A Sample will work as well as using the entire dataset provided it is representative of the dataset**.
    - A sample is representative if it has approximately same properties as original dataset.
    - Sampling Approaches (*Refer IDS Notebook and T3 Page 48*):
        - Simple Random Sampling
          - With Replacement
            - Objects are not removed as they are being sampled.
            - Same object can be picked more than once.
            - Simpler to analyze when compared with without replacement
          - Without Replacement
            - Objects are removed as they are being sampled.
        - Stratified Sampling
        - Progressive or Adaptive Sampling
          - In both of the above cases selecting proper sample size is hard.
          - So Progressive Sampling is used which will start with a small sample size and gradually increase the size until sufficient sample size is obtained.
          - However there is a need to judge if the sample size is large enough.
3. [Dimensionality Reduction](machine-learning/dimensionality-reduction/dimensionality-reduction.md)
4. Feature Subset Selection
    - **Embedded Approach**: Happens implicitly as part of Data Mining Algorithm
    - **Filter Approach**: Features are selected before running Data Mining Algorithm
    - **Wrapper Approach**: Use target data mining algorithm as black box to find best feature
5. Feature Creation
6. Discretization and Binarization
7. Variable Transformation

## Epicycle of Data Analysis

1. Start and Refine Question
2. Exploratory Data Analysis
3. Build Stat Models
4. Interpret Results
5. Communicate Them

For each of the above steps, iterate through the following:

1. Set Expectations
2. Collect Data
3. Revise those expectations

This iteration is called Epicycle.

## Data Models

