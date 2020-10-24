# R-project

#EXERCISE : 2.1
#enters fill-ups into R 
miles=c(65311,65624,65908,66219,66499,66821,67145,67447)				
#gives the number of miles between fill-ups.
x=diff(miles) 									
#Print out the value
x																
#[1] 313 284 311 280 322 324 302


#EXERCISE : 2.2
#enters commute times into R
commutes=c(17,16,20,24,22,15,21,15,17,22)	
#find the longest commute time
max(commutes)															
#[1] 24
#find the average
mean(commutes)															
#[1] 18.9
#find the minimum
min(commutes)															
#[1] 15
#Replace 24 by 18
commutes[4]=18															
#Print out the new vector
commutes																	
#[1] 17 16 20 18 22 15 21 15 17 22
#find the new average
mean(commutes)														
#[1] 18.3
#How many times was your commute 20 minutes or more
sum(commutes>=20)							
#[1] 4
#We found that for 4 times commute is 20 minutes or more
#percentage of commutes that are less than 17
(sum(commutes<17)*100)/length(commutes) 
#[1] 30


#EXERCISE : 2.3
#enters cell phone bill into vector bill
bill=c(46,33,39,37,46,30,48,32,49,35,30,48)
# find the total amount spent this year on the cell phone	
sum(bill)										
#[1] 473
#find the smallest amount spent in a month
min(bill)										
#[1] 30
#find the largest amount spent in a month
max(bill)										
#[1] 49
#How many months was the amount greater than $40
sum(bill>40)								
#[1] 5
#percentage of  months was the amount greater than $40
(sum(bill>40)*100)/length(bill)										
#[1] 41.66667


#EXERCISE : 2.4
#Enter prices to vector car
car=c(9000,9500,9400,9400,10000,9500,10300,10200)		
#average using sum()
sum(car)/length(car)													
#[1] 9662.5
#comparing average value with Edmund's estimate of 9500
(sum(car)/length(car))-car[2]
#[1] 162.5 
#average value is higher than Edmund's estimate of 9500 
#Find minimum value	
min(car)					
#[1] 9000
#Find maximum value	
max(car)																
#[1] 10300


#EXERCISE : 2.5
x=c(1,3,5,7,9)
y=c(2,3,5,7,11,13)
#Adds 1 to each value of X
x+1																	
#[1]  2  4  6  8 10
#Multiplies 2 to each value of y
y*2																	
#[1]  4  6 10 14 22 26
#How many elements are there in vector x
length(x)													
#[1] 5
#How many elements are there in vector Y
length(y)																
#[1] 6
#Adds X and Y (with corresponding values)
x+y                             
#[1]  3  6 10 14 20 14
#How many numbers are there which are greater than 5
sum(x>5)												
#[1] 2
#Add numbers which are greater than 5
sum(x[x>5])															
#[1] 16
#How many numbers are there which are greater than 5 or less than 3
sum(x>5|x<3)															
#[1] 3
#Print out value of 3rd index of Y Vector
y[3]																	
#[1] 5
#Print all values of Y except value of 3rd index
y[-3]                            
#[1]  2  3  7 11 13
#Print  values of Y by taking x values as index
y[x]                            
#[1]  2  5 11 NA NA         
#NA means value is not available in that index
#Print values of Y vector which are greater than or equal to 7
y[y>=7]																
#[1]  7 11 13

#EXERCISE : 2.5
#enters values into vector x
x=c(1,8,2,6,3,8,5,5,5,5)
#Finds the average value using sum function	
sum(x)/10
#[1] 4.8
#print log10(Xi) for each i
log10(x)																																								
#[1] 0.0000000 0.9030900 0.3010300 0.7781513 0.4771213 0.9030900 0.6989700 0.6989700
#[9] 0.6989700 0.6989700
(x-4.4)/2.875
#[1] -1.1826087  1.2521739 -0.8347826  0.5565217 -0.4869565  1.2521739  0.2086957
#[8]  0.2086957  0.2086957  0.2086957
#find the difference between the largest and smallest values of x
max(x)-min(x)														
#[1] 7
#find the difference between the largest and smallest values of x using built in function
diff(range(x)	)													
#[1] 7

#Exercise :3
#Exercise:3.1
#Enter in the data
#60 85 72 59 37 75 93 7 98 63 41 90 5 17 97
# Make a stem and leaf plot.
x <- c(60, 85, 72, 59, 37, 75, 93, 7, 98, 63, 41, 90, 5, 17, 97)
stem(x)
# The decimal point is 1 digit(s) to the right of the |

#0 | 577
#2 | 7
#4 | 19
#6 | 0325
#8 | 50378

#Exercise 3.2

x <- c(80, 82, 88, 91, 91, 95, 95, 97, 98, 101, 106, 106, 109, 110, 111)
hist(x)

#Exercise: 3.3
x1 <- rnorm(100)
hist(x1)
x2 <- rnorm(100)
hist(x2)
#  as these are 2 distinct generations of rnorm,
# their histograms are different...

#Exercise: 3.4
install.packages("Hmisc")
install.packages("UsingR", dependencies = TRUE)
library(UsingR)
data(south)
class(south)
#[1] "numeric"
summary(south)
#   Min. 1st Qu.  Median    Mean 3rd Qu.    Max. 
#   6.00   10.25   12.00   13.97   15.50   33.00 
hist(south)
boxplot(south)
#  south is skewed, with outliers
data(crime)
class(crime)
#[1] "data.frame"

summary(crime)
#     y1983            y1993       
# Min.   :  53.7   Min.   :  83.3  
# 1st Qu.: 245.4   1st Qu.: 328.8  
# Median : 397.9   Median : 535.5  
# Mean   : 437.5   Mean   : 606.8  
# 3rd Qu.: 553.0   3rd Qu.: 758.1  
# Max.   :1985.4   Max.   :2832.8 

c1 <- as.numeric(crime[[1]])
c2 <- as.numeric(crime[[2]])
hist(c1)
boxplot(c1)
#   The same goes for the crime dataset

data(aid)
summary(aid)
#   Min. 1st Qu.  Median    Mean 3rd Qu.    Max. 
#     42.29   95.28  114.20  123.60  144.60  253.50 

class(aid)
#[1] "numeric"

hist(aid)
boxplot(aid)
# aid is symmetric, with an outlier

#Exercise: 3.5
data(bumpers)
hist(bumpers)
mean(bumpers)
#[1] 2122.478
median(bumpers)
#[1] 2129
sd(bumpers)
#[1] 798.4574
data(firstchi)
hist(firstchi)
mean(firstchi)
#[1] 23.97701
median(firstchi)
#[1] 23
sd(firstchi)
#[1] 6.254258
data(math)
hist(math)
mean(math)
#[1] 54.9
median(math)
#[1] 54
sd(math)
#[1] 9.746264

#Exercise: 3.6
failures <- c(0, 1, 0, NA, 0, 0, 0, 0, 0, 1, 1, 1, 0, 0, 3, 0, 0, 0, 0, 0, 2, 0, 1)
table(failures, useNA='always')
#failures
#   0    1    2    3 <NA> 
#  15    5    1    1    1
mean(failures)
#[1] NA
mean(failures, na.rm=TRUE)
#[1] 0.4545455

#Exercise: 3.7
data(pi2000)
summary(pi2000)
#   Min. 1st Qu.  Median    Mean 3rd Qu.    Max. 
#  0.000   2.000   5.000   4.546   7.000   9.000 
hist(pi2000)
simple.freqpoly(pi2000)
table(pi2000)
#pi2000
#  0   1   2   3   4   5   6   7   8   9 
#  181 213 207 189 195 205 200 197 202 211
table(pi2000)/length(pi2000)
#pi2000
#     0      1      2      3      4      5      6      7      8      9 
#     0.0905 0.1065 0.1035 0.0945 0.0975 0.1025 0.1000 0.0985 0.1010 0.1055

#Exercise: 3.8
#  ... through a bit of trial and error, settling on bw=0.2
hist(pi2000, 10, prob=T)
lines(density(pi2000, bw=0.2), col='blue')


#Exercise 3.9:



#Exercise: 4.1
#  1. create separate tables for Q1 and Q2 

tmp <- read.table(textConnection("1 3 5 1
2 3 2 3
3 3 5 1
4 4 5 1
5 3 2 1
6 4 2 3
7 3 5 1
8 4 5 1
9 3 4 1
10 4 2 1"))

tmp <- t(tmp[-1])
rownames(tmp) <- c('Q1', 'Q2', 'Q3')

#  table for Q1
q1 <- factor(rep('Q1', 10))
r1 <- factor(tmp[1,], levels=c(1,2,3,4,5))
table.q1 <- table(q1, r1)
q1
barplot(table.q1, 
        main="4.1 - Rankings for Q1",
        xlab="Rankings",
        col='darkblue', 
        legend.text=T)
dev.off()

#  table for Q2
q2 <- factor(rep('Q2', 10))
r2 <- factor(tmp[2,], levels=c(1,2,3,4,5))
table.q2 <- table(q2, r2)

barplot(table.q2, 
        main="4.1 - Rankings for Q2",
        xlab="Rankings",
        col='red', 
        legend.text=T)
dev.off()

#  2. create a contigency table
q1_2 <- factor(rep(c('Q1', 'Q2'), each=10))
r1_2 <- factor(append(tmp[1,], tmp[2,]), levels=c(1,2,3,4,5))
table(q1_2, r1_2)

#  3. stacked table of Q2 and Q3

q2_3 <- factor(rep(c('Q2', 'Q3'), each=10))
r2_3 <- factor(append(tmp[2,], tmp[3,]), levels=c(1,2,3,4,5))
table.q2_3 = table(q2_3, r2_3)
barplot(table.q2_3, 
        main="4.1 - Q2 vs Q3",
        xlab="Rankings",
        col=c('red', 'darkgreen'),
        legend=T)
dev.off()

#  4. all Q's, side-by-side

q.all <- factor(rep(c('Q1', 'Q2', 'Q3'), each=10))
r.all <- factor(append(append(tmp[1,], tmp[2,]), tmp[3,]), levels=c(1,2,3,4,5))
table.all <- table(q.all, r.all)
barplot(table.all, 
        main="4.1 - All Q's, Side-by-side",
        xlab="Rankings",
        col=c('darkblue', 'red', 'darkgreen'),
        legend=T,
        beside=T)
dev.off()
---------------------------------------------------------------------------------------------------------
  #Exercise: 4.2
  library(MASS)
data(package='MASS')
attach(UScereal)
summary(UScereal)
# mfr       calories        protein             fat            sodium     
# G:22   Min.   : 50.0   Min.   : 0.7519   Min.   :0.000   Min.   :  0.0  
# K:21   1st Qu.:110.0   1st Qu.: 2.0000   1st Qu.:0.000   1st Qu.:180.0  
# N: 3   Median :134.3   Median : 3.0000   Median :1.000   Median :232.0  
# P: 9   Mean   :149.4   Mean   : 3.6837   Mean   :1.423   Mean   :237.8  
# Q: 5   3rd Qu.:179.1   3rd Qu.: 4.4776   3rd Qu.:2.000   3rd Qu.:290.0  
# R: 5   Max.   :440.0   Max.   :12.1212   Max.   :9.091   Max.   :787.9  
#
# fibre            carbo           sugars          shelf      
# Min.   : 0.000   Min.   :10.53   Min.   : 0.00   Min.   :1.000  
# 1st Qu.: 0.000   1st Qu.:15.00   1st Qu.: 4.00   1st Qu.:1.000  
# Median : 2.000   Median :18.67   Median :12.00   Median :2.000  
# Mean   : 3.871   Mean   :19.97   Mean   :10.05   Mean   :2.169  
# 3rd Qu.: 4.478   3rd Qu.:22.39   3rd Qu.:14.00   3rd Qu.:3.000  
# Max.   :30.303   Max.   :68.00   Max.   :20.90   Max.   :3.000  
#
# potassium          vitamins 
# Min.   : 15.00   100%    : 5  
# 1st Qu.: 45.00   enriched:57  
# Median : 96.59   none    : 3  
# Mean   :159.12                
# 3rd Qu.:220.00                
# Max.   :969.70

df <- UScereal

#  1. The relationship between manufacturer and shelf
#     both are CATEGORIES

barplot(table(df$shelf, df$mfr), 
        main="4.2 - Manufacturer & Shelf",
        xlab="Manufacturer",
        ylab="Shelf",
        col=rainbow(3),
        legend=T)
dev.off()

#  2. The relationship between fat and vitamins
#     fat is NUMERICAL, vitamains are CATEGORICAL

boxplot(fat ~ vitamins,
        main="4.2 - Vitamins & Fat",
        xlab="Vitamins",
        ylab="Fat")
dev.off()

#  3. the relationship between fat and shelf
#     fat is NUMERICAL, shelf if CATEGORICAL

boxplot(fat ~ shelf,
        main="4.2 - Shelf & Fat",
        xlab="Shelf",
        ylab="Fat")
dev.off()

#  4. the relationship between carbohydrates and sugars
#     both carbo and sugars are NUMERICAL, and possibly
#     with correlation?
#     plotting points and linear fit attempt to see
#     if there is a relation...

plot(carbo, sugars,
     main="4.2 - Carbo & Sugars",
     xlab="Carbo",
     ylab="Sugars")
lm <- lm(sugars ~ carbo)
abline(lm, col="red")
dev.off()

#  5. the relationship between fibre and manufacturer
#      mfr is CATEGORICAL, fibre is NUMERICAL

boxplot(fibre ~ mfr,
        main="4.2 - Mfr & Fibre",
        xlab="Mfr",
        ylab="Fibre")
dev.off()

#  6. the relationship between sodium and sugars
#     sodium and sugars are both NUMERICAL
#     plotting points and linear fit to see if there
#     is some relation

plot(sugars, sodium,
     main="4.2 - Sugars & Sodium",
     xlab="Sugars",
     ylab="Sodium")
lm <- lm(sodium ~ sugars)
abline(lm, col="red")
dev.off()

#  7. Are there other relationships you can predict and investigate?
#     a. How about plotting Sugars to Calories?

plot(sugars, calories,
     main="4.2 - Sugars & Calories",
     xlab="Sugars",
     ylab="Calories")
lm <- lm(calories ~ sugars)
abline(lm, col="red")
dev.off()

#     a. How about plotting to Carbo to Fat?

plot(carbo, fat,
     main="4.2 - Carbo & Fat",
     xlab="Carbo",
     ylab="Fat")
lm <- lm(fat ~ carbo)
abline(lm, col="red")
dev.off()

detach(UScereal)

  #Exercise:4.3
  data(package='MASS', mammals)
attach(mammals)
summary(mammals)
#      body              brain        
# Min.   :   0.005   Min.   :   0.14  
# 1st Qu.:   0.600   1st Qu.:   4.25  
# Median :   3.342   Median :  17.25  
# Mean   : 198.790   Mean   : 283.13  
# 3rd Qu.:  48.203   3rd Qu.: 166.00  
# Max.   :6654.000   Max.   :5712.00 

#  1. compare Pearson and Spearman correlation
#     ... yes, they appear to be similar...
cor(body, brain, method='pearson')
# [1] 0.9341638

cor(body, brain, method='spearman')
# [1] 0.9534986

#  2. plot 

plot(body, brain,
     main="4.3. - Body & Brain",
     xlab="body",
     ylab="brain")
lm.a <- lm(brain ~ body)
abline(lm.a, col="red")
dev.off()

summary(lm.a)
#
# Call:
# lm(formula = brain ~ body)
#
# Residuals:
#     Min      1Q  Median      3Q     Max 
# -810.07  -88.52  -79.64  -13.02 2050.33 
#
# Coefficients:
#                 Estimate Std. Error t value Pr(>|t|)    
# (Intercept) 91.00440   43.55258    2.09   0.0409 *  
# body         0.96650    0.04766   20.28   <2e-16 ***
# ---
# Signif. codes:  0 e***f 0.001 e**f 0.01 e*f 0.05 e.f 0.1 e f 1 
#
# Residual standard error: 334.7 on 60 degrees of freedom
# Multiple R-squared: 0.8727,     Adjusted R-squared: 0.8705 
# F-statistic: 411.2 on 1 and 60 DF,  p-value: < 2.2e-16 

#  3. plot with logarithms of variables

plot(log1p(body), log1p(brain),
     main="4.3 - Body & Brain, log values",
     xlab="log1p(body)",
     ylab="log1p(brain)")
lm.b <- lm(log1p(brain) ~ log1p(body))
abline(lm.b, col="red")
dev.off()

summary(lm.b)
#
# Call:
# lm(formula = log1p(brain) ~ log1p(body))
# 
# Residuals:
#      Min       1Q   Median       3Q      Max 
# -1.27379 -0.57842 -0.04617  0.40597  2.05871 
# 
# Coefficients:
#              Estimate Std. Error t value Pr(>|t|)    
# (Intercept)  1.40033    0.14208   9.856 3.69e-14 ***
# log1p(body)  0.89959    0.04578  19.652  < 2e-16 ***
# ---
# Signif. codes:  0 e***f 0.001 e**f 0.01 e*f 0.05 e.f 0.1 e f 1 
#
# Residual standard error: 0.7927 on 60 degrees of freedom
# Multiple R-squared: 0.8655,     Adjusted R-squared: 0.8633 
# F-statistic: 386.2 on 1 and 60 DF,  p-value: < 2.2e-16 

detach(mammals)
  
#Exercise: 4.4
  data(package='UsingR', homedata)
attach(homedata)

summary(homedata)
#     y1970            y2000        
# Min.   :     0   Min.   :   7400  
# 1st Qu.: 57000   1st Qu.: 161400  
# Median : 68900   Median : 251700  
# Mean   : 70821   Mean   : 268370  
# 3rd Qu.: 80500   3rd Qu.: 335600  
# Max.   :297200   Max.   :1182800

#  1. plot indicates a strong correlation 
#     linear model fits well
#     there are some outliers, but neglible
#     outliers may be luxury homes in trending 
#     neighborhoods?

plot(y1970, y2000,
     main="4.4 - Home Prices: 1970 & 2000",
     xlab="1970",
     ylab="2000")
lm.c <- lm(y2000 ~ y1970)
abline(lm.c, col="red")
dev.off()

summary(lm.c)
#
# Call:
# lm(formula = y2000 ~ y1970)
# 
# Residuals:
#     Min      1Q  Median      3Q     Max 
# -416665  -36308     809   34372  536605 
# 
# Coefficients:
#              Estimate Std. Error t value Pr(>|t|)    
# (Intercept) -1.040e+05  2.337e+03  -44.51   <2e-16 ***
# y1970        5.258e+00  3.147e-02  167.07   <2e-16 ***
# ---
# Signif. codes:  0 e***f 0.001 e**f 0.01 e*f 0.05 e.f 0.1 e f 1 
# 
# Residual standard error: 58000 on 6839 degrees of freedom
# Multiple R-squared: 0.8032,     Adjusted R-squared: 0.8032 
# F-statistic: 2.791e+04 on 1 and 6839 DF,  p-value: < 2.2e-16

#  2. predict price home selling for 75000 in 1970
b <- coef(lm.c)[[1]]
b
m <- coef(lm.c)[[2]]
m
predicted.price <- 75000*m + b
predicted.price

detach(homedata)

  #Exercise:4.5
  data(package='UsingR', 'florida')
attach(florida)

names(florida)
# [1] "County"     "GORE"       "BUSH"       "BUCHANAN"   "NADER"      "BROWN"     
# [7] "HAGELIN"    "HARRIS"     "MCREYNOLDS" "MOOREHEAD"  "PHILLIPS"   "Total"      

summary(florida)
#      County        GORE             BUSH           BUCHANAN     
# ALACHUA : 1   Min.   :   788   Min.   :  1316   Min.   :   9.0  
# BAKER   : 1   1st Qu.:  3055   1st Qu.:  4746   1st Qu.:  46.5  
# BAY     : 1   Median : 14152   Median : 20196   Median : 114.0  
# BRADFORD: 1   Mean   : 43341   Mean   : 43356   Mean   : 258.5  
# BREVARD : 1   3rd Qu.: 45974   3rd Qu.: 56542   3rd Qu.: 285.5  
# BROWARD : 1   Max.   :386518   Max.   :289456   Max.   :3407.0  
# (Other) :61                                                     
#     NADER          BROWN           HAGELIN          HARRIS      
# Min.   :  19   Min.   :   4.0   Min.   :  0.0   Min.   :   0.0  
# 1st Qu.:  95   1st Qu.:  23.5   1st Qu.:  3.0   1st Qu.:   1.0  
# Median : 562   Median : 116.0   Median : 13.0   Median :   4.0  
# Mean   :1441   Mean   : 280.7   Mean   : 34.1   Mean   : 156.3  
# 3rd Qu.:1871   3rd Qu.: 321.5   3rd Qu.: 33.5   3rd Qu.:   8.5  
# Max.   :9986   Max.   :3211.0   Max.   :444.0   Max.   :9888.0  
#                                                                      
#   MCREYNOLDS       MOOREHEAD         PHILLIPS           Total       
# Min.   :  0.00   Min.   :  0.00   Min.   :   0.00   Min.   :  2403  
# 1st Qu.:  1.00   1st Qu.:  4.00   1st Qu.:   3.00   1st Qu.:  8080  
# Median :  3.00   Median : 12.00   Median :  10.00   Median : 34941  
# Mean   : 19.03   Mean   : 27.45   Mean   :  63.82   Mean   : 88978  
# 3rd Qu.:  5.00   3rd Qu.: 32.00   3rd Qu.:  20.50   3rd Qu.:102874  
# Max.   :658.00   Max.   :167.00   Max.   :2927.00   Max.   :625269

#  1. use the simple.lm function in the UsingR package to plot
#     and locate those 2 outliers...
library(UsingR)
simple.lm(BUSH,BUCHANAN)
#
# Call:
# lm(formula = y ~ x)
#
# Coefficients:
# (Intercept)            x  
#   45.289861     0.004917  

## NOTE
#  you would have to click on the active graphics 
#  window on the 2 outlier points to obtain their
#  indices
#identify(BUSH, BUCHANAN, n=2)
# [1] 13 50

BUSH[13]
# [1] 289456

BUCHANAN[13]
# [1] 561

BUSH[50]
# [1] 152846

BUCHANAN[50]
# [1] 3407

florida[13,]
#   County   GORE   BUSH BUCHANAN NADER BROWN HAGELIN HARRIS MCREYNOLDS MOOREHEAD PHILLIPS  Total
#13   DADE 328702 289456      561  5355   759     119     88         36       124       69 625269

florida[50,]
#       County   GORE   BUSH BUCHANAN NADER BROWN HAGELIN HARRIS MCREYNOLDS MOOREHEAD PHILLIPS  Total
#50 PALM BEACH 268945 152846     3407  5564   743     143     45        302       103      188 432286

df <- florida[(County!='DADE' & County!='PALM BEACH'),]
simple.lm(df$BUSH, df$BUCHANAN, pred=BUSH[50])
#        1 
# 711.6168 
#
# ...
# Coefficients:
# (Intercept)            x  
#   38.536279     0.004404 

#  ... and even when removing these 2 outliers,
#      there doesn't seem to be appreciable difference

plot(BUSH, BUCHANAN,
     main="4.5 - Florida: Bush vs Buchanan",
     xlab="Bush",
     ylab="Buchanan")
abline(lm(BUCHANAN ~ BUSH), 
       col="red", 
       lty=1)
abline(lm(df$BUCHANAN ~ df$BUSH), 
       col="darkblue", 
       lty=2)
legend("topright", 
       c("w/ outliers", "w/o outliers"), 
       text.col=c('red', 'darkblue'), 
       col=c("red", "darkblue"), 
       lty=1:2,
       inset=0.05, 
       cex=0.8)
dev.off()

detach(florida)

  #Exercise:4.6
  data(package="UsingR", emissions)
attach(emissions)

summary(emissions)
#      GDP            perCapita          CO2        
# Min.   :  59900   Min.   : 2507   Min.   :  54.0  
# 1st Qu.: 123100   1st Qu.:13393   1st Qu.:  77.0  
# Median : 206250   Median :20993   Median : 200.0  
# Mean   : 830427   Mean   :17724   Mean   : 669.4  
# 3rd Qu.: 683500   3rd Qu.:22250   3rd Qu.: 547.5  
# Max.   :8083000   Max.   :29647   Max.   :6750.0 


plot(perCapita, CO2,
     main="4.6 - Emissions: Per-Capita vs CO2",
     xlab="perCapita",
     ylab="CO2")
abline(lm(CO2 ~ perCapita), 
       col="red", 
       lty=1)

#  1. Guess which country is the sole outlier?
#identify(perCapita, CO2, n=1)
#[1] 1

##emissions[1,]
##                  GDP perCapita  CO2
## UnitedStates 8083000     29647 6750

#  ... but even w/out this outlier, the regression line
#      doesn't much change (kind of sad, really)
abline(lm(emissions[-1]$CO2 ~ emissions[-1]$perCapita),
       col="darkblue", 
       lty=2)
legend("topleft", 
       c("w/ outlier", "w/o outlier"), 
       text.col=c('red', 'darkblue'), 
       col=c("red", "darkblue"), 
       lty=1:2,
       inset=0.05, 
       cex=0.8)
dev.off()

detach(emissions)

  #Exercise:4.7
  data(package="UsingR", babies)
attach(babies)

summary(babies)
#       id          pluralty    outcome       date        gestation          sex   
# Min.   :  15   Min.   :5   Min.   :1   Min.   :1350   Min.   :148.0   Min.   :1  
# 1st Qu.:5286   1st Qu.:5   1st Qu.:1   1st Qu.:1444   1st Qu.:272.0   1st Qu.:1  
# Median :6730   Median :5   Median :1   Median :1540   Median :280.0   Median :1  
# Mean   :6001   Mean   :5   Mean   :1   Mean   :1536   Mean   :286.9   Mean   :1  
# 3rd Qu.:7583   3rd Qu.:5   3rd Qu.:1   3rd Qu.:1627   3rd Qu.:288.0   3rd Qu.:1  
# Max.   :9263   Max.   :5   Max.   :1   Max.   :1714   Max.   :999.0   Max.   :1  
#       wt            parity            race             age              ed       
# Min.   : 55.0   Min.   : 0.000   Min.   : 0.000   Min.   :15.00   Min.   :0.000  
# 1st Qu.:108.8   1st Qu.: 0.000   1st Qu.: 0.000   1st Qu.:23.00   1st Qu.:2.000  
# Median :120.0   Median : 1.000   Median : 3.000   Median :26.00   Median :2.000  
# Mean   :119.6   Mean   : 1.932   Mean   : 3.206   Mean   :27.37   Mean   :2.922  
# 3rd Qu.:131.0   3rd Qu.: 3.000   3rd Qu.: 7.000   3rd Qu.:31.00   3rd Qu.:4.000  
# Max.   :176.0   Max.   :13.000   Max.   :99.000   Max.   :99.00   Max.   :9.000  
#       ht             wt1          drace             dage            ded       
# Min.   :53.00   Min.   : 87   Min.   : 0.000   Min.   :18.00   Min.   :0.000  
# 1st Qu.:62.00   1st Qu.:115   1st Qu.: 0.000   1st Qu.:25.00   1st Qu.:2.000  
# Median :64.00   Median :126   Median : 3.000   Median :29.00   Median :4.000  
# Mean   :64.67   Mean   :154   Mean   : 3.665   Mean   :30.74   Mean   :3.189  
# 3rd Qu.:66.00   3rd Qu.:140   3rd Qu.: 7.000   3rd Qu.:35.00   3rd Qu.:5.000  
# Max.   :99.00   Max.   :999   Max.   :99.000   Max.   :99.00   Max.   :9.000  
#      dht             dwt           marital           inc            smoke       
# Min.   :60.00   Min.   :110.0   Min.   :0.000   Min.   : 0.00   Min.   :0.0000  
# 1st Qu.:70.00   1st Qu.:165.0   1st Qu.:1.000   1st Qu.: 2.00   1st Qu.:0.0000  
# Median :73.00   Median :190.0   Median :1.000   Median : 4.00   Median :1.0000  
# Mean   :81.67   Mean   :505.4   Mean   :1.038   Mean   :13.16   Mean   :0.8681  
# 3rd Qu.:99.00   3rd Qu.:999.0   3rd Qu.:1.000   3rd Qu.: 7.00   3rd Qu.:1.0000  
# Max.   :99.00   Max.   :999.0   Max.   :5.000   Max.   :98.00   Max.   :9.0000  
#     time            number      
# Min.   : 0.000   Min.   : 0.000  
# 1st Qu.: 0.000   1st Qu.: 0.000  
# Median : 1.000   Median : 1.000  
# Mean   : 1.748   Mean   : 2.604  
# 3rd Qu.: 1.000   3rd Qu.: 3.000  
# Max.   :99.000   Max.   :98.000 

cor(age, wt1, method="pearson")
# [1] 0.06273172
cor(age, wt1, method="spearman")
# [1] 0.1453316

lm.babies <- lm(wt1 ~ age)

# ... and plot shows this lack of correlation...

plot(age, wt1,
     main="4.7 - Babies: Age vs Weight",
     xlab="Age",
     ylab="Weight")
abline(lm.babies, col="red")
dev.off()

# let's just double-check this lack of correlation

par(mfcol=c(2,1))
plot(lm.babies, which=1)
plot(lm.babies, which=2)
dev.off()

summary(lm.babies)
# Call:
# lm(formula = wt1 ~ age)
#
# Residuals:
#     Min      1Q  Median      3Q     Max 
# -118.88  -39.13  -27.57  -12.13  857.05 
#
# Coefficients:
#        Estimate Std. Error t value Pr(>|t|)    
# (Intercept) 114.6541    18.2974   6.266  5.1e-10 ***
# age           1.4366     0.6506   2.208   0.0274 *  
# ---
# Signif. codes:  0 e***f 0.001 e**f 0.01 e*f 0.05 e.f 0.1 e f 1 
#
# Residual standard error: 147.6 on 1234 degrees of freedom
# Multiple R-squared: 0.003935,   Adjusted R-squared: 0.003128 
# F-statistic: 4.875 on 1 and 1234 DF,  p-value: 0.02743

cor(ht, wt1, method="pearson")
# [1] 0.6010033
cor(ht, wt1, method="spearman")
# [1] 0.5036179

lm.babies <- lm(wt1 ~ ht)

# ... and again, plot shows lack of correlation...

plot(ht, wt1,
     main="4.7 - Babies: Height vs Weight",
     xlab="Height",
     ylab="Weight")
abline(lm.babies, col="red")
dev.off()

# double-check!

par(mfcol=c(2,1))
plot(lm.babies, which=1)
plot(lm.babies, which=2)
dev.off()

summary(lm.babies)
# Call:
# lm(formula = wt1 ~ ht)
#
# Residuals:
#     Min      1Q  Median      3Q     Max 
# -614.89  -40.28  -15.77   13.18  940.80 
#
# Coefficients:
#         Estimate Std. Error t value Pr(>|t|)    
# (Intercept) -938.4516    41.4926  -22.62   <2e-16 ***
# ht            16.8924     0.6395   26.41   <2e-16 ***
# ---
# Signif. codes:  0 e***f 0.001 e**f 0.01 e*f 0.05 e.f 0.1 e f 1 
#
# Residual standard error: 118.2 on 1234 degrees of freedom
# Multiple R-squared: 0.3612,     Adjusted R-squared: 0.3607 
#  F-statistic: 697.8 on 1 and 1234 DF,  p-value: < 2.2e-16 

detach(babies)
  
#Exercise:4.8
  attach(women)
summary(women)
#     height         weight     
# Min.   :58.0   Min.   :115.0  
# 1st Qu.:61.5   1st Qu.:124.5  
# Median :65.0   Median :135.0  
# Mean   :65.0   Mean   :136.7  
# 3rd Qu.:68.5   3rd Qu.:148.0  
# Max.   :72.0   Max.   :164.0  


plot(height, weight,
     main="4.8 - Women: Height vs Weight",
     xlab="Height",
     ylab="Weight")
abline(lm(weight ~ height), col="red")
dev.off()

detach(women)
  
#Exercise:4.9
  attach(mtcars)
summary(mtcars)
#      mpg             cyl             disp             hp       
# Min.   :10.40   Min.   :4.000   Min.   : 71.1   Min.   : 52.0  
# 1st Qu.:15.43   1st Qu.:4.000   1st Qu.:120.8   1st Qu.: 96.5  
# Median :19.20   Median :6.000   Median :196.3   Median :123.0  
# Mean   :20.09   Mean   :6.188   Mean   :230.7   Mean   :146.7  
# 3rd Qu.:22.80   3rd Qu.:8.000   3rd Qu.:326.0   3rd Qu.:180.0  
# Max.   :33.90   Max.   :8.000   Max.   :472.0   Max.   :335.0  
#     drat             wt             qsec             vs        
# Min.   :2.760   Min.   :1.513   Min.   :14.50   Min.   :0.0000  
# 1st Qu.:3.080   1st Qu.:2.581   1st Qu.:16.89   1st Qu.:0.0000  
# Median :3.695   Median :3.325   Median :17.71   Median :0.0000  
# Mean   :3.597   Mean   :3.217   Mean   :17.85   Mean   :0.4375  
# 3rd Qu.:3.920   3rd Qu.:3.610   3rd Qu.:18.90   3rd Qu.:1.0000  
# Max.   :4.930   Max.   :5.424   Max.   :22.90   Max.   :1.0000  
#       am              gear            carb      
# Min.   :0.0000   Min.   :3.000   Min.   :1.000  
# 1st Qu.:0.0000   1st Qu.:3.000   1st Qu.:2.000  
# Median :0.0000   Median :4.000   Median :2.000  
# Mean   :0.4062   Mean   :3.688   Mean   :2.812  
# 3rd Qu.:1.0000   3rd Qu.:4.000   3rd Qu.:4.000  
# Max.   :1.0000   Max.   :5.000   Max.   :8.000  

#  1. names?
names(mtcars)
# [1] "mpg"  "cyl"  "disp" "hp"   "drat" "wt"   "qsec" "vs"   "am"   "gear"
# [11] "carb"

#  2. max mpg?
max(mtcars$mpg)
# [1] 33.9

#  3. and which car is it?
mtcars[mpg==max(mpg),]
#                 mpg cyl disp hp drat    wt qsec vs am gear carb
# Toyota Corolla 33.9   4 71.1 65 4.22 1.835 19.9  1  1    4    1

#  4. list first 5 cars 
mtcars[1:5,]
#                    mpg cyl disp  hp drat    wt  qsec vs am gear carb
# Mazda RX4         21.0   6  160 110 3.90 2.620 16.46  0  1    4    4
# Mazda RX4 Wag     21.0   6  160 110 3.90 2.875 17.02  0  1    4    4
# Datsun 710        22.8   4  108  93 3.85 2.320 18.61  1  1    4    1
# Hornet 4 Drive    21.4   6  258 110 3.08 3.215 19.44  1  0    3    1
# Hornet Sportabout 18.7   8  360 175 3.15 3.440 17.02  0  0    3    2

#  5. Valiant's hp?
mtcars['Valiant',]$hp
# [1] 105

#  6. Merc 450LC?
mtcars['Merc 450SLC',]
#              mpg cyl  disp  hp drat   wt qsec vs am gear carb
# Merc 450SLC 15.2   8 275.8 180 3.07 3.78   18  0  0    3    3

#  7. cyl vs mpg?

plot(cyl, mpg,
     main="4.9 - Cars: cyl vs mpg",
     xlab="Cylinders",
     ylab="MPG")
abline(lm(mpg ~ cyl), col="red")
dev.off()

detach(mtcars)

#Exercise 4.10


#Exercise: 5.1
data(package="UsingR", emissions)
summary(emissions)
#      GDP            perCapita          CO2        
# Min.   :  59900   Min.   : 2507   Min.   :  54.0  
# 1st Qu.: 123100   1st Qu.:13393   1st Qu.:  77.0  
# Median : 206250   Median :20993   Median : 200.0  
# Mean   : 830427   Mean   :17724   Mean   : 669.4  
# 3rd Qu.: 683500   3rd Qu.:22250   3rd Qu.: 547.5  
# Max.   :8083000   Max.   :29647   Max.   :6750.0  

attach(emissions)

plot(GDP, CO2,
     main="5.1 - emissions, w/ outlier")
# guess who the single outlier is???
#identify(locator(1), n=1)
#[1] 1
dev.off()

plot(GDP[-1], CO2[-1],
     main="5.1 - emissions w/out outlier")
dev.off()
detach(emissions)

  #Exercise: 5.2
  data(package="UsingR", chips)
summary(chips)
#     wafer11          wafer12        wafer13        wafer14      
#  Min.   : 840.0   Min.   : 850   Min.   : 830   Min.   : 850.0  
#  1st Qu.: 982.5   1st Qu.: 960   1st Qu.: 970   1st Qu.: 972.5  
#  Median :1030.0   Median :1020   Median :1020   Median :1005.0  
#  Mean   :1014.7   Mean   :1009   Mean   :1014   Mean   :1010.7  
#  3rd Qu.:1050.0   3rd Qu.:1060   3rd Qu.:1060   3rd Qu.:1060.0  
#  Max.   :1120.0   Max.   :1120   Max.   :1120   Max.   :1120.0  
#     wafer21          wafer22          wafer23        wafer24    
#  Min.   : 840.0   Min.   : 900.0   Min.   : 910   Min.   : 900  
#  1st Qu.: 992.5   1st Qu.: 982.5   1st Qu.: 980   1st Qu.: 990  
#  Median :1020.0   Median :1025.0   Median :1015   Median :1020  
#  Mean   :1016.0   Mean   :1024.7   Mean   :1020   Mean   :1021  
#  3rd Qu.:1060.0   3rd Qu.:1070.0   3rd Qu.:1068   3rd Qu.:1060  
#  Max.   :1120.0   Max.   :1130.0   Max.   :1110   Max.   :1140 


boxplot(chips, main="5.2 - chips")
dev.off()

library(UsingR)

simple.densityplot(chips)
dev.off()
#  slight variations on mean, but they all seem to be similar

  #Exercise: 5.3
  data(package="UsingR", chicken)
summary(chicken)
#     Ration1         Ration2     Ration3     
#  Min.   :2.000   Min.   :3   Min.   :5.000  
#  1st Qu.:3.000   1st Qu.:4   1st Qu.:6.000  
#  Median :4.000   Median :5   Median :6.000  
#  Mean   :4.154   Mean   :5   Mean   :6.385  
#  3rd Qu.:5.000   3rd Qu.:6   3rd Qu.:7.000  
#  Max.   :7.000   Max.   :7   Max.   :8.000  


boxplot(chicken, main="5.3 - chicken")
dev.off()

  #Exercise: 5.4
  library(MASS)
data(package="UsingR", kid.weights)
summary(kid.weights)
#       age             weight           height      gender 
#  Min.   :  3.00   Min.   : 10.00   Min.   :12.00   F:129  
#  1st Qu.: 12.25   1st Qu.: 22.00   1st Qu.:28.00   M:121  
#  Median : 39.00   Median : 32.00   Median :36.00          
#  Mean   : 47.95   Mean   : 38.38   Mean   :36.52          
#  3rd Qu.: 69.75   3rd Qu.: 45.00   3rd Qu.:43.00          
#  Max.   :144.00   Max.   :150.00   Max.   :67.00 

attach(kid.weights)
age.yr = cut(age, seq(0,144,by=12), labels=0:11)


boxplot(weight ~ age.yr, main="5.4 - age vs. weights")
dev.off()
detach(kid.weights)
#  a clear upward trend in weight, with the range increasing as 
#  the child gets older

  #Exercise: 5.5
  data(package='UsingR', carbon)
summary(carbon)
#     Monoxide           Site  
#  Min.   :0.1050   Min.   :1  
#  1st Qu.:0.1087   1st Qu.:1  
#  Median :0.1170   Median :2  
#  Mean   :0.1172   Mean   :2  
#  3rd Qu.:0.1212   3rd Qu.:3  
#  Max.   :0.1420   Max.   :3  

attach(carbon)

boxplot(Monoxide ~ Site, main="5.5 - Monoxide by Site")
dev.off()
detach(carbon)

 #Exercise: 5.6
  data(package='UsingR', babies)
summary(babies)
#       id          pluralty    outcome       date        gestation          sex   
# Min.   :  15   Min.   :5   Min.   :1   Min.   :1350   Min.   :148.0   Min.   :1  
# 1st Qu.:5286   1st Qu.:5   1st Qu.:1   1st Qu.:1444   1st Qu.:272.0   1st Qu.:1  
# Median :6730   Median :5   Median :1   Median :1540   Median :280.0   Median :1  
# Mean   :6001   Mean   :5   Mean   :1   Mean   :1536   Mean   :286.9   Mean   :1  
# 3rd Qu.:7583   3rd Qu.:5   3rd Qu.:1   3rd Qu.:1627   3rd Qu.:288.0   3rd Qu.:1  
# Max.   :9263   Max.   :5   Max.   :1   Max.   :1714   Max.   :999.0   Max.   :1  
#       wt            parity            race             age              ed       
# Min.   : 55.0   Min.   : 0.000   Min.   : 0.000   Min.   :15.00   Min.   :0.000  
# 1st Qu.:108.8   1st Qu.: 0.000   1st Qu.: 0.000   1st Qu.:23.00   1st Qu.:2.000  
# Median :120.0   Median : 1.000   Median : 3.000   Median :26.00   Median :2.000  
# Mean   :119.6   Mean   : 1.932   Mean   : 3.206   Mean   :27.37   Mean   :2.922  
# 3rd Qu.:131.0   3rd Qu.: 3.000   3rd Qu.: 7.000   3rd Qu.:31.00   3rd Qu.:4.000  
# Max.   :176.0   Max.   :13.000   Max.   :99.000   Max.   :99.00   Max.   :9.000  
#       ht             wt1          drace             dage            ded       
# Min.   :53.00   Min.   : 87   Min.   : 0.000   Min.   :18.00   Min.   :0.000  
# 1st Qu.:62.00   1st Qu.:115   1st Qu.: 0.000   1st Qu.:25.00   1st Qu.:2.000  
# Median :64.00   Median :126   Median : 3.000   Median :29.00   Median :4.000  
# Mean   :64.67   Mean   :154   Mean   : 3.665   Mean   :30.74   Mean   :3.189  
# 3rd Qu.:66.00   3rd Qu.:140   3rd Qu.: 7.000   3rd Qu.:35.00   3rd Qu.:5.000  
# Max.   :99.00   Max.   :999   Max.   :99.000   Max.   :99.00   Max.   :9.000  
#      dht             dwt           marital           inc            smoke       
# Min.   :60.00   Min.   :110.0   Min.   :0.000   Min.   : 0.00   Min.   :0.0000  
# 1st Qu.:70.00   1st Qu.:165.0   1st Qu.:1.000   1st Qu.: 2.00   1st Qu.:0.0000  
# Median :73.00   Median :190.0   Median :1.000   Median : 4.00   Median :1.0000  
# Mean   :81.67   Mean   :505.4   Mean   :1.038   Mean   :13.16   Mean   :0.8681  
# 3rd Qu.:99.00   3rd Qu.:999.0   3rd Qu.:1.000   3rd Qu.: 7.00   3rd Qu.:1.0000  
# Max.   :99.00   Max.   :999.0   Max.   :5.000   Max.   :98.00   Max.   :9.0000  
#     time            number      
# Min.   : 0.000   Min.   : 0.000  
# 1st Qu.: 0.000   1st Qu.: 0.000  
# Median : 1.000   Median : 1.000  
# Mean   : 1.748   Mean   : 2.604  
# 3rd Qu.: 1.000   3rd Qu.: 3.000  
# Max.   :99.000   Max.   :98.000 

attach(babies)

pairs(babies)
dev.off()

#  ... now, looking at this pair-wise comparison, 
#      which seem to have a linear relation?

plot(parity, age, 
     main="5.6 - babies: Linear Relations?")
abline(lm(age ~ parity), col='red')
dev.off()


plot(age, dage, 
     main="5.6 - babies: Linear Relations?")
abline(lm(dage ~ age), col='red')
dev.off()

#  ... make a scatter plot of birthweight and gestation,
#      using different pch for the level of 'factor' smoke
#      (smoke is not really a factor, but numeric!!!)...
plot(wt ~ gestation, 
     main="5.6 - babies: gestation vs weight")
rect(par("usr")[1],par("usr")[3],par("usr")[2],par("usr")[4],col = "gray")
tmp = levels(factor(smoke))
points(wt ~ gestation, 
       pch=smoke, 
       col=heat.colors(n=length(tmp)))
legend(locator(1), 
       title="Factor: smoke",
       cex=0.8,
       legend=tmp, 
       pch=smoke, 
       col=heat.colors(n=length(tmp)),
       horiz=T)

dev.off()

  
  
