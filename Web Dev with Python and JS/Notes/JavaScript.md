JavaScript
-JS is a programming language that runs inside a web browser and runs client-side.
-Client-side processes reduce the load on the server, and often makes it faster.

When inside HTML code, it's enclosed in <script> tags. 

Some JS events:
- onmouseover : triggers when an element is hovered over
- onkeydown : triggers when a key is pressed
- onkeyup : triggers when a key is released
- onload : triggers when a page is loaded
- onblur : triggers when an object loses focus (when moving away from an input box, for example)

DOM: Document Object Model --> Essentially the contents of a webpage
- JS can manipulate and change the contents of the DOM.

              function hello() {
                  document.querySelector('h1').innerHTML = 'Goodbye!';
              }
- In this function, document refers to the current web page being displayed. 
- querySelector('tag') is a function that looks through a page for a certain CSS selector, and returns that element. Instead of 
  a tag, '.class' and '#id' can also be used.
- querySelector will only select and return the first result. 
- The innerHTML property of an element is the HTML content within the element's tags. 
 
let is a keyword used to define variables.

Conditional statements
    
    <script>
      let counter = 0;

      function count() {
          counter++;
          document.querySelector('#counter').innerHTML = counter;

          if (counter % 10 === 0) {
              alert(`Counter is at ${counter}!`);
          }
      }
  </script>

% is the modulus operator, returning the remainder of the first number divided by the second.

=== checks for exact equality. When 2 things are identical, it will return true. 

The argument to alert is like a template literal in Python. 

${counter} will be replaced by the value of the counter variable. 

` backticks ` are used to delimit a template literate. They essentially let us dynamically generate content. (A variable in this case).


    document.addEventListener('DOMContentLoaded', function() {
                  document.querySelector('button').onclick = count;
              });
              
     addEventListener is a function, which, like it suggests, waits for an event to occur. It can also take other
     functions as values. This is called HIGHER ORDER FUNCTIONS which means that functions can be passed around like other values.
     The function being called is a CALLBACK FUNCTION. The callback is called when the event being listened for occurs. In this case, 
     when the entire HTML structure is loaded by the browser (DOMContentLoaded), then the function is called. 
     
     JS can be factored out of the HTML code as well, so that the HTML file isn't bogged down,
     and it's reusable! 
        <script src="filename.js"</script>
     
     VARIABLES
     -const: defines a constant variable that CANT be redefined.
     -let: defines a variable LOCAL to the scope of the innermost curly braces surrounding it.
     -var: defines a variable that is LOCAL to the FUNCTION it's defined in. 
     
JS can also modify the style (CSS properties) of elements.
    
ARROW FUNCTIONS: Defined without using the word function. Rather, just with a pair of () enclosing
any arguments, followed by an arrow, and then the body enclosed in curly braces. 

    () => {
      alert('Hello, world!');
     }

The keyword 'this' refers to whatever value the function is being operated on. 

The setInterval function takes another function and then the interval (milliseconds) after 
which the passed function will be called over and over.

    document.addEventListener('DOMContentLoaded', () => {
                  setInterval(count, 1000);
              });

              let counter = 0;

              function count() {
                  counter++;
                  document.querySelector('#counter').innerHTML = counter;
              }

JavaScript can use local storage to keep track of some state information.
localStorage is the variable that JS can store info at. getItem and setItem can be called
on localStorage or either load or save data. 



