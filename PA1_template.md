# Reproducible Research: Peer Assessment 1


## Loading and preprocessing the data
```{R,ECHO=TRUE}
unzip(zipfile="activity.zip")
setwd("/home/chase/repro/RepData_PeerAssessment1/")
activitydata <- read.csv("activity.csv",header=TRUE)
activityday <- transform(activitydata,date=as.Date(date))
```

## What is mean total number of steps taken per day?
```R
steps <- tapply(activityday$steps, activityday$date, FUN = sum, na.rm = TRUE)
hist(steps,breaks=30,main="Steps Per Day By Frequency",xlab="Daily Steps")
```

## What is the average daily activity pattern?



## Imputing missing values



## Are there differences in activity patterns between weekdays and weekends?
