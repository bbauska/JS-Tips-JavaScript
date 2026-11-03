<p>Check out this code.</p>
<pre>
1 if ((x === y || a === b) && c === d) {
2   g = h;
3 }
4 else {
5   e = f;
6 }
</pre>

<p>In the code above, if either of the first conditions is true, and, in addition, the third
condition is true, then g is assigned h. Otherwise, e is assigned f.</p>

<p>There's another way to code this, using nesting.</p>

<pre>
1 if (c === d) {
2   if (x === y) {
3     g = h;
4   }
5   else if (a === b) {
6     g = h;
7   }
8   else {
9     e = f;
10   }
11 }
12 else {
13   e = f;
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

<p>Suppose you code a prompt that asks, "Where does the Pope live?"</p>

<p>If the user answers correctly, you display an alert congratulating him.
This is the code.</p>

<pre>
1 var x = prompt("Where does the Pope live?");
2 if (x === "Vatican") {
3 alert("Correct!");
4 }
</pre>

<p>If the user enters "Vatican" in the prompt field, the congratulations alert displays. If he
enters something else, nothing happens. (This simplified code doesn't allow for other correct
answers, like "The Vatican." I don't want to get into that now.)</p>

<p>There's a lot to take in here. Let's break it down.</p>

<p>An if statement always begins with if. The space that separates it from the parenthesis is
new to you. I've taught you to code alerts and prompts with the opening parenthesis running up
against the keyword: alert("Hi"); Now I'm asking you not to do that in an if statement. It's
purely a matter of style, but common style rules sanction this inconsistency.</p>

<p>Following the if keyword-plus-space is the condition that's being tested—does the
variable that's been assigned the user's response have a value of "Vatican"?</p>

<p>The condition is enclosed in parentheses.</p>

<p>If the condition tests true, something happens. Any number of statements might execute. In
this case, only one statement executes: a congratulatory alert displays.</p>

<p>The first line of an if statement ends with an opening curly bracket. An entire if statement
ends with a closing curly bracket on its own line. Note that this is an exception to the rule that
a statement ends with a semicolon. It's common to omit the semicolon when it's a complex
statement that's paragraph-like and ends in a curly bracket.</p>

<p>But what about that triple equal sign? You might think that it should just be an equal sign,
but the equal sign is reserved for assigning a value to a variable. If you're testing a variable
for a value, you can't use the single equal sign.</p>

<p>If you forget this rule and use a single equal sign when you should use the triple equal
sign, the code won't run properly.</p>

<p>As you might expect, you can use a variable instead of a string in the example code.</p>

<pre>
1 var correctAnswer = "Vatican";
2 if (x === correctAnswer) {
3 alert("Correct!");
4 }
</pre>

<p>When a condition is met, you can have any number of statements execute.</p>

<pre>
1 var correctAnswer = "Vatican";
2 if (x === correctAnswer) {
3 score++;
4 userIQ = "genius";
5 alert("Correct!");
6 }
</pre>



