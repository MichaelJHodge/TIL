Front Ends

Single-page Apps (SPAs) take content and combine them into a single page that pulls new info from the
server whenever it's  needed (through methods like AJAX). 

HTML5 History API: Allows for the manipulation of a browser's history and URL even if the page is still a single-page design. Whenever a new "page" is accessed, the client cna 'push' a new URL state. 

- The history.pushState() function can be used to change the browser's history. the first argument is any data that should be associated with the push, the second argument is the title of the page being pushed, and the third argument is the URL being pushed.

- When the state is popped (onpopstate), 'e', the event that just took place, has a state property that contains all the data that was pushed with that state. Then, that data is used to update the contents of the page. 

Window and Document
- Variables, which are JS objects on which operations can be performed and that have properties that can be accessed, such as size and position.
- window.innerWidth: window width
- window.innerHeight: window height
- document.body.offsetHeight: entire height of the HTML body's document, of which the window height is likely just a smaller portion
- window.scrollY: How far down the page has been scrolled (in pixels). 

JS Templating 
- One issue with JS is that as we build more complex UIs, the code gets a bit messy. 
- JS templating solves this, allowing for the creation of templates in JS that define the HTML, while also allowing for substitution inside that template for adding different content. 

CSS ANIMATION
- The ability to have CSS properties change over time WHILE the page is running.
- @keyframes name: Defines a CSS animation, called 'name' in this case. 
- BUT: with CSS alone, these animations will run as soon as the webpage is loaded. To control animation, JS can be used to modify the CSS properties with 'animationPlayState'. 

Animation with JS
-  animation-iteration-count specifies how many times the animation should be run.
- When we first load a page, the animation can be paused with: animationPlayState = 'paused'; We could then be able to activate it with a button that changes the state to = 'running';

SVG Animation: Scalable Vector Graphic - a graphical element determined by lines, angles, and shapes.
- Can be used to draw things that simple HTML elements, like divs, don't allow for. 
- D3 is a JS data visualization library that allows us to create these elements programatically. 
      
      <html>
      <head>
          <script src="https://d3js.org/d3.v4.min.js"></script>
      </head>
      <body>
          <svg id="svg" style="width:100%; height:800px"/>
      </body>
      <script>

          const svg = d3.select('#svg');

          svg.append('circle')
             .attr('cx', 200)
             .attr('cy', 200)
             .attr('r', 90)
             .style('fill', 'green');

      </script>
      </html>

- d3.selent gets access to an HTMl element. 
- Animations can also be added to SVGs. 
- Animations can be delayed or triggered on certain events. 

