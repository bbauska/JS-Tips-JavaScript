<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<h1>Getting the current date and time</h1>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<p>Your webpage includes a notice telling the user the current local date and time in his particular time zone. 
But what is the current date and time? Here's how JavaScript finds out.</p>
<pre>
var rightNow = new Date();
</pre>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<p>The statement above creates something called a <i>Date object</i>. This is what it looks like.</p>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~ 01. date object (full) ~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<a href="https://www.w3.org/2009/cheatsheet/" target="_blank" rel="noopener noreferrer">
<img class="displayed border"
  src="./images/tips-date-01.jpg?raw=true"
<!--  loading="lazy" -->
  title="Date object (full)"
  alt="Date object (full)."
  style="width:100%;" />
</a>

<p>Note that JavaScript gets this information from the user's computer. It is only as accurate
as the computer's date and time settings. For example, if the user just moved from the U.S.
West Coast to the U.S. East Coast and hasn't reset the time zone on his computer, the computer
will still be on Pacific Time. The Date object, too, will be on Pacific Time.</p>

<p>The Date object may resemble a string, but it isn't one. For example, you can't use methods on it like 
<b>charAt</b>, <b>indexOf</b>, or <b>slice</b>.</p>

<p>If you need the Date object to be a string, you can convert it to one the same way you convert a number 
to a string.</p>

<pre>var dateString = rightNow.toString();</pre>

<p>The code above converts the Date object represented by the variable rightNow to a
string and assigns the string to the variable dateString.</p>

<p>Most of the time, you'll just want to extract some of the information from the Date object
without converting it to a string.</p>

<p>I'm going to show you how to extract the individual pieces of the Date object. In this
chapter I'll get you started with the first piece. In the next chapter I'll cover the rest.
The following code creates a new Date object, assigns it to the variable rightNow,
extracts the day of the week, and assigns the day of the week to the variable theDay.</p>

<pre>
  1 var rightNow = new Date();
  2 var theDay = rightNow.getDay();
</pre>

<p>In the diagram of the Date object that I showed you above, the day of the week was
represented as "Mon." But when you extract the day of the week from the object, it's
represented as a number. Days are designated by a number from 0 for Sunday through 6 for
Saturday. This means that you'll need a bit of code to convert it back into a day name like
"Mon."</p>

<pre>
  1 var dayNames = ["Sun", "Mon", "Tue", "Wed", "Thu", "Fri", "Sat"];
  2 var now = new Date();
  3 var theDay = now.getDay();
  4 var nameOfToday = dayNames[theDay];
</pre>

<p>Here's what's going on:</p>
<ol>
  <li>1. Creates an array of days starting with "Sun" and assigns it to dayNames.</li>
  <li>2. Creates a new Date object and assigns it to now.</li>
  <li>3. Extracts the day of the week as a number and assigns it to theDay.</li>
  <li>4. Uses the day number as an index to specify the correct array element, i.e. the day name.</li>
</ol>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<h1>Extracting parts of the date and time</h1>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<p>Here's a summary of important methods for extracting pieces of the Date object.</p>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~ 02. date extraction methods ~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<a href="https://www.w3.org/2009/cheatsheet/" target="_blank" rel="noopener noreferrer">
<img class="displayed border"
  src="./images/tips-date-02.jpg?raw=true"
<!--  loading="lazy" -->
  title="Date extraction methods"
  alt="Date extraction methods."
  style="width:100%;" />
</a>

<p>Let's look at the rest of the extraction methods. Like
getDay, getMonth gives you not the spelled-out name of the month shown in the Date object,
but a number. The following code produces a month number ranging from 0 for January through
11 for December.</p>

<pre>
  1 var d = new Date();
  2 var currentMonth = d.getMonth();
</pre>

<p>getDate gives you a number for the day of the month.</p>
<pre>
var dayOfMonth = d.getDate();
</pre>
<p>getFullYear gives you a 4-digit number for the year.</p>

<pre>
var currYr = d.getFullYear();
</pre>

<p>getHours gives you a number from 0 through 23 corresponding to midnight through 11 p.m.</p>
<pre>
var currentHrs = d.getHours();
</pre>

<p>getMinutes gives you a number from 0 through 59.</p>
<pre>
var currMins = d.getMinutes();
</pre>

<p>getSeconds gives you a number from 0 through 59.</p>
<pre>
var currSecs = d.getSeconds()
</pre>

<p>getMilliseconds gives you a number from 0 through 999.</p>
<pre>
var currMills = d.getMilliseconds();
</pre>

<p>getTime gives you the number of milliseconds that have elapsed since midnight, Jan. 1, 1970.</p>
<pre>
var millsSince = d.getTime();
</pre>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<h1>Specifying a date and time</h1>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<p>How many days before the U.S. Social Security program goes broke? Let's start with the estimated date. 
According to the system's trustees, the money will run out in 2035. They didn't pin down an exact date.</p>
<p>Let's pick the middle of the year—June 30. Okay, that's the hard part—pinpointing doomsday. Once we have 
that, constructing a day-by-day countdown is a JavaScript romp. You already know how to do the first step, 
creating a Date object for the current date and time:</p>
<pre>
1 var today = new Date();
</pre>

<p>Next, you create a second Date object. But this time you specify the future date, June 30, 2035.</p>
<pre>
2 var doomsday = new Date("June 30, 2035");
</pre>

<p>Notice how the date is specified. It's in quotes. The month is spelled out. There's a comma after the 
day of the month. The year is expressed in four digits. Next, you extract from both dates the milliseconds 
that have elapsed since the reference date of January 1, 1970.</p>
<pre>
3 var msToday = today.getTime();
4 var msDoomsday = doomsday.getTime();
</pre>

<p>You calculate the difference.</p>

<pre>
5 var msDiff = msDoomsday - msToday;
</pre>

<p>Some simple math converts the milliseconds to days.</p>

<pre>
6 var dDiff = msDiff / (1000 * 60 * 60 * 24);
</pre>

<p>The huge number created by the math inside the parentheses converts the milliseconds into seconds (1000), 
minutes (60), hours (60), and days (24). You want a number that represents whole days, so you round down. The 
following statement rounds the number of days, which is probably a floating-point number, down to an integer.</p>

<pre>
7 dDiff = Math.floor(dDiff);
</pre>

<p>Here's the whole thing, condensed into something that looks more like production code.</p>

<pre>
1 var msDiff = new Date("June 30, 2035").getTime() - new Date().getTime();
2 var daysTillDoom = Mathfloor(msDiff / (1000 * 60 * 60 * 24));
</pre>

<p>Line 1 subtracts the milliseconds since the reference date of the current moment from the milliseconds since 
the reference date of June 30, 2035. Line 2 converts the milliseconds to days and rounds down.</p>
<p>If the time is important, you can specify that as well.</p>

<pre>
var d = new Date("July 21, 1983 13:25:00");
</pre>

<p>Note the form used to specify the time: No comma after the date. 24-hour time. Colons
separating hours, minutes, and seconds.</p>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<h1>Changing elements of a date and time</h1>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<p>You can change individual elements of a Date object. Here's a summary:</p>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~ 03. change date elements ~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<a href="https://www.w3.org/2009/cheatsheet/" target="_blank" rel="noopener noreferrer">
<img class="displayed border"
  src="./images/tips-date-03.jpg?raw=true"
<!--  loading="lazy" -->
  title="Change Date elements"
  alt="Change Date elements."
  style="width:100%;" />
</a>

<!-- tips-date-03.jpg - image of example and results change date/time -->

<p>setFullYear sets the year of an existing Date object without changing any other element.</p>

<pre>
1 var d = new Date();
2 d.setFullYear(2001);
</pre>

<p>Line 1 creates a new Date object for the current moment. Line 2 changes the year of the Date object 
to 2001, leaving all other elements of the Date object intact. setMonth sets the month of an existing 
Date object without changing any other element.

<pre>
1 var d = new Date();
2 d.setMonth(11);
</pre>

<p>Line 1 creates a new Date object for the current moment. Line 2 changes the month of the Date object to 
11 (December), leaving all other elements of the Date object intact. 
setDate sets the day of the month of an existing Date object without changing any other
element.</p>

<pre>
1 var d = new Date();
2 d.setDate(15);
</pre>

<p>Line 1 creates a new Date object for the current moment. Line 2 changes the date of the
Date object to the 15th of the month, leaving all other elements of the Date object intact.
setHours sets the hours of an existing Date object without changing any other element.</p>

<pre>
1 var d = new Date();
2 d.setHours(13);
</pre>

<p>Line 1 creates a new Date object for the current moment. Line 2 changes the hours of the
Date object to the 13th hour (1 p.m.), leaving all other elements of the Date object intact.
setMinutes sets the minutes of an existing Date object without changing any other
element.</p>

<pre>
1 var d = new Date();
2 d.setMinutes(05);
</pre>

<p>Line 1 creates a new Date object for the current moment. Line 2 changes the minutes of
the Date object to 5 minutes after the hour, leaving all other elements of the Date object intact.
setSeconds sets the seconds of an existing Date object without changing any other
element.</p>

<pre>
1 var d = new Date();
2 d.setSeconds(55);
</pre>

<p>Line 1 creates a new Date object for the current moment. Line 2 changes the seconds of
the Date object to the 55 seconds after the minute, leaving all other elements of the Date object
intact.</p>

<p>setMilliseconds sets the milliseconds of an existing Date object without changing any other element.</p>

<pre>
1 var d = new Date();
2 d.setMilliseconds(867);
</pre>

<p>Line 1 creates a new Date object for the current moment. Line 2 changes the milliseconds
of the Date object to 867 milliseconds after the second, leaving all other elements of the Date
object intact.</p>
