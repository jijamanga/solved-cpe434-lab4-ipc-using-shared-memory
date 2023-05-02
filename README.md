Download Link: https://assignmentchef.com/product/solved-cpe434-lab4-ipc-using-shared-memory
<br>
Write the code for two distinct C processes that are not part of a parent-child relation. They both attach to shared memory area containing a new type structure with four data types (first number, second-number, Sum and Flag). The first process must set the values for first and second numbers, then it updates the value of flag to 1 (which means there is new data). The second process is to find the sum of these two numbers and display the sum of the two values and changes the flag to zero. Two processes continue running until the first process sets the value of flag to -1.

Hint

Define the shared structure like:

<table width="589">

 <tbody>

  <tr>

   <td width="589">struct ​info ​{  float ​value1​, ​value2​;  float ​sum​;  int ​flag​;};# define KEY ((key_t)(1234))# define SEGSIZE sizeof (struct info)</td>

  </tr>

 </tbody>

</table>







Topics for theory:  <strong>shmget()​</strong>: ​<em>int shmget(key_t key, size_t size, int shmflg);  </em>

It returns the identifier of the shared memory segment associated with the value of ​<em>key​</em>. Based on a value of ​<em>shmflg​</em>, either a new segment is created or identifier of already created segment  <strong>shmat()​</strong>: ​<em>void *shmat(int shmid, const void *shmaddr, int shmflg);  </em>

It attaches the shared memory segment identified by ​<em>shmid ​</em>and returns the pointer in the calling process address space.  <strong>shmctl()​</strong>: ​<em>int shmctl(int shmid, int cmd, struct shmid_ds *buf);  </em>

It performs the control operation in the shared memory segment identified by ​<em>shmid​</em>. The operation is as defined by value ​<em>shmid  </em>

<strong>shmdt()​</strong>: ​<em>int shmdt(const void *shmaddr);  </em>

This function detaches the shared memory segment identified by ​<em>shmaddr </em>

<strong>Please visit Study_Lab05andLab04.pptx file page 1-10 for demo examples.  </strong>

<h2>Deliverables</h2>

<h3>Lab Report</h3>

The following material in each section is expected:

<ol>

 <li>Cover page with your name, lab number, course name, and dates</li>

 <li>Theory/Background (Material or methods relevant to the lab, a few sentences on each)

  <ol>

   <li>shmget()</li>

   <li>shmat()</li>

   <li>shmctl()</li>

   <li>shmdt()</li>

  </ol></li>

 <li>Observations (Show output demonstrating the two processes can use the shared memory correctly.)

  <ol>

   <li>Process 1 can set value1, value2, and flag</li>

   <li>Setting flag to -1 by process 1 should cause both processes to terminate</li>

   <li>The second process sets sum to the sum of value1 and value2. It should display the result.</li>

  </ol></li>

 <li>Conclusion (Did your program work as expected, what can you take away from the lab?)</li>

 <li>Appendix (for source code, submit the text in a table)</li>

</ol>

The report should be submitted as a single pdf document with the source code for your program within it.

<h3>Recorded Demonstration</h3>

The following material in each section is expected:

<ol>

 <li>Introduce yourself and give the name of the lab</li>

 <li>Show and discuss how your program works</li>

 <li>Compile the program</li>

 <li>Show that the two processes interact as required</li>

 <li>Recordings should be around 5 to 7 minutes on average</li>

</ol>




The recorded demonstration should be submitted as an mp4 file. <strong> </strong>