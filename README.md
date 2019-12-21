# Marketing_method_selection_using_A-B_test_python

The dataset contains the following:

Group,Day,Method,Actions,Returns,Conversion Rate

-Group: there are 1000 groups ranginf from 0-999,

-Day: the number of days on which we have run this experiment (90 days)

-Methods: A marketing method to get returns, there are two in the dataset, specifically A and B,

-Actions: The number of Actions taken to get a return,

-Returns: How many were converted after taking actions.

-Conversion Rate: Returns / Actions,


Problem Statement: In the 90 days for which we run the experiment, the goal is to optimize the returns in the said period.
The two methods A and B can be used to get returns.
We are supposed to develop a methodology that will give us highest returns, i.e it will choose the method on its ownto a single method only rather than running 2 methods for eg 

Group 0 method A gives 50 returns 
Group 0 method B gives 250 returns  after observing the data for 30 days

from that point onwards, the algorithm should do the following, 


Group 0 method B gives 200 returns 
Group 0 method B gives 200 returns for the rest of the days 


The goal is that algorithm should know on its own when to shift from one method to another based on the A/B testing in minimum number of days with greater possible returns.
