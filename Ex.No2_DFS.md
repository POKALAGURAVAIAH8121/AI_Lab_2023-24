# Ex.No: 2  Implementation of Depth First Search
### DATE: 26-08-2025                                                                           
### REGISTER NUMBER : 212222040114
### AIM: 
To write a python program to implement Depth first Search. 
### Algorithm:
1. Start the program
2. Create the graph by using adjacency list representation
3. Define a function dfs and take the set “visited” is empty 
4. Search start with initial node. Check the node is not visited then print the node.
5. For each neighbor node, recursively invoke the dfs search.
6. Call the dfs function by passing arguments visited, graph and starting node.
7. Stop the program.
### Program:

```
# Implementation of Depth First Search

graph = {
  '5' : ['3','7'],
  '3' : ['2', '4'],
  '7' : ['8'],
  '2' : [],
  '4' : ['8'],
  '8' : []
}

visited = set()  

def dfs(visited, graph, node):  # function for dfs 
    if node not in visited:
        print(node)
        visited.add(node)
        for neighbour in graph[node]:
            dfs(visited, graph, neighbour)

# Driver Code
print("Following is the Depth-First Search")
dfs(visited, graph, '5')

```

### Output:

<img width="390" height="203" alt="image" src="https://github.com/user-attachments/assets/7945c8b6-e37d-4ca2-816c-7fd660d778c0" />



### Result:
Thus the depth first search order was found sucessfully.
