Download Link: https://assignmentchef.com/product/solved-comp9311-assignment3
<br>
Consider the B+ tree shown in the following as an original tree.

Answer the following questions:

<ul>

 <li>(2 marks) There are currently 18 records in this tree. How many additional records could be added to this tree without changing its height (give the maximum possible number)?</li>

 <li>(3 marks) Show the B+ tree after inserting a data entry with key 3 into the original tree.</li>

 <li>(3 marks) Show the B+ tree after deleting the data entry with key 91 from the original tree.</li>

</ul>

<h2>Question 2</h2>

Consider a relation R(a,b,c,d,e,f,g,h) containing 10,000,000 records, where each data page of the relation holds 10 records. R is organised as a sorted file with the search key R.a. Assume that R.a is a candidate key of R, with values lying in the range 0 to 9,999,999. For the relational algebra <sup>!</sup><em>π</em>{<em>a</em>,<em>b</em>}(<em>σ</em>(<em>a</em>&gt;2,000,000 <em>and a</em>&lt;8,000,000)(<em>R</em>)), state which of the following approaches (or combination thereof) is the most likely to be the cheapest:

<ol>

 <li>Access the sorted file for R directly.</li>

 <li>Use a clustered B+ tree index on attribute R.a.</li>

 <li>Use a clustered B+ tree index on attribute R.b.</li>

 <li>Use a linear hashed index on attribute R.a.</li>

 <li>Use a clustered B+ tree index on attributes (R.a, R.b).</li>

 <li>Use a linear hashed index on attribute s (R.a, R.b).</li>

</ol>

We assume that the database considers index-only plans. Index-only plans allow an index to contain all columns required to answer the query.  It means that by using index-only plans, you will not have to access the data records in the file that contain the queried relations.

<h2>Question 3</h2>

Consider the schedule below. Here, R(*) and W(*) stand for ‘Read’ and ‘Write’, respectively. <em>T</em>! <sub>1</sub>, !<em>T</em><sub>2</sub>, !<em>T</em><sub>3</sub> and <em>T</em>! <sub>4</sub> represent four transactions and !<em>t<sub>i</sub></em> represents a time slot.

<table width="552">

 <tbody>

  <tr>

   <td width="42">Time</td>

   <td width="42"><em>t</em>! 1</td>

   <td width="42"><em>t</em>! 2</td>

   <td width="42"><em>t</em>! 3</td>

   <td width="42"><em>t</em>! 4</td>

   <td width="42"><em>t</em>! 5</td>

   <td width="42"><em>t</em>! 6</td>

   <td width="42"><em>t</em>! 7</td>

   <td width="42"><em>t</em>! 8</td>

   <td width="42"><em>t</em>! 9</td>

   <td width="42"><em>t</em><sup>! </sup>10</td>

   <td width="42"><em>t</em><sup>! </sup>11</td>

   <td width="42"><em>t</em><sup>! </sup>12</td>

  </tr>

  <tr>

   <td width="42"><em>T</em> 1</td>

   <td width="42"> </td>

   <td width="42">R(B)</td>

   <td width="42"> </td>

   <td width="42"> </td>

   <td width="42"> </td>

   <td width="42">R(A)</td>

   <td width="42">W(B)</td>

   <td width="42"> </td>

   <td width="42">W(A)</td>

   <td width="42"> </td>

   <td width="42"> </td>

   <td width="42"> </td>

  </tr>

  <tr>

   <td width="42"><em>T</em> 2</td>

   <td width="42"> </td>

   <td width="42"> </td>

   <td width="42">R(A)</td>

   <td width="42">W(A)</td>

   <td width="42"> </td>

   <td width="42"> </td>

   <td width="42"> </td>

   <td width="42"> </td>

   <td width="42"> </td>

   <td width="42"> </td>

   <td width="42"> </td>

   <td width="42"> </td>

  </tr>

  <tr>

   <td width="42"><em>T</em> 3</td>

   <td width="42"> </td>

   <td width="42"> </td>

   <td width="42"> </td>

   <td width="42"> </td>

   <td width="42"> </td>

   <td width="42"> </td>

   <td width="42"> </td>

   <td width="42">R(B)</td>

   <td width="42"> </td>

   <td width="42">W(B)</td>

   <td width="42"> </td>

   <td width="42"> </td>

  </tr>

  <tr>

   <td width="42"><em>T</em> 4</td>

   <td width="42">R(A)</td>

   <td width="42"> </td>

   <td width="42"> </td>

   <td width="42"> </td>

   <td width="42">W(A)</td>

   <td width="42"> </td>

   <td width="42"> </td>

   <td width="42"> </td>

   <td width="42"> </td>

   <td width="42"> </td>

   <td width="42">R(B)</td>

   <td width="42">W(B)</td>

  </tr>

 </tbody>

</table>

Each transaction begins at the time slot of its first Read, and commits right after its last Write (same time slot).

Regarding the following questions, give and justify your answers.

<ul>

 <li>Assume a checkpoint is made between <em>t</em>! <sub>4</sub> and <em>t</em>! <sub>5</sub>, what should be done to the four transactions when the crash happens between  <em>t</em>! <sub>7</sub> and <em>t</em>! <sub>8</sub>. (2 marks)</li>

 <li>Is the transaction schedule conflict serialisable? Give the precedence graph to justify your answer. (2 marks)</li>

 <li>Construct a schedule (which is different from above) of these four transactions which causes deadlock when using two-phase locking protocol. If no such schedule exists, explain why. (2 marks)</li>

 <li>Construct a schedule (which is different from above) of these four transactions which <strong>does not</strong> cause deadlock when using two-phase locking protocol. If no such schedule exists, explain why. (2 marks)</li>

</ul>