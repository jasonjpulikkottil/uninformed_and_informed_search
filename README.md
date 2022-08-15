# Uninformed and Informed Search
<p>
	Implement a search algorithm that can find a route between any two
	<br />
	Uninformed &amp; Informed Search
	<br />
	cities. Your program will be called find_route, and will take exactly
	<br />
	commandline arguments as follows:
	<br />
	find_route input_filename origin_city
	<br />
	destination_city heuristic_filename
	<br />
	An example command line is:
	<br />
	find_route input1.txt Bremen Kassel (For doing Uninformed search)
	<br />
	or
	<br />
	find_route input1.txt Bremen Kassel h_kassel.txt (For doing Informed
	<br />
	search)
	<br />
	If heuristic is not provided then program must do uninformed search.
	<br />
	Argument input_filename is the name of a text file such as, that
	<br />
	describes road connections between cities in some part of the world.
	<br />
	For example, the road system described by file input1.txt can be
	<br />
	visualized in Figure 1 shown above. You can assume that the input
	<br />
	file is formatted in the same way as input1.txt: each line contains
	<br />
	three items. The last line contains the items "END OF INPUT", and
	<br />
	that is how the program can detect that it has reached the end of the
	<br />
	file. The other lines of the file contain, in this order, a source city, a
	<br />
	destination city, and the length in kilometers of the road connecting
	<br />
	directly those two cities. Each city name will be a single word (for
	<br />
	example, we will use New_York instead of New York), consisting of
	<br />
	upper and lowercase letters and possibly underscores.
	<br />
	IMPORTANT NOTE:
	<br />
	YOUR CODE
	<br />
	SHOULD WORK WITH ANY INPUT FILE FORMATTED AS SPECIFIED
	<br />
	ABOVE.
	<br />
	The program will compute a route between the origin city and the
	<br />
	destination city, and will print out both the length of the route and the
	<br />
	list of all cities that lie on that route. It should also display the number
	<br />
	of nodes expanded and nodes generated. For example,
	<br />
	find_route input1.txt Bremen Kassel
	<br />
	should have the following output:
	<br />
	nodes expanded: 12
	<br />
	nodes generated: 20
	<br />
	distance: 297.0 km
	<br />
	route:
	<br />
	Bremen to Hannover, 132.0 km
	<br />
	Hannover to Kassel, 165.0 km
	<br />
	and
	<br />
	find_route input1.txt London Kassel
	<br />
	should have the following output:
	<br />
	nodes expanded: 7
	<br />
	nodes generated: 7
	<br />
	distance: infinity
	<br />
	route:
	<br />
	none
	<br />
	For full credit, you should produce outputs identical in format to the
	<br />
	above two examples.
	<br />
	If a heuristic file is provided then program must perform Informed
	<br />
	search. The heuristic file gives the estimate of what the cost could
	<br />
	be to get to the given destination from any start state (note this is
	<br />
	just an estimate). In this case the command line would look like
	<br />
	find_route input1.txt Bremen Kassel h_kassel.txt
	<br />
	Here the last argument contains a text file what has the heuristic
	<br />
	values for every state wrt the given destination city (note different
	<br />
	destinations will need different heuristic values). For example, you
	<br />
	have been provided a sample file h_kassel.txt which gives the
	<br />
	heuristic value for every state (assuming kassel is the goal). Your
	<br />
	program should use this information to reduce the number of nodes
	<br />
	it ends up expanding. Other than that, the solution returned by the
	<br />
	program should be the same as the uninformed version. For
	<br />
	example,
	<br />
	find_route input1.txt Bremen Kassel h_kassel.txt
	<br />
	should have the following output:
	<br />
	nodes expanded: 3
	<br />
	nodes generated: 8
	<br />
	distance: 297.0 km
	<br />
	route:
	<br />
	Bremen to Hannover, 132.0 km
	<br />
	Hannover to Kassel, 165.0 km
</p>
