# Link Prediction in Signed Networks

Information Retrieval course project done at IIT Kharagpur(Spring Semester,2017)

*Under guidance of Prof. Pawan Goyal, Prof. Animesh Mukherjee and Sandipan Sikdaar.*

Link Prediction in complex networks is a well defined and researched problem by the research community. But traditional link predictions algorithms fail in signed networks. Where +ve sign of edges might suggest friendship and -ve sign might suggest enemy relationship.

-------

### Dataset
Both the dataset are directed and signed networks.
 - Slashdot
 - Epinions

--------

### Dependency
  - NetworkX
  - iPython Notebook

---------

### Approach
  - Remove 20% edges from the original network.(This will be our ground truth while testing.ie. Test Set).
  - Treat network as undirected and unsigned at first.
  - For each pair of vertices which does not already have an edge between them compute their Resource Allocation Similarity.
  - Take top edges.
  - Give those edges to Neural Network to predict it's class.(+ve Forward, +ve Backward,-ve Forward, -ve Backward).

--------

### Features of Neural Network
  - 16 Triad Structure
  - +ve In-degree of both nodes
  - +ve Out-degree of both nodes
  - -ve In-degree of both nodes
  - -ve Outdegree of both nodes
  - Number of common neighbors

--------

### References
  - Jure Leskovec, Daniel Huttenlocher, Jon Kleinberg. “Predicting Positive and Negative Links in Online Social Networks”. http://www.cs.cornell.edu/home/kleinber/www10-signed.pdf
  - Victor Martinez, Fernando Berzal, and Juan-Carlos Cuberoa. “Survey of Link Prediction in Complex Networks”. ACM Computing Surveys (CSUR)Volume 49 Issue 4, February 2017 Article No. 69. http://dl.acm.org/citation.cfm?id=3012704
  - Aric A. Hagberg, Daniel A. Schult and Pieter J. Swart, “Exploring network structure, dynamics, and function using NetworkX”, in Proceedings of the 7th Python in Science Conference (SciPy2008), Gäel Varoquaux, Travis Vaught, and Jarrod Millman (Eds), (Pasadena, CA USA), pp. 11–15, Aug 2008 https://networkx.github.io/
  - Cytoscape: a software environment for integrated models of biomolecular interaction networks. Shannon P, Markiel A, Ozier O, Baliga NS, Wang JT, Ramage D, Amin N, Schwikowski B, Ideker T. Genome Research 2003 Nov; 13(11):2498-504
