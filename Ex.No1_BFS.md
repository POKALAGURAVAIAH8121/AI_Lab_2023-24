# Ex.No: 1  Implementation of Breadth First Search 
### DATE:                                                                            
### REGISTER NUMBER : 
### AIM: 
To write a python program to implement Breadth first Search. 
### Algorithm:
1. Start the program
2. Create the graph by using adjacency list representation
3. Define a function bfs and take the set “visited” is empty and “queue” is empty
4. Search start with initial node and add the node to visited and queue.
5. For each neighbor node, check node is not in visited then add node to visited and queue list.
6.  Creating loop to print the visited node.
7.   Call the bfs function by passing arguments visited, graph and starting node.
8.   Stop the program.
### Program:
```
# Define the graph
graph = {
    '5': ['3', '7'],
    '3': ['2', '4'],
    '7': ['8'],
    '2': [],
    '4': ['8'],
    '8': []
}

# Lists to keep track of visited nodes and the queue
visited = []
queue = []

# Function to perform BFS
def bfs(visited, graph, node):
    # Mark the starting node as visited and enqueue it
    visited.append(node)
    queue.append(node)

    while queue:
        # Dequeue a node from the queue
        m = queue.pop(0)
        print(m)

        # Iterate through neighbors of the dequeued node
        for neighbour in graph[m]:
            if neighbour not in visited:
                visited.append(neighbour)
                queue.append(neighbour)

# Driver code
print("Following is the Breadth-First Search")
bfs(visited, graph, '5')
```

### Output:
<img width="813" height="235" alt="image" src="https://github.com/user-attachments/assets/455d0b04-2b05-43b4-a63a-de068ebf7298" />

### Result:
Thus the breadth first search order was found sucessfully.
