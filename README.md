## EXP01-Implement-Depth-First-Search-Traversal-of-a-Graph

##AIM:
To Implement Depth First Search Traversal of a Graph using Python 

## THEORY:
Depth First Traversal (or DFS) for a graph is like Depth First Traversal of a tree. The only catch here is that, unlike trees, graphs may contain cycles (a node may be visited twice). Use a Boolean visited array to avoid processing a node more than once. A graph can have more than one DFS traversal. Depth-first search is an algorithm for traversing or searching trees or graph data structures. The algorithm starts at the root node (selecting some arbitrary node as the root node in the case of a graph) and explores as far as possible along each branch before backtracking. Step 1: Initially, stack and visited arrays are empty.

1.Queue and visited arrays are empty initially. Stack and visited arrays are empty initially.

<img width="446" alt="image" src="https://github.com/Nagadurg/19AI405FUNDAMENTALSOFARTIFICIALINTELLIGENCE/assets/94185707/11229e7a-76bd-458e-9167-a4adae173734">

Queue and visited arrays are empty initially. Stack and visited arrays are empty initially.

2. Visit 0 and put its adjacent nodes which are not visited yet into the stack.

<img width="388" alt="image" src="https://github.com/Nagadurg/19AI405FUNDAMENTALSOFARTIFICIALINTELLIGENCE/assets/94185707/794946af-f724-4eb5-a584-6490ca536a62">

Visit node 0 and put its adjacent nodes (1, 2, 3) into the stack Visit node 0 and put its adjacent nodes (1, 2, 3) into the stack

3.Now, Node 1 at the top of the stack, so visit node 1 and pop it from the stack and put all of its adjacent nodes which are not visited in the stack.

<img width="375" alt="image" src="https://github.com/Nagadurg/19AI405FUNDAMENTALSOFARTIFICIALINTELLIGENCE/assets/94185707/5e59b046-1f76-439b-987a-f0bcb9039d35">

Visit node 1 Visit node 1

4. Now, Node 2 at the top of the stack, so visit node 2 and pop it from the stack and put all of its adjacent nodes which are not visited (i.e, 3, 4) in the stack.

<img width="455" alt="image" src="https://github.com/Nagadurg/19AI405FUNDAMENTALSOFARTIFICIALINTELLIGENCE/assets/94185707/38a9729d-a02f-4d25-bcce-d0b5c0b029ea">

Visit node 2 and put its unvisited adjacent nodes (3, 4) into the stack Visit node 2 and put its unvisited adjacent nodes (3, 4) into the stack

5. Now, Node 4 at the top of the stack, so visit node 4 and pop it from the stack and put all of its adjacent nodes which are not visited in the stack.

<img width="445" alt="image" src="https://github.com/Nagadurg/19AI405FUNDAMENTALSOFARTIFICIALINTELLIGENCE/assets/94185707/90dd8473-821f-426c-8ad1-91d6602e1542">

Visit node 4 Visit node 4

6.Now, Node 3 at the top of the stack, so visit node 3 and pop it from the stack and put all of its adjacent nodes which are not visited in the stack.

<img width="440" alt="image" src="https://github.com/Nagadurg/19AI405FUNDAMENTALSOFARTIFICIALINTELLIGENCE/assets/94185707/c5d33d87-3a02-49c2-beb0-8f69268d389f">

Now, the Stack becomes empty, which means we have visited all the nodes, and our DFS traversal ends.

## ALGORITHM:
1.Construct a Graph with Nodes and Edges

2.Depth First Search Uses Stack and Recursion

3.Insert a START node to the STACK

4.Find its Successors Or neighbors and Check whether the node is visited or not

5.If Not Visited, add it to the STACK. Else Call The Function Again Until No more nodes needs to be visited.

## PROGRAM:
```
Name: Chevula Naga urga
Regno:212221230014
```
```
#import defaultdict
from collections import defaultdict
def dfs(graph,start,visited,path):
    path.append(start)
    visited[start]=True
    for neighbour in graph[start]:
        if visited[neighbour]==False:
            dfs(graph,neighbour,visited,path)
            visited[neighbour]=True
    return path
graph=defaultdict(list)
n,e=map(int,input().split())
for i in range(e):
    u,v=map(str,input().split())
    graph[u].append(v)
    graph[v].append(u)
#print(graph)
start='A'
visited=defaultdict(bool)
path=[]
traversedpath=dfs(graph,start,visited,path)
print(traversedpath)
```
## Sample Input:
<img width="22" alt="image" src="https://github.com/Nagadurg/19AI405FUNDAMENTALSOFARTIFICIALINTELLIGENCE/assets/94185707/177c6383-dce4-4a10-9f7c-968d22a7f541">

## Sample Output:

<img width="229" alt="image" src="https://github.com/Nagadurg/19AI405FUNDAMENTALSOFARTIFICIALINTELLIGENCE/assets/94185707/73326738-2d4e-4976-97ea-9a0905f65eb1">

## RESULT:
Thus,a Graph was constructed and implementation of Depth First Search for the same graph was done successfully.












