**********************************************************************
 *  readme.txt template                                                   
 *  WordNet
**********************************************************************/

Name: Tómas Helgi Stefánsson           
Login: tomass09@ru.is  
Hópur: 2

Partner name: Sigrún Lára Sverrisdóttir      
Partner login: sigrunls14@ru.is  
Hópur: 7


/**********************************************************************
 *  Describe concisely the data structure(s) you used to store the 
 *  information in synsets.txt. Why did you make this choice?
 **********************************************************************/

We used an array. We thought it would be the simplest.


/**********************************************************************
 *  Describe concisely the data structure(s) you used to store the 
 *  information in hypernyms.txt. Why did you make this choice?
 **********************************************************************/

We used a digraph. It was recomended in the project description.

/**********************************************************************
 *  Describe concisely the algorithm you used to check if the digraph 
 *  is rooted and the algorithm you used to check if the digrah is a DAG.  
 *  What is the order of growth of the best case 
 *  running time as a function of the number of vertices V and the 
 *  number of edges E in the digraph? And what is the order of growth 
 *  of the worst case running time?
 *
 *  Be careful! It is very easy to get these wrong. Keep in mind
 *  what the 'best case' and 'worst case' entail. Don't forget about
 *  the fact that starting a breadth first search in Java means 
 *  initializing edgeTo[] arrays, etc.
 **********************************************************************/

Description:
rooted = What we did in the constructor was that we used V() to find the number of vertexes and then we used adj() in a for loop to check how many edges each vertex had. 


DAG = we used DirectedCycle(). It finds a directed cycle in a digraph and runs in O(E + V) time. The constructor takes time proportional to <em>V</em> + <em>E</em> in the worst case.


method                               best case            worst case
------------------------------------------------------------------------
rooted check http://algs4.cs.princeton.edu/42digraph/Digraph.java.html

DAG check http://algs4.cs.princeton.edu/42digraph/DirectedCycle.java.html 



/**********************************************************************
 *  Describe concisely your algorithm to compute the shortest ancestral
 *  path in SAP.java? What is the order of growth of the worst-case
 *  running time of your methods as a function of the number of
 *  vertices V and the number of edges E in the digraph? What is the
 *  order of growth of the best-case running time?
 **********************************************************************/

Description: We usedBreadthFirstDirectedPaths that returns an array of size of paths from v every other node.
Runs in O(E + V) time.


method                               best case                                    worst case
--------------------------------------------------------------------------------------------
length(int v, int w)               Smíðum alltaf tvö breadthfirstdirectpath           sama
                                   þannig að best case er 2*E+V  

ancestor(int v, int w)             Smíðum alltaf tvö breadthfirstdirectpath           sama
                                   þannig að best case er 2*E+V

length(Iterable<Integer> v,        Smíðum alltaf tvö breadthfirstdirectpath           sama
                                   þannig að best case er 2*E+V
       Iterable<Integer> w)

ancestor(Iterable<Integer> v,      Smíðum alltaf tvö breadthfirstdirectpath           sama
                                   þannig að best case er 2*E+V
         Iterable<Integer> w)




/**********************************************************************
 *  If you implemented an extra credit optimization describe it here.
 **********************************************************************/
 None that we know off.

/**********************************************************************
 *  Known bugs / limitations.
 **********************************************************************/
 None that we know off.

/**********************************************************************
 *  Describe whatever help (if any) that you received.
 *  Don't include readings, lectures, and recitation classes, but do
 *  include any help from people (including course staff, lab TAs,
 *  classmates, and friends) and attribute them by name.
 **********************************************************************/
We got help from our TA in class.

/**********************************************************************
 *  Describe any serious problems you encountered.                    
 **********************************************************************/
We initialized our digraph by the hypernym line size but should have used the synset size. So we got a offByOne and spent countless hours to find our error.

/**********************************************************************
 *  If you worked with a partner, assert below that you followed
 *  the protocol as described on the assignment page. Give one
 *  sentence explaining what each of you contributed.
 **********************************************************************/

We used pair programming so we both contributed. Also we discussed our problems and drew them on a board. 


/**********************************************************************
 *  List any other comments here. Feel free to provide any feedback   
 *  on how much you learned from doing the assignment, and whether    
 *  you enjoyed doing it.                                             
 **********************************************************************/
