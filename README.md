# Miniproject_5

You are provided with data on interactions with advertising campaigns on a platform over 6 days, as well as a table with characteristics of advertising clients (those who placed these ads).

## Tasks:

1. Examine the distribution of the number of impressions and clicks. Calculate the average number of impressions and clicks on ads for the entire period (round to the nearest whole number).
2. Create a graph showing the distribution of ad impressions over the entire period.
3. Calculate the rolling average of impressions with a window size of 2. What is the rolling average value for April 6, 2019 (round to the nearest whole number)?
4. Rolling averages are often used to detect anomalies in data. Plot the values of the arithmetic mean by day and the rolling average of the number of impressions on the same graph. On which day is the largest absolute difference observed between the arithmetic mean and the rolling average? Do not consider days where the rolling average is NaN.
5. Write a function to find the problematic ad (with the highest/lowest number of impressions) on the day with the largest absolute anomaly.
6. Now, load data about advertising clients and find the average number of days from the client's creation date to their first advertising campaign launch.
7. Calculate the conversion rate from creating an advertising client to launching the first ad within 365 days. Provide the answer in percentage format rounded to two decimal places. (Filter based on the value in the format pd.Timedelta(365, unit='d'))
8. Let's divide our clients into intervals from creation to the launch of the first ad, with each interval being 30 days. Determine how many unique clients launched their first ad within the first month of their existence (0-30 days). Use the following intervals for the pd.cut method: [0, 30, 90, 180, 365].
9. Now, display these categories with the number of unique clients in an interactive chart.

## Data Description:

[ads_data.csv] - Data on interactions with advertising campaigns

- date: Date
- time: Time
- event: Action (view/click)
- platform: Platform
- ad_id: Ad ID
- client_union_id: Advertiser's account ID
- campaign_union_id: Advertising campaign ID
- ad_cost_type: Payment type
- ad_cost: Price
- has_video: Whether there is a video
- target_audience_count: Audience size

[ads_clients_data.csv] - Characteristics of advertising clients

- date: Date
- client_union_id: Advertiser's account ID
- community_id: Community ID
- create_date: Date of client creation
