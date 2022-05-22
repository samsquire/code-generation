# code-generation
Can we generate sourcecode for algorithms automatically?

# a star algorithm

A star algorithm is kind of intelligent, it uses a cost function and a heuristic.

What is the cost function for lines of code? That get nearer to the output values?

Project the output data or desired result onto a multidimensional surface.

We move the inputs the lines of code to change the output movement.

But what of ordering of code?

One line of code changes the possibilities for the next line of code.

The neighbours of the current code are the possibilities of the current line of code.

What if the reverse mapping? From desired output to source data.

How do you move toward an answer with the intermediately generated code?

Transform the shape of the input data to the destination data

Join on all the fields of objects

Rule recognition if the pattern is the same for all joins.

If not there is some other property.

Could have a set of primitives: create new object, create recursive call, loop

Then when the structure of the input data matches output data you need to find the conditions to get to the output structure.

The distance function needs to compare the input data structure to the candidate data structure.

But without brute forcing how do you search an opportunity in depth. You need intelligence to go in a direction

I thought of an idea to use a* algorithm to "walk" toward a solution that solves a programming problem. Each neighbour can be a weighted list of programming tasks such as if statement, for each, assignment, recursive call. How do you map example data structures transformations to code that fulfils the changes to the data structure? You need a cost function that decreases when the output gets nearer to the solution. What does the cost function for code solving a problem look similar to?

If you project the desired code variables onto a multidimensional space and with a time dimension, where each variable has a assignment algebra you can imagine the input code causing movements to the output algebra for each variable 

How do you measure that a solution gets nearer to the solution when you haven't planned what you could do

It should be a multidimensional walk toward a solution that solves the programming problem.

I want to generate the btree algorithm and other algorithms with this approach

I should provide example inputs to output mappings and join the Data between the input and output and try recalculate the processing steps to go from one to the other but I am having problems deciding what the cost function looks like.

If you project the desired code variables onto a multidimensional space and with a time dimension, where each variable has a assignment algebra you can imagine the input code causing movements to the output algebra for each variable 

How do you measure that a solution gets nearer to the solution when you haven't planned what you could do

It should be a multidimensional walk toward a solution that solves the programming problem.

I want to generate the btree algorithm and other algorithms with this approach

I should provide example inputs to output mappings and join the Data between the input and output and try recalculate the processing steps to go from one to the other but I am having problems deciding what the cost function looks like.

.:en
We can scan the output structure and generate facts of each relationship of data.

We can compare where the data moved through based on a path traversal of source data to destination data. Generate a patch.

This has a pointer to this object to this piece of data.

Input data

Node1 is root

Node1 children node2

Node1 children node3

Example 1

Insert a node node4

Desired Output data

Node1 is root

Node1 children node2

Node1 children node3

Node1 children node4

Patch

Node1 inserted into node1 children

Why node1? Theorise.

Node1 is root

Run operators against node1, node4

Len(node1.children) <= Maxsize


Example 2

Node split - insert node5

Input data

Root node is node1

Node1 children node2

Node1 children node3

Node1 children node4

Desired target data

Root node is node3

Node3 children node1

Node3 children node2

Node3 children node4

Node4 children node5

This represents a node split as each node can only have 3 items inside it.

How do we learn the rule that a node can only have 3 nodes?

Insert a constant into the system of facts

MaxSize is 3
Insert operators in system
Len(node.children)
MaxSize
== Equal to
>= Greater than or equal to
<= Less than or equal to
> Greater than
< Less than

Run every permutation of each operator to decide to do patch command steps.

Patch instructions
Node1 is no longer root node
Node3 is root node
Node2 children is node1
Remove node4 from node1
Why was node4 removed from node1
Why was node4 added to node3

Theorise. What fact was true.
Compare node1 properties to node4
Eventually....
Len(node1.children) == MaxSize
Add node4 to node3
Why?
Theorise. What fact is true
Node4 >= Node3 true
Does >= hold for all examples? Or is it more complicated
Twist operation. One goes down, one goes up and going down joins one going down.
Root = A
Node1 is A
New root = B

Twist operation is -
Root = B
B.children = A


And see where the data moves. We need to generate the steps that deterministically creates the same structure with the same data in the right places.

There shall be patterns. So there is usually a property in the object that is compared against to do a btree split.

So there is at most one field or a comparison that determines the destination of the object in the btree.

I thought we can randomly generate condition statements for each input object.

Walk the patch and insert condition objects.

It's a graph transformation problem

# dueto and structure algebra idea

Match patterns in example input to output structure.

Base rules. Algebraic transformations that can be applied over input data.

Algebraic Equivalencies of triples 

Dueto means provide a reasoning why the triple matches the algebraic pattern.

One pattern can infer multiple other triples regarding the data structure 

Triples can represent most data structures.

Loops

Binary search pattern.

Input data

Node1 children node2
Node2 index 0
Node1 children node3
Node3 index 1
Node1 children node4
Node4 index 2
Node1 isSorted children
Node1 children node5
Node5 index 3

Search node1.children node3
= Node3
Due to
Node3 index 3


Binary search in one line of code

```
recursive( initialValue(node1.children, s)

÷(point=middle=m,sides=s)
value(m) == input = output
if value(m) > searchValue then s=s[0] else s=s[1]
)
```

Node.3.children 

Search node4
= Node4

Serialize python code as triples and as nested trees
Track variable mutation
Tree search
Tree transformation
Loops

Truth maintenance?

When examples exclude a search result that proves something false we need to retract the solution and algorithm fragments found


Patterns

While current != None:
  Body
  current = current.parent

Patch why due to

Patch finds loops
Nested tree patch

B tree in one line of code
```
insert t node = recursive_deepest_first(items=t.children,item=t,
lastRecursion=l)(
if len(t.children) == 0 t.activate()
location = reversed(t.children).find(item=i, item.value >= node.value)
output = insert t node
if len(t.children) > 3 {
replace(t, Node(value=t.children÷(point=middle=m) 
= m.value,children.sort(item=i,sortKey=i.value)=t) 
output = l.t }
else deepest t.children.append(node)
)
```

How do we get nearer to the output?

Each matched function should produce output that is nearer in structure
To the output.

Combine functions together arbitrarily.
Relationships of input data.

Travelling salesman problem

```
tsp cities = {
(array(name=pairs)=cities
.permutations(name=pair, 2))
.permutations(name=solution, previous=s[i][1], size=len(cities), value+=(solution[-1][1], solution[0][0]))
thread(solution, rule(index, item)=(if item[i][0]==item[i-1][1] then item[i][0] else reject, item[i][1]))
euclidean_distance(name=distance, pair[0], pair[1])
euclidean_distance(name=solution_distance, solution)
sort(name=per_order, distance, order=ascending)
sort(name=solution_order, solution_distance, order=ascending)
pairs = first(per_order, solution_order)
= pairs
}
```

# a star algorithm

```
insert index priorityQueue value = {
recursive( initialValue(priorityQueue, s)
÷(point=middle=m,sides=s)
size = len(s) if size == 0 then s.insert(value)
if index[str(value)] < index[str(m)] then s=s[0] else s=s[1]
)
}

neighbours node =
= neighbours = [(node[0] + 1, node[1]),
(node[0], node[1] + 1),
(node[0] - 1, node[1]),
(node[0], node[1] - 1),
(node[0] + 1, node[1] + 1),
(node[0] - 1, node[1] - 1),
(node[0] + 1, node[1] - 1),
(node[0] - 1, node[1] + 1)
]
path ComeFrom target = {
= path ComeFrom (ComeFrom.get(str(target)) or reject)
}

astar map start target heuristic = {
gScore = {}
fScore = {}
ComeFrom = {}
gScore[str(start)] = 0
fScore[str(start)] = heuristic(start)
OpenSet = [start]
recursive(OpenSet, item=current,
OpenSet.remove(0)
neighbours(current), item=neighbour {
euclidean_range(name=range, current, neighbour)
if str(current) == str(target) then = path ComeFrom target
tentative_gScore = gScore[str(current)] + range
if tentative_gScore < gScore[current] then {
  if neighbour not in OpenSet then insert fScore OpenSet neighbour
  ComeFrom[neighbour] = current
  gScore[str(neighbour)] = tentative_gScore
  fScore[str(neighbour)] = tentative_gScore + heuristic(neighbour) 
}
})
}
```

# how to execute this algrebralang

Parse example built in loops

Need to generate loops, and interleave them.

Need to topological sort of the variables.

Need to know where the cut points of loops where we can insert concurrent stackframes

Recursion - access to recursive stackframes. such as last

Only 

# heuristics

What does generic code look like? What's it's shape
Can we use shapes to identify heuristics of fitness of things to try before other things?
Share intermediate values try achieve a sequence.


 * Use a variable created in a loop
 * + 1 - 1 in arguments on loop.
 * 
