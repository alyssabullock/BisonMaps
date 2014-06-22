BisonMaps
=========

Bison Maps project (safe-anchorage-5379.herokuapp.com)

Program Phase 1:

BisonMaps.java; The main program reads in a map from a file, and continually reads in two integers from the user and print out the shortest path from the first number (s) to the second number (d). The mapData file contains all of the information for the map including the number of vertices and edges, the x and y coordinates for all of the vertices and all of the connecting edges. The inputFile contains a list of all of the buildings (first 51 points) and the name of the building in which they correspond to on the campus.

Dijkstra.java; Dijkstra’s algorithm goes through each point (starting with one of the two inputed numbers) and finds the adjacent point with the shortest distance then switches to that point and repeats the same process until connects the two inputed numbers.

EuclideanGraph.java; Creates a graph on points in the plane, the weights of the edges being the Euclidean distances.

In.java; Reads in the data.

IndexPQ.java; Keeps track a copy of the priorities in a queue.

InIterator.java; Iterates to the next element.

Point.java; Create points in the plane and determines the Euclidean distance between the point and the main point that is looking for shortest distance.

StdIn.java; Helps read in the data.

Program Phase 2:

BisonMaps.java; Gets the instance of DataConnector. The main program displays a main menu, checks the user input for valid menu options and then sends to corresponding method in DataConnector or quits the program.

DataConnector.java (singleton class); Establishes a connection to a Heroku database and queries all of the data and puts them in data structures. showBuildings, showResources, and showDepartments methods use the descriptions, layers, and departmentLocation data structures respectively to display information. getDirections and findResources methods send data structure information to Euclidean to create the graph and then go to the printPath method to display results. printPath method sends start and end points to Dijkstra getPath in order to get the shortest path in an array of steps then prints it out.

Dijkstra.java; Dijkstra’s algorithm goes through each point (starting with one of the two inputed numbers) and finds the adjacent point with the shortest distance then switches to that point and repeats the same process until connects the two inputed numbers.

EuclideanGraph.java; Creates a graph on points in the plane, the weights of the edges being the Euclidean distances.

In.java; Reads in the data.

IndexPQ.java; Keeps track a copy of the priorities in a queue.

InIterator.java; Iterates to the next element.

Point.java; Create points in the plane and determines the Euclidean distance between the point and the main point that is looking for shortest distance.

StdIn.java; Helps read in the data. (Worked perfectly before but for some reason in main menu there is a problem now with user being able to enter in another menu option. However, works perfectly fine with sub menu in findResources method.)

Program Phase 3:

BisonMapsServlet.java; Puts the database information into data structures and sends user to index.jsp.

DirectionFinderServlet.java; Supposed to get the values selected by the user and send to get the path then send path to directionsOutput.jsp. (mine just sends to directionsOutput.jsp.

ResourceFinderServlet.java; Supposed to get the values selected by the user and send to get the path then send path to resourcessOutput.jsp. (mine just sends to resourcesOutput.jsp.

index.jsp; Shows the main page and link options at the top.

directions.jsp; Gives the user the option of choosing which building to start with and which building to end with and allows them to submit it.

directionsOutput.jsp; Shows the step by step directions between the two selected points.

resources.jsp; Gives the user the option of choosing which building to start with and which resource to look for and allows them to submit it.

resourcesOutput.jsp; Shows the step by step directions between the starting point and closest point with selected resource.

showBuilding.jsp; Shows all of the buildings and their cartesian coordinates.

showResources.jsp; Shows all of the resources and which buildings have them.

showDepartments.jsp; Shows all of the departments and which building they are in.
