The situation is that, I'd like to calculate the original width/height proportion in order to enlarge or shrink the image proportionally.     
Firstly, I used <code>offsetWidth/offsetHeight</code>, but both offsetWidth and offsetHeight returned to be "0".    
The problem happened that the image needed to be loaded first so that its width and height could be acquired. However, when the codes run, the image has not been loaded successfully yet.    
The solution to this is to use ```callback function```.    
Thanks for the answer on [StackOverflow](http://stackoverflow.com/questions/11442712/get-width-height-of-remote-image-from-url)     
The callback function can be written like that:    
<code>function getMeta(url, callback) {
    var img = new Image();
    img.src = url;
    img.onload = function() { callback(this.width, this.height); }
}
getMeta(
  "http://snook.ca/files/mootools_83_snookca.png",
  function(width, height) { alert(width + 'px ' + height + 'px') }
);
</code>
