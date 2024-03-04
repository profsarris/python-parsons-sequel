---
# There are three Python exercises on this page.
# Try and solve them all!
<p>Drag or shuffle the blocks of code in the practice problems below. Remember to indent where appropriate by dragging blocks to the right. To check your work, press the “Get Feedback” button. To start over, press the “Reset Problem” button.</p>
<h3>Q1</h3>
<p> This first program will take a list of colors and a list of shapes. It will then combine every possible color and shape and print them to the screen.</p>
<p> To get your solution in the same order that the grader expects, if two statements could be in either order, choose the statement dealing with <b>color</b> <i>first</i> and <b>shape</b> <i>second</i>.</p>
<p> To also help you out and give you a freebie, the statement initializing the new list should come <i>first</i></p>
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
  var initial = "result = []\n" +
    "colors = [&#039;red&#039;, &#039;yellow&#039;, &#039;blue&#039;]\n" +
    "shapes = [&#039;circle&#039;, &#039;triangle&#039;, &#039;square&#039;]\n" +
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
<code>18</code><br>
<p> This Parsons problem contains a <b>distractor</b> - a line of code that doesn't belong. Drag only the lines of code that belong from the left to the right. In this problem, there is only one line that doesn't belong.</p>

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
    "  return total\n" +
    "if num == 42: #distractor";
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

<p></p>
<h3>Q3</h3>
<p> This next problem is a function. Its purpose is to take in a list of colors, a list of things, and a filename. For each thing in the list of things, it will choose a random color from the list of colors and pair it with the thing, then write it to the file. Each color/thing pair will be separated by a space and written on its own line.</p>
<p>Example</p>
<p>If the parameters to the function are:</p>
<code>colors = ['red', 'yellow', 'blue']<br>
vehicles = ['car', 'truck', 'boat']<br>
filename = "/content/drive/My Drive/vehicles.txt"<br>
<p>then mixmaster(colors, vehicls, filename) should return:</p>
<code>red car<br>
yellow truck<br>
blue boat</code><br>
<p>Of course, each time you run this program, the colors will be different because they are randomly chosen.</p>
<p> This Parsons problem contains <b><i>two</i></b> <b>distractors</b> - lines of code that don't belong. Drag only the lines of code that belong from the left to the right. In this problem, there are two lines that don't belong.</p>

<div id="03-sortableTrash" class="sortable-code"></div> 
<div id="03-sortable" class="sortable-code"></div> 
<div style="clear:both;"></div> 
<p> 
    <input id="03-feedbackLink" value="Get Feedback" type="button" /> 
    <input id="03-newInstanceLink" value="Reset Problem" type="button" /> 
</p> 
<script type="text/javascript"> 
(function(){
  var initial = "import random\n" +
    "def mixmaster(colors, things, filename):\n" +
    "  with open(filename, &quot;w&quot;) as out:\n" +
    "    for thing in things:\n" +
    "      index = random.randint(0, len(colors)-1)\n" +
    "      color = colors[index]\n" +
    "      out.write(color + &quot; &quot; + thing + &quot;&#92;n&quot;)\n" +
    "with open(filename, &quot;r&quot;) as in: #distractor\n" +
    "for color in colors #distractor";
  var parsonsPuzzle = new ParsonsWidget({
    "sortableId": "03-sortable",
    "max_wrong_lines": 10,
    "grader": ParsonsWidget._graders.LineBasedGrader,
    "exec_limit": 2500,
    "can_indent": true,
    "x_indent": 50,
    "lang": "en",
    "show_feedback": true,
    "trashId": "03-sortableTrash"
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
