The notebooks in this folder were used to explore the data and find communities.

- 'Initial Data Exploration.ipynb' contains degree distributions of retweet/reply networks, smoothened with complementary CDF. It also includes time series plots of retweets/replies, and a time series of the unique connections that emerge in reverse chronological order. Using communities from the 'Community Detection.ipynb', time series plots are split by retweet/reply communities to whom they are retweeting/replying to in other retweet/reply communities.

- 'Community Detection.ipynb' uses the greedy modularity algorithm from NetworkX to find communities. The greatest component consisted of 4029 out of the 4079 core users and modularity optimisation was applied after loops were removed. The behaviour of loops in modularity optimisation was observed and illustrated in a simple example with two 4-vertex cliques connected by a node with a loop.
