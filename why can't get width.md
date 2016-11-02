We know that <code>object.style.width</code> can be used to get object's width. However, it has some limits.    

* <code>object.style.width</code> can only be used to get the width when the width or height is inline style.     
* In other words, if there's no specific inline style to set width or height, you will get <code>null</code> from this piece of code.    
* If we want to get the current width or height of a certain object, and this object has no inline style. We can use <code>object.offsetWidth</code> or <code>object.offsetHeight</code> instead.   

