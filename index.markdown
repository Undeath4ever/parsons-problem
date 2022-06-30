<div id="Hello_World-sortableTrash" class="sortable-code"></div> 
<div id="Hello_World-sortable" class="sortable-code"></div> 
<div style="clear:both;"></div> 
<p> 
    <input id="Hello_World-feedbackLink" value="Get Feedback" type="button" /> 
    <input id="Hello_World-newInstanceLink" value="Reset Problem" type="button" /> 
</p> 
Wir wollen herausfinden, ob die eingetippte Zahl gerade oder ungerade ist.
Dies ist ein zweidiemensionales Parson Problem: bringe die Blöcke in die richtige Reihenfolge und achte auf die Python übliche einrückung deines codes. 
<script type="text/javascript"> 
(function(){
  var initial = "public static void main(String args[])\n" +
    "{\n" +
    "System.out.println(&quot;Hello World!&quot;)\n" +
    "}\n" +
    "print(Hello World!) #distractor";
  var parsonsPuzzle = new ParsonsWidget({
    "sortableId": "Hello_World-sortable",
    "max_wrong_lines": 10,
    "grader": ParsonsWidget._graders.LineBasedGrader,
    "exec_limit": 2500,
    "can_indent": false,
    "x_indent": 50,
    "lang": "en",
    "show_feedback": true,
    "trashId": "Hello_World-sortableTrash"
  });
  parsonsPuzzle.init(initial);
  parsonsPuzzle.shuffleLines();
  $("#Hello_World-newInstanceLink").click(function(event){ 
      event.preventDefault(); 
      parsonsPuzzle.shuffleLines(); 
  }); 
  $("#Hello_World-feedbackLink").click(function(event){ 
      event.preventDefault(); 
      parsonsPuzzle.getFeedback(); 
  }); 
})(); 
</script>

<div id="sortableTrash" class="sortable-code"></div> 
<div id="sortable" class="sortable-code"></div> 
<div style="clear:both;"></div> 
<p> 
    <input id="feedbackLink" value="Get Feedback" type="button" /> 
    <input id="newInstanceLink" value="Reset Problem" type="button" /> 
</p> 
<script type="text/javascript"> 
(function(){
  var initial = "num = input(&quot;Wähle eine Zahl: &quot;)\n" +
    "mod = num % 2\n" +
    "if mod &gt; 0:\n" +
    "    print(&quot;Deine Zahl ist ungerade.&quot;)\n" +
    "else:\n" +
    "    print(&quot;Deine Zahl ist gerade.&quot;)\n" +
    "print(Deine Zahl ist ungerade.) #distractor\n" +
    "print(Deine Zahl ist gerade.) #distractor";
  var parsonsPuzzle = new ParsonsWidget({
    "sortableId": "sortable",
    "max_wrong_lines": 10,
    "grader": ParsonsWidget._graders.LineBasedGrader,
    "exec_limit": 2500,
    "can_indent": true,
    "x_indent": 50,
    "lang": "en",
    "show_feedback": true,
    "trashId": "sortableTrash"
  });
  parsonsPuzzle.init(initial);
  parsonsPuzzle.shuffleLines();
  $("#newInstanceLink").click(function(event){ 
      event.preventDefault(); 
      parsonsPuzzle.shuffleLines(); 
  }); 
  $("#feedbackLink").click(function(event){ 
      event.preventDefault(); 
      parsonsPuzzle.getFeedback(); 
  }); 
})(); 
</script>
