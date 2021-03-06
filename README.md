# IDS6145(SimTech 2018) - Research Plan

> * Group Name: The Quarter Dirty Dozen
> * Group participants names: Brian Varns, Gabrielle Vasquez, Matthias Weber
> * Project Title: City-Traffic-Planning

Our project is dealing with the issue of city-planning and in special measures that can decrease the traffic in certain areas (e.g. by adding new roads). We decided to take the example of the Autobahn (A10) that is surrounding Berlin as our model. Once we create this model we want to analyze the resulting traffic data (including hotspots) to identify where traffic is at its worst. Once we determine these spots we will add additional highways to determine if this will alleviate traffic or cause additional hotspots to arise in different areas.

![Berlin Road Map](images/Berlin_road_map.png)

**Figure 1: Map of A10**

## General Introduction

Congestion on any modern highway greatly reduces our quality of life and steals our valuable free time.  There have been many proposed solutions to fix this issue, such as autonomous vehicles, connected vehicles, ramp metering, and active traffic monitoring.  (Dvosrsky, 2014)  These technologies will allow vehicles to move in a more efficient manner on roadways and move them along the most efficient path to their destination.  However, these technologies are years, if no decades away from realization and the cost of implementation would cost hundreds of millions of dollars.  Are these new technology really the solution to this issue or can some common sense could put an end to traffic congestion? 

## Problem Statement: 

A 2010 RAND study noted that traffic congestion is created by an imbalance in the supply of and demand for road space.  This, coupled with the fact that we have limited options to build ourselves new roads that bypass these issues, is creating traffic jams in large cities on a scale never seen before.  (Sorensen, et al. 2010)  Autobahns located in Germany in 2017 experienced: (Mcintosh, 2018)

+ Traffic jams increased by 4 percent in 2017 or by 723,000 more than 2016.

+ The length of the jams in 2017 totalled 1,448,000 kilometers (899,745 miles), a rise of 5 percent.

+ Road users were stuck in traffic for a total of 457,000 hours, a rise of 9 percent.

## Motivation:

Traffic congestion on the Autobahn is amongst the worst in the world.  This congestion has many issues that are similar amongst many different roadways in the world and has taken a toll on driving safety, air quality, and quality of life for its citizens. Future technologies are being created to ease this issue, but are many years away from being effectively implemented.  If a simple solution can be found, by adding key roadways, it will save countries millions of dollars and allow for further research to identify how to alleviate traffic congestion in other cities. 

## Proposed Solution:

To complete this experiment the researchers will conduct a study to identify a strategy to reduce traffic congestion that could be implemented in different cities across the world.  For the purpose of this experiment we will use the Autobahn 10 in Germany.  The researchers reviewed literature related to congestion and typical driving patterns of humans, examined existing data for traffic flow on and off of the Autobahn, and will analyze historical hotspots for traffic congestion.  With this data we will create a model of the Autobahn, of vehicles (cars), and of drivers.  Once created we will run this model to identify key hotspots on the Autobahn and develop simple bypasses for alleviating this congestion.

## Contributions:
+ Our research should present a resilient approach/guidance for city-planner to fight the common traffic problems of congestion
+ Our research will be replicable to allow large cities to analyze their traffic congestion.
+ Our code and models will be open sourced to be used by any individual or organization.

## The Model
Our created model is a good abstraction of the given problem, due to the fact that we tried to focus on the core elements “Road” and “Vehicle”. The element “Road” is consisting out of “Lanes” and several “ON/Off-sections”. Whereas the element “Vehicle”, that will interact with the previous mentioned parts, is consisting out of the elements “Car”.  The vehicle component will have the ability for freedom of movement, meaning they will have the ability to enter and exit freely to get to their destination; the "Vehicle" will operate simliarly to typical, human driving behaviors in that the "Vehicle" driving behavior will be more predictiable than humans.  This will be part of their programing and is the reason we left out “People” from the experiment.  

![Structural_Diagram](images/Structural_Diagram.PNG)

**Figure 2: Object Diagram**

![Behavioral_Diagram](/images/Behavioral_Diagram.PNG) 

**Figure 3: Behavior Diagram**

We identified these elements, due to the following requirements:
+ The simulation should mimic the traffic-situation on the A10, that is surrounding Berlin (Germany)
+ The simulation-model must pay attention to the dimension of the corresponding and used roads
+ The model should just pay attention to the major in- and outflow areas
+ The position of the in- and outflow areas should be based on their counterparts in the real world
+ The simulation must handle 2 different kind of vehicles (car and truck) 
+ The simulation must include car following behaviour
+ As a data source the simulation must use appropriate collected and realistical data
+ The simulation should show whether infrastructural improvements can significantly reduce congestions or not


## Fundamental Questions
In the first part of our project, we want to clarify if the traffic situation can be adequately mapped, including the existing restrictions on the traffic flow.  Our primary question here focuses on determining the peak traffic times and locations of congestion.  Our primary question, “Can we reduce traffic through common sense city planning”, will then be tested through our experiment.  We will do this by identifying if infrastructural measures can reduce traffic congestion (by adding one or more streets of the same type) or even eliminate them. Or whether the restrictions take place in another area and therefore other suitable measures need to be researched.

## Expected Results

For our two fundamental questions we expect for first identify traffic congestion during peak times.  We expect these conjestion areas to align with heavy traffic flow from the busiest on and off ramps identified in Figure 8.  Once identified we will attempt to allieviate this traffic through addition or subtraction of roads (on and off ramps, highways).  Below are some proposed solutions to reduced traffic congestions bz adding routes in along different parts of the A10:4

Road from North to South
![Expected 1](images/Berlin_N_S.png)

**Figure 4: Expected Results (v1)**

Road from West to East
![Expected 2](images/Berlin_W_E.png)

**Figure 5: Expected Results (v2)**

Bypass from North to South and East to West
![Expected 3](images/Berlin_BOTH.png)

**Figure 6: Expected Results (v3)**

## Research Methods

**Models

For this simulated experiment, we will be developing simulated cars and agents to mimic the common driving behaviors of everyday human, civilians. The sample size that we have implemented within the simulation was based on real and synthetic data that we have derived  from www.bast.de and http://www.autobahnatlas-online.de/A10.htm.

**Experimental Protocol 

For the purpose of this project, we will be implementing an agent-based simulation using AnyLogic to simulate our experiment. We plan on running our simulation 10 times to ensure our data accurate to the best of its capabilities. 

**Experimental Paradigm 
 
In setting up the simulation, we have ensured that the agents developed best mimicked the driving behaviors of humans by having them have the possibility of committing am rear-end accident. These agents were developed based from a comparison study conducted by McDonald, Curry,  Kandadai, Sommers, & Winston (2014). They found after looking at data comparing across ages and genders that the most common crash incident to occur among all groups were rear-ended accidents. Such accidents will be simulated into a design to mimic one of the possible ways that highway traffic could occur. 
Overall, the simulation will be developed in such a way to accurately mimic the typical behaviors we see in human driving behaviors and functions of motor vehicles.
 
## Data

The below image includes the 14 identified On/Off-sections, with the amount of vehicles per day for the road-section between these areas.  We will use this data to determine how many cars will enter and exit the points of the A10 and identify where and when traffic congestion occurs.

![Ramps Data](images/Ramps_Traffic.png)

**Figure 7: On/Off-sections**

The length of the A10 is 195 km in total and the locations for the On/Off-sections are located at the following autobahn-positions:

![Berlin_Ramps_Positions](/images/Berlin_Ramps_Positions.png)

**Figure 8: A10 Real Data**

The A10 consists of three lanes of traffic heading in both directions.  There is one exception, which is between point 9 and point 14 where the A10 offers two lanes for each direction.
 
## Results

This experiment was conducted in two phases, the first phase required us to develop a model to represent the behaviors of the A10.  The first phase was complete once we ran the simulation and collected data on where hotspots developed on the A10.  The second phase was to develop a bypass and see if this changed the behavior of the model and relieved these hotspots.  This phase was complete once we had run our simulations and gathered the data for analysis.  

**PHASE 1**

With the model of the A10 developed we needed to implement behaviors into the agents (vehicles) that would allow them to decide whether they wanted to stay on the road, or take the next off-ramp.  To do this we developed stay probabilities in each of the decision nodes, this was set to 80% meaning the cars had a 20% chance to get off the A10 at each off ramp.  We did this to ensure cars would only stay on the A10 for approximately 4-5 off ramps, an accurate behavior we gathered from our real world data, while some would stay on the A10 for no more than 8 off ramps.  It's important to note that this probability did not change for the remainder of the experiment.

Additionally, we needed to develop accurate traffic flow that would represent the A10 during morning and afternoon traffic.  To do this we utilized our real world data represented in Figure 7.  This data was then assigned to the requisite on ramp and divided by two, half the number being assigned to the two on ramps in an area.  Because this model was built to 1/10 scale we then took those numbers and multiplied them by .1, which gave us our traffic source numbers for each of the on ramps.  These values remained the same for all experiments.  

With the model completed we add a distribution map that allowed us to track how long each agent was on the A10. The purpose of this plot was to gather how long each agent stays on the A10 and to allow us to determine if the solution we developed actually helped to decrease (or possibly increase) the overall traffic times.  The last thing the researchers did to the model was an added heat map that depicted in green, yellow, orange, and red where hotspots were developing (depending on the average speed in that section).  Below is an image of the model after running and the corresponding result.

![PHASE 1](images/Denisty_v1.png)
**Figure 9: Density Map - Phase 1 (before Bypass)**

We could see that there were two primarily traffic flow issues from Phase 1.  Hotspots were occurring at intersections 10 and 13, while the rest of the A10 ran smoothly.  These are the areas of the road, right before or after the intersections, where the number of lanes are changing from 3 to 2 or 2 to 3 lanes. Each run of the simulation gave us the same results where traffic always seemed to back up at these on and off ramps (Figures 10 & 11).

![Intersection 10](images/Section10.png)

**Figure 10: Intersection 10 Hotspot**

![Intersection 13](images/Section13.png)

**Figure 11: Intersection 13 Hotspot**

Data collected from the distribution plot shows how long each of the entities stayed on the A10 during the simulation.  It is important to note that this data was collected and analyzed in Days, meaning we got very small numbers for each of the plot values, this data was then collected and analyzed by the researchers and calculated into minutes for the purpose of this paper.  Figure 12 displays an image of the distribution plot and a table of our results.

![Phase 1 Plot](images/Traffic_Distr_v1.png)

**Figure 12: Phase 1 Distribution Plot**

|         |            |   |   |   | | | |
| ------------- |:-------------:| -----:| -----:| -----:| -----:| -----:| -----:|
|Experiment|Count|Mean|Min|Max|Deviation|Mean Confidence|Sum|
|**Phase 1**|11,251|8 Min 38 Sec|6.579E-4|53 Min 17 Sec|7 Min 12 Sec|9.456E-5|63.265 Days|

**Table 1: Phase 1 Data**

Phase 1 results show that on average vehicles stayed on the A10 for a total of 8 minutes and 38 seconds, with a min so small it's hard to calculate in minutes and a max of 53 minutes and 17 seconds.  It is far to assume that vehicles who had the highest average time in the system were stuck between intersections 10 and 13 of the model.  In an attempt to fix this issue and to determine if we could get the A10 to have minimum to no traffic hotspots, we decided to develop a bypass that is located between intersection 9 and 10 and between  ran from intersection 10 to intersection 13.

**PHASE 2**

Once we determined where we were going to build our bypass we added additional code that allowed the cars to determine if they were going to take the bypass, or stay on the road.  To control this we set up three sub phases that set different probabilities that people would take the bypass or stay on the A10.  We did this to determine if the German Government could set up some sort of Quick Pass, like Florida has, to control the number of cars that can take the bypass at a given time.  This sort of control would allow them to manage traffic flow better, assuming that a bypass was beneficial to the A10.

The bypass was built using a two lane system, meaning there were two lanes going each way.  The on and off ramps were controlled through a decision node that had an assigned bypass probability.  This probability was set to "1 - bpProb" and we then created a parameter that allowed us to set a value to determine this probability.  This value indicated the probability that agents would take this bypass.  We then ran three experiments changing this value to 0.3, 0.5, and 0.7 to determine if controlling the number of vehicles on the bypass could alleviate traffic on the A10.

![Model with Bypass Code](images/Model_overview_v2.png)

**Figure 13: Model with Bypass**

**Phase 2: Sub Phase 1**

Phase 2(1) set the bypass probability to 0.3 meaning only 30% of the vehicles would choose to take the bypass.  The remaining 70% would continue on the A10 with behaviors established in Phase 1. Figure 14 displays an image of the simulation once the run was completed along with an image of the data.  

![Sub Phase 1 Model](images/Density_v2_30.png)

**Figure 14: Phase 2(1) Model**

The traffic map shows that minimal utilization of the bypass actually freed up the traffic jam from intersection 13 and allowed traffic to move at a slower pace, but not become congested where vehicles would barely move.  However, this bypass did create more traffic on intersections 2, 3, 4, 5, 7, 8, 9, 10, 11 and 14, however these were not complete traffic jams, but rather slower moving traffic.  It's important to note that no behaviors (i.e. speed limits) of the agents were changed for Phase 2 - the model and agents behaved the same.  The bypass seemed to allow the traffic to move more freely, but at a decreased speed.  

![Phase 2(1) Data](images/Traffic_Distr_v2_30.png)

**Figure 15: Phase 2(1) Distribution Plot**

|         |            |   |   |   | | | |
| ------------- |:-------------:| -----:| -----:| -----:| -----:| -----:| -----:|
|Experiment|Count|Mean|Min|Max|Deviation|Mean Confidence|Sum|
|**Phase 2(1)**|7,995|8 Min 38 Sec|6.677E-4|59 Min 2 Sec|8 Min 38 Sec|1.377E-4|49.238 Days|

**Table 2: Phase 2(1) Data**

Phase 2(1) results indicate that on average vehicles stayed on the A10 for a total of 8 minutes and 38 seconds, which was indentical to Phase 1.  Similar to Phase 1, the minimum calculatation was too small to convert into minutes, however the max is where the two experiments began to deviate.  The max of phase 2(1) was 59 minutes and 2 seconds, which was almost a six minute increase.  This can be seen in the increased mean confidence as well. This meant that the cars generally stayed longer on the A10.  This is most likely due to the slower traffic times depicted by the traffic map.  It is fair to say that this simulation created the best model that behaved like real traffic, but this issue will be addressed in the Discussion section of this paper.

**Phase 2: Sub Phase 2**

Phase 2(2) set the bypass probability to 0.5 meaning 50% of the vehicles would choose to take the bypass.  The remaining 50% would continue on the A10 with behaviors established in Phase 1.  Below is an image of the simulation once the run was completed and an image of the data.  

![Phase2(2) Data](images/Density_v2.png)

**Figure 16: Phase 2(2) Model**

The traffic map shows that increase utilization of the bypass created additional traffic between all intersections except between 3-4, 5-6, 9-10, and 11-12.  This did create traffic jams at intersections 2, 6, 10, and 13.  These areas had traffic that wouldn't move for long periods of time because of the number of vehicles that arrived at this location at any given moment.     

![Phase 2(2) Data](images/Traffic_Distr_v2.png)

**Figure 17: Phase 2(2) Data**

|         |            |   |   |   | | | |
| ------------- |:-------------:| -----:| -----:| -----:| -----:| -----:| -----:|
|Experiment|Count|Mean|Min|Max|Deviation|Mean Confidence|Sum|
|**Phase 2(2)**|7,218|8 Min 38 Sec|6.32E-4|57 Min 36 Sec|8 Min 38 Sec|1.443E-4|43.828 Days|

**Table 3: Phase 2(2) Data**

Phase 2(2) results show that on average vehicles stayed on the A10 for a total of 8 minutes and 38 seconds which was the exact same as Phase 1 and Phase 2(1).  Again, like Phase 1 and Phase 2(1) the min was so small it's hard to calculate in minutes, however the max is where the three experiments deviate.  The max of phase 2(2) was 57 minutes and 36 seconds, which was almost a four minute increase from Phase 1, but a 2 minute decrease from phase 2(1).  This can be seen in the increased mean confidence as well from Phase 1, meaning the cars generally stayed longer on the A10.  This is most likely due to the slower traffic times depicted by the traffic map, which unlike phase 2(1) was increased at many more intersections.  This increase in traffic and traffic jams, resulting in slower traffic was less efficient than Phase 1, but slightly more efficient than phase 2(1).  Unlike phase 2(1) however, the model behavior wasn't the most efficient as traffic jams created cars that bunched up far too much, this issue will be further explained in the discussion.

**Phase 2: Sub Phase 3**

Phase 2(3) set the bypass probability to 0.7 meaning 70% of the vehicles would choose to take the bypass.  The remaining 30% would continue on the A10 with behaviors established in Phase 1.  Below is an image of the simulation once the run was completed and an image of the data.  

![Phase2(3) Data](images/Density_v2_70.png)

**Figure 18: Phase 2(3) Model**

The traffic map shows that increase utilization of the bypass created additional traffic between all intersections except between 3-4, 5-6, 9-10, 11-12 and 13-14.  This was an improvement from Phase 2(2) as not as many cars decided to stay on the A10 and instead use the bypass.  However once they moved 1-2 intersections pass the bypass traffic began to slow greatly.  This caused high traffic at many of the following intersections.  Additionally, there were traffic jams created at intersections 2 and 13, which alleviated intersection 10 from Phase 1, but not intersection 13.    

![Phase 2(3) Data](images/Traffic_Distr_v2_70.png)

**Figure 19: Phase 2(3) Data**

|         |            |   |   |   | | | |
| ------------- |:-------------:| -----:| -----:| -----:| -----:| -----:| -----:|
|Experiment|Count|Mean|Min|Max|Deviation|Mean Confidence|Sum|
|**Phase 2(3)**|6,664|8 Min 38 Sec|6.683E-4|57 Min 36 Sec|8 Min 38 Sec|1.536E-4|39.494 Days|

**Table 3: Phase 2(3) Data**

Phase 2(3) results show that on average vehicles stayed on the A10 for a total of 8 minutes and 38 seconds which was identical to Phase 1 and Phase 2(1), and Phase 2(2).  Similar to Phase 1, Phase 2(1) and Phase 2(2), the minimum was too small to convert to minutes, however the max is where the three experiments deviate.  The max of phase 2(3) was 57 minutes and 36 seconds, which was almost a four minute increase from Phase 1, a 2 minute decrease from phase 2(1); these numbers did not differ from Phase 2(2).  This can be seen in the increased mean confidence as well from Phase 1. This meant that the cars were staying longer on the A10.  This is most likely due to the slower traffic times depicted by the traffic map, which unlike phase 2(1) and phase 2(2) was increased at many more intersections.  This increase in traffic and traffic jams, resulting in slower traffic was less efficient than Phase 1, slightly more efficient than phase 2(1) and very similar to phase 2(2).  Unlike phase 2(1) however, the model behavior wasn't the most efficient as traffic jams created cars that bunched up far too much, this issue will be further explained in the discussion.

**ANALYSIS**

Analysis of Phase 1 and Phase 2 runs shows that creating a bypass did not alleviate the traffic issue.  Phase 1 of the experiment had better results across the board, while generating more agents for the model to gather data on.  The primary point to analyze for the researchers was Max Time spent on the A10.  We analyzed all other data, but overall wanted to know if we could decrease traffic through a simple addition of another roadway.  By creating a bypass we simply seemed to push traffic further down the A10 and slow the rest of it down.  Because of the 4-6 minute increase in max time during all runs of phase 2 we can safely say that our hypothesis was proved incorrect.

It is important to note why the Phase 2 runs had fewer agents.  This was because of the increased traffic generated at additional roadways and intersections on our model.  If the roads were too busy the model would continue to produce agents until the on ramp was full, once it was full it would stop producing agents until a spot was freed up by a car entering the A10.  Because our bypass created additional and slower traffic at intersections this meant fewer agents to collect data on.  This will be discussed further in the discussion portion of the paper as to limiting factors of AnyLogic.

## Discussion

Our hypothesis was to test if one or multiple bypasses would be a sufficient method that can decrease traffic-jams. We conducted a series of test through methods of modeling, simulating and analyzing the traffic on the A10. Based on the statistics and density maps that we've collected during our simulation runs, we discovered that the implementation of the bypass on the A10 had a negative effect on the overall time of cars staying on the A10.

But we also discovered a number of limitations that were related to the simulation-software. The most interesting behavior we've been able to observe was that vehicles had a tenacity to collide (and stacked on top of each other) in specific regions.
We have put in the efforts to modify the affected areas to eliminate the issues of these type of collision, however, these actions tend to not affect the behavior no matter what we tried to implement/modify (elongating roads, changing the appearance of the lanes, add/remove possible movements on intersections, enable/disable stop lines etc.).

Another limitation to note was the limiting factor of the "Personal Learning Edition" of Anylogic.
We had disovered this issue when we were developing our bypass; we were adding the corresponding blocks to the traffic-process. We then relaized that AnyLogic's Personal Learning Edition limits users to 200 blocks for their process implementation. In Phase 1 we had to use 169 blocks and when we were developing Phase 2, we had reached this limit of 200 blocks. This setback forced us to leave out 1 possible route in our modeled process; this enabled us to stay below 200 blocks.

Due to this limitation it was not possible to model multiple bypasses. Therefore we focused on a single bypasss to prove our hypothesis. Also, due to this limitation, we haven't been able to analyze the impact of trucks on the overall traffic. 

Due to complications from the build of our simulation, we have come to the possibility of two reasons as to why this would occur: 1) the AnyLogic program was not built to be able to handle a simulation of this type and/or another program should be used to model this issue (or Anylogics Professional Edition) or 2) adjustments to the construction of the A10 must be made. AnyLogic is primarily a multimethod simulation modeling tool meant to model discrete, agent-based, and system dynamics. Given this, this makes AnyLogic ideal for investigating road traffic systems, which is what we were interested in. We had chosen to model and simulate our problem with the AnyLogic system because of its ability to model the characteristics of road traffic (traffic jams, cars entering and exiting from exits and roads, etc.). Working more with this system, we started seeing issues with our simulation in that we had collisions occurring in areas of the A10; cars were getting stuck on the exits. We discovered that the methods we were going about with trying to solve this issue were not working, which then leads us to believe that the AnyLogic system was not ideal for such a model. 

Note: even a smaller road-system from previous students, that was provided by Dr. Kider, showed this kind of behavior of colliding cars, when it comes to intersections.

Additional the AnyLogic Personal Learning Edition only allows users to run models for only an hour. This limited us in using real world data to accurately simulate problems that run for a minimum of 24 hours. We also assumed that the AnyLogic Personal Learning Edition lacks processing power in that it is unable to handle the amount of variables, parameters, agents, etc. that we have included within our model - is it not built for such high, processing power models that contained high values.
For example, when we tried to use the exponential-function for the arrival-rate, the source did not produced any further entities.
All these factors forced us to simplify the code or assume specific behaviors to be able to model this project.

Furthermore, we discovered that the system is also limited in creating a high amount of entities (we used 28 sources for the cars). We also observed, that the amount of cars varies. When we just changed the StayProb and/or BpProb (we didn't changed the arrival rates). We suppose, that the system was just creating an entity, if there was space on the road. Another reason for this result could be that cars were pushed into the system when calculation-power was available. With an added bypass, the road-length increased and, therefore, we expected that the road-system should be able to handle more cars. We then observed that less entities had been created.

To sum up the most interesting part of this project/problem was the research on how we could model and simulate a highway-traffic that has neither a beginning nor an end. Looking back on this, we believed it would have been best to not choose a highway with 14 on-/off-areas (by using a fictional scenario of a smaller version of the A10). A smaller highway system would have possibly allowed us to implement additional functions and to be able to observe their impact on our model and the behavior of the agents.

Overall, we learned a lot about building up a traffic-network by using Anylogic and are sure that we will be able to create a sufficient model for a smaller scenario (e.g. a standard-intersection). 

## Future Work

For future implementation, we would first of all like to run our model in the Professional Edition of AnyLogic because, as stated in the previous section, the Personal Learning Edition had a lot of limitations (e.g. code-size < 200 blocks, simulation-time < 1 hour), that forced us to simplify and assume certain characteristics of the system to be able to run our model to have relevant results. We would want to utilize the features in the AnyLogic Professional Edition, in hopes that we can run our model more realistic and to be able to observe the resulting impact of these and other possible modifications. Further, we believe that we will not be as limited in what we can do with our model and also run it for a full day versus the one hour maximum from AnyLogic's Personal Learning Edition. 

Having additional 6 months, we would also try to implement our scenario in other available simulation- or programming-languages and trying to identify the differences in their results. One of this possible simulation-language is VISSIM that is specialized in the field of traffic-simulation (In contrast to Anylogic, which is a very good all-round simulation tool that is able to solve smaller problems from different areas satisfactorily).

We would also be interested in testing a gaming engine to help visualize and simulate our model that was originally built in this experiment. We would lean towards using Unreal Engine to run/explore such a realization of our traffic-system because of their visual coding system - this system is similar to AnyLogic. 

Overall, future work should focus on finding a system that can handle the processing needs of a complex, dynamic traffic-model and look into different methods of importing real world data into this system to then replicate the environments that were are looking to solve these problems for.


## References

Dvorsky, G. (2014). Here’s how to get rid of traffic jams.  Found at: https://io9.gizmodo.com/could-new-technologies-make-traffic-jams-a-thing-of-the-1602353172

McDonald, C. C., Curry, A. E., Kandadai, V., Sommers, M. S., & Winston, F. K. (2014). Comparison of teen and adult driver crash scenarios in a nationally representative sample of serious crashes. Accident Analysis & Prevention, 72, 302-308.

Navigation und Service. (2018). Retrieved February 22, 2018, from http://www.bast.de/DE/Verkehrstechnik/Fachthemen/v2-verkehrszaehlung/Aktuell/zaehl_aktuell_node.html?cms_map=1&cms_filter=true&cms_jahr=Jawe2016&cms_land=12&cms_strTyp=&cms_str=&cms_dtvKfz=&cms_dtvSv= 

Mcintosh J. (2018).  German traffic jams piled on misery for drivers in 2017.  Found at:http://www.dw.com/en/german-traffic-jams-piled-on-misery-for-drivers-in-2017/a-42268383

Scholl, P. (2018). Autobahnatlas. Retrieved February 22, 2018, from http://www.autobahnatlas-online.de/A10.htm
Sorensen, P., Wachs, M., Daehner, E., Kofner, A., Ecola, L., Hanson, M., Yoh, A., Light, T., Griffin, J. (2010). Reducing Traffic Congestion in Los Angeles. Found at: https://www.rand.org/pubs/research_briefs/RB9385.html


