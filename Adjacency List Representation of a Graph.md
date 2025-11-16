# Ex. No: 17E - Adjacency List Representation of a Graph

## AIM:
To write a Python program to demonstrate the **adjacency list representation** of the given graph.

---

## ALGORITHM:

**Step 1**: Start the program.

**Step 2**: Define a class `AdjNode` to create a node for each adjacent vertex:
- Store the **vertex number**.
- Store the **link to the next adjacent node**.

**Step 3**: Define a class `Graph` to create the graph using adjacency lists:
- Initialize the **number of vertices**.
- Create a **list (array)** of size `V`, where each element is initially `None`.

**Step 4**: Define a method `add_edge(src, dest)` to:
- Add `dest` to the adjacency list of `src`.
- Add `src` to the adjacency list of `dest` (for **undirected graphs**).

**Step 5**: Define a method `print_graph()` to:
- Traverse the adjacency list of each vertex.
- Print the **vertex** and its **adjacent nodes**.

**Step 6**: In the main program:
- Create a `Graph` object with `V` vertices.
- Call `add_edge()` for all desired edges.
- Call `print_graph()` to display the adjacency list.

**Step 7**: End the program.

---

## PYTHON PROGRAM

```
Name : Divyashree G
Reg No : 212223060062
Python3 program to generate a graph
# for a given fixed degrees

# A function to print the adjacency matrix.
def printMat(degseq, n):
	
	# n is number of vertices
	mat=[[0]*n for i in range (n)]
	for i in range (n):
	    for j in range(i+1,n):
	        if(degseq[i]>0 and degseq[j]>0):
	            degseq[i]-=1
	            degseq[j]-=1
	            mat[i][j]=1
	            mat[j][i]=1
	#------CODE HERE-----
	

			# For each pair of vertex decrement
			# the degree of both vertex.
				
	#------CODE HERE-----
	
	# Print the result in specified form
	print("      ", end ="")
	for i in range(n):
		print(" ", "(", i, ")", end ="")
	print()
	print()
	for i in range(n):
		print("  ", "(", i, ")", end = " ")
		for j in range(n):
			print("  ", mat[i][j], end = " ")
		print()

# Driver Code
degseq=[]
for i in range(0, 5):
    ele = int(input())
  
    degseq.append(ele)
#degseq =[v0,v1,v2,v3,v4]

n = len(degseq)
printMat(degseq, n)

```

## OUTPUT
<img width="1053" height="316" alt="image" src="https://github.com/user-attachments/assets/7d673838-3ed2-4381-9ed4-438c4649110e" />

## RESULT
Thus,a Python program to demonstrate the **adjacency list representation** of the given graph is successfully executed.
