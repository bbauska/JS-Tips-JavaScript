<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<h1>Generating random numbers</h1>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<p>Suppose you want to simulate the throw of a die. In the simulation, you want it to randomly come up 
1, 2, 3, 4, 5, or 6. The first step is to ask JavaScript to generate a random number. (Well, it's 
almost random, technically known as pseudo-random, but it's close enough to random for most purposes.)
The following code generates a pseudo-random number, with 16 decimal places, ranging from 0.0000000000000000 
through 0.9999999999999999 and assigns it to the variable randomNumber.</p>
<pre>
var randomNumber = Math.random();
</pre>
<p>The function always delivers a 16-place decimal that ranges from 0.0000000000000000 to 0.9999999999999999. 
We can convert the decimal to an integer by multiplying by one hundred quadrillion (1 followed by 17 zeroes):</p>
<pre>
0.0000000000000000 * 100000000000000000 = 0
0.7474887706339359 * 100000000000000000 = 7474887706339359
0.9999999999999999 * 100000000000000000 = 9999999999999999
</pre>
<p>Trillions of possible numbers are more than we need in our virtual die throw. We just
want six possible numbers, 1 through 6. So instead of multiplying by a hundred quadrillion, our
first step is to multiply the giant decimal by 6.</p>
<pre>
0.0000000000000000 * 6 = 0
0.7474887706339359 * 6 = 4.7474887706339359
0.9999999999999999 * 6 = 5.9999999999999994
</p>
<p>Intuition may tell you that you can finish the job by rounding, but that doesn't work out
mathematically. Because nothing rounds up to 0 and nothing rounds down to 6, the numbers in
the middle, which are reached both by rounding up and rounding down, will come up almost
twice as often. But we can give all the numbers an equal chance if we add 1 to the result, then
round down. Here's the code for our virtual die throw.</p>
<pre>
1 var bigDecimal = Math.random();
2 var improvedNum = (bigDecimal * 6) + 1;
3 var numberOfStars = Math.floor(improvedNum);
</pre>
<p>This is what happens in the code above, line by line:</p>

<ol>
  <li>1. Generates a 16-place decimal and assigns it to the variable bigDecimal.</li>
  <li>2. Converts the 16-place decimal to a number ranging from 0.0000000000000000 through 
  5.9999999999999999, then adds 1, so the range winds up 1.0000000000000000 through 
  6.9999999999999999. This number is assigned to the variable improvedNum.<li>
  <li>3. Rounds the value represented by improvedNum down to the nearest integer that ranges
  from 1 through 6.</li>
</ol>

<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
# Getting the current date and time
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->

Your webpage includes a notice telling the user the current local date and time in his particular time zone. 
But what is the current date and time? Here's how JavaScript finds out.

var rightNow = new Date();

The statement above creates something called a Date object. This is what it looks like.

Note that JavaScript gets this information from the user's computer. It is only as accurate
as the computer's date and time settings. For example, if the user just moved from the U.S.
West Coast to the U.S. East Coast and hasn't reset the time zone on his computer, the computer
will still be on Pacific Time. The Date object, too, will be on Pacific Time.
The Date object may resemble a string, but it isn't one. For example, you can't use
methods on it like charAt, indexOf, or slice.
If you need the Date object to be a string, you can convert it to one the same way you
convert a number to a string.

var dateString = rightNow.toString();

The code above converts the Date object represented by the variable rightNow to a
string and assigns the string to the variable dateString.
Most of the time, you'll just want to extract some of the information from the Date object
without converting it to a string.
I'm going to show you how to extract the individual pieces of the Date object. In this
chapter I'll get you started with the first piece. In the next chapter I'll cover the rest.
The following code creates a new Date object, assigns it to the variable rightNow,
extracts the day of the week, and assigns the day of the week to the variable theDay.

1 var rightNow = new Date();
2 var theDay = rightNow.getDay();

In the diagram of the Date object that I showed you above, the day of the week was
represented as "Mon." But when you extract the day of the week from the object, it's
represented as a number. Days are designated by a number from 0 for Sunday through 6 for
Saturday. This means that you'll need a bit of code to convert it back into a day name like
"Mon."

1 var dayNames = ["Sun", "Mon", "Tue", "Wed", "Thu", "Fri", "Sat"];
2 var now = new Date();
3 var theDay = now.getDay();
4 var nameOfToday = dayNames[theDay];

Here's what's going on:
1. Creates an array of days starting with "Sun" and assigns it to dayNames.
2. Creates a new Date object and assigns it to now.
3. Extracts the day of the week as a number and assigns it to theDay.
4. Uses the day number as an index to specify the correct array element, i.e. the day name.

<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
# Extracting parts of the date and time
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->

1 var d = new Date();
2 var currentMonth = d.getMonth();

  getDate gives you a number for the day of the month.

var dayOfMonth = d.getDate();

  getFullYear gives you a 4-digit number for the year.

var currYr = d.getFullYear();

  getHours gives you a number from 0 through 23 corresponding to midnight through 11 p.m.

var currentHrs = d.getHours();

  getMinutes gives you a number from 0 through 59.

var currMins = d.getMinutes();

  getSeconds gives you a number from 0 through 59.

var currSecs = d.getSeconds()

  getMilliseconds gives you a number from 0 through 999.

var currMills = d.getMilliseconds();

  getTime gives you the number of milliseconds that have elapsed since midnight, Jan. 1, 1970.

var millsSince = d.getTime();

<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
# Specifying a date and time
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
How many days before the U.S. Social Security program goes broke? Let's start with the estimated date. 
According to the system's trustees, the money will run out in 2035. They didn't pin down an exact date. 
Let's pick the middle of the year—June 30. Okay, that's the hard part—pinpointing doomsday. Once we have 
that, constructing a day-by-day countdown is a JavaScript romp. You already know how to do the first step, 
creating a Date object for the current date and time:

1 var today = new Date();

<p>Next, you create a second Date object. But this time you specify the future date, June 30, 2035.</p>

2 var doomsday = new Date("June 30, 2035");

<p>Notice how the date is specified. It's in quotes. The month is spelled out. There's a comma after the 
day of the month. The year is expressed in four digits. Next, you extract from both dates the milliseconds 
that have elapsed since the reference date of January 1, 1970.</p>

3 var msToday = today.getTime();
4 var msDoomsday = doomsday.getTime();

<p>You calculate the difference.</p>

5 var msDiff = msDoomsday - msToday;

<p>Some simple math converts the milliseconds to days.</p>

6 var dDiff = msDiff / (1000 * 60 * 60 * 24);

<p>The huge number created by the math inside the parentheses converts the milliseconds into seconds (1000), 
minutes (60), hours (60), and days (24). You want a number that represents whole days, so you round down. The 
following statement rounds the number of days, which is probably a floating-point number, down to an integer.</p>

7 dDiff = Math.floor(dDiff);

<p>Here's the whole thing, condensed into something that looks more like production code.</p>

1 var msDiff = new Date("June 30, 2035").getTime() - new Date().getTime();
2 var daysTillDoom = Mathfloor(msDiff / (1000 * 60 * 60 * 24));

<p>Line 1 subtracts the milliseconds since the reference date of the current moment from the milliseconds since 
the reference date of June 30, 2035. Line 2 converts the milliseconds to days and rounds down.</p>
<p>If the time is important, you can specify that as well.</p>

var d = new Date("July 21, 1983 13:25:00");

<p>Note the form used to specify the time: No comma after the date. 24-hour time. Colons
separating hours, minutes, and seconds.</p>



<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
# Changing elements of a date and time
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<p>You can change individual elements of a Date object. Here's a summary:</p>

<!-- image-34.jpg - image of example and results change date/time -->

<p>setFullYear sets the year of an existing Date object without changing any other element.</p>

1 var d = new Date();
2 d.setFullYear(2001);

<p>Line 1 creates a new Date object for the current moment. Line 2 changes the year of the Date object 
to 2001, leaving all other elements of the Date object intact. setMonth sets the month of an existing 
Date object without changing any other element.

1 var d = new Date();
2 d.setMonth(11);

<p>Line 1 creates a new Date object for the current moment. Line 2 changes the month of the Date object to 
11 (December), leaving all other elements of the Date object intact. 
setDate sets the day of the month of an existing Date object without changing any other
element.</p>

1 var d = new Date();
2 d.setDate(15);

Line 1 creates a new Date object for the current moment. Line 2 changes the date of the
Date object to the 15th of the month, leaving all other elements of the Date object intact.
setHours sets the hours of an existing Date object without changing any other element.

1 var d = new Date();
2 d.setHours(13);

Line 1 creates a new Date object for the current moment. Line 2 changes the hours of the
Date object to the 13th hour (1 p.m.), leaving all other elements of the Date object intact.
setMinutes sets the minutes of an existing Date object without changing any other
element.

1 var d = new Date();
2 d.setMinutes(05);

Line 1 creates a new Date object for the current moment. Line 2 changes the minutes of
the Date object to 5 minutes after the hour, leaving all other elements of the Date object intact.
setSeconds sets the seconds of an existing Date object without changing any other
element.

1 var d = new Date();
2 d.setSeconds(55);

Line 1 creates a new Date object for the current moment. Line 2 changes the seconds of
the Date object to the 55 seconds after the minute, leaving all other elements of the Date object
intact.
setMilliseconds sets the milliseconds of an existing Date object without changing any
other element.

1 var d = new Date();
2 d.setMilliseconds(867);

Line 1 creates a new Date object for the current moment. Line 2 changes the milliseconds
of the Date object to 867 milliseconds after the second, leaving all other elements of the Date
object intact.









