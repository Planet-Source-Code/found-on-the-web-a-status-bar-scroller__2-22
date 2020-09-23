<div align="center">

## A Status Bar Scroller


</div>

### Description

A scroller is text which scrolls on the status bar of the browser. Scrollers are very popular with JavaScript authors (esp. newbies like ourselves) and equally unpopular with the rest of the Web community. (Found at:A beginner's guide to Javascript:http://www.geocities.com/SiliconValley/Park/2554/scroller.html)
 
### More Info
 
How much programming does it take to create a scroller? Twenty lines, to be exact, as you will see. But before we go into the code, let us understand what features of JavaScript makes the scroller possible.

First is the ability to write to the status bar using the window.status property like this:

window.status = "This will appear in the status bar"

The second is the setTimeout() function. This function takes two parameters. The first is a string specifying the JavaScript statement to be executed on triggering and the second is a number specifing time in milliseconds after which triggering occurs.

Our scroller is essentially a function which, on each invocation, moves the text on the scroll bar a little to the left and then calls setTimeout() to invoke itself after a small interval of time.

The only other function we use is substring() which is a method of the string object. If name="JavaScript", then name.substring(4,9) will return "Script". You get the general idea, right?


<span>             |<span>
---                |---
**Submitted On**   |
**By**             |[Found on the Web](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByAuthor/found-on-the-web.md)
**Level**          |Unknown
**User Rating**    |4.3 (13 globes from 3 users)
**Compatibility**  |
**Category**       |[Graphics](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByCategory/graphics__2-75.md)
**World**          |[Java](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByWorld/java.md)
**Archive File**   |[](https://github.com/Planet-Source-Code/found-on-the-web-a-status-bar-scroller__2-22/archive/master.zip)





### Source Code

```
<SCRIPT LANGUAGE="JavaScript">
  <!-- Start of scroller script
  var scrollCounter = 0;
  var scrollText  = "Any text here";
  var scrollDelay  = 70;
  var i = 0;
  while (i ++ < 140)
	scrollText = " " + scrollText;
  function Scroller()
  {
	window.status = scrollText.substring(scrollCounter++,
			  scrollText.length);
	if (scrollCounter == scrollText.length)
	  scrollCounter = 0;
	setTimeout("Scroller()", scrollDelay);
  }
  Scroller();
  // End of scroller script -->
</SCRIPT>
```

