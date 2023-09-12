---
# There are five Python exercises on this page.
# Try and solve them all!
<p>Drag or shuffle the blocks of code in the practice problems below. Remember to indent where appropriate by dragging blocks to the right. To check your work, press the “Get Feedback” button. To start over, press the “Reset Problem” button.</p>
<h3>Q1</h3>
<p> This first program should ask the user for a number. The program will then count down from that number until it gets to zero, after which it will print 'Blast off!</p>
<p>Example</p>
<code>Enter a number: 5<br>
5<br>
4<br>
3<br>
2<br>
1<br>
0<br>
Blast off!</code>
<div id="02-sortableTrash" class="sortable-code"></div> 
<div id="02-sortable" class="sortable-code"></div> 
<div style="clear:both;"></div> 
<p> 
    <input id="02-feedbackLink" value="Get Feedback" type="button" /> 
    <input id="02-newInstanceLink" value="Reset Problem" type="button" /> 
</p> 
<script type="text/javascript"> 
(function(){
  var initial = "num = int(input(&quot;Enter a number: &quot;))\n" +
    "for count in range(num, -1, -1):\n" +
    "	print(count)\n" +
    "print(&quot;Blast off!&quot;)";
  var parsonsPuzzle = new ParsonsWidget({
    "sortableId": "02-sortable",
    "max_wrong_lines": 10,
    "grader": ParsonsWidget._graders.LineBasedGrader,
    "exec_limit": 2500,
    "can_indent": true,
    "x_indent": 50,
    "lang": "en",
    "show_feedback": true
  });
  parsonsPuzzle.init(initial);
  parsonsPuzzle.shuffleLines();
  $("#02-newInstanceLink").click(function(event){ 
      event.preventDefault(); 
      parsonsPuzzle.shuffleLines(); 
  }); 
  $("#02-feedbackLink").click(function(event){ 
      event.preventDefault(); 
      parsonsPuzzle.getFeedback(); 
  }); 
})(); 
</script>
<p></p>
<h3>Q2</h3>
<p> This next problem is a function. Its purpose is to find the largest number in a list of positive numbers.</p>
<p>Example</p>
<code>print(find_largest[5, 3, 1, 2, 10, 4, 2, 8]))<br>
10</code>
<p></p>
<div id="03-sortableTrash" class="sortable-code"></div> 
<div id="03-sortable" class="sortable-code"></div> 
<div style="clear:both;"></div> 
<p> 
    <input id="03-feedbackLink" value="Get Feedback" type="button" /> 
    <input id="03-newInstanceLink" value="Reset Problem" type="button" /> 
</p> 
<script type="text/javascript"> 
(function(){
  var initial = "def find_largest(numlist):\n" +
    "  smallest = -1\n" +
    "  for num in numlist:\n" +
    "    if num &gt; smallest:\n" +
    "      smallest = num\n" +
    "  return smallest";
  var parsonsPuzzle = new ParsonsWidget({
    "sortableId": "03-sortable",
    "max_wrong_lines": 10,
    "grader": ParsonsWidget._graders.LineBasedGrader,
    "exec_limit": 2500,
    "can_indent": true,
    "x_indent": 50,
    "lang": "en",
    "show_feedback": true
  });
  parsonsPuzzle.init(initial);
  parsonsPuzzle.shuffleLines();
  $("#03-newInstanceLink").click(function(event){ 
      event.preventDefault(); 
      parsonsPuzzle.shuffleLines(); 
  }); 
  $("#03-feedbackLink").click(function(event){ 
      event.preventDefault(); 
      parsonsPuzzle.getFeedback(); 
  }); 
})(); 
</script>
<p></p>
<h3>Q3</h3>
<p> This next program asks the user for numbers until the total sum of those numbers is greater than 20. If the user enters something that is not a number, the program will ignore the input and print a message to the user. Once the total sum is greater than 20, the program prints the total and ends.</p>
<p>Example</p>
<code>Enter a number: 7<br>
Enter a number: 5<br>
Enter a number: marshmallow<br>
Silly user! That's not a number!<br>
Enter a number: 6
Enter a number: 8
You total sum is 26</code>
<div id="04-sortableTrash" class="sortable-code"></div> 
<div id="04-sortable" class="sortable-code"></div> 
<div style="clear:both;"></div> 
<p> 
    <input id="04-feedbackLink" value="Get Feedback" type="button" /> 
    <input id="04-newInstanceLink" value="Reset Problem" type="button" /> 
</p> 
<script type="text/javascript"> 
(function(){
  var initial = "sum = 0\n" +
    "while sum &lt; 20:\n" +
    "  resp = input(&quot;Enter a number: &quot;)\n" +
    "  try:\n" +
    "    sum = sum + int(resp)\n" +
    "  except:\n" +
    "    print(&quot;Silly user. That&#039;s not a number!&quot;)\n" +
    "print(&quot;Your total sum is&quot;, sum)";
  var parsonsPuzzle = new ParsonsWidget({
    "sortableId": "04-sortable",
    "max_wrong_lines": 10,
    "grader": ParsonsWidget._graders.LineBasedGrader,
    "exec_limit": 2500,
    "can_indent": true,
    "x_indent": 50,
    "lang": "en",
    "show_feedback": true
  });
  parsonsPuzzle.init(initial);
  parsonsPuzzle.shuffleLines();
  $("#04-newInstanceLink").click(function(event){ 
      event.preventDefault(); 
      parsonsPuzzle.shuffleLines(); 
  }); 
  $("#04-feedbackLink").click(function(event){ 
      event.preventDefault(); 
      parsonsPuzzle.getFeedback(); 
  }); 
})(); 
</script>
<p></p>
<h3>Q4</h3>
<p> This next program should ask the user for numbers until they type 'quit'. Then the program should give the user the total of all the numbers they typed. </p>
<p>Example</p>
<code>Enter a number: 5<br>
Enter a number: 2<br>
Enter a number: 3<br>
Enter a number: quit<br>
Your total is 10</code>
<div id="01-sortableTrash" class="sortable-code"></div> 
<div id="01-sortable" class="sortable-code"></div> 
<div style="clear:both;"></div> 
<p> 
    <input id="01-feedbackLink" value="Get Feedback" type="button" /> 
    <input id="01-newInstanceLink" value="Reset Problem" type="button" /> 
</p> 
<script type="text/javascript"> 
(function(){
  var initial = "total = 0\n" +
    "while True:\n" +
    "  user_input = input(&quot;Enter a number: &quot;)\n" +
    "  if user_input == &quot;quit&quot;:\n" +
    "    break\n" +
    "  num = int(user_input)\n" +
    "  total = total + num\n" +
    "print(&quot;Your total is&quot;, total)";
  var parsonsPuzzle = new ParsonsWidget({
    "sortableId": "01-sortable",
    "max_wrong_lines": 10,
    "grader": ParsonsWidget._graders.LineBasedGrader,
    "exec_limit": 2500,
    "can_indent": true,
    "x_indent": 50,
    "lang": "en",
    "show_feedback": true
  });
  parsonsPuzzle.init(initial);
  parsonsPuzzle.shuffleLines();
  $("#01-newInstanceLink").click(function(event){ 
      event.preventDefault(); 
      parsonsPuzzle.shuffleLines(); 
  }); 
  $("#01-feedbackLink").click(function(event){ 
      event.preventDefault(); 
      parsonsPuzzle.getFeedback(); 
  }); 
})(); 
</script>
<p></p>
<h3>Q5</h3>
<p> This next program should create a random number and then ask a user a math question using that number. If the user enters the number correctly, the program says 'Correct!' otherwise it apologizes and gives the real answer. The program continues asking questions until the user enters 'done'.</p>
<p>Example</p>
<code>What is 12 + 12: 24<br>
Correct!<br>
What is 18 + 18: 42<br>
Sorry. The answer was 36<br>
What is 24 + 24: 48<br>
Correct!<br>
What is 47 + 47: done<br>
Thanks for playing and Bye!</code>
<p></p>
<div id="05-sortableTrash" class="sortable-code"></div> 
<div id="05-sortable" class="sortable-code"></div> 
<div style="clear:both;"></div> 
<p> 
    <input id="05-feedbackLink" value="Get Feedback" type="button" /> 
    <input id="05-newInstanceLink" value="Reset Problem" type="button" /> 
</p> 
<script type="text/javascript"> 
(function(){
  var initial = "import random\n" +
    "while True:\n" +
    "  num = random.randint(1, 100)\n" +
    "  question = &quot;What is &quot; + str(num) + &quot; + &quot; + str(num) + &quot;? &quot;\n" +
    "  resp = input(question)\n" +
    "  if resp == &quot;done&quot;:\n" +
    "    break\n" +
    "  if int(resp) == (num + num):\n" +
    "    print (&quot;Correct&quot;)\n" +
    "  else:\n" +
    "    print(&quot;Sorry. The answer was &quot;, str(num+num)) \n" +
    "print(&quot;Thanks for playing and Bye!&quot;)";
  var parsonsPuzzle = new ParsonsWidget({
    "sortableId": "05-sortable",
    "max_wrong_lines": 10,
    "grader": ParsonsWidget._graders.LineBasedGrader,
    "exec_limit": 2500,
    "can_indent": true,
    "x_indent": 50,
    "lang": "en",
    "show_feedback": true
  });
  parsonsPuzzle.init(initial);
  parsonsPuzzle.shuffleLines();
  $("#05-newInstanceLink").click(function(event){ 
      event.preventDefault(); 
      parsonsPuzzle.shuffleLines(); 
  }); 
  $("#05-feedbackLink").click(function(event){ 
      event.preventDefault(); 
      parsonsPuzzle.getFeedback(); 
  }); 
})(); 
</script>
