# Sawmill Dataset
A case study demonstrating the use of social network analysis techniques to create a network visualization that explores the communication linkages between employees in a sawmill plant that was collected as part of a sociological study (Michael and Massey, 1997). This study was initiated by the management at the sawmill plant because they were having difficulty getting the production workers to accept a new initiative.

## Data
The dataset used to demonstrate the use of social network analysis techniques in this case study is the Sawmill dataset comprised of two CSV files. The *Sawmill[Nodes].csv* file contains 2 columns (ID and Label) with 36 nodes recorded in a mixed graph type. The *Sawmill[Edges].csv* file contains 5 columns (Source, Target, Type, ID, Weight) with 62 edges recorded in a directed graph type. 

In the dataset, attributes relating to ethnicity/language and section (i.e., location) an employee works within the mill are encoded in the node labels. The label designations include: H = Hispanic; E = English; P = Planer section; M = Mill section; Y = Yard section.

The Sawmill dataset is within this repository within the folder titled *Data*, and it can be directly accessed using https://github.com/martell-n-tardy/Data-Visualization/blob/main/SuperDrugs%20Dataset/superdrugs-prescriptions.xlsx.

## Purpose
To create a network visualization in Gephi that models the communication structure within the sawmill plant and provides insight into the identifying the individual(s) who are best positioned to act as an information broker (i.e., a 'gatekeeper' or liaison) between management and the production workers to effectively help gain the acceptance for their the new initiative. 

## Initializing Social Network 
### 1. Begin by visualizing the network: Force Atlas 2 layout
Scaling set to 1000 and stronger gravity option selected
![](https://github.com/martell-n-tardy/Data-Visualization/blob/main/Sawmill%20Dataset/NetworkImages/SawmillNetwork.png)

### 2. Run network metrics
![](https://github.com/martell-n-tardy/Data-Visualization/blob/main/Sawmill%20Dataset/NetworkImages/NetworkMetrics.png)

### 3. Run modularity algorithm and color-code node attributes according to Modularity class
![](https://github.com/martell-n-tardy/Data-Visualization/blob/main/Sawmill%20Dataset/NetworkImages/ModularityAlgorithm.png)

### 4. Increase size of nodes and add labels
![](https://github.com/martell-n-tardy/Data-Visualization/blob/main/Sawmill%20Dataset/NetworkImages/LabeledNetwork.png)

## Metric Analysis 
### Question 1: What is the average degree?
**Answer:** 1.722

### Question 2: What is the network diameter?
**Answer:** 8

### Question 3: What is the Modularity value? Is this value indicative of good community structure?
**Answer:** 0.55 and Yes, because the value is greater than 0.3

### Question 4: How many classes are produced?
**Answer:** 4

### Question 5: What observations can you make on the groupings? 
**Answer:** 
* Class 0 makes up 19.44% of the network and contains all of the English-speaking employees in the Planer section and leadership (Forester, Kiln Operator, Mill Manager and Owner) within the organization. 
* Class 1 makes up 19.44% of the network as well, but contains all the employees in the Yard section and English-speaking Mill section of the organization.
* Class 2 makes up 30.56% of the network and contains only the Hispanic employees in the Planer section of the organization.
* Class 3 makes up 30.56% of the network as well and contains only the Hispanic employees in the Mill section of the organization.

### Question 6: Who has the highest betweenness score? 
**Answer:** HM-1 (Juan) at 147.0

### Question 7: What are the betweenness and closeness values of the Mill Manager? 
**Answer:** Betweenness value is 22.833333 and the closeness value is 0.8.

## Conclusion
### Observations
* In the Sawmill Corporation the communication structure has clear groupings based on the criteria of an employee being categorized as English-speaking or Non-English speaking. 
* English-speaking employees are observed to be grouped together based on the section of the organization they work within. For instance, English-speaking employees in the Mill section of the organization show stronger connections with one another (as seen in blue in the network) and weaker connections to the Hispanic employees in the Mill section (as seen in green in the network) of the organization. 
* There is a strong connection between the employees in the Yard section of the organization with the English-speaking Mill section of the organization (as seen in blue in the network).
* Within this organization management and the Planer section of the organization share strong ties and are grouped together in a class of their own (class 0, orange color). 
* There is a strong grouping of Hispanic employees by the section of the organization they worked within (see the purple and green classes in the network). 
* There appears to be connections from class 0 to others in the organization, but only to one or two people in the other class groupings. 

### Recommendations
The area of opportunity for this organization is in decreasing the multiple points of contact between management (in orange) and the other groups in the organization (blue, green and purple). To do this, group orange will need to identify a strong liaison within the network that can transcend the barrier of language and their labeled section within the organization. Looking at the visualization of the network it can be seen that: 
* HM-1 (Juan) is the only node that already shows connections to each class of the network. 
* HM-1 (Juan) has strong ties within the Mill section he belongs to and to key employees in all three of the other classes present in the network. 
* HM-1 (Juan) has the highest Betweenness Centrality by far within the network.

**As a result, I would recommend that the Sawmill plant management choose HM-1 (Juan) as the liaison between management and production workers.**

All network images used in this case study are available within the folder titled *NetworkImages* or can be accessed directly using https://github.com/martell-n-tardy/Data-Visualization/tree/main/US%20Airline%20Dataset/Dashboards
