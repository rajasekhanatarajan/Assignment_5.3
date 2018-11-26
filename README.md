# Assignment_5.3
#1.Import dataset from the following link: AirQuality Data Set

Perform the following written operations:

#1. Read the file in Zip format and get it into R.

#2. Create Univariate for all the columns.

#3. Check for missing values in all columns.

#4. Impute the missing values using appropriate methods.

#5. Create bi-variate analysis for all relationships.

#6. Test relevant hypothesis for valid relations.

#7. Create cross tabulations with derived variables.

#8. Check for trends and patterns in time series.

#9. Find out the most polluted time of the day and the name of the chemical compound.

1 ->

1.unzip("x.zip")

for (i in files.temp)

unzip(i)

airqual <- read.table("C:/Desktop/airquality.txt")

airquality <- read.csv("~/CUNY/Bridge Classes/R Programming/Week4/airquality.csv", row.names=1) head(airquality)

2.ggplot(airquality, aes(x = Ozone)) + geom_histogram(binwidth = 5, fill="green", color="black")

3.We can use two colsums or apply. Please see below

colSums(is.na(airquality))

    or 
apply(is.na(airquality),2,sum)

4.md.pattern(airquality)

5.t.test(airquality)

6.We need to use Z value to find check whether H0 is accepted or rejected

7.table(airquality)

8.ts(inputData,frequency = 1, start = c(2018, 2)
