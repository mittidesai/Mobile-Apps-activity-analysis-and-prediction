Step 1:

Exploratory Analysis

Loaded the data into a pandas data frame to remove anomalies and fill missing values.

Saved the clean data into a .csv file

Step 2:

Loaded the clean data into a PostgreSQL database.

Used windowing function to create sessions out of activities.

Exported the Sessionized data into a .csv file.

Step 3:

Loaded the Sessionized data into a pandas data frame to conduct further analysis.


Below are my findings:


Question 1: (Sessions)

(Please refer Sessionized Acitivity Analysis Python Notebook)

1. Sessionized the activities for every child doing the activities within a period of 30 minutes using the window function in SQL.

2. Average number of activities per session for every child is 6.

3. Average number of unique games per user per session is 1-2(1.5).


Question 2: (Retention)

(Please refer Retention Analysis Python Notebook)

1. General analogy for the trend of duration for all users is they start at a lower pace experience an high in their playing duration and again come to a low.

2. Average lifetime of a user is 58 days i.e. approximately 2 months.

3. On an average a user plays 1-2 games per session.

4. Every child spends more time playing other games than the one he started with in that session. (The other games may contain the same game the child started as his first game in the same session but reopening it after playing another game).


Question 3: (Modeling)

(Please refer Fitting a Model Python Notebook)

1. Yes, a Logistic Regression model with the independent variable X as childid and dependent variable as weeknumber can be used to predict in which the next activity shall take place. Using which we can get all the predicted childid’s of users whose next predicted date is in the coming week for 7 days, next 2 weeks for 15 days and 4 weeks for 30 days.

2. An alternative theory is to create a time-series analysis model using the childid as the independent variable and dayofweek as the dependent variable using which we can figure out which days of the day the particular child is most likely to perform another activity.


Question 4: (Interesting Insights)

(Please refer Interesting Insights Python Notebook )

1. For a particular child the duration for the initial sessions is longer than the later sessions. Hence time spent on a game by a child decreases eventually

2. Monster Rhymes has the maximum number of sessions whereas Letter Lullaby has 0-3 sessions(Not played at all)

3. Plotting the createdat and childid’s it is obvious that the childid increases chronoligically for every new user.

4. As the childid is on the lower range for Farming and Monster Rhymes they seem to be games played by older users and Jiggity Jamble and Letter Fishing are newer games being used by newer users.

5. Equal distribution of new users by gender.

6. Females tend to play for a longer duration compared to Males.

7. Males tend to play more often but for a lesser duration as they have significantly more count of sessions.

8. Lagoon is the game played for the maximum duration and as previously explained Females tend to play it for a longer duration compared to Males.

9. Also, Females play Farming for a much longer duration as compared to Males.

10. In general Males tend to have more sessions and Monter Rhymes seems to be a very popular game amongst them.

11. On the contrary to previously discussed Males open Farming more often compared to Females but end up closing it right away.

12. Girls of comparatively higher age play our games compared to boys.

13. Farming and Space Cows are played for maximum sessions on iOS platform.

14. Letter Lullaby is played only on Android. Space Cows is played by more children on Android. Farming is not played on Android at all.

15. Jiggity Jamble and Monster Rhymes is not played on Android at all.

16. Once females start playing they play for a longer time. Males open various games multiple times and play for a shorter time.



