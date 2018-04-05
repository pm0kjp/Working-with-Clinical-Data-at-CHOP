---
title: Examining Clinical Data
description: So, you've received some .csv files of clinical data.  How can you take a look at your data to confirm the data quality and prepare for the next steps?

---
## Accessing your clinical data files

```yaml
type: NormalExercise
lang: r
xp: 100
skills: 1
key: dce89f43d6
```

For the sake of this course, we'll provide you with some .csv files that contain (fabricated) clinical data.  These fabricated datasets are intended to be similar to what you might receive from a data pull from CHOP's EHR.  We'll begin by examining this data to understand what it looks like and check for completeness.

`@instructions`
Use `read.csv()` to access the data at  https://s3.amazonaws.com/chop-dbhi-arcus-education-course-assets/sample_demographic.csv.  Then use `str()` to examine the structure of your data!

`@hint`
Unsure of how to use `read.csv`?  Type `?read.csv()` in the console to the right.
Unsure of how to use `str`?  Type `?str()` in the console to the right.


`@sample_code`
```{r}
demographics <- read.csv(# put your data source here!)
str(# put the object name you want to examine here!)
```
`@solution`
```{r}
demographics <- read.csv("https://s3.amazonaws.com/chop-dbhi-arcus-education-course-assets/sample_demographic.csv")
str(demographics)
```
`@sct`
```{r}
test_error()
test_function("read.csv",
              not_called_msg = "Make sure to call `read.csv()`")
test_function("str",
              not_called_msg = "Make sure to call `str()`")
test_object("demographics",
            undefined_msg = "Make sure to define `demographics`!",
            incorrect_msg = "Did you assign the contents of `https://s3.amazonaws.com/chop-dbhi-arcus-education-course-assets/sample_demographic.csv` to `x`?")
success_msg("Great job.  By the way, it's considered good style to write spaces either side of the assignment arrow.")
```




