Download Link: https://assignmentchef.com/product/solved-artificial-intelligence-part-1
<br>
<strong>Resource-Allocation Graph: </strong>

❖ <strong><em>About the graph: </em></strong>

The graph consists of a set of vertices and a set of edges. The vertices represent all the active processes in the system {P1, P2, …, Pn} as well as all the resource types in the system {R1, R2, …, Rm}. The dots found in each resource square represent the number of instances of that resource. A directed edge from process Pi to resource type Rj (Pi → Rj) signifies that Pi has requested an instance of Rj and is currently waiting for that resource. A directed edge from resource type Rj to process Pi (Rj → Pi) signifies that an instance of Rj has been allocated to Pi.

A process releases its allocated resources only when it acquires all the resources it needs (all its requests are fulfilled). So, if the graph contains no cycles, no process in the system is deadlocked. Otherwise, a deadlock may exist. If each resource type has exactly one instance, then a cycle implies that a deadlock has occurred. On the other hand, if each resource type has several instances, a cycle doesn’t necessarily imply that a deadlock has occurred. In the previous figure, a cycle exists; however, there is no deadlock. This is because process P4 can release its instance of resource R2. That resource can then be allocated to P3, breaking the cycle.

<ul>

 <li><strong><em>What you are required to do: </em></strong></li>

</ul>

You are required to make a prolog program that determines whether a graph can reach a safe state (with no deadlock) or not and if the graph can reach a safe state, you should output the process execution order that made the graph be in such a state. You will have to define the graph data as facts and define the necessary predicates/rules that detect deadlocks. <strong>For simplicity, assume we only have 2 resource types (R</strong><strong>1 and R</strong><strong>2). </strong>

<ul>

 <li><strong><em>A sample test case: </em></strong></li>

</ul>

This test case shows the sample input that should be entered and the sample output for the graph in the previous figure. <strong><em> </em></strong>

?- safe_state(X).

X = [p2, p4, p1, p3].

Notice that that graph has different solutions.

❖ <strong><em>The input file: </em></strong>

The input file should look somewhat like the opposite figure, but you can adjust the facts/predicates if you need to. <strong><em> </em></strong>























































<strong><em> </em></strong>


