HTML (HyperText Markup Language) - layout/structure of a webpage. 
- Made up of tags, with data being in between them. 

CSS (Cascading Style Sheets) - a language that interacts with and styles HTML, changing the way HTML looks by following a series of rules. 

- Two important tags allow us to divide our webpage into sections: 
<div></div> the vertical division of a webpage
and 
<span> </span> section of a webpage inside a text (for example)

'#' to access an id (when styling)
. to access a class (when styling) 

A ‘pseudoclass’ is a special state of an HTML element. In one example, the state is whether or not the cursor is hovering over a button.

A ‘pseudoelement’ is a way to affect certain parts of an HTML element. 

Responsive design is the idea that a website should look good regardless of the platform its viewed from.

Another tool is ‘flexbox’. Flexbox allows for the reorganization of content based on the size of the viewport.

BOOTSTRAP

Bootstrap is a CSS library written to help make clean, responsive, and nice-looking websites without having to remember the gritty details about flexboxes or grids everytime a layout needs to be set up.

To import/use Bootstrap: <link rel="stylesheet" href="https://stackpath.bootstrapcdn.com/bootstrap/4.1.1/css/bootstrap.min.css" integrity="sha384-WskhaSGFgHYWDcbwN70/dfYBj47jz9qbsMId/iRN3ewGhXQFZCSftd1LZCfmhktB" crossorigin="anonymous">

Bootstrap uses a column-based model where every row in a website is divided into 12 individual columns, and different elements can be alloted a different number of columns to fill.

SASS 

Sass is a new language built on top of CSS which gives it a little more power and flexibility when designing CSS stylesheets and allows for the generation of stylesheets in a programmatic way. Ultimately, Sass just makes writing CSS easier.

In order to use Sass, it must first be installed. Once installed, we can execute sass style.scss style.css to compile our Sass file style.scss into sass.css, which can actually be linked to and interpreted by an HTML file.

One feature of Sass is variables, which are defined as so: $color: red;. Anywhere $color is passed as a value for a CSS property, e.g. color: $color, red will be used.

SASS INHERITANCE
Inheritance is similar to the object-oriented concept. It allows for slight tweaking of a general style for different components.

      %message {
           font-family: sans-serif;
            font-size: 18px;
            font-weight: bold;
         }

      .specificMessage {
      @extend %message;
      background-color: green;
         } 


%message defines a general pattern that can be inherited in other style definitions using the @extend %message syntax. In addition, other style properties can be added.
