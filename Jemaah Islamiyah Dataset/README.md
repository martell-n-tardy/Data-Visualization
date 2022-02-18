# Jemaah Islamiyah Dataset
A case study demonstrating the use of social network analysis techniques to create a network visualization that explores the communication structure of information within the terrorists cell Jemaah Islamiyah. Jemaah Islamiyah was responsible for the Bali bombings in 2002. The recording of the interaction of the cell began following the  meeting in the Hotel Harem in Denpasar on October 6, when the group was considered to go ‘operationally covert’, and concluded when the majority of the group had left Bali before the implementation of the operation on October 11, 2002. 

## Data
The dataset used for this case study comes from the publication Koschade, Stuart (2006) A Social Network Analysis of Jemaah Islamiyah: The Applications to Counter-Terrorism and Intelligence. Studies in Conflict and Terrorism Vol. 29(6):pp. 559-575. The relationships between terrorists concern who exchanged information with whom (communications exchanges). The valued relations represent the strength of the relations between the individuals, with a score of one signifying the weakest relationship such as a single text message or a financial transaction, and five signifying the strongest relationship such as individuals who resided together, or individuals who had numerous weak contacts over the period in question.

The data is in format UCINET, CSV and is a 1-mode matrix 17 x 17 person by person, undirected and valued.

The Jemaah Islamiyah dataset can be directly accessed from the UCI Network Data Repository: Covert Networks site using https://sites.google.com/site/ucinetsoftware/datasets/covert-networks/jemaah-islamiyah-koschade?authuser=0.

## Purpose
To create a network visualization in Gephi that models the communication structure within the Jemaah Islamiyah cell and provides insight into the identifying structural features and patterns into how a terriost group such as this one communicates efficiently and securely important information within their organization.

## Visualizing Social Network 
### Fruchterman Reingold Layout
* Fruchterman Reingold layout was chosen because it gave the clearest view of all nodes within the network with no overlap. 
* Node size was increased to 15 in order to see all 17 actors within the network clearly. 
* Labeling was applied so that all actors could be identified by some sort of label or ID during the analysis process.

![](https://github.com/martell-n-tardy/Data-Visualization/blob/main/Jemaah%20Islamiyah%20Dataset/NetworkImages/JI%20Network.png)

## Visualizing Centralization
* To explore the centralization of this network the statistical computation of the average degree, average weighted degree and eigenvector centrality were executed within the Gephi software. 
* To create the final visualization for the centralization of this network I first produced the degree of centrality using the ranking of the nodes by color. The colors were selected based on visibility of range between a pale pink (low centrality score) to dark purple (high centrality score). 
* Degree centrality does not take in consideration weight, so I ran the same analysis for the eigenvector centrality using the ranking of nodes by the same color scheme again and felt I produced a more accurate depiction of the JI network.
* Since degree centrality does not take weight into account, only the count of an actor's ties, the calculation of the eigenvector centrality, which does take weight into consideration, is plotted as well for comparison. 
* In the visualizations below a color scale from lowest (pale pink) to highest (dark purple) centrality is plotted.

### Degree Centrality
![](https://github.com/martell-n-tardy/Data-Visualization/blob/main/Jemaah%20Islamiyah%20Dataset/NetworkImages/DegreeCentrality.png)

* SAMUDRA has the highest centrality (dark purple) due to the number of ties this actor has in the network. 
* Most of the ties within the JI network are between nine individuals marked in colors pink and purple: SAMUDRA (purple), IDRIS (dark pink), MUKLAS (dark pink), IMRON (bright pink), DULMATIN (bright pink), AZAHARI (bright pink), GHONI (bright pink), PATEK (bright pink) and SARIJO (bright pink) and therefore are the central actors in the JI network. 
* The weaker ties in the network are comprised of eight individuals marked in colors pink and pale pink: FERI ( pink), AMROZI (pale pink), MUBAROK (pale pink), RAUF (pale pink), HIDAYAT (pale pink), JUNAEDI (pale pink), ARNASAN (pale pink) and OCTAVIA (pale pink).
* Therefore, the observed weaker ties could be actors in the network that can be removed without causing an issue in the distribution of plans or ideas in the JI network. 
* FERI (pink) shows multiple ties to the group of key actors in bright pink, yet has the lowest score of degree centrality. 
* This could prove to mean that the removal of FERI causes no negative effect to the flow of information in the network or that FERI's purpose in the network is to have low contact with the rest of the network for a reason unknown. 

### Eigenvector Centrality 
![](https://github.com/martell-n-tardy/Data-Visualization/blob/main/Jemaah%20Islamiyah%20Dataset/NetworkImages/EigenvectorCentrality.png)

* The strongest ties (high eigenvalue centrality) in the network are still between the nine actors observed in the 'Degree Centrality' figure above. 
* Since eigenvalue centrality takes the weight of these ties into account, the strength of these ties between the nine should be explored more closely. 
* These nine key actors can now be placed into clusters or communities to see how the structure of the organization plays a role in the distribution of information throughout the network. 

## Visualizing Modularity 
![](https://github.com/martell-n-tardy/Data-Visualization/blob/main/Jemaah%20Islamiyah%20Dataset/NetworkImages/ModularityClass.png)

* The modularity of the network was 0.326 and produced three classes. 
* Class 0 (orange) comprised 29.41% of the network’s connections. 
* Class 1 (purple) comprised 41.18% of the network’s connections. 
* Class 2 (green) comprised 29.41% of the network’s connections.

### JI Network By Position
To understand the modularity visual better, the position held by each actor in the network must be presented. In the JI network there are five positions.

![](https://github.com/martell-n-tardy/Data-Visualization/blob/main/Jemaah%20Islamiyah%20Dataset/NetworkImages/NetworkPositions.png)

* The Command Team (MUKLAS, SAMUDRA and IDRIS) and AMROZI and MUBAROK from the Operation Assistants sector held strong communication ties within the network. 
* IMRON is a part of the Operation Assistants sector as well, but apparently was a strong liaison between Class 0 and Class 1 
* This is comprised of the Bomb Makers and one of the Suicide Bombers (DULMATIN, SARIJO, PATEK, GHONI, AZAHARI and FERI). 
* Class 2 comprised of Team Lima and the other Suicide Bomber (RAUF, JUNAEDI, OCTAVIA, HIDAYAT and ARNASAN). 

## Conclusions
* No Suicide Bomber shared strong communication ties with any of the Command Team. 
* It appears FERI was the main Suicide Bomber since there was direct ties with the bomb makers themselves. 
* ARNASAN appears to be more of a secondary bomber that can be used if an opportunity presented itself to the operations assistants in the field or to the Command Team member SAMUDRA. 
* SAMUDRA was the most important actor in the network, since he is the only node that shows ties between each class or cluster of nodes in the network. 
* This makes SAMUDRA the weakest actor in the network, since his removal would cause an immediate breakdown in communication between Team Lima and the Suicide Bomber ARNASAN if SAMUDRA were imprisoned or killed.

All network images used in this case study are available within the folder titled *NetworkImages* or can be accessed directly using https://github.com/martell-n-tardy/Data-Visualization/tree/main/Sawmill%20Dataset/NetworkImages.
