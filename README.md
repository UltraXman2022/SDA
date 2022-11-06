<h1>Project description</h1>
You work as an analyst for the telecom operator Megaline. The company offers its clients two prepaid plans, Surf and Ultimate. The commercial department wants to know which of the plans brings in more revenue in order to adjust the advertising budget.<br>

You are going to carry out a preliminary analysis of the plans based on a relatively small client selection. You'll have the data on 500 Megaline clients: who the clients are, where they're from, which plan they use, and the number of calls they made and text messages they sent in 2018. Your job is to analyze clients' behavior and determine which prepaid plan brings in more revenue.

<h2>Description of the plans</h2>
Note: Megaline rounds seconds up to minutes, and megabytes to gigabytes. For calls, each individual call is rounded up: even if the call lasted just one second, it will be counted as one minute. For web traffic, individual web sessions are not rounded up. Instead, the total for the month is rounded up. If someone uses 1025 megabytes this month, they will be charged for 2 gigabytes.
<h3>Surf</h3>
<ol><li>Monthly charge: $20</li>
<li>500 monthly minutes, 50 texts, and 15 GB of data</li>
<li>After exceeding the package limits:</li></ol>
<ul><li>1 minute: 3 cents</li>
<li>1 text message: 3 cents</li>
<li>1 GB of data: $10</il></ul>
<h3>Ultimate</h3>
<ol><li>Monthly charge: $70</li>
<li>3000 monthly minutes, 1000 text messages, and 30 GB of data</il>
<li>After exceeding the package limits:</li></ol>
<ul><li>1 minute: 1 cent</li>
<li>1 text message: 1 cent</li>
<li>1 GB of data: $7</li></ul>

<h2>Instructions on completing the project</h2>
<h3>Step 1. Open the data file and study the general information</h3>
File path:
/datasets/megaline_calls.csv Download dataset
/datasets/megaline_internet.csv Download dataset
/datasets/megaline_messages.csv Download dataset
/datasets/megaline_plans.csv Download dataset
/datasets/megaline_users.csv Download dataset
<h3>Step 2. Prepare the data</h3>
<ul><li>Convert the data to the necessary types</il>
<li>Find and eliminate errors in the data</li></ul>
Explain what errors you found and how you removed them.
For each user, find:
<ul><li>The number of calls made and minutes used per month</il>
<li>The number of text messages sent per month</il>
<li>The volume of data per month</il>
<li>The monthly revenue from each user (subtract the free package limit from the total number of calls, text messages, and data; multiply the result by the calling plan value; add the monthly charge depending on the calling plan)<ul></il>
<h3>Step 3. Analyze the data</h3>
Describe the customers' behavior. Find the minutes, texts, and volume of data the users of each plan require per month. Calculate the mean, variance, and standard deviation. Plot histograms. Describe the distributions.
<h3>Step 4. Test the hypotheses</h3>
<ul><li>The average revenue from users of Ultimate and Surf calling plans differs</li>
<li>The average revenue from users in NY-NJ area is different from that of the users from other regions</li></ul>
You decide what alpha value to use
<h4>Explain:</h4>
<ul><li>How you formulated the null and alternative hypotheses</li>
<li>What criterion you used to test the hypotheses and why</li></ul>
<h3>Step 5. Write an overall conclusion</h3>
Format: Complete the task in Jupyter Notebook. Put the programming code in code cells and text explanations in markdown cells, then apply formatting and headings.
<h3>Description of the data</h3>
Remember! Megaline rounds seconds up to minutes, and megabytes to gigabytes. For calls, each individual call is rounded up: even if the call lasted just one second, it will be counted as one minute. For web traffic, individual web sessions are not rounded up. Instead, the total for the month is rounded up. If someone uses 1025 megabytes this month, they will be charged for 2 gigabytes.
<ul><li>The users table (data on users):
<li>user_id — unique user identifier
<li>first_name — user's name
<li>last_name — user's last name
<li>age — user's age (years)
<li>reg_date — subscription date (dd, mm, yy)
<li>churn_date — the date the user stopped using the service (if the value is missing, the calling plan was being used when this database was extracted)
<li>city — user's city of residence
<li>plan — calling plan name
<li>The calls table (data on calls):
<li>id — unique call identifier
<li>call_date — call date
<li>duration — call duration (in minutes)
<li>user_id — the identifier of the user making the call
<li>The messages table (data on texts):
<li>id — unique text message identifier
<li>message_date — text message date
<li>user_id — the identifier of the user sending the text
<li>The internet table (data on web sessions):
<li>id — unique session identifier
<li>mb_used — the volume of data spent during the session (in megabytes)
<li>session_date — web session date
<li>user_id — user identifier
<li>The plans table (data on the plans):
<li>plan_name — calling plan name
<li>usd_monthly_fee — monthly charge in US dollars
<li>minutes_included — monthly minute allowance
<li>messages_included — monthly text allowance
<li>mb_per_month_included — data volume allowance (in megabytes)
<li>usd_per_minute — price per minute after exceeding the package limits (e.g., if the package includes 100 minutes, the 101st minute will be charged)
<li>usd_per_message — price per text after exceeding the package limits
<li>usd_per_gb — price per extra gigabyte of data after exceeding the package limits (1 GB = 1024 megabytes)</ul></li>
