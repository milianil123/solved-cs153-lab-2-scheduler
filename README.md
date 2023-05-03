Download Link: https://assignmentchef.com/product/solved-cs153-lab-2-scheduler
<br>
<span style="font-size: 2em;">1. Getting Started</span>

5/5 - (1 vote)

Download a new directory of starter code of XV6 for Lab2 from this <a class="reference external" href="https://github.com/mit-pdos/xv6-public">link</a>.

To get started, look at the file <code class="docutils literal notranslate"><span class="pre">proc.c</span></code>.

<h2>2. Assignment (95%)</h2>

In this part of the assignment, you will change the scheduler from a simple round-robin to a priority scheduler. Add a priority value to each process (lets say taking a range between 0 to 31). The range does not matter, it is just a proof of concept. When scheduling from the ready list you will always schedule the highest priority thread/process first. All the processes should have a default initial priority of 10.

Add a system call to change the priority of a process. A process can change its priority at any time. If the priority becomes lower than any process on the ready list, you must switch to that process.

<strong>Goals</strong>: Understand how the scheduler works. Understand how to implement a scheduling policy and characterize its impact on performance. Understand priority inversion and a possible solution for it.

<h2>3. Bonus Section (upto 10%)</h2>

Implement up to two of the next three items. Each is a 5% bonus. To get credit for a bonus part, you must also develop a user test that will illustrate it.

<ul>

 <li><p class="first">To avoid starvation, implement aging of priority. If a process waits increase its priority. When it runs, decrease it. (Possible Bonus 1)   </li>

 <li><p class="first">Implement priority donation/priority inheritance. (Possible Bonus 2)   </li>

 <li><p class="first">Add fields to track the scheduling performance of each process. These values should allow you to compute the turnaround time and wait time for each process. Add a system call to extract these values or alternatively print them out when the process exits. (Possible Bonus 3)</li>

</ul>

<h2>4. Questions to Explore</h2>

<ul class="simple">

 <li>Explain how the current scheduler works, including interaction with the timer.</li>