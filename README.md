Zepto-viewport-checker
=======================

Little script that detects if an element is in the viewport and adds a class to it.

Installation
------------
Just include the script and Zepto in your website <head> tag and call it on the elements you want to check.
```code
<head>
    <script src="http://cdnjs.cloudflare.com/ajax/libs/zepto/1.1.4/zepto.js"></script>
    <script src="zepto.viewportchecker.js"></script>

    <script>
        $(document).ready(function(){
            $('.dummy').viewportChecker();
        });
    </script>
</head>
```

Options
-------
The current available options are:
```code
$('.dummy').viewportChecker({
    classToAdd: 'visible', // Class to add to the elements when they are visible
    offset: 100, // The offset of the elements (let them appear earlier or later)
    repeat: false, // Add the possibility to remove the class if the elements are not visible
    activeSectionSelector: ".view.active", // optional. if you have elements in hidden sections of the app, this selector allows to specify what container should be considered "active". can be any css selector.
    callbackFunction: function(elem, action){} // Callback to do after a class was added to an element. Action will return "add" or "remove", depending if the class was added or removed
});
```

Prevent viewportChecker from firing
-------
To make the plugin work better along other changes you might be doing to the DOM, we added a convenient `avoidVieportCheck` class.

Adding this class will prevent viewportChecker from doing any change to the element on the element.


Use case
--------
The guys from web2feel have written a little tutorial with a great example of how you can use this script with jQuery. It's going to work in the same way with Zepto.
You can check the [tutorial here](http://www.web2feel.com/tutorial-for-animated-scroll-loading-effects-with-animate-css-and-jquery/) and the [demo here](http://web2feel.com/freeby/scroll-effects/index.html).
 
