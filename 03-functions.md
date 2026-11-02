A function is a block of JavaScript that robotically does the same thing again and again,
whenever you invoke its name. It saves you repetitive coding and makes your code easier to
understand.
On your website, suppose there are several pages where you want to display an alert that
tells the user the current time. (To keep it simple, we'll settle for 24-hour time rather than
converting to a.m. and p.m.) The code might look like this.
1 var now = new Date();
2 var theHr = now.getHours();
3 var theMin = now.getMinutes();
4 alert("time: " + theHr + ":" + theMin);
You could write this block of code over and over again, every time you need it. Or you
could write it once as a function, naming it, say, tellTime. After that, this is the only code
you'll need in order to make the whole block execute:
tellTime();
Whenever JavaScript sees that short statement, the time-telling block executes.
This is how you package the one-off code above as a repeatable function:
