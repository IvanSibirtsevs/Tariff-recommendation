# Tariff recommendation

***The mobile operator Megaline found out that many customers use archival tariffs. They want to build a system that can analyze customer behavior and offer users a new tariff: "Smart" or "Ultra".
I have at my disposal data on the behavior of customers who have already switched to these tariffs. You need to build a model for the classification problem that will select the appropriate rate.
It is necessary to build a model with the highest possible accuracy value. To pass the project successfully, you need to bring the percentage of correct answers to at least 0.75.***

## Tariff Description
### ***Tariff "Smart"***
1. Monthly fee: 550 rubles
2. Included 500 minutes of talk, 50 messages and 15 GB of internet traffic
3. The cost of services above the tariff package:
- minute of conversation: 3 rubles
- message: 3 rubles
- 1 GB of Internet traffic: 200 rubles
### ***Tariff "Ultra"***
1. Monthly fee: 1950 rubles
2. Included 3000 minutes of calls, 1000 messages and 30 GB of internet traffic
3. The cost of services above the tariff package:
-- minute of conversation: 1 ruble
-- message: 1 ruble
-- 1 GB of Internet traffic: 150 rubles


- Opening a data file and examining it.
- Separation of the initial data into training, validation and test sets.
- Study the quality of different models by changing the hyperparameters.
- Checking the quality of the model on a test sample.
- Checking the model for sanity


## Data Description
### Each object in the data set is information about the behavior of one user per month. Known:
- `calls` - number of calls,
- `minutes` — total duration of calls in minutes,
- `messages` — number of sms messages,
- `mb_used` - used Internet traffic in Mb,
- `is_ultra` - what tariff did you use during the month ("Ultra" - 1, "Smart" - 0).
### Users table (user information):
- `user_id` - unique user ID
- `first_name` - username
- `last_name` - user last name
- `age` — user age (years)
- `reg_date` — tariff connection date (day, month, year)
- `churn_date` — date when the tariff was terminated (if the value is omitted, then the tariff was still valid at the time of data upload)
- `city` — user's city of residence
- `tariff` — tariff plan name
### Table calls (information about calls):
- `id` — unique call number
- `call_date` — call date
- `duratio`n — call duration in minutes
- `user_id` — identifier of the user who made the call
### Messages table (message information):
- `id` — unique message number
- `message_date` — message date
- `user_id` - ID of the user who sent the message
### internet table (information about internet sessions):
- `id` — unique session number
- `mb_used` — amount of Internet traffic spent per session (in megabytes)
- `session_date` — internet session date
- `user_id` - user ID
### Tariffs table (tariff information):
- `tariff_name` — tariff name
- `rub_monthly_fee` — monthly subscription fee in rubles
- `minutes_included` - the number of minutes of conversation per month included in the subscription fee
- `messages_included` - the number of messages per month included in the subscription fee
- `mb_per_month_included` - the amount of Internet traffic included in the subscription fee (in megabytes)
- `rub_per_minute` - the cost of a minute of conversation in excess of the tariff package (for example, if the tariff includes 100 minutes of conversation per month, then - from 101 minutes a fee will be charged)
- `rub_per_message` - the cost of sending a message in excess of the tariff package
- `rub_per_gb` - the cost of an additional gigabyte of Internet traffic in excess of the tariff package (1 gigabyte = 1024 megabytes)

