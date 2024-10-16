# Statistical Computing and Data Analysis

**Author**: Muhammad Usman  
**Course Code**: STAT-711  

This repository contains material for the course **Statistical Computing and Data Analysis**.

---

## Week 01: Reading and Analyzing CSV Data

### Loading the CSV Data File

We will begin by loading a CSV file using the `read.table()` function. The dataset is stored in `data.csv` and contains various columns including `Age`, `Name`, `Marks`, and `Gender`.

```r
df <- read.table(file = "data.csv",
                 header = TRUE,
                 sep = ",")
```

### Basic Characteristics of the `df` Data Frame

Once the data is loaded, we can explore its structure and characteristics using the following commands:

```r
# View the data in the data frame
df
View(df)

# Display column names
names(df)

# Show the structure of the data frame
str(df)

# Access individual columns
df$Age
df$Name
df$Marks

# Get the number of rows and columns
nrow(df)
ncol(df)
dim(df)

# View the first and last few rows
head(df)
tail(df, 2)
```

### Basic Descriptive Statistics

Next, we calculate some basic statistics for the `Age` and `Marks` columns:

```r
# Calculate mean, variance, and standard deviation
mean(df$Age)
mean(df$Marks)
var(df$Age)
sd(df$Age)

# Calculate the median
median(df$Age)

# Calculate quantiles
quantile(df$Age, probs = 0.75)
quantile(df$Age, probs = c(0.25, 0.5, 0.75))

# Summary statistics for the entire data frame
summary(df)
```

### Frequency Tables and Proportions

You can create frequency tables and calculate the percentage distribution for categorical variables like `Gender`:

```r
# Frequency table for Gender
table(df$Gender)

# Save the table as an object and view it
tab1 <- table(df$Gender)
tab1

# Calculate proportions (as percentages)
prop.table(tab1) * 100
```

### Subsetting the Data

To subset the data, you can use the following commands to extract the first five rows of the data frame:

```r
# Subset the first five rows
df2 <- df[1:5, ]
df2
```

### Other Basic Operations

Here are a few additional examples of basic R operations:

```r
# Creating sequences
1:10
c(1, 3, 5)
1:5
```
