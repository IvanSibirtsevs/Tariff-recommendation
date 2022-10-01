# Tariff recommendation

***The mobile operator Megaline found out that many customers use archival tariffs. They want to build a system that can analyze customer behavior and offer users a new tariff: "Smart" or "Ultra".
I have at my disposal data on the behavior of customers who have already switched to these tariffs. You need to build a model for the classification problem that will select the appropriate rate.
It is necessary to build a model with the highest possible accuracy value. To pass the project successfully, you need to bring the percentage of correct answers to at least 0.75.***

### Tariff Description
***Tariff "Smart"***
1. Monthly fee: 550 rubles
Included 500 minutes of talk, 50 messages and 15 GB of internet traffic
The cost of services above the tariff package:
minute of conversation: 3 rubles
message: 3 rubles
1 GB of Internet traffic: 200 rubles
***Tariff "Ultra"***
Monthly fee: 1950 rubles
Included 3000 minutes of calls, 1000 messages and 30 GB of internet traffic
The cost of services above the tariff package:
minute of conversation: 1 ruble
message: 1 ruble
1 GB of Internet traffic: 150 rubles


- Opening a data file and examining it.
- Separation of the initial data into training, validation and test sets.
- Study the quality of different models by changing the hyperparameters.
- Checking the quality of the model on a test sample.
- Checking the model for sanity


Data Description
Each object in the data set is information about the behavior of one user per month. Known:
- `calls` - number of calls,
- `minutes` — total duration of calls in minutes,
- `messages` — number of sms messages,
- `mb_used` - used Internet traffic in Mb,
- `is_ultra` - what tariff did you use during the month ("Ultra" - 1, "Smart" - 0).
