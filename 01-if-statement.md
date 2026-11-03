<p>Check out this code.</p>
<pre>
1 if ((x === y || a === b) && c === d) {
2 g = h;
3 }
4 else {
5 e = f;
6 }
</pre>
<p>In the code above, if either of the first conditions is true, and, in addition, the third
condition is true, then g is assigned h. Otherwise, e is assigned f.</p>

<p>There's another way to code this, using nesting.</p>

<pre>
1 if (c === d) {
2 if (x === y) {
3 g = h;
4 }
5 else if (a === b) {
6 g = h;
7 }
8 else {
9 e = f;
10 }
11 }
12 else {
13 e = f;
14 }
</pre>

<p>Nest levels are communicated to JavaScript by the positions of the curly brackets. There
are three blocks nested inside the top-level if. If the condition tested by the top-level if—that c
has the same value as d—is false, none of the blocks nested inside executes. The opening curly
bracket on line 1 and the closing curly bracket on line 11 enclose all the nested code, telling
JavaScript that everything inside is second-level.</p>

<p>For readability, a lower level is indented 2 spaces beyond the level above it.
In the relatively simple set of tests and outcomes shown in this example, I would prefer to
use the more concise structure of multiple conditions. But when things get really complicated,
nested ifs are a good way to go.</p>





