**Depth First Search on Tree Structure**

This repository contains a simple implementation of a depth-first search (DFS) on a tree-like structure. The tree is composed of Node objects, where each node can have multiple children. The depthFirstSearch method traverses the tree, visiting each node in a depth-first order and returning the result in an array.

**Class Overview**

**Node**: The Node class represents a node in a tree. Each node has a name and a list of children. The class provides methods for:

-> Adding a child node.

-> Performing a depth-first search on the tree.

**Methods**

Constructor: 

Node(name) -> Creates a new Node object with the specified name and an empty list of children.

addChild(name) -> Adds a new child node with the specified name to the current node's list of children.

Returns the current node, allowing for method chaining.

depthFirstSearch(array): Traverses the tree in depth-first order, starting from the current node, and appends the name of each visited node to the provided array.
Returns the updated array with the traversal order.
Code Example

	const { Node } = require('./path-to-node-class');
	
	// Create the root node
	const root = new Node('A');
	
	// Add children to the root
	root.addChild('B').addChild('C').addChild('D');
	
	// Add children to node B
	root.children[0].addChild('E').addChild('F');
	
	// Add a child to node D
	root.children[2].addChild('G').addChild('H');
	
	// Perform Depth First Search
	const result = root.depthFirstSearch([]);
	console.log(result); // Output: ['A', 'B', 'E', 'F', 'C', 'D', 'G', 'H']
 
In this example:

The tree structure is built starting from the root node "A".

Depth-first search begins from the root and visits each child in depth-first order, returning the order in an array.

Example Tree

	        A
	      / | \
	     B  C  D
	    / \    / \
	   E   F  G   H
		
DFS Traversal Order: ['A', 'B', 'E', 'F', 'C', 'D', 'G', 'H']

**Time and Space Complexity**

Time Complexity: O(V + E), where V is the number of vertices (nodes) and E is the number of edges (connections between nodes). The method visits each node and edge once.

Space Complexity: O(V), due to the recursive call stack and the space required for the array to hold all node names.


License: This project is licensed under the MIT License - see the LICENSE file for details.
