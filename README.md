# Multi-Trader
MQL4 program to execute and manage open trades

This Meta Trader plug-in(Expert Advisor/EA) creates a dashboard with simple buttons to easily mangage multi-trading strategy.

The strategy - When a particular direction is determined (Determining underlying trend/direction of a particular currency will not be discussed.) Between three to one trades will br opened to towards trend. While maintainning one stop out level for all trades, each trade will carry a different level of take profit and lot sizes. 

Once the trade with the shortest Take Profit is closed. The strategy requires the tradeer to manually adjust all the stop out levels to break even. Once the second take profit level is reached,  the remeaining stops will be moved to last closed trades break even point. This will continue untill all trades are closed.

The Expert Advisors main functions:

1. Easily open multiple trades with one click with default parameters(configured at initialization) for stop,TP and lot sizes. The paramerts can be changed while running by typing in the values in the custom dashboard. No need to restrat the Exper Advisor.

2. Actively manage trades when the plug-in loaded to the client terminal. All trade details are stored in Terminal's Global Variables threfore the Expert Advisor will manage unlimited amount of trading setups across multiple currency pairs even after crash/re-start of the computer.


Minor Features:
1. Input validation - In price mode the price and lots is required to insert precisely. Therefore eleminating trader's exposure to rounding off gains/losses.  or simply the trader can resort to default values set at the initialization which is more convienient.

2. Trade pre-checks - The EA will not initiate trades if the brokers minimum distance rules are broken even by one single trade. This will ensure that the trader will not end up partially opening trades(failing to implement the trading strategy 100%).

3. Built in visual improvements - Most EAs will come with their own template files that the user is required to install and activate/deactivate manually before the EA is loaded. However Multi trader comes with built-in theme where it applies its theme/ dashboards and buttons at initialization and restore to the default state when the plugin is removed.
 
4. Cleaning obsolete Global variables - The client terminal automatically deletes global variables which are not used for 30 days. However The EA cleans obsolete global variables stored in the terminal at every de-initialization.
