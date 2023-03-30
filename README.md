# Multi-Source-Personalized-Page-Rank-of-Large-Graphs
This repository contains two Python scripts: mapper.py and reducer.py. The scripts implement the Personalized PageRank algorithm for a directed graph, and can be used to calculate the PageRank scores of each node in the graph for a given set of source nodes.

## Mapper.py
mapper.py reads input from standard input and outputs the adjacency list representation of the input graph. The input graph is expected to be in the following format:
`source_node\ttarget_node`
The mapper script outputs the adjacency list representation of the input graph in the following format:
`source_node\tnode1 node2 node3 ...`

## Reducer.py
reducer.py reads the adjacency list representation of the input graph produced by mapper.py, and calculates the PageRank scores of each node in the graph for a given set of source nodes. The output of the reducer script is the PageRank scores of each node in the graph, along with the source nodes used to calculate the scores.

The reducer script uses the Personalized PageRank algorithm, which is a variation of the classic PageRank algorithm that takes into account a set of source nodes that are of particular interest to the user.

The input to the reducer script is the adjacency list representation of the input graph in the following format:
`source_node\tnode1 node2 node3 ...`

The output of the reducer script is in the following format:
`source_node\tnode\tpagerank_score`

## How to run the code
 
 Use the following command to run the code:
 `cat input.txt | python mapper.py | sort | python reducer.py > output.txt`
