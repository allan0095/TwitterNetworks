- File 'climate_top_100_anon_reply_retweet.zip' is a zipped text file.
Each line contains anonymized data from a user timeline.  Each line is in the form:
[user identifier, <list of retweeted users>, <list of replied to users>]

Each user is assigned a unique number.  If the number is less than 10000 then it corresponds to a 'core' user.
A core user is one for which we have a user timeline (and so has a line in this file associated with this user).
If the number is greater or equal to 10000 then this is a 'noncore' user, i.e. a user who has been replied to, 
or retweeted by a core user.

As an illustrative example consider the following:
[10, [20,10,1020,3,11203,3],[13001,558,11882]]

This is a representation of the retweets and replies for user 10.  The order of the users in the retweets and replies is chronological.
The time data is available, but I have left it out at this stage, to keep the files smaller and clearer.  
We can see that it is possible for the same user to appear multiple times.  This could be a measure of the strength of a connection 
between two users.  The user may also retweet or reply to their own content.

The core users were selected in the following way:
1. Daily retweet frequencies containing the keyword 'climate' were aggregated for the period November 2019 to June 2020
2. The top 100 retweets (by frequency) were selected for each day
3. The users who were retweeted are the core users.
4. Not all users who formed the 'top 100 retweet' sets were captured.  Some accounts were already deleted when user timelines were collected.

- File 'climate_top_100_anon_reply_retweet_wtimes.txt.gz' contains a similar structure to above but with timestamps.

An illustrative example:

[10, [('Tue Nov 03 00:13:20 +0000 2020', 1290), ('Tue Nov 03 00:12:26 +0000 2020', 1302), ('Tue Nov 03 00:10:28 +0000 2020', 10000)]]
