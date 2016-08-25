- Today I used DOM sentence: **document.getElementsByClassName**
- The specific situation is that I'd like to give dynamic value to these div that are with the same class name.
- However, the debug tool shows that **Uncaught TypeError: Cannot read property 'width' of undefined**.
- The problem occurs because there are more than one child in the nodelist, while **element.style.width** can only be used to the specific one node.
- Thus the solution is that :
   
   <code>for (var i = 0; i < className('slider_pic').length; i++) {    
    document.getElementsByClassName('slider_pic')[i].style.width = currentWidth + "px" ;
				}</code>
				
				
