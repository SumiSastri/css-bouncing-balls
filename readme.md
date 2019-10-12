GENERAL PRINCIPLES:

Cascading Style Sheets - introduced to style HTML and give page shape and structure
Separation of concerns in-line css moved to separate files
Critical render path - browsers read HTML first then CSS
The way that the browser reads CSS is that it cascades down the sheet
It reads the selector property and property value top down
Therefore if there are are 2 h1's then the last one takes precedence over the first

As it is a style selector in the DOM document.querySelector refers to the CSS selectors
(Double check this)

SYNTAX

selector {
	property: property value;
}

attributes
    name
    value
    class
    id

syntax convention - lower case separated by dashes no spaces
It is a name value pair where the value is a string therefore "" notation

name="example name"
value="example value"


STYLE AND QUERY SELECTORS

CSS is more of a programming language in the sense it has a block of code that runs
within the parenthesis

Like so
```
p {
  margin: 10px;
}
```

This says make the p element selected by the CSS selector have a margin of 10 pixels
To select class (notated by dot - class generic)
To select id (notated by hash - id is unique)
name and value are identified by the assigned string
name="form-name" where form-name becomes the identifier
Name and value become important in java-script and esp react-js

CLEARING BROWSER DEFAULTS
```
* {
  box-sizing: border-box;
}
```
RESPONSIVE DESIGN - MOBILE FIRST

Break-points - 320 OR 400 (phone)
Tablet (600-640)
Full-screen-(800-900)

```
@media only screen and (max-width: 840px) {
  main {
    flex-direction: row;
  }

  header h1 {
    font-size: 30px;
  }
```

Using vh

```
main {
    height: calc(100vh - 80px - 80px);
  }
```
-- for flexbox
```
html, body {
  margin: 0;
  padding: 0;
```
Clear-fix

only needed if you do not use flex box or CSS grid

```
.clearfix:after{
  display: table;
  content:"";
  clear: both;
};
```

SPECIFICITY OF NODES

```
.grid-wrapper ul li {
  width: calc(33.33% - 20px);
  margin-bottom: 30px;
}

.grid-wrapper ul li:nth-child(1):after {
  content: "1";
}

.grid-wrapper ul li:nth-child(2):after {
  content: "2";
}

.grid-wrapper ul li:nth-child(3):after {
  content: "3";
```
  RESPONSIVENESS
```
 Tablet 
@media only screen and (max-width: 960px) {
  main .column {
    width: 50%;
  }

  main .column:last-child {
    width: 100%;
  }

  header nav ul li {
    display: none;
  }

  header nav > ul > li:nth-child(1), header nav > ul > li:nth-child(4) {
    display: block;
  }

  header h1 {
    font-size: 40px;
  }

  header .subnav li:nth-child(1) {
    float: right;
    display: block;
  }

  header .subnav li:nth-child(1) a:before {
    content: '\2630';
  }

  header .subnav li {
    display: none;
  }
}

}
SASS
sass --watch scss/main.scss:css/style.css

```

RESOURCES
[http://www.w3schools.com/css/css3_transitions.asp]
[http://www.w3schools.com/cssref/sel_last-child.asp]
[http://www.w3schools.com/cssref/sel_hover.asp]


Images - Image tags - [https://developer.mozilla.org/en-US/docs/Web/HTML/Element/img]

FURTHER READING

[http://www.w3schools.com/css/css3_transitions.asp]
[http://www.w3schools.com/cssref/sel_last-child.asp]
[http://www.w3schools.com/cssref/sel_hover.asp)]
Normalize link [https://necolas.github.io/normalize.css/]\

```
<link 
rel=“stylesheet” 
href=“https://cdnjs.cloudflare.com/ajax/libs/bulma/0.7.2/css/bulma.css“
>
<link 
rel="stylesheet" href="https://use.fontawesome.com/releases/v5.7.0/css/all.css" 
integrity="sha384-lZN37f5QGtY3VHgisS14W3ExzMWZxybE1SJSEsQp9S+oqd12jhcu+A56Ebc1zFSJ" 
crossorigin="anonymous"
>
```

