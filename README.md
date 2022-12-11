# Hamburger-Menu
Responsive menu for mobile or browser in css

This hamburger menu uses only html and css: there are no resource files or javascript. Try out the menu here. The web page consists of four sections; header, main, panel, and footer. The hamburger menu is contained within the header section. The garish color scheme is to make it easier to identify the different components. CSS is heavily commented and should be minified before use in production.  

How It Works
The hamburger button itself is a <div> containing two <span> tags.    You must set the tabindex property on the div tag to make it function like a button.  If tabindex is set, you can use the :focus psuedo selector in CSS to trigger expanding and contracting the menu.  You can also construct a hamburger menu using a checkbox and a label, but it is better to use a <div>.  The reason is you can contract the menu anytime the div loses focus. If you use a checkbox, the user must click on either the  checkbox or the label to alter the checked state and close the menu. 

The hamburger icon, consisting of three horizontal lines, is constructed inside the first <span>. The label for the icon is contained in the second span. To make the icon, we set the content of the span to nothing, but we give the span a height, width, and background color to make it appear as the middle horizontal line (the hamburger). We then use the two CSS pseudo properties, ‘before’ and ‘after’ to create the top and bottom lines (the two buns) for that span. 

When the user clicks on the hamburger icon, we convert it to an ‘X’. We hide the middle line and rotate the top and bottom lines 45 degrees. When the <div> loses focus, or the user clicks on the ‘X’, we convert back to the hamburger icon. How do we know when the user clicks the ‘X’?  We turn off pointer-events whenever the div has focus.  The next mouse click anywhere causes the div to lose focus  and we convert everything back to its previous state. 

