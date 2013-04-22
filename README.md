math-genealogy-tools
=====================
A python script to collect data from the mathematics genealogy project and
generate genealogy graphs, combine graphs, etc.

## Requirements:
- pygraphviz
- Geneagrapher
- pyparsing==1.5.7
- pydot 

## Usage:
Method `graph_genealogy(name, mathid)` from `build_genealogy.py` builds a math genealogy graph for a single individual.
Input arguments are the indiviudal's name (as a string), and their Mathematics Genealogy Project id number (available at
the end of the url for their page).

Example:
```python
graph_genealogy("Tristan A. Hearn", 162833) #name, mathid
```

Method `graph_combined_genealogy(name_mathid_pairs)` from `build_genealogy.py` builds a math genealogy graph for a list
of individuals, then generates their combined genealogy graph.
Input argument is a list of indiviudal's name-id number pairs.

Example:
```python
graph_combined_genealogy([["Tristan A. Hearn", 162833],
                          ["Terry Tao", 43967],
                          ["David Alber", 110487]])
```
