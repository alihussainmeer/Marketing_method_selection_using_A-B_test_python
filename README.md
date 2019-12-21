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


The ipynb file has been attached, the logic behind the programming has also been mentioned, 

How it works? : The first forloop gives the group number on which we are goinf to deal with, in the second
farloop we have the days so that for each day we can know how much we have got in returns for both A and B separately
so that later on we can find which one is best using the various functions which we ahve created

I have taken a minimum of 10 days to start with each group, so for each method in one group i will start with 
10 days for Action and same for Returns and evaluate their respective conversion rate which i will store in an array named meth_A and meth_B.<\br>
Similarly we have an array to store the percentage difference and p-val until atleast" 150 actions" have been taken 
by each method or it is less than that for "45 days". If any group qualifies any of them, then we choose either A or B 
based on the conditon. There was one more case wherein both A and B were 0 for 45 days so in that case we can choose any of
the method. I have taken a threshold of 20% in percentage difference and 0.05 for p-value.

At the end of the program we are generating a file which tells us which method we have chosen for which group and
what are the returns before and after.
"""
