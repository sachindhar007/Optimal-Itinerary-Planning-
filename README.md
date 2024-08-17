# Optimal Itinerary Planning for Heritage Sites using TSP

# Introduction : 
This project focuses on optimizing the travel route for visiting multiple heritage sites across India using the Traveling Salesman Problem (TSP). The goal is to determine the shortest possible path that visits each city exactly once and returns to the starting point, minimizing the overall travel distance.

# Problem Definition : 
The project involved solving a TSP for 15 heritage sites spread across different regions of India. The challenge was to find the optimal sequence of visiting these sites such that the total travel distance is minimized. We utilized Python, specifically Pyomo and the CBC solver, to model and solve this optimization problem.

# Data Preparation and Preprocessing :
I began by reading a dataset containing the names of 15 cities representing heritage sites. Using the Geopy library, we obtained the latitude and longitude of each city, enabling us to compute the pairwise distances between all cities using the Haversine formula, which accurately calculates distances between geographic coordinates on a sphere.

# Key Libraries Used:
    Geopy for obtaining city coordinates (latitude and longitude).
    Haversine formula for distance calculations.
    Pyomo for mathematical modeling and solving the TSP.
    Folium for visualizing the optimal travel route on an interactive map.

# Model Formulation : 
We formulated the problem as a mixed-integer linear programming (MILP) model using Pyomo. The model included binary decision variables to represent the connections between cities and an objective function to minimize the total travel distance. The CBC solver was then used to find the optimal solution.
    Key components of the model:
    Decision Variables: Binary variables indicating whether a direct path between two cities is part of the solution.
    Objective Function: Minimize the total travel distance by summing the distances between connected cities.
    Constraints: Ensure that each city is visited exactly once and that there are no sub-tours (smaller cycles within the solution).

# Solution and Visualization : 
The optimal route was identified by solving the TSP model. The final solution provided the sequence in which the cities should be visited to achieve the minimum travel distance of 5643.5 km.
To visualize the results, we mapped the optimal route using Folium, highlighting the travel path between the heritage sites. The interactive map allowed us to analyze the route and better understand the solution

# Technical Approach Summary : 
Geopy was used to fetch coordinates for the cities.
Haversine formula was applied to calculate pairwise distances between cities.
Pyomo and CBC solver were employed to model and solve the TSP, determining the optimal travel sequence.
Folium was utilized to visualize the optimized route, providing an interactive map for better analysis.

# Results and Key Insights : 
The project successfully optimized the travel route for the 15 heritage sites, achieving a total distance of 5643.5 km. The visualization provided by Folium further enhanced the interpretability of the results, allowing for a clear representation of the optimal path.

# Conclusion : 
This project demonstrated the effectiveness of combining mathematical modeling, geographic data analysis, and visualization techniques in solving routing problems. The application of the TSP to itinerary planning showcases the potential for optimizing real-world travel and logistics scenarios.

