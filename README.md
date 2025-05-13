# cs29003-lab-7-disoint-set-union-solved
**TO GET THIS SOLUTION VISIT:** [CS29003 Lab 7-Disoint Set Union Solved](https://www.ankitcodinghub.com/product/cs29003-lab-7-disoint-set-union-solved/)


---

📩 **If you need this solution or have special requests:** **Email:** ankitcoding@gmail.com  
📱 **WhatsApp:** +1 419 877 7882  
📄 **Get a quote instantly using this form:** [Ask Homework Questions](https://www.ankitcodinghub.com/services/ask-homework-questions/)

*We deliver fast, professional, and affordable academic help.*

---

<h2>Description</h2>



<div class="kk-star-ratings kksr-auto kksr-align-center kksr-valign-top" data-payload="{&quot;align&quot;:&quot;center&quot;,&quot;id&quot;:&quot;92890&quot;,&quot;slug&quot;:&quot;default&quot;,&quot;valign&quot;:&quot;top&quot;,&quot;ignore&quot;:&quot;&quot;,&quot;reference&quot;:&quot;auto&quot;,&quot;class&quot;:&quot;&quot;,&quot;count&quot;:&quot;0&quot;,&quot;legendonly&quot;:&quot;&quot;,&quot;readonly&quot;:&quot;&quot;,&quot;score&quot;:&quot;0&quot;,&quot;starsonly&quot;:&quot;&quot;,&quot;best&quot;:&quot;5&quot;,&quot;gap&quot;:&quot;4&quot;,&quot;greet&quot;:&quot;Rate this product&quot;,&quot;legend&quot;:&quot;0\/5 - (0 votes)&quot;,&quot;size&quot;:&quot;24&quot;,&quot;title&quot;:&quot;CS29003 Lab 7-Disoint Set Union Solved&quot;,&quot;width&quot;:&quot;0&quot;,&quot;_legend&quot;:&quot;{score}\/{best} - ({count} {votes})&quot;,&quot;font_factor&quot;:&quot;1.25&quot;}">

<div class="kksr-stars">

<div class="kksr-stars-inactive">
            <div class="kksr-star" data-star="1" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="2" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="3" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="4" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="5" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
    </div>

<div class="kksr-stars-active" style="width: 0px;">
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
    </div>
</div>


<div class="kksr-legend" style="font-size: 19.2px;">
            <span class="kksr-muted">Rate this product</span>
    </div>
    </div>
<div class="page" title="Page 1">
<div class="layoutArea">
<div class="column">
Problem Statement

Mr. Scrooge is a renowned treasure hunter. Recently, he came across a map which shows possible treasure buried deep inside the earth. The place has m × n chambers with stone walls between every two adjacent chambers. The map also contains a spell which can be used to remove the stone walls, but it can only be used at most mn − 1 times. The most precious treasure is located just beside the last chamber. Mr. Scrooge not only wants to find the treasure, he also wants to explore each of the chambers since he thinks there might be some valuables in other chambers as well. He does not know which stone walls have to be removed to access each of the chambers. If he cannot find the treasure within mn − 1 stone wall removal, the spell will lose its potential. Luckily, Mr. Scrooge knows about the disjoint set data structure which he can effectively apply to solve this problem.

(b) Final grid after the stone-walls are re- (a) Initial grid moved

You can think of the chambers like a grid. The above figure illustrates the initial and the final grid. In the initial grid, all the chambers are separated by stone walls. There is one entry point in the top left of the grid and the treasure is right beside the bottom right chamber. In the final grid, Mr. Scrooge has successfully found the treasure and all the chambers are accessible from the start chamber.

Stone walls should be removed to achieve the following characteristics:

• Walls should be selected randomly as candidates for removal.

• A stone wall should not be removed if the two chambers on either side of the wall are already connected by some other path.

• The chambers are fully connected, i.e., every chamber is reachable from the start chamber.

</div>
</div>
<div class="layoutArea">
<div class="column">
1

</div>
</div>
</div>
<div class="page" title="Page 2">
<div class="layoutArea">
<div class="column">
Let C be a set of size s. Let C1,C2,…,Ct be pairwise disjoint subsets of C such that C = ∪kt=1Ck. For our application, C is the set of mn chambers, and Ck are the connected chambers. We represent each Ck as a rooted tree connected only by parent pointers. We assume that the parent of a root is the root itself. We identify the tree with the root, i.e., in order to find the subset Ck to which an individual element c ∈ C belongs, we start at the node storing c, move up the tree following parent pointers, and return the root.

Write the following three functions for implementing the disjoint-set data structure with union-by-rank and path compression.

<ul>
<li>makeset : Initially, the chambers are isolated from one another, i.e., each chamber belongs to a singleton set. Create an m × n array C of nodes. Let the parent pointer of each node point to itself. Also set the rank field of each node to zero.</li>
<li>findset : Given a node, i.e., (i,j)-th chamber, locate and return the root of the tree (connected area) to which the (i,j)-th chamber belongs. Also apply path compression technique while finding the root.</li>
<li>mergeset : Given two distinct root pointers x and y, make the root of the smaller tree a child of the root of the larger tree. If both roots have the same rank, increase rank of new root by one.
To randomly select walls for removal, you will also need to maintain a separate list of walls eligible for removal. There are two types of walls : horizontal walls and vertical walls. Create an (m − 1) × n array H for the horizontal walls, and an m × (n − 1) array V for the vertical walls. Note that the outer walls need not be removed, so these arrays do not consider outer walls.

Input

The program should accept the number of rows m and columns n of the grid as command-line arguments. If no command line arguments are given, it should default to 10 rows by 10 columns.

Part-1

Initialize C, H, and V corresponding to the chambers, horizontal wall, and vertical walls, respectively. Implement the disjoint-set data structure. Use the following definition for a node.

<pre>typedef struct _node {
   int rank;
</pre>
<pre>   struct _node *parent;
} node;
</pre>
Part-2

Write a function findtreasure that removes mn − 1 stone walls such that all the chambers (including the first and the final chambers) are in the same set.

At this point, call findset for the first and final chambers and verify that these are in the same set. Print appropriate message in console.

Part-3

Write a function printgrid for printing the initial and final grid. The grid is printed in ASCII using the vertical bar (|) and dash characters (−−−) to represent stone walls, and plus (+) for corners. The start and end chambers should have exterior openings as shown in the sample output.

Main function

In the main function, do the followings:
</li>
</ul>
<ul>
<li>Read m and n from the console.</li>
<li>Initialize the arrays C, H, and V . Print the initial grid.</li>
<li>call findtreasure to remove the mn − 1 stone walls so that the first and final chambers are connected. Print the final grid.
You can verify that when less than mn−1 stone walls are removed, the chambers may not be fully connected even though the end chamber may be reached from the start chamber.
</li>
</ul>
</div>
</div>
<div class="layoutArea">
<div class="column">
2

</div>
</div>
</div>
<div class="page" title="Page 3">
<div class="layoutArea">
<div class="column">
Sample 1:

Input :

56

Output :

<pre>The final chamber can be reached from the start chamber.
Initial Grid
</pre>
+ +—+—+—+—+—+ ||||||| +—+—+—+—+—+—+ ||||||| +—+—+—+—+—+—+ ||||||| +—+—+—+—+—+—+ ||||||| +—+—+—+—+—+—+ |||||| +—+—+—+—+—+—+

Final Grid

+ +—+—+—+—+—+ |||| + + + +—+—+ + |||| + +—+—+ +—+ + |||| + + + + +—+ + ||| ||| + + + +—+ + + ||| | +—+—+—+—+—+—+

Notes

<ol>
<li>At the time of evaluation, the input data might be different from the one given here.</li>
<li>Your code should show the output in the given format in the console. You do not need to write the output to a file.</li>
<li>For randomization, you can use the rand() function to generate random numbers. At the beginning of your main function, you can add srand((unsigned int)time(NULL)) to generate different random numbers in different runs of your code.</li>
</ol>
</div>
</div>
</div>
