# Xplore Maps

 
Xplore Maps is a user-friendly map application designed to display essential information for various cities worldwide. Developed in C++, it fetches data from the OpenStreetMap Database API and utilizes GTK for rendering graphics.

> **Note:** This project was developed for the ECE297 course at the University of Toronto. As such, the source code is not publicly accessible.

## Main Features
- **Interactive Navigation**: Navigate and zoom using on-screen buttons.
- **City Selection**: Choose maps for different cities via a dropdown menu.
- **Detailed Map Display**: Show streets, street names, parks, rivers, lakes, buildings, and more.
- **POIs**: Display points of interest such as restauraunts, hospitals, banks and entertainment.
- **Subways**: Displays the various subway lines and the subway stations along a particular subway line for a selected city.
- **Pop-Over Info**: Click on Intersections to view detailed information such as the intersection name and points of interest nearby.
- **Search Functionality**: Use the search bar to locate intersections, points of interest and features.
- **Pathfinding**: Determine the optimal route between two intersections.
- **Navigation Instructions**: Provide step-by-step driving directions from one location to another.
- **Weather**: Displaying real-time weather information in the selected city.
- **Help Menu**: Access user assistance and guidance.

## Algorithms

### Pathfinding using A* Search Algorithm
Xplore Maps uses the A* Search algorithm to find the shortest path between intersections. By considering travel time, the algorithm employs a greedy approach, always moving to the intersection with the lowest time cost. The heuristic used is the Euclidean distance between the start and end intersections, divided by the city's maximum speed limit, favoring routes that quickly bring us closer to the destination.

### Traveling Salesman/Courier Problem - NP Hard Problem
For a set of dropoff/pickup points and start/end intersections, our algorithm seeks the optimal path that visits all specified points. As this is an NP Hard problem, our approach initially finds several "mediocre" solutions and iteratively improves them.

- **Baseline Solution**: We start at each possible depot (starting point) and use a greedy algorithm to travel to the nearest pickup or dropoff point.
- **Optimization**: From the best "baseline" solution, we incorporated different methods such as Two-opt, Multi-start, Or-opt, and simulated annealing to further optimize our solution.

## Images and Videos

### POI

![POI](https://github.com/tahakh03/ECE297-Xplore-Maps/blob/main/Images%20and%20Videos/POI.png)

### Weather

![Weather](https://github.com/tahakh03/ECE297-Xplore-Maps/blob/main/Images%20and%20Videos/Weather.png)

### Switching Between Cities


