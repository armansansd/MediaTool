MediaTool
=========

Signage Tool Hear


I'm using a "contenteditable" span,  
if you want to use a textarea, this javascript can help you :

```jQuery(function($){
	function copy_to_print_helper(){
		$('#title_print').text($('.title').val());
		  }
		$('.title').bind('keydown keyup keypress cut copy past blur change', function(){
		copy_to_print_helper(); // consider debouncing this to avoid slowdowns!
		  });
		 copy_to_print_helper(); // on initial page load
   });
