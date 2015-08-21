#MathX Integration Instructions


MathX is a jQuery plugin and will be dependant on the jQuery library.  Make sure that your platform accepts jQuery and no other JavaScript libraries conflict with it.

##Setup

To begin, include the necessary css and js files in the `head` of your website:

###Include CSS
The css works with the Symbola font, which is ideal for typing and reading math.
```
<link href='http://mathx.co/gotit/mathx/css/mathx.css' rel='stylesheet' type='text/css'>
```

###Include JS
First, add the jQuery library to ensure the MathX plugin will be able to be initialized.
```
<script src="http://mathx.co/gotit/mathx/js/jquery/jquery-2.1.3.min.js"></script>
```

Next, add the MathX JS core
```
<script src="http://mathx.co/gotit/mathx/js/mathx.js"></script>
```

Great, setup is done.  Time to instantiate MathX.

##Initiate MathX
MathX works by creating `div`s that behave like `textarea`s with the ability to input text formatted as mathematical notation.  Creating a MathX textbox is simple.

###HTML
In the body of your site, create a `div` that will serve as the MathX "textbox".  Specify a classname attribute for the textbox (name attributes will not work).  
```
<div class="mytextbox"></div>
```

###MathX Call
Now use the classname specified to transform the div into a MathX textbox.
```
<script>
// Initialize textbox with MathX
	 $(".mytextbox").mathX({
        placeholderText: "Type '//' to enter Math Mode",
        placeholderIcon: false,
        mathJax: false,
        mathModeOnly: false,
        edition: "Master Edition",
        userGuide: false
      });
</script>
```

There, the `div` is now a MathX textbox.  Now to write math...

###Typing Math
If the MathX call is initialized with `mathModeOnly: false`, then you must type `\\` to enter 'Math Mode'.  Here you can build complex expressions with familiar syntax.  Just to highlight a few:

* <kbd>^</kbd> is Superscript
* <kbd>_</kbd> is Subscript
* <kbd>/</kbd> is Fractions/Divisions
* <kbd>tab</kbd> is to navigate

Type symbols by their names (i.e. type 'pi' to get &pi;, 'sqrt' to get &radic;, etc.)

Contact **Timon Safaie** if you have any problems: timon@demonstranda.com

Enjoy!



