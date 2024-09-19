---
title: "JavaScript Tips - First 151"
author: "bbauska"
date created: "9/18/2024 Wed 4+pm"
date last editted: "9/18/2024 Wed 1+pm"

output: 
  markdown:
    with some style
---
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<h1 id="js-tips">JS-TIPS (1st 151 things to learn)</h1>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<h4>JavaScript Tips, Tricks, and Techniques.  Moderate to intermediate level of knowledge, overall.</h4>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<h2 id="1-fundamentals">1. Fundamentals</h2>  <!-- 1 thru 14 -->
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<ol type="1">
  <li>What is Javascript?<br/>
  Javascript is basically scripting language used to make web pages
  more interactive as it can be inserted into HTML.
  Javascript is understood by all modern web browsers.</li>
  <li>What are features of Javascript?
    <ul style="list-style-type:disc">
      <li>Input validation : Javascript allows you to validate user input before sending it 
      to server for backend operations.</li>
    <li>Control over browser : Javascript gives more control over browser due to which you can 
      change the background colour of this page as well as the text on the browser's status bar.</li>
    <li>Detect browser and OS : Javascript enables you to detect user’s browser and OS due to 
      which you can perform platform dependant operations.</li>
    <li>Handling date and time : Javascript enables you to write code based users date and time, 
      it also enables you to capture users date and time as user and server may be in different 
      time zone.</li>
    <li>Generating HTML on fly : Javascript enables you to dynamically generate HTML.</li>
    </ul>
  </li>
  <li>What are advantages of Javascript?
    <ul style="list-style-type: circle">
      <li>Faster speed : JavaScript is fast because it run immediately within the client-side browser. 
        Javascript is not dependant on network unless backend data is required to be processed. 
        Need to compile Javascript on the client–side as it is interpreted directly by web browsers.</li>
      <li>Interoperability : Javascript can be inserted into web page regardless of extension. 
    Within other languages such as Perl and PHP it can be used inside the script.</li>
      <li>Rich interfaces : Javascript has vast libraries like (charts, drag and drop, sliders etc.) 
    which enables you to provide attractive look to your website.</li>
      <li>Reduction in server load : Since Javascript is client-side scripting language it reduces 
        load on website servers as many operations can be performed at client-side which reduces 
        load on server and enables it to serve to more users.</li>
    </ul>
  </li>
  <li>What are disadvantages of Javascript?
    <ul style="list-style-type: square">
      <li>Client-side security : JavaScript code executes in users computer hence in some cases 
        it can be manipulated for malicious purpose.</li>
      <li>Browser support : JavaScript is sometimes interpreted differently by different browsers.</li>
    </ul>
  </li>
  <li>What is difference between Javascript and ECMAScript?<br/>
    JavaScript is a scripting language that has been formed by keeping ECMAScript specification 
    at its core. ECMAScript is nothing but a standard or specification defined in order to create 
    different scripting languages and one of them is JavaScript.<br/>
    Javascript, Jscript and ActionScript are few scripting languages that follow ECMAScript 
    specifications.</li>
  <li>Who developed Javascript?<br/>
    JavaScript was created in 1995 by Brendan Eich during his time at Netscape Communications. It 
    was inspired by Java, Scheme and Self.</li>
  <li>How to insert Javascript in Web page?<br/>
    You can use &lt;script&gt; tag in html. &lt;script&gt; tag has type attribute which 
    defined which code is there inside the script tag.<br/>
    You can use &lt;script&gt; element in web pages in following ways:
      <ul style="list-style-type="disc">
        <li>In head element</li>
        <li>In body element</li>
        <li>As an external script file</li>
      </ul>
    To use Javascript as a scripting language for web pages in &lt;head&gt; or &lt;body&gt; 
    you can define type as “text/javascript”. e.g.,<br/>
      &lt;script type=”text/javascript”&gt;<br/>
      &lt;/script&gt;<br/>
    Sometime you may need to use same Javascript code in several web
    pages, in such cases you can store Javascript code in external file and
    save file as &lt;filename&gt;.js file.
    Then this script can be made available to web page using src attribute of &lt;script&gt; tag e.g.<br/>
    &lt;script src=”external file URL”&gt;
    &lt;/script&gt;</li>
  <li>What are advantages of using external javascript?<br/>
    Placing JavaScript code in external js files has few advantages over inline scripts:<br/>
    <ul style="list-style-type="circle">
      <li>Segregating HTML and JavaScript code helps to manage the code base better.</li>
      <li>To improve development output designers can work along with coders in parallel without 
      code conflicts.</li>
      <li>This approach also works well with modern source code version control systems like GIT 
      and SVN.</li>
      <li>Each of these files can maintain history.</li>
      <li>Segregating HTML and JavaScript makes code as well as HTML is easily readable.</li>
      <li>Segregated external JavaScript files are cached by browsers and can speed up page load times.</li>
      <li>These small js files can be minified to reduce the size and make it not readable 
      by humans, using Google closure or YUI Compressor or other.</li>
      <li>Many popular JavaScript libraries are available as hosted on content delivery networks 
      (cdn) and you can simply point to them using the URL in the src, this avoids copying the 
      js file to local folder.</li>
      <li>Using external JS you can take benefits of advanced tools such as RequireJS or CommonJS 
      to load these scripts logically and modularly.</li>
    </ul>
  </li>
  <li>Is Javascript a case sensitive language?<br/>
    Yes, Javascript is case sensitive scripting language. Variables, functions, keywords 
    must have consistent casing otherwise it will not be recognized by Javascript and 
    will generate error. e.g.<br/>
      var pratik;<br/>
      var praTik;<br/>
    In above case pratik and praTik will be considered as different variables.</li>
  <li>Is Semicolon compulsory in Javascript at end of the statement?<br/>
    No, it is not necessary to use semicolon at end of the statement still it will be considered 
    as valid statement.</li>
  <li>What are different data types in Javascript?<br/>
    Below are basic data types in Javascript:<br/>
    <b>Primitive Data Types:</b>
    <ul style="list-style-type="square">
      <li>Number: Represent numeric values, both integer and float.</li>
      <li>String: Sequence of characters are represented using String.</li>
      <li>Boolean: Represent Boolean value, true or false.</li>
      <li>Undefined: Represent undefined value.</li>
      <li>Null: Represent null.</li>
    </ul>
    <b>Non-Primitive Data Types:</b>
    <ul style="list-style-type="disc">
      <li>Object: Represent more complex data structure.</li>
      <li>Array: Represent group of elements.</li>
      <li>RegExp: Represent regular expression.</li>
    </ul>
  </li>
  <li>How to add comment?<br/>
    JavaScript provides two kinds of comments:<br/>
    Single-line comments and multiline comments.<br/>
    Single-line comments start with // and are terminated by the end of the line:<br/>
    e.g. x++; // single-line comment<br/>
    Multiline comments are delimited by /&ast; and &ast;/:
    e.g. /&ast; This <br/>
      is a multiline<br/>
      comment.<br/>
    ​  &ast;/</li>
  <li>What is Javascript engine?<br/>
    JavaScript engine is a computer program used to execute Javascript code.
    JS engines were developed by web browser vendors and every major
    browser has one.<br/>
    Chrome V8 from google is most used engine, Google chrome use it.
    SpiderMonkey is developed by Mozilla for use in firefox.
    JavaScriptCore is Apples engine for its Safari browser.</li>
  <li>What are different Javascript frameworks that you know?<br/>
    Many frameworks are based on Javascript now, below are few of them:

| js framework  | &amp; library  | &amp; framework  | &amp; library  | &amp; framework  | &amp; library  |
|---|---|---|---|---|---|
| <a href="https://reactjs.org/" target="_blank">React</a>   | <a href="https://angularjs.org/" target="_blank">Angular</a>  | <a href="https://vuejs.org/" target="_blank">Vue.js</a>   | <a href="https://nodejs.org/en/" target="_blank">Node.js</a>   | <a href="https://expressjs.com/" target="_blank">Express.js</a>  | <a href="https://www.meteor.com/" target="_blank">Meteor.js</a> |
| <a href="https://nextjs.org/" target="_blank">Next.js</a>  | <a href="https://emberjs.com/" target="_blank">Ember.js</a>  | <a href="https://backbonejs.org/" target="_blank">Backbone.js</a>  | <a href="https://svelte.dev/" target="_blank">Svelte</a>  | <a href="https://www.gatsbyjs.com/" target="_blank">Gatsby</a>  | Remix  |
| <a href="https://nuxt.com/" target="_blank">Nuxt.js</a>  | Astro  | Solid  | <a href="https://github.com/CesiumGS/cesium" target="_blank">Cesium</a>  | <a href="https://zzz.dog/" target="_blank">Zdog</a>  | <a href="https://www.vantajs.com/" target="_blank">Vanta.js</a>  |
| <a href="https://github.com/micku7zu/vanilla-tilt.js" target="_blank">Tilt.js</a>  | <a href="https://github.com/micku7zu/vanilla-tilt.js" target="_blank">Tilt.js</a>  | <a href="https://threejs.org/" target="_blank">Three.js</a>  | <a href="https://www.sencha.com/products/extjs/" target="_blank">ExtJS</a>  | <a href="https://mithril.js.org/" target="_blank">Mithril</a>  | <a href="https://jquery.com/" target="_blank">jQuery</a>  |
| <a href="https://playcanvas.com/" target="_blank">PlayCanvas</a>  | <a href="https://polymer-library.polymer-project.org/" target="_blank">Polymer</a>  | <a href="http://aurelia.io/" target="_blank">Aurelia</a>  | <a href="https://alpinejs.dev/" target="_blank">Alpine.js</a>  | <a href="https://d3js.org/" target="_blank">D3.js</a>  | <a href="https://underscorejs.org/" target="_blank">Underscore.js</a>  |
| <a href="https://lodash.com/" target="_blank">Lodash</a>  | <a href="https://pixijs.com/" target="_blank">PixiJS</a>  | <a href="https://animejs.com/" target="_blank">Anime.js</a>  | <a href="https://rishabhp.github.io/bideo.js/" target="_blank">Bideo.js</a>  | <a href="https://www.chartjs.org/" target="_blank">Chart.js</a>  | <a href="https://nosir.github.io/cleave.js/" target="_blank">Cleave.js</a>  |
| <a href="https://glimmerjs.com/" target="_blank">Glimmer</a>  | <a href="https://sarcadass.github.io/granim.js/" target="_blank">Granim.js</a>  | <a href="https://github.com/alvarotrigo/fullPage.js/" target="_blank">fullPage.js</a>  | <a href="https://leafletjs.com/" target="_blank">Leaflet</a>  | <a href="https://multiple.js.org/" target="_blank">Multiple.js</a>  | <a href="https://momentjs.com/" target="_blank">Moment.js</a>  |
| <a href="https://masonry.desandro.com/" target="_blank">Masonry</a>  | <a href="http://omniscientjs.github.io/" target="_blank">Omniscient</a>  | <a href="http://parsleyjs.org/" target="_blank">Parsley</a>  | <a href="https://popper.js.org/" target="_blank">Popper.js</a>  | <a href="https://github.com/sindresorhus/screenfull.js/" target="_blank">Screenfull.js</a>  | <a href="https://vocajs.com/" target="_blank">Voca</a>  |
| <a href="https://getbootstrap.com/" target="_blank">Bootstrap</a> | <a href="https://mochajs.org/" target="_blank">Mocha</a> | <a href="https://ionicframework.com/" target="_blank">Ionic</a> | <a href="https://webix.com/" target="_blank">Webix</a> | <a href="https://p5js.org/" target="_blank">p5</a> | <a href="https://www.babylonjs.com/" target="_blank">Babylon.js</a> |
| <a href="https://github.com/aframevr/aframe" target="_blank">Aframe</a> | <a href="https://zeptojs.com/" target="_blank">Zepto</a> | <a href="https://createjs.com/" target="_blank">CreateJS</a> | <a href="https://nightwatchjs.org/" target="_blank">Nightwatch.js</a> | <a href="https://stimulus.hotwired.dev/" target="_blank">Stimulus</a> | <a href="https://nativescript.org/" target="_blank">NativeScript</a> |
| <a href="https://relay.dev/" target="_blank">Relay</a> | <a href="https://cycle.js.org/" target="_blank">Cycle.js</a> | <a href="https://flightjs.github.io/" target="_blank">Flight</a> | <a href="http://trykickoff.com/" target="_blank">Kickoff</a> | <a href="https://cylonjs.com/" target="_blank">Cylon.js</a> | <a href="https://jestjs.io/" target="_blank">Jest</a> |
| <a href="https://feathersjs.com/" target="_blank">Feathers</a> | <a href="http://bootboxjs.com/" target="_blank">Bootbox.js</a> | <a href="https://modernizr.com/" target="_blank">Modernizr</a> | <a href="https://cube.dev/" target="_blank">Cube.js</a> | <a href="https://requirejs.org/" target="_blank">RequireJS</a> | <a href="https://jasmine.github.io/" target="_blank">Jasmine</a> |
| <a href="https://qunitjs.com/" target="_blank">QUnit</a> | <a href="https://github.com/soulwire/sketch.js" target="_blank">sketch.js</a> | <a href="https://github.com/wso2/jaggery" target="_blank">Jaggery</a> | <a href="https://kangoextensions.com/" target="_blank">Kango</a> | <a href="https://www.cappuccino.dev/" target="_blank">Cappuccino</a> | <a href="https://konvajs.org/" target="_blank">Konva</a> |
| <a href="https://sproutcore.com/" target="_blank">SproutCore</a> | <a href="https://webix.com/" target="_blank">Webix</a> | <a href="https://github.com/quirkey/sammy" target="_blank">Sammy</a> | <a href="https://seemple.js.org/#!home" target="_blank">Seemple.js</a> | <a href="https://socket.io/" target="_blank">Socket.IO</a> | <a href="https://xstyled.dev/" target="_blank">xstyled</a> |
| <a href="http://vanilla-js.com/" target="_blank">VanillaJS</a> | <a href="https://github.com/linnovate/mean" target="_blank">MEAN</a> | <a href="https://github.com/flatiron/flatiron" target="_blank">Flatiron</a> | <a href="https://ripplejs.github.io/" target="_blank">ripple.js</a> | <a href="https://sailsjs.com/" target="_blank">Sails.js</a> | <a href="https://mochi.github.io/mochikit/" target="_blank">MochiKit</a> |
| <a href="https://optimizely.github.io/nuclear-js/" target="_blank">NuclearJS</a> | <a href="https://ampersandjs.com/" target="_blank">Ampersand.js</a> | <a href="https://heisenbergjs.github.io/heisenberg/" target="_blank">Heisenberg.js</a> | <a href="https://marionettejs.com/" target="_blank">Marionette</a> | <a href="https://pagerjs.com/" target="_blank">pager.js</a> | <a href="https://canjs.com/" target="_blank">CanJS</a> |
| <a href="http://rivetsjs.com/" target="_blank">Rivets.js</a> | Preact | Alpine | Aurealia | Polymer | Mithril |
| Backend JS: <b>Express</b> | Nest | Meteor |  |  |  |

  </li>
</ol>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<h2 id="2-vars">2. Variables, Operators and Statements</h2>  <!-- 15 thru 36 -->
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<ol start="15">
  <li>Explain variable in Javascript.<br/>
    Basically, variable is used for temporary storage of data. It has name, value and 
    memory address. You have to declare variable before using it for storing data.<br/>
    Below is syntax to declare variable: var variablename;<br/>
    Here var is keyword and variablename is name of the variable.<br/>
    You can also define multiple variables using single statement as:
	<pre>var variable1, variable2, variable3;</pre>
    Value can be assigned to variable as:
	<pre>var variablename = value;</pre>
  </li>
  <li>What is var?<br/>
    The var statement declares a variable and can also optionally initialize its value.<br/>
    Variables are declared using var as below,<br/>
    var varname1 &lbrack;= value1&rbrack; &lbrack;, varname2 &lbrack; = value2&rbrack; ... &lbrack;, varnameN
    &lbrack;= valueN&rbrack;&rback;];</li>
  <li>What is let?<br/>
    The ‘let’ allows you to declare variables that are limited in scope to
    the particular block, expression on which it is used or statement.
    Variables are declared using let as below,<br/>
    let var1 &lbrack;= value1&rbrack; &lbrack;, var2 &lbrack;= value2&rbrack;&rbrack; &lbrack;, ..., varN &lbrack;= valueN&rbrack;;</li>
  <li>What is const?<br/>
    Constants are block-scoped, much like variables defined using the let statement. The 
    value of a constant cannot change through reassignment, and it can't be re-declared.</li>
  <li>What is difference between let and var?<br/>
    The variable defined with var is available anywhere within the function hence ’var’ 
    keyword has function scope.<br/>
    The let has a Block Scope. A variable declared with ‘let’ keyword has a scope only with in that block.</li>
  <li>What is difference between let and const?<br/>
    ‘let’ allows you change the value of variable any number of times.
    Using ‘const’, after the first assignment of the value we cannot redefine the value again.</li>
  <li>What is automatic type conversion?<br/>
    When Javascript tries to operate on a wrong date type it will try to convert the 
    value to a “right” type.</li>
  <li>What are operators in Javascript?<br/>
    An operator is a symbol or word which is used to perform particular operation.<br/>
    Arithmetic, Assignment, Comparison, Logical and Conditional Operators are types of operators.</li>
  <li>Explain different types of operators in Javascript.<br/>
    Below are types of operators:<br/>
    <ul>
      <li>Arithmetic operators : Arithmetic operators are used to perform arithmetic between 
        variables and values. Addition (+), Subtraction (&dash;), Multiplication (&ast;), Division
        (/), Modulus (%), Increment (++) and Decrement (--) are arithmetic operators.</li>
      <li>Assignment operators : Assignment operators are used to assign values to variables. 
        =, +=, -=, *=, /=, %= are Assignment operators.</li>
      <li>Comparison operators : Comparison operators are used to compare variables or values. 
        Equal to (==), equal value and type (===), not equal (!=), not equal value or type 
        (!==), less than (&lt;), greater than (&gt;), less than or equal to (&lt;=) and 
        greater than or equal to (&gt;=) are comparison operators.</li>
      <li>Logical operators : Logical operators allow program to make decision based on multiple 
        conditions logic. Logical operators used for decision making are And (&amp;&amp;), or 
        (&vert;&vert;), not (!).</li>
      <li>Conditional operator : Conditional operators are used to assign values to variable 
        conditionally. (condition) ? value1: value2 is conditional operator.</li>
    </ul>
  </li>
  <li>What are control flow statements?<br/>
    You can change the sequence in which Javascript statements are executed by using control 
    flow statements. Below are types of control flow statements:<br/>
    Selection statements: Selection statements use condition to determine which group of 
    statements should be executed, if….else, if and switch are selection statements.<br/>
    Loops: Loops allow you to execute group of statements repeatedly till a condition is 
    satisfied, while, do…while and for are loops.<br/>
    Jump statements: Jump statements are used to break or exit loop, break and continue 
    are jump statements.</li>
  <li>What is break statement?<br/>
    Break statement stops execution of loop entirely.</li>
  <li>What is continue statement?<br/>
    Continue statement stops execution of current iteration in a loop and
    continues with next iteration of loop.</li>
  <li>What is the difference between comparing variables using "==" and "===" operator?
    The ‘==’ operator tests for abstract equality i.e. it does the required
    type conversions before doing the equality comparison.
    But the ‘===’ operator tests for strict equality i.e. it will not do the
    type conversion thus if the two values are not of the same type, when
    compared, it will return false.</li>
  <li>What is typeof operator?<br/>
    The typeof operator is used to get the data type of its operand. The operand can be 
    either a literal or a data structure such as variable, function or an object. e.g.<br/>
    console.log(typeof somevar);<br/>
    The typeof operator returns below values as string: object, Boolean, function, 
    number, string and undefined.</li>
  <li>What is variable hoisting?<br/>
    In Javascript regardless of where the actual declaration has been
    made, all variable declarations that are using var, are hoisted/lifted
    to the top of their functional/local scope (if declared inside a
    function) or to the top of their global scope (if declared outside of a
    function).
    This lifting of scopes is called hoisting. Hence,
<pre>​bla = 2;
var bla;
// ...is implicitly understood as:
var bla;
bla = 2;</pre>
  </li>
  <li>What is difference between undefined and null?<br/>
    The undefined means a variable has been declared but has no value has yet been assigned.
    On the other hand, null is basically a value which has been assigned.
    Also, undefined is a type itself (undefined) while null is an object.
    Unassigned variables are initialized with a default value of undefined
    by JavaScript or undefined can be assigned to variable through code.
    Whereas JavaScript never sets a value to null. That must be done programmatically.</li>
  <li>What is output of null == undefined?<br/>
    null == undefined will return true.<br/>
    However, null === undefined will return false.</li>
  <li>What are escape characters?<br/>
    Escape characters (backslash) is used before special characters like
    ampersand, single quotes, double quotes and apostrophes to display them. e.g.
<pre>console.log(‘I\’m Brian Bauska’); ☐ Correct syntax
console.log(‘I’m Brian Bauska’); ☐ Syntax error</pre>
    In above example, if backslash is not used before single quotes this
    line will give syntax error.
  </li>
  <li>How to create array in javascript?<br/>
    You can define arrays using the array literal as follows-<br/>
<pre>var a = &lbrack;&rbrack;;
var b = &lbrack;1, 2, 3&rbrack;;</pre>
  </li>
  <li>How to create three dimensional array?<br/>
    You can define three dimensional arrays using the array as follows:<br/>
    var threedimensionalarray = &lbrack;&lbrack;&lbrack;&rbrack;&rbrack;&rbrack;;</li>
  <li>What are the variable naming conventions in JavaScript?<br/>
    The following rules are to be followed while naming variables in JavaScript:<br/>
    You are not allowed to use any of the reserved keyword as variable name.
    JavaScript variable names should not begin with a numbers (0-9).
    They must start with a letter or the underscore character.
    JavaScript variable names are case sensitive.</li>
  <li>Why you should not prefer to use global variables?<br/>
    Global variable can be created by many developers resulting in
    duplicate global variables.
    Duplicate variable can overwrite the value of your variable.</li>
</ol>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<h2 id="3-functions">3. Functions</h2>  <!-- 37 thru 54 -->
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<ol start="37">
  <li>What are functions?<br/>
    Function is a collection of statements which can be used anywhere in
    program, it is used to perform specific task.
    </li>
  <li>What are types of functions in Javascript?<br>
    Below are the types of functions:<br>
    <b>Named</b>: Functions which have name at the time of definition are named functions. e.g. 
	<pre>function print() {
  ​   console.log(“This is named function!!!”);
   }</pre>
   <b>Anonymous</b>: Functions which do not have names are anonymous functions.<br/>
   var print=function() {<br/>
  ​ console.log(“This is anonymous function!!!”);<br/>
   }</li>
  <li>What are frequently used built-in global functions?<br/>
    Alert(), prompt(),isNan(), eval(), isFinite(), confirm(), parseInt(),
    parseFloat(), escape(), unescape() are most frequently used built-in
    global functions.</li>
  <li>What is isNaN?<br/>
    It is a function which determine whether or not value is an illegal 
    number. The isNan() method returns true if the passed value is 
    NaN(Not a number) and is of type number, else it returns false.<br/>
    e.g.<br>
    Input: ‘213’<br/>
    Output: false<br/>
    Input:’hello’<br/>
    Output: true</li>
  <li>What is parseInt?<br/>
    The parseInt is a function which parses the string and returns the integer value found in string.</li>
  <li>What is alert?<br/>
    The alert() function is used to display information in message box.</li>
  <li>What is confirm?<br/>
    The confirm() function displays a message box with two buttons, Ok and cancel. When you click the 
    Ok button, the function returns true. When you click cancel button function returns false.</li>
  <li>What is charAt?<br/>
    The charAt() function returns character from specified index. e.g.
	<pre>var str=”Pratik”;
  ​ ​ console.log(str.charAt(0));
  ​ ​ Output : P</pre>
  <li>What is indexOf?<br/>
    This function returns the index within the calling string object of first occurrence 
    of the specified value and returns index of found occurrence or -1 if not found. e.g.
<pre>var str=”This is javascript book”;
console.log(str .indexOf(“javascript”));
Output: 8</pre>
  </li>
  <li>What are function scopes?<br/>
    Scope defines accessibility of function and its variables. In Javascript scope is 
    divided into two categories:<br/>
    <ul>
      <li><b>Global</b> : Function with global scope can be accessed anywhere in the program.</li>
      <li><b>Local</b> : Function with local scope can be accessed only within its parent function.</li>
    </ul></li>
  <li>What is strict mode?<br/>
    Strict mode prevents certain actions and throws more exceptions. The statement “use strict” 
    orders browser to use the Strict mode, which is a reduced and safer feature set of JavaScript.<br/>
    Strict mode eliminates some silent errors in JavaScript by changing them to throw errors.<br/>
    Strict mode resolves mistakes that make it difficult for JavaScript engines to perform optimizations 
    hence strict mode code can sometimes run faster than identical code that’s not strict mode.<br/>
    Strict mode forbids some syntax likely to be defined in future versions of ECMAScript.<br/>
    It prevents, or throws errors, when unsafe actions are taken (such as gaining access to the 
    global object). It disables features that are confusing or poorly thought out.
    Due to Strict mode it becomes easier to write secure JavaScript.<br/>
    Strict mode applies to individual functions or to entire scripts. It doesn't apply to block statements 
    enclosed in {} braces; attempting to apply it to such contexts does nothing.<br/>
    To invoke strict mode for an entire script, put statement "use strict" before any other statements.<br/>
    To invoke strict mode for a function, put statement "use strict" in the function's body 
    before any other statements.</li>
  <li>What is function closure?<br/>
    A closure is a feature in JavaScript where an inner function has access to the outer (enclosing) function’s variables.</li>
  <li>What is callback function?<br/>
    A function passed into another function as an argument, which is then invoked inside the outer 
    function to complete some kind action is called as callback function. e.g.
<pre>function showName(name) {
  alert('User name is:' + name);
}
function displayName(callback) {
  var name = prompt('Please enter name to be displayed');
  callback(name);
}
displayName(showName);</pre>
  </li>
  <li>What is setTimeout function?<br/>
    The setTimeout() function executes function at specified interval.<br/>
    setTimeout(expression, timeout);<br/>
    Here, expression is the function/code that is called only once and timeout is number of milliseconds 
    to wait before calling the function. The clearTimeout() function is used to deactivate or 
    cancel timer set by setTimeout() fuction.</li>
  <li>What is setInterval function?<br/>
    The setInterval() function executes a function after a specified time interval.<br/>
   ​ setInterval(expression, timeout);<br/>
    Here, expression specifies function/code to be called after particular time interval and timeout 
    specifies the time interval between function calls.<br/>
    The clearInterval() function is used to cancel or deactivate the timer set by 
    setInterval() function.</li>
  <li>What is difference between setInterval and setTimeout functions?<br/>
    The setTimeout(expression, timeout) runs the function once after timeout
    The setInterval(expression, timeout) runs the function in intervals repeatedly, with 
    length of timeout between them.</li>
  <li>What is encodeURI() method?<br/>
    The encodeURI() method encodes a Uniform Resource Identifier by replacing each 
    instance of particular characters by one, two, three or four escape sequences 
    representing UTF-8 encoding of character.</li>
  <li>What is decodeURI() method?<br/>
    The decodeURI() method decodes a Uniform Resource Identifier previously created by 
    encodeURI().</li>
</ol>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<h2 id="4-events">4. Events</h2>  <!-- 55 thru 64 -->
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<ol start="55">
  <li>What are Events?<br/>
    Events are actions or occurrences that happen in the system you are programming to 
	which you can respond in some way. Events are handled by function known as event handler.</li>
  <li>What are different events in Javascript?<br/>
    Few of the important events are listed below:<br/>
	<b><i>Input Events</i></b><br/>
    - • onsubmit - triggers on submitting a form.<br/>
	- • onselect - triggers on selecting an element.<br/>
	- • onchange - triggers when changes happen to an element.<br/>
	- • onfocus - triggers when windows gets focus.<br/>
	- • onreset - triggers when user clicks reset button.<br/>
    - • onblur - triggers when window loses focus.<br/>
    - • onkeyup - triggers on releasing a key.<br/>
    - • onkeydown - triggers on pressing a key.<br/>
    <b><i>Click Events</i></b><br/>
    - • onclick - trigger on clicking a mouse button.<br/>
    - • ondblclick - triggers on double clicking mouse button.<br/>
    <b><i>Mouse Events</i></b><br/>
    - • ondrag - triggers when element is dragged.<br/>
    - • ondragend - triggers when drag ends.<br/>
    - • ondragstart - triggers when drag starts.<br/>
    - • ondragenter - triggers when dragged element is dropped.<br/>
    - • ondragleave - triggers on leaving target while dragging element.<br/>
    - • onmouseover - triggers when mouse pointer moves over element.<br/>
    - • onmousedown - triggers on pressing mouse button.<br/>
    - • onmouseup - triggers on releasing mouse button.<br/>
    - • onscroll -​ triggers on scrolling a scroll bar of an element.<br/>
	<b><i>Load Events</i></b><br/>
    - • onload- triggers when page has been loaded.<br/>
    - • onerror- triggers when an error occurs when loading an image.<br/>
    - • onunload- triggers when browser closes document.</li>
  <li>What are event handlers?<br/>
    Event handler is a routine that is used to deal with event, allowing programmers to 
	write code that will be executed when event occurs.</li>
  <li>What is addEventListener() method?<br/>
    The addEventListener() method attaches an event handler to specified element.
    You can add multiple event handlers to one element. It is possible to add event 
	listener to any DOM object. e.g.
<pre>document.getElementById(“someUniqueDivId”).addEventListener(“click”, respondtoclick);
function respondtoclick() {
  console.log(“Do some stuff!!!”);
}</pre>
  </li>
  <li>How to remove event listener from any element?<br/>
The removeEventListener() is an inbuilt function in JavaScript which
removes an event handler from an element for attached event.
Below example show how to remove event listener which was added
in previous example. e.g.
<pre>document.getElementById(“someUniqueDivId”).removeEventListener("click", respondtoclick);</pre>
</li>
  <li>What are different key codes?<br/>
It is necessary to know the codes associated with keys to identify
which key is pressed in the code.<br/>
Below table gives key codes:<br/>
<pre>
Key
CodeKey
CodeKey
CodeKey
Code
backspace 8
A 65
numpad 0 96
semi-colon 186
Tab 9
B 66
numpad 1 97
equal sign 187
Enter 13
C 67
numpad 2 98
comma 188
Shift 16
D 68
numpad 3 99
dash 189
Ctrl
17E
69numpad 4
100period
190
Alt
18F
70numpad 5
101forward slash 191
pause/break
19G
71numpad 6
102grave accent
192
caps lock
20H
72numpad 7
103open bracket
219
escape
27I
73numpad 8
104back slash
220
page up
33J
74numpad 9
105close braket
221
page down
34K
75multiply
106single quote
222
End
35L
76add
107
home
36M
77subtract
109
left arrow
37N
78decimal point 110
up arrow
38O
79divide
111
right arrow
39P
80f1
112
down arrow
40Q
81f2
113
insert
45R
82f3
114
delete
46S
83f4
115
0
48T
84f5
116
1
49U
85f6
117
2
50V
86f7
118
3
51W
87f8
119
4
52X
88f9
120
5
53Y
89f10
121
6
54Z
90f11
122
7
55left window key
91f12
123
8
56right window key
92num lock
144
9
57select key
93scroll lock
145
</pre>
</li>
<li>What is event bubbling?<br/>
When an event happens on an element, it first runs the handlers on
that particular element, after that handlers on its parent runs, this
happens all the way up on all other ancestors.
This bubbling of events from child to parent is called event bubbling.
A click on inner &lt;p&gt; first runs onclick on that &lt;p&gt;, then on outer
&lt;div&gt;, then on outer &lt;form&gt; and so on till document object.
This process is called “bubbling”, because events “bubble” from the
inner element up through parent like a bubble in the water.</li>
  <li>Is it possible to stop event bubbling?<br/>
Yes, by using method event.stopPropagation().
If you want to stop the event flow from event target to top element
in DOM, event.stopPropagation() method stops the event to travel to
the bottom to top.</li>
<li>What is event capturing?<br/>
In the capturing phase:<br/>
The browser checks to see if the element's outer-most ancestor
(&lt;html&gt;) has an onclick event handler registered on it during the
capturing phase, and runs it if so.
Then it moves on to the next element inside &lt;html&gt; and does the
same thing, then the next one, and so on until it reaches the element
that was actually clicked on.
The capturing phase is not often used. Usually it is invisible to us.</li>
<li>What is event delegation?<br/>
Event delegation concept relies on the fact that if you want some
code to run when you click on any one of a large number of grouped
child elements, you can set the event listener on their parent and
have events that happen on them bubble up to their parent, instead
of having to set the event listener on every child individually.
A good example is a series of list items &lt;li&gt; — You can set
the click event listener on the parent &lt;ul&gt;, if you want each one of
them&lt;li&gt; to pop up a message when clicked and it will bubble to
the list items.</li>
</ol>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<h2 id="5-objects">5. Objects</h2>  <!-- 65 - 81 -->
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<ol start="65">
  <li>What is Object?<br/>
The object is collection of properties and methods.
Object in Javascript are variables as well. Object can have properties
any data types (String, Number, Boolean etc.).<br/>
Object properties can be primitive values, other objects and
functions. e.g.
<pre>var book = {
​  name : “Javascript Book”,
​  auther: “Pratik Bandal”,
​  pages: 100
}</pre>
  </li>
  <li>What are ways to create objects?<br/>
In Javascript you can create objects through following ways:
Using literals:
Using object literal you can basically create object by using name
value pairs inside curly {} braces.
e.g.
<pre>var book = {
​ name : “Javascript Book”,
​ auther: “Pratik Bandal”,
​ pages: 100
}</pre>
Using new keyword with built-in object constructor function:
Using new keyword you can create object and then set its properties
as below,
e.g.
<pre>var book= new Object();
person.name= "John";
person.auther= "Doe";
person.pages= 50;</pre>
Using new keyword with built-in user defined constructor function:
We first create a constructor function and then get objects using
‘new’ keyword. e.g.
<pre>function Book(name, author, pages) {
this.name = name;
this.author = author;
this.pages = pages;
}</pre>
And then we create Book object as below,
​  <pre>var book = new Book(“Javascript Book”, ”Pratik Bandal”, 100);</pre>
Using Object.create():
The Object.create() method creates a new object, using an existing
object as the prototype
of the newly created object.
e.g.
<pre>​ const person = {
​ ​ isHuman: false,
​ ​ printIntroduction: function () {
​ };​ ​ }​ ​ ​ console.log(`Am I human? ${this.isHuman}`);
​ const me = Object.create(person);</pre>
</li>
  <li>Which are built-in or native objects?<br/>
JavaScript provides Number, Boolean, String, Array, Date, Math,
RegExp which are built in objects.</li>
  <li>What is ‘this’ keyword?<br/>
The this keyword refers to the object it belongs to.
In an object method, this refers to the object to which method
belongs.
When used alone, the owner is the Global object, so this refers to the
Global object (Windows object).
In a function, this refers to the Global object (Windows object).
In strict mode, when used in a function, this is undefined.
In HTML event handlers, this refers to the element in html that
received the event.</li>
  <li>What is String object?<br/>
String object is basically sequence of characters. String object
provides number of methods to perform required operations on
String object.
It provides methods like charAt(), charCodeAt(), concat(), indexOf(),
match(), slice(), split(), substr(), toLowerCase(), toUpperCase(),
valueOf(), toString() which provides important functionalities that
can be performed on string.</li>
  <li>What is Number object?<br/>
The number is Javascript wrapper object which allows you to work
with numerical values.
Number object is created as,
<pre>var numberVar = new Number(&lbrack;value&rbrack;);</pre>
It provides methods like
<pre>isNaN(),
isFinite(),
isInteger(),
isSafeInteger(), parseInt(), parseFloat() to work with numbers.</pre>
</li>
  <li>What is Boolean object?<br/>
The Boolean object wraps a boolean value.
Boolean object is created as,
var booleanVar = new Boolean([value]).
If the value is omitted or is 0, -0, null, false, NaN, undefined, or the
empty string (""), the object has an initial value of false. All other
values, including any object or the string "false", create an object
with an initial value of true.</li>
  <li>Explain about Array object.<br/>
The Array is a global object that is used to store different elements
for the construction of arrays.
Array object is created as,
<pre>new Array(ele0, ele1&lbrack;, ...&lbrack;, eleN&rbrack;&rbrack;)
new Array(arrayLength)
</pre></li>
  <li>Explain about Date object.<br/>
The JavaScript Date object represents a single moment in time. Date
objects use a unix timestamp which is a integer value that is number
of milliseconds since 1 January 1970.
Date object is created as,
<pre>new Date();
new Date(value);
new Date(dateString);
new Date(year, monthIndex &lbrack;, day &lbrack;, hours &lbrack;, minutes &lbrack;, seconds &lbrack;, milliseconds&rbrack;&rbrack;&rbrack;&rbrack;);</pre>
</li>
  <li>Explain about Math object.<br/>
Math is a built-in object that has methods and properties for
mathematical constants and functions.
Unlike the other global objects, Math does not have a constructor. All
methods and properties of Math are static.
It provides methods like sin(x), cos(x), tan(x), exp(x), floor(x),
max(&lbrack;x&lbrack;, y&lbrack;, …&rbrack;&rbrack;), min(&lbrack;x&lbrack;, y&lbrack;, …&rbrack;&rbrack;&rbrack;), pow(x, y), random(),
round(x), trunc(x) for mathematical operations.</li>
  <li>Explain about RegExp object.<br/>
The RegExp constructor is used to create a regular expression object
for matching text with a pattern.
Date object is created as,
<pre>new RegExp(pattern&lbrack;, flags&rbrack;)</pre></li>
  <li>What is namespace<br/>
In JavaScript, namespace is a single global object which will contain
all our functions, methods, variables.
Javascript don’t provide default namespace you have to create it, so
all functions, variables and object in Javascript are by default global.</li>
  <li>How to create namespace?<br/>
Below is example to create namespace and access function within it:
<pre>var myProjectNameSpace = {
​  projectfunctionone: function() {},
  projectfunctiontwo: function() {}
}
...
myProjectNameSpace. Projectfunctionone();</pre>
</li>
  <li>What is prototype in javascript?<br/>
All objects in Javascript have property called as prototype,
the prototype is an object which has a constructor properties by
default.
The prototype object is associated with every functions and objects
by default in JavaScript, where function's prototype property is
accessible and modifiable and object's prototype property is not
visible.
The prototype property allows you to add properties and methods to
any object. e.g.
<pre>somecustomcreationobject.prototype.age=29;</pre>
</li>
  <li>What is prototypal inheritance?<br/>
Object have property called as prototype which can refer to other
object.
When you want to read a property from object, and it’s missing,
JavaScript automatically takes it from the prototype. This is called
“prototypal inheritance”.</li>
  <li>What is difference between call() and apply()?<br/>
The Function.prototype.call() method calls a function with a
provided this value and arguments provided individually.
It is necessary to know arguments of function when using call()
method.
The Function.prototype.apply() method calls a function with a
provided this value, and arguments provided as an array (or an
array-like object).
It is necessary to know arguments of function when using apply()
method.</li>
  <li>What is Promise?<br/>
The Promise object represents the eventual completion (or failure) of
an asynchronous operation along with its resulting value.
A Promise is a proxy for a value which may or may not be known
when the promise is created.
It allows you to associate handlers with an asynchronous action's
eventual success value or failure reason.
This enables asynchronous methods return values like synchronous
methods: instead of immediately returning final value, the
asynchronous method returns a promise to provide the value at some
point in the future.</li>
</ol>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<h2 id="6-bom">6. Browser Object Model</h2>  <!-- 82 - 96 -->
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<ol start="82">
  <li>What is Browser Object Model?<br/>
The browser object model (BOM) is a hierarchy of browser objects
that are used to manipulate methods and properties associated with
the Web browser itself.
The default object of browser is window means you can invoke all
the functions of window by specifying window or directly
Objects that make up the BOM include the window object, navigator
object, screen object, location object, history, and the document
object.</li>
  <li>What is Window Object?<br/>
In a tabbed browser, each tab is represented as Window object.
Every object, variable, and function defined in a web page uses of
the window as its Global object.
Window object provides methods like alert(), blur(), close(),
confirm(), print(), prompt(), open().</li>
  <li>What alert method in window object?<br/>
Alert dialogs are typically used when users has to be made aware of
something that they have no control over, such as errors.
Often alert dialogs pops up when the user enters invalid data into a
form.<br/>
When alert() is called,the browser creates a system message box that
displays the given text with an OK button.<br/>
For example, the following line of code causes the message box in to
be displayed:
<pre>alert(“Your error message!!!”);</pre>
</li>
  <li>Explain confirm method of window object.<br/>
A confirm dialog appears similar to an alert dialog.
The main difference between them is the presence of a Cancel button
along with the OK button in the confirm dialog, which allows the
user to confirm if a given action should be taken.<br/>
For example, the following line of code displays the confirm dialog
shown in Figure 
<pre>confirm(“Do you wish to proceed?”);</pre>
</li>
<li>Explain prompt method of window object.<br/>
The prompt method is used to display dialog with input from user.
Along with OK and Cancel buttons, prompt dialog also has a text box
where the user is asked to enter some data.<br/>
The prompt() method accepts two arguments: the text to display to
the user and the default value for the text box (which can be an
empty string if you so desire). The following line results in the
window displayed:
<pre>prompt("Enter the country","USA");</pre></li>
  <li>How to redirect other webpage?<br/>
It is possible to redirect to other webpage in javascript by directly
assigning value to window.location or by using
location.assign(),location.replace() and location.reload() methods.</li>
  <li>What is Navigator Object?<br/>
The navigator object is used to get browser information like name,
version, type, language. It has methods like javaEnabled() and
taintEnabled().</li>
  <li>How to identify operating system of client device?<br/>
“Navigator.appVersion” is used to find operating system of client
device.</li>
  <li>What is History Object?<br/>
The History object consist of array of URLs which are visited by a
user in browser.
History object provides method like back(), forward() and go().</li>
  <li>How to load previous page in browser programmatically?<br/>
history.back() can be used to load previous page in browser through
code.</li>
  <li>How to load next page in browser programmatically?<br/>
history.forward() can be used to load next page in browser through
code.</li>
  <li>What is go method of history object?<br/>
The go() method loads a specific URL from the history list.
history.go(number|URL)<br/>
number|URL parameter can either be a number which goes to the
URL within the specific position (1 goes forward one page, -1 goes
back one page), or a string. The string has to be a partial or full URL,
and the function will go to the first URL that matches the string.</li>
  <li>What is Screen Object?<br/>
The Screen object consist of information about display screen like
height, width and colour bits of screen.</li>
  <li>What is Location Object?<br/>
The Location object consist of information about current URL of
window object.
Location object provides methods like assign(), reload and replace().</li>
  <li>How to print a web page?<br/>
The window.print() will print the current web page when invoked.</li>
</ol>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<h2 id="7-dom">7. Document Object Model</h2>  <!-- 97 thru 111 -->
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<ol start="97">
  <li>What is Document Object?<br/>
The Document object represents HTML document that is displayed in
window. Document object has properties which allows access and
modification of document content.
The way document is accessed and modified is called Document
Object Model or DOM.<br/>
Document object provides methods like open(), close(), write(),
getElementById(), getElementByName(), getElementByTagName().</li>
  <li>What is DOM?<br/>
The Document Object Model (DOM) represents HTML or XML page
in such a way that programs can change document structure, content
and style.<br/>
The DOM represents the document as nodes as well as objects.<br/>
The DOM is object oriented representation of web page, which can
be modified by scripting language like Javascript.</li>
  <li>What are DOM nodes?<br/>
According to the W3C HTML DOM standards, everything in HTML
can be represented as nodes.<br/>
Document node represents whole document.<br/>
Element node represents every HTML element such as HTML, HEAD,
BODY, A, H1 etc.<br/>
Text node represents text content inside the element.
Attribute node represents every HTML attribute.<br/>
Node has node properties that contain information about the node<br/>
The nodeName property specifies name of the node.<br/>
The nodeValue property specifies value of the node.<br/>
The nodeType property specifies type of the node.</li>
  <li>How to get element with id in DOM?<br/>
The getElementById() method of document object can be used to get
element using id. e.g.
<pre>document.getElementById(“myUniqueId”);</pre></li>
  <li>How to get element using class in DOM?<br/>
The getElementByClassName() method of document object can be
used to get element using class. e.g.
<pre>document.getElementByClassName(“myClass”);</pre></li>
  <li>How to get content of any element?<br/>
The innerHTML property is useful for getting or replacing the
content of HTML elements.</li>
  <li>What are DOM levels?<br/>
The W3C DOM specifications are divided into different levels where
each level contain some required and optional modules.<br/>
Level 0: Provide low-level set of interfaces.<br/>
Level1: DOM level 1 can be described in two parts: CORE and HTML.<br/>
CORE provides a low level interfaces that can be used to represent
any structured document.<br/>
HTML provides high-level interfaces that can be used to represent
HTML document.<br/>
Level2: Consist of six specifications:<br/>
CORE2, VIEWS, EVENTS, STYLE, TRAVERSAL and RANGE.<br/>
CORE2: extends functionality of CORE specified by DOM level 1.<br/>
VIEWS: views allow programs to dynamically access and manipulate
content of document.<br/>
EVENTS: events are scripts that are executed when user reacts to web page.<br/>
STYLES: allow programs to dynamically access and manipulate
content of style sheets.<br/>
TRAVERSAL: allows programs to dynamically traverse the document.<br/>
RANGE: allows programs to dynamically identify range of content in
document.<br/>
Level3: consists of five different specifications: CORE3, LOAD, SAVE,
VALIDATIONS, EVENTS and XPATH.<br/>
CORE3: extents functionality of CORE specified by DOM level 2.
LOAD and SAVE: allows program to dynamically load the content of
XML document into DOM document and save DOM document into
XML document by serialization.<br/>
VALIDATION: allows program to dynamically update the content and
structure of document while ensuring the document is valid.<br/>
EVENTS: extents functionality of Events specified by DOM level 2.<br/>
XPATH: XPATH is a path language that can be used to access DOM
tree.</li>
  <li>What are deferred scripts?<br/>
By default, Javascript files will interrupt parsing of HTML document
in order for them to be fetched and executed.<br/>
The defer attribute tells browser to only execute the script file once
the HTML document has been fully parsed.<br/>
&lt;script defer src=”myscript.js”&gt;<br/>
This reduces loading time of web page and web page is displayed
faster.</li>
  <li>What are asynchronous scripts?<br/>
By default, Javascript files will interrupt parsing of HTML document
in order for them to be fetched and executed.<br/>
The async attribute is used to indicate browser that script file can be
executed asynchronously.<br/>
&lt;script async src=”somescript.js”&gt;<br/>
The HTML parser does not have pause at the point it reaches the
script tag to fetch and execute, the execution can occur whenever the
script becomes ready after being fetched in parallel with document
parsing.</li>
  <li>What is difference between attribute and property?<br/>
Attributes: Provide more details on an element like id, type, value
etc.<br/>
Property: Value assigned to the property like type=”text”,
value=’Name’ etc.</li>
  <li>What is the difference between innerHTML & innerText?<br/>
innerHTML: It will process an HTML tag if found in a string<br/>
innerText: It will not process an HTML tag if found in a string</li>
  <li>What is the difference between textContent & innerText?<br/>
The textContent returns every element in the node.<br/>
The innerText is aware of styling and won't return the text of
“hidden” elements.</li>
  <li>What is HTMLCollection?<br/>
The HTMLCollection interface represents a generic collection of
elements (in document order) and offers methods & properties for
selecting from the list.<br/>
HTMLCollection has length property which returns the number of
items in the collection.<br/>
It is not possible to iterate over HTMLCollection list using forEach by
default.</li>
  <li>What is NodeList?<br/>
NodeList objects are collections of nodes which are usually returned
by properties such as Node.childNodes and functions such as document.querySelectorAll().<br/>
NodeList has length property which returns the number of nodes in nodelist.<br/>
for...of loops will loop over NodeList objects accurately.</li>
  <li>What are frames?<br/>
Frame divides page into section and in each section different page
can be displayed.</li>
</ol>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<h2 id="8-cookies">8. Cookies</h2>  <!-- 112 thru 120 -->
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<ol start="112">
  <li>What is cookie?<br/>
The Cookies are small items of data that consists of name and value
pair. Cookies are stored on your computer so that it can be accessed
by your web browser.<br/>
A web browser and server communicate through HTTP which is
stateless protocol.<br/>
Stateless protocol treats each request independently, so server does not 
keep data after sending it to browser. With cookies such data can be 
fetched directly from stored cookie file instead of communicating with server.
For example when user visits web page, user name can be stored in 
cookie. Now when next time user visits the page cookie belonging to
the page is added to the request. This way server gets necessary data
“remembered” by cookie.</li>
  <li>How cookie helps client server HTTP communication?<br/>
When a user sends a request to the server, then each of that request
is treated as a new request sent by the different user.
When receiving an HTTP request, a server can possibly send a Set-
Cookie header with the response.
Now, whenever a user sends a request to the server, the cookie is
added with that request automatically. Due to the cookie, the server
recognizes the users
Where are cookies stored?<br/>
During browsing session browser stored cookies in memory, at the
time of quitting they go to file called as cookies.txt.
Different browser store cookies file in a different location on disk.
For instance, on windows chrome stores the cookies in below
location, C:\Users\&lt;YourUser&gt;\AppData\Local\Google\Chrome
\User Data\Default\
As cookie expires it is no longer saved on hard drive.
115. Where are parameters of cookie?<br/>
There are six parameters of cookie: name, value, expires, path,
domain and security.<br/>
The name and value are required whereas all other parameters are
optional.
<pre>document.cookie=”name=VALUE;expires=DATE;path=PATH;domain=DOMAIN;secure”;</pre>
Name and Value : The first part of cookie must have name and
value. The entire name/value must be a single string with no
commas, semicolons or whitespace charactors.<br/>
Expires : The cookie will disappear when user exits the browser, to
give more life to the cookies you must set an expiration date in the
following format.<br/>
DD-Mon-YY HH:MM:SS GMT<br/>
Path : Usually the path is set to root level directory (‘/’), which
means the cookie is available for all the pages of your site. If you
want the cookie to be readable in specific directory &lt;directoryname&gt;,
path should be specified as path=&lt;directoryname&gt;.<br/>
Domain : Some websites have lots of domains. The purpose of the
‘domain’ is to allow cookies to other subdomains. In case, if website
is http://www.&lt;domain&gt;.com
with subdomains
http://www.&lt;subdomainone&gt;.&lt;domain&gt;.com
and http://www.&lt;subdomaintwo&gt;.&lt;domain&gt;.com.<br/>
If web page on subdomainone set a cookie pages on subdomaintwo cannot read that
cookie. But if you add domain=&lt;domain&gt; then all subdomains
ending with &lt;domain&gt; can read the cookie.<br/>
Secure : The last parameter of cookie is secure which is a Boolean
value. Its default value is false. If cookie is marked as secure then
cookie will be sent to web server and try to retrieve it using secure
communication channel.</li>
  <li>Can user disable cookies?<br/>
Yes, user can disable cookies from browser.
In chrome, you can go to settings--&gt;Advanced Settings--&gt;Privacy
and security--&gt;Content setting--&gt;Cookies and disable cookies.</li>
  <li>How to create cookie?<br/>
When visitor visits web page for first time he enters his or her name.
This name will be stored in cookies as below,
<pre>function createCookie(username, value) {
​ document.cookie=username + ”=” + value;
}</pre>
</li>
  <li>How to read cookie?<br/>
Javascript cookies can be read like this,
<pre>var x = document.cookie;</pre>
</li>
  <li>How to delete cookie?<br/>
While deleting cookie you don’t have to specify value.
Javascript cookies can be deleted by specifying expires parameter to
a past date.
<pre>
document.cookie=”username=; 
expires=Thu, 01 Jan 1970 00:00:00 UTC; path= /; ”;
</pre>
Some browsers will not let you delete cookie if you don’t specify the
path.</li>
  <li>What is difference between local storage and session storage?<br/>
Local Storage : For every HTTP request, the data is not sent back to
the server (HTML, images, JavaScript, CSS, etc) reducing the total
traffic between client and server. Data will stay until it is manually
cleared using settings or through program.<br/>
Session Storage : It is similar to local storage; the only difference is
data stored in local storage has no expiration time whereas data
stored in session storage gets cleared when the page session ends.
Session Storage will cleared when the browser is closed.</li>
</ol>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<h2 id="9-formValidation">9. Form validation</h2>  <!-- 121 thru 130 -->
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<ol start="121">
  <li>What is form validation?<br/>
Form validation verifies whether all fields in form are filled
according to required format.
If data entered by user is not according to format then appropriate
error message is displayed to the user.
Forms can be validated using server-side as well as client-side
validations.
Server-side validation is more secure and required server connection
to validate, whereas client-side validation is quicker and doesn’t
require server connection but it is less secure.
Javascript is used for client side validation.
Advantages of client side validation is that, it saves time, reduces
load on server and can validate form element even before form is
submitted.</li>
  <li>What is required attribute?<br/>
The required attribute in HTML element prevents that element being
submitted as blank.
e.g.
<pre>&lt;input type=”text” name=”employeename” required&gt;</pre>
In above case, as long as text field employeename is blank form
submission will be prevented.</li>
  <li>What is pattern attribute?<br/>
The pattern attribute specifies a regular expression against which
elements value is checked.
If element value does not match the regex pattern form submission
will be prevented.
e.g
<pre>&lt;input type=”text” name=”employeename” pattern=”&lbrack;A-Za-z&rbrack;”&gt;</pre>
In above case, if employee name contains value which is not
alphabet then form submission will be prevented.</li>
  <li>How to validate form using Javascript function?<br/>
Below example shows validation of form using Javascript.
Here, we have created form having name input and then when while
saving save validateName function will be called and it will validate
if name is blank.
<pre>&lt;script&gt;
function validateName() {
​ var name = document.nameform.name.value;
​ if(name==undefined || name==””) {
​ ​ alert(“Kindly enter the name!!!”);
​ ​ return false;
​ }
​ Return true;
}
&lt;/script&gt;
&lt;form
  name=”nameform”
  method=”post”
  onsubmit=”return
  validateform()”&gt;
  Name: &lt;input type=”text” name=”name”&gt;
  &lt;input type=”submit” name=”save”&gt;
&lt;/form&gt;</pre>
</li>
  <li>How to validate email in the form?<br/>
Below function can be used to validate email in the form.
<pre>function validateEmail(emailField){
  var reg = /^(&lbrack;A-Za-z0-9_\-\.&rbrack;)+\@(&lbrack;A-Za-z0-9_\-\.&rbrack;)+\.(&lbrack;A-
    Za-z&rbrack;{2,4})$/;
  if (reg.test(emailField.value) == false)
    {
    alert('Invalid Email Address');
    return false;
    }
  return true;
}</pre>
</li>
  <li>How to validate field without submitting form?<br/>
To validate field without submitting form you can use validation
function in onblur event of input field.<br/>
<pre>&lt;input type="text" onblur="validateEmail(this);" /&gt;</pre>
Here, input field will be available to validateEmail function.</li>
  <li>What is .test method?<br/>
The .test() API runs a search for a match between a regex and a
string.<br/>
The .test() API returns a Boolean(true/false), returns true if test
passes and false if it doesn’t.
Using .test() returns no data, so don’t expect any.</li>
  <li>What is .match method?<br/>
Using .match() is best when you are expecting data back in test
result, .match() returns an array with matches or simply null if there
are none.
With match you won’t just be testing for presence of data, you will
also see if data pattern exist and return that data.</li>
  <li>How to validate Date?<br/>
<pre>function validateDate(dateField) {
  var reg = /^([0-9]{2})\/([0-9]{2})\/([0-9]{4})$/
  if (reg.test(dateField.value) == false) {
    alert(“Invalid Date!!!”);
    return false;
  }
    return true;
  }</pre>
</li>
  <li>How to allow number only in input field?<br/>
<pre>function validateNumber(numField) {
  var reg = /^[0-9]+$/
  if (reg.test(numField.value) == false) {
    alert(“Invalid Number!!!”);
      return false;
  }
      return true;
  }</pre>
</li>
</ol>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<h2 id="10-errorHandling">10. Error and Exception Handling</h2>  <!-- 131 thru 135 -->
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<ol start="131">
  <li>What is error object?<br/>
When an exception occurs, an object representing the error is
constructed and thrown.<br/>
The Error constructor creates an error object.<br/>
When runtime errors occur, instances of Error objects are thrown.
The Error object can be used as a base object for user-defined
exceptions.
<pre>var error = new Error("error message");</pre>
“Error” objects contain two properties, “name” and “message”. The
“name” property specifies the type of exception The “message”
property provides a more detailed description of the exception.
The “message” gets its value from the string passed to the
constructor of exception.</li>
  <li>What are different error types in Javascript?<br/>
Below are primary error types in javascript:<br/>
SyntaxError : Raised when syntax error occurs while parsing the
Javascript code.<br/>
RangeError : Raised when numeric value exceeds allowed range.<br/>
EvalError : Raised when the eval() function is used in an incorrect
manner.<br/>
ReferenceError : Raised when an invalid reference is used<br/>
TypeError : Raised when type of variable is not as expected.<br/>
URIError : Raised when the encodeURI() or decodeURI() functions
are used in an inaccurate manner.<br/>
InternalError : Raised when internal error in the javascript engine is
thrown.</li>
  <li>How to handle exceptions in JavaScript?<br/>
JavaScript uses the try...catch...finally statement as well as the throw
operator to handle exceptions.<br/>
You can catch user-defined and runtime exceptions, but you cannot
catch JavaScript syntax errors.</li>
  <li>Explain try…catch…finally.<br/>
Try : wraps suspicious code that may throw an error in try block.<br/>
Catch : Write code to do something when error occurs in catch
block. The catch block can have parameters which will give you
error information. Usually, catch block is used to log an error or
display specific messages to the user.<br/>
Finally : code in finally block will always be executed regardless of
the occurrence of an error. The finally block is usually used to
complete the remaining task or reset variables that might have
changed before error occurred in try block.</li>
  <li>How to throw exceptions programmatically?<br/>
It is possible to throw exceptions programmatically using “throw”
statement.<br/>
There is no restriction on data type that can be thrown as an
exception. e.g.
<pre>throw “error occurred!!”;
throw new SyntaxError(“syntax error occurred!!”);</pre>
</li>
</ol>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<h2 id="11-debug">11. Debugging</h2>  <!-- 136 thru 145 -->
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<ol start="136">
  <li>136. What is debugging?<br/>
Debugging is the process of detecting and fixing existing and
potential errors in software code that can cause it to behave
unexpectedly.
To debug a program, programmer has to start with problem, identify
source of the problem and then fix it.
Sometimes it takes more time debugging a program than coding it.
  <li>What is debugger keyword?<br/>
Debugger statement stops the execution of Javascript. If debugging
functionality is not available, this statement has no effect.
Debugger keyword is like breakpoint in script source code.
e.g.
<pre>function someErroraniousFunction() {
​ debugger;
​ code;
}</pre>
  </li>What is console object?<br/>
Console object provides access to browsers debugging console.<br/>
If browser supports debugging you can use console.log() method to
display required text in debugging window.<br/>
Console object provides methods like debug(), log(), error(), info(),
trace(), warn() which are useful for code debugging.</li>
  <li>How to activate debugging in browser?<br/>
You can activate debugging in browser by pressing F12 and then
select console in debugger menu.</li>
  <li>How to get mobile devices view of webpage in desktop browser?<br/>
In browser press F12,
Then click on toggle device toolbar,
Then, select device for which you want webpage view.</li>
  <li>How to deactivate breakpoint in browser?<br/>
This can be done by clicking on “deactivate breakpoints” icon in
“Sources” tab of browser developer tool.</li>
  <li>How to pause script execution?<br/>
This can be done by clicking on “pause script execution” icon in
“Sources” tab of browser developer tool.</li>
  <li>How to execute function line by line while debugging?<br/>
This can be done by clicking on "Step into next fnuction call" icon in
"Sources" tab of browser developer tool.<br/>
How to execute function without stepping into it while
debugging?<br/>
This can be done by clicking on “Step over next function call” icon in
“Sources” tab of browser developer tool.</li>
  <li>What is code smell?<br/>
In computer programming, a code smell is any characteristic in the
source code of a program which possibly indicates a deeper problem.
Determining what is a code smell and what is not a code smell is
subjective, and varies by language, developer, and development
methodology.<br/>
The two main know open source tools used for JavaScript code
analysis are JSLint and JSHint, the second being a fork of the first
one. There are however many different tools that try to achieve the
same goal and you might find something more suited to your own
needs</li>
</ol>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<h2 id="12-ajax">12. AJAX overview</h2>  <!-- 146 thru 151 -->
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<ol start="146">
  <li>What is AJAX?<br/>
AJAX stands for Asynchronous Javascript and XML. It is collection of
related technologies like Javascript, XML, JSON, HTML and
XMLHttpRequest etc.
AJAX allows you to send and receive data asynchronously without
reloading web page and hence makes web pages more fast and
interactive.</li>
  <li>What is difference between GET and POST?<br/>
<table border="1" style="width:200px">
  <thead>
    <tr>
      <th></th>
      <th>GET</th>
      <th>POST</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>History</td>
      <td>Parameters remain in browser history as they are part of URL.</td>
	  <td>Parameters are not saved in browser history.</td>
    </tr>
    <tr>
      <td>Security</td>
      <td>GET is less secure as data sent as part of URL.</td>
      <td>POST is more secure than GET because parameters are not stored in browser history.</td>
    </tr>
	<tr>
	  <td>Parameters</td>
	  <td>Parameter data is limited to what you can stuff in URL. Safest to use less than 2K of parameters.</td>
      <td>Parameters can contain uploaded data files and larger data than GET.</td>
	</tr>
	<tr>
	  <td>Caching</td>
      <td>Can be cached.</td>
      <td>Not cached.</td>
    </tr>
  </tbody>
</table></li>
  <li>What is XMLHttpRequest object?<br/>
XMLHttpRequest object is used for asynchronous communication
between client and server.<br/>
It provides methods like open(), send(), setRequestHeader() for
exchanging data between client and server.</li>
  <li>How to make HTTP GET call using AJAX?<br/>
To make HTTP call in AJAX, you first need to initialize a new
XMLHttpRequest() object.<br/>
Specify URL endpoint, HTTP method (GET) to open() method of
XMLHttpRequest() object.<br/>
Then call send() method to hit the request.<br/>
Receive the response using XMLHttpRequest.onreadystatechange
property. e.g.
<pre>const xmlHttpRequest = new XMLHttpRequest();
xmlHttpRequest.open(“GET”,”http://some.domain.com/method”);
xmlHttpRequest.send();
xmlHttpRequest.onreadystatechange=(e)=&gt;{
​ console.log(xmlHttpRequest.responceText);
}</pre></li>
  <li>How to make HTTP POST call using AJAX?<br/>
To make HTTP call in AJAX, you first need to initialize a new
XMLHttpRequest() object.<br/>
Specify URL endpoint, HTTP method (POST) to open() method of
XMLHttpRequest() object.<br/>
Then call send() and pass data to send() method to hit the request.
Receive the response using XMLHttpRequest.onreadystatechange
property. e.g.
<pre>const xmlHttpRequest = new XMLHttpRequest();
xmlHttpRequest.open(“POST”,”http://some.domain.com/method”);
xmlHttpRequest.send(“fname=Pratik&lname=Bandal”);
xmlHttpRequest.onreadystatechange=(e)=>{
​ console.log(xmlHttpRequest.responceText);
}</pre></li>
  <li>What are HTTP status codes?<br/>
HTTP status code are the standard response code given by web site
servers. These codes help identify the cause of problem when web
page or other resource does not load properly.<br/>
<b>4xx Client Error:</b><br/>
This category of HTTP status code includes those where request for a
web page or other resource contains bad syntax or cannot be filled
for some other reason, presumably due to fault of client.<br/>
Some common client error HTTP status codes are<br/>
<b>404 (Not Found)</b>, <b>403 (Forbidden) and 400 (Bad request).</b><br/>
<b>5xx Client Error:</b><br/>
This category of HTTP status code include those where the request
for a web page or other resource is understood by the websites server
but is incapable of filling it for some reason.<br/>
Some common server error HTTP status codes are<br/>
<b>500 (Internal server error), 503 (Service Unavailable) and 502 (Bad Gateway).</b><br/>
There are also <b>1xx, 2xx and 3xx</b> code that are informational, confirm
success or dictate redirection which are not errors, so you shouldn’t
be alerted about them.<br/></li>
</ol>
<p>You may also like to read (available on amazon):<br/>
Angular Interview Questions and Answers: Includes Angular 8, 7, 6, 5, 4 and 2<br/>
Core Java Interview Questions and Answers: Includes Java 12, 11, 10, ...<br/>
That does it.  the end...</p>
