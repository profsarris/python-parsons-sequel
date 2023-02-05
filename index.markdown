---
# There are five Python exercises on this page.
# Try and solve them all!

layout: default
<p> This first program should ask the user for numbers until they type 'done'. Then the program should give the user the total of all the numbers they typed. </p>
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
    "  ans = int(resp)\n" +
    "  if int(ans) == (num + num):\n" +
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
