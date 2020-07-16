20200622212226

### JS Event Handlers

An event is handed to the top of the dom, from where it propagates down to the element onto which the event should be applied. It stands to reason, therefore, that **an event listener attached to the global object** will call its handler _prior_ to a listener that has been attached to the element itself.

E.g. if I have a click handler on the document object like so:

`$(document).click(function(e) {
		   if (!$(e.target).is('.panel-body')) {
       	$('.collapse').collapse('hide');	    
  }
  });`
  
  Then I add a .click handler on some div inside the body called "myDiv":
  
`$('#myDiv').click(function(e) {
		   if (!$(e.target).is('.panel-body')) {
       	alert("helloooo");	    
  }
  });`
  
  the result will be that .collapse will be hidden first, then alert('helloooo') will fire because document is the parent of (all elements and so also) '#myDiv' div element.
  
  #javascript #code #webdev #programming 