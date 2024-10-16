# Statistical Computing and Data Analysis

Author: Muhammad Usman

Course Code: STAT-711

This is Git repository containing material about Statistical Computing and Data Analysis.

## Week 01
# Reading CSV data file
```{r}
df <- read.table(file = "data.csv",
                 header = T,
                 sep=",")

df
# View the data
View(df)
names(df)
str(df)
df$Age
df$Name
df$Marks
nrow(df)
ncol(df)
dim(df)
head(df)
tail(df, 2)

# Some statistics
mean(df$Age)
mean(df$Marks)
var(df$Age)
sd(df$Age)
median(df$Age)


quantile(x = df$Age, 
         probs = 0.75)
quantile(x = df$Age, 
         probs = c(0.25, 0.5, 0.75))

summary(df)
table(df$Gender)
tab1 <- table(df$Gender)
tab1
prop.table(tab1)*100

1:10
c(1,3,5)
1:5
1


df2 <- df[1:5 , ]
df2
```
