# Data Directory

## Dataset Information

This project uses the **Spambase Dataset** from the UCI Machine Learning Repository.

### Automatic Download

The dataset is automatically downloaded when you run the notebook or script using the `ucimlrepo` package. No manual download is required.

### Dataset Details

- **Source**: UCI Machine Learning Repository
- **Dataset ID**: 94
- **URL**: https://archive.ics.uci.edu/dataset/94/spambase
- **Instances**: 4,601 emails
- **Features**: 57 numerical attributes
- **Target**: Binary classification (spam = 1, not spam = 0)

### Feature Description

The dataset contains 57 continuous real attributes:

**Word Frequency Features (48 features)**
- `word_freq_WORD`: Percentage of words in the email that match WORD
- Examples: word_freq_make, word_freq_address, word_freq_all, etc.

**Character Frequency Features (6 features)**
- `char_freq_CHAR`: Percentage of characters in the email that match CHAR
- Characters: `;`, `(`, `[`, `!`, `$`, `#`

**Capital Letter Statistics (3 features)**
- `capital_run_length_average`: Average length of uninterrupted sequences of capital letters
- `capital_run_length_longest`: Length of longest uninterrupted sequence of capital letters
- `capital_run_length_total`: Total number of capital letters in the email

### Citation

If using this dataset, please cite:

```
Hopkins, Mark, Reeber, Erik, Forman, George, and Suermondt, Jaap. (1999). 
Spambase [Dataset]. UCI Machine Learning Repository. 
https://doi.org/10.24432/C53G6X
```

### Notes

- All feature values are continuous (real numbers)
- No missing values in the dataset
- Class distribution: approximately 39.4% spam, 60.6% legitimate emails
- Dataset is relatively balanced for binary classification