<div id="Hello_World-sortableTrash" class="sortable-code"></div> 
<div id="Hello_World-sortable" class="sortable-code"></div> 
<div style="clear:both;"></div> 
<p> 
    <input id="Hello_World-feedbackLink" value="Get Feedback" type="button" /> 
    <input id="Hello_World-newInstanceLink" value="Reset Problem" type="button" /> 
</p> 
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
