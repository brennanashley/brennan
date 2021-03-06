---
toc: true
layout: post
description: Portfolio Project Unit 1
categories: [portfolio, sports]
title: College Predicted Successful NBA Career
---
# Relationship Between Attending a Power 6 Conference for Basketball and Having a Successful NBA Career

---

## The Intro

Have you ever wondered what are the odds that a player from a small college will have a successful professional career? Well, I have. So I tried to determine if attending a Power Six Conference for college basketball correlates to having a successful career in the NBA. 

Many times watching the NBA or NFL, I am surprised when the players share the name of the college they attended. I am often expecting to hear nothing but Alabama or Oklahoma for football, and only Kentucky or Duke for basketball. But often, what I hear is not what I expected. So, I wanted to test to see if there is truly a correlation to having a long, successful career and the college attended. If there is, it would make sense to me. But maybe the big school only helps you get into the professional league, and from there everyone has as good of a shot at having a long career. We shall see.

## The Background

Sam Bowie is a name you may or may not know. He was a 7’1 center at Kentucky. He was picked by the Trailblazers in the 1984 NBA draft, the second pick in the first round. He was picked BEFORE Michael Jordan. And he was one of the biggest NBA busts of all time. Tyler Hansborough was a more recent player for UNC, from 2005 to 2009. He was a star in the ACC and was the 13th pick in the 2009 draft to the Pacers. He bounced around from the Pacers to the Raptors to the Hornets for seven years with little playing time before moving to the basketball leagues in China, where he currently plays. On the other hand, the Celtics’ Larry Bird was one of the greatest players of all time, and he attended Indiana State University.

For a certain number of years attending college wasn't mandatory, and several notable players were drafted straight from high school. A few of these players include Kevin Garnett (‘95), Kobe Bryant (‘96), and LeBron James (‘03). In 2005 the rules of the league were updated, and to be eligible for the draft one had to be 19 years old. So since then, and before 1995, every player had at least attended some college. It is likely that any player good enough to be drafted from high school would have attended a major conference. However, since we are only looking at the relationship between conference attended and lasting NBA career, this will not affect our data, as players that had no college experience were dropped from the list.

For college basketball, the top conferences are known as the Power 6 Conferences. These conferences are the Big Ten, Big East, Big 12, ACC, SEC, and the Pac-12. We'll see if attending one of these conferences correlates to a successful career.


## The Data

The dataset used was found on Kaggle, published by Omri Goldstein. The data on this file was scraped from basketball-reference.com. The dataset contains aggregate individual statistics in the NBA since 1950, 67 seasons, from basic box-score attributes such as points, assists, and rebounds to more advanced money-ball like features such as Value Over Replacement. It does not have data from seasons since 2017.

## The Statistics

For determining if there is a relationship between attending a Power 6 Conference and having a successful NBA Career, we will use a Chi-Square Test of Interdependence. The hypotheses are as follows: 
-Ho: There is no relationship between college attended and successful NBA career.
-Ha: There is a relationship between college attended and successful NBA career.

### Data Wrangling // Feature Engineering
The dataset only showed the starting and ending year for each player. From here I subtracted the two to calculate the total years played for each player. From here, I found the average NBA career length to be 4.17 years. Then I created a new "Successful Career" that includes those players that played for at least double the amount of time as an average NBA career, so at least 9 years. Roughly 20% of the players received a “Yes” for “Successful Career”, so this seemed like a fitting measure.
 
I also created a label for Power Six Conference, and I applied to each row to find who attended a qualifying school. I dropped any row with NAN for college, as we only want to compare those that went. Of the 4248 players included in the dataset that attended a college, 2179 attended a Power 6 conference, while 2069 did not. So 51% of players have attended a Power 6 conference, with 49% going to smaller conferences or Division 2.

### Statistical Methods
I used a chi square test of independence, the chi2_contingency function, to see if there was a correlation between Power 6 conference and a successful career in the NBA.

## The Results

After doing the test, the p-value is: 2.9795317795864165e-08. This is a very small p-value, so we would reject the null hypothesis and assume there is a relationship between college attended and successful NBA career. 

## The visualizations

![image](https://user-images.githubusercontent.com/76409576/109405670-9d5a4380-7938-11eb-97f0-2fb18dc489a8.png)

This barplot from Seaborn shows that the average number of years played for not attending a Power 6 is just under 4, and for attending a Power 6 is just over 4.

![image](https://user-images.githubusercontent.com/76409576/109405682-a64b1500-7938-11eb-8a66-b5206be2b62d.png)

This catplot shows different career lengths and how many players correspond. A hue was added to show the difference between conference attended. 

![image](https://user-images.githubusercontent.com/76409576/109405685-af3be680-7938-11eb-9d2d-be7e1f4a77ff.png)
This barplot shows that those that had a successful career more often attended a Power 6.

## The Conclusion

There, in fact, is a relationship between attending a Power 6 Conference for basketball and having a successful NBA career.

### Limitations
Some schools, like Gonzaga, are top programs, though they are in a smaller conference. Adam Morrison, from Gonzaga was one of the top picks in his draft year, although he did become a bust. So it's possible that we could've included these select schools that are outside of the Power 6 conferences, but are still top programs. Also, we could've dropped the years from 1995 to 2005 where attending college wasn't required to join the NBA, this could also alter our data. 

### Similar Analyses.
- need to find another similar analysis. check conferences websites perhaps..
- 
### Questions Raised.
It's possible that riding the bench at a Power 6 conference would not correlate as highly as being a starter on the team. Or, if we took out Division 2 and lower schools, would there be a difference in Power 6 Conferences to other Division 1 schools. We could break down the data further to understand these relationships. 

## The Recap

While there is no proven causation, there is a significant correlation with attending a major conference and having a long NBA career. So, I would recommend anyone interested in that to go to Duke.

# Thank You.


