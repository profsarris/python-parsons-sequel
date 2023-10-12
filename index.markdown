---
# There are three Python exercises on this page.
# Try and solve them all!
<p>Drag or shuffle the blocks of code in the practice problems below. Remember to indent where appropriate by dragging blocks to the right. To check your work, press the “Get Feedback” button. To start over, press the “Reset Problem” button.</p>
<h3>Q1</h3>
<p> This first program will take a list of colors and a list of shapes. It will then combine every possible color and shape and print them to the screen.</p>
<p> To get your solution in the same order that the grader expects, if two statements could be in either order, choose the statement dealing with color first and shape second.</p>
<p>Example</p>
<code>['red circle', 'red triangle', 'red square', 'yellow circle', 'yellow triangle', 'yellow square', 'blue circle', 'blue triangle', 'blue square']<br>
</code>

<div id="01-sortableTrash" class="sortable-code"></div> 
<div id="01-sortable" class="sortable-code"></div> 
<div style="clear:both;"></div> 
<p> 
    <input id="01-feedbackLink" value="Get Feedback" type="button" /> 
    <input id="01-newInstanceLink" value="Reset Problem" type="button" /> 
</p> 
<script type="text/javascript"> 
(function(){
  var initial = "colors = [&#039;red&#039;, &#039;yellow&#039;, &#039;blue&#039;]\n" +
    "shapes = [&#039;circle&#039;, &#039;triangle&#039;, &#039;square&#039;]\n" +
    "result = []\n" +
    "for color in colors:\n" +
    "  for shape in shapes:\n" +
    "    result.append(color + &quot; &quot; + shape)\n" +
    "print (result)";
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
<h3>Q2</h3>
<p> This next problem is a function. Its purpose is to read from the file passed in. On each line of the file are numbers separated by spaces. totaler() will add all of the numbers together and return that number</p>
<p>Example</p>
<p>If the file numbers.txt contains:</p>
<code>1 1 1<br>
2 2 2<br>
3 3 3<br></code>
<p>then totaler("numbers.txt") should return:</p>
<code>18</code><br><p></p>
<div id="02-sortableTrash" class="sortable-code"></div> 
<div id="02-sortable" class="sortable-code"></div> 
<div style="clear:both;"></div> 
<p> 
    <input id="02-feedbackLink" value="Get Feedback" type="button" /> 
    <input id="02-newInstanceLink" value="Reset Problem" type="button" /> 
</p> 
<script type="text/javascript"> 
(function(){
  var initial = "def totaler(filename):\n" +
    "  total = 0\n" +
    "  with open(filename, &quot;r&quot;) as nums:\n" +
    "    for line in nums:\n" +
    "      numlist = line.split()\n" +
    "      for num in numlist:\n" +
    "        total = total + int(num)\n" +
    "  return total";
  var parsonsPuzzle = new ParsonsWidget({
    "sortableId": "02-sortable",
    "max_wrong_lines": 10,
    "grader": ParsonsWidget._graders.LineBasedGrader,
    "exec_limit": 2500,
    "can_indent": true,
    "x_indent": 50,
    "lang": "en",
    "show_feedback": true,
    "trashId": "02-sortableTrash"
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
