``` My situation is like this: ```     
I was going to build a "login" form that require users to input their name and password. When users click on the button "submit", the form's method is "GET".
The js code will receive these two inputs and check with records by using Ajax.      
- Firstly, I write the submit button like that :    
```<button type="submit" id="login">submit</button>  <script>document.getElementById("login").addEventListener('click',Ajax,false);</script>```.    
The result is that *Ajax returned status code 0*.    
- By looking up the usage of ``type="submit"``, I found that it has its own callback which refers to that the form will be submited to the server side. And there's one more thing need to be noticed *[``<button></button>`` has default type attribute which is ``type="submit"``].    
- According to this, there are two main solutions for this problem.     
  1. change the ``<button>`` code into ``<input type="button">``, then addEventListener to input.    
  2. change the callback of submit() to your own function. 
