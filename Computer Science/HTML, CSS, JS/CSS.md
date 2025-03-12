Check what the `em` in `font-size: 2em;` means
# Introduction
- Styles are seperated from the primary layout of the webpage as it allows to map different "themes" to the same structure.

- Allow multiple definitions
	- Latest takes precedence
 
# Different ways to use CSS
## Inline CSS
- Directly add style to the tag
- ```html
	<h1 style="color:blue; text-align:center;">
	Heading 1
	</h1>
	```
- <p style="color:red;">I think it might be unique to the element that the style is applied to<p>
## Internal CSS
- Embed inside the `<head>` tag
- Any styles to be mentioned are enclosed within the `<style>` tag.
- ```html
  <head>
	  <style>
		  h1{
			  color:blue;
			  text-align:center;
		  }
	  </style>
  </head>
  ```
## External CSS
- Extract common content for reuse.
- Multiple CSS files can be included.
- Latest definition of the style takes precedence.
- The HTML file should contain a link to the external css file to be able to use the styles
	- ```html
	  <head>
			  <link rel="stylesheet" href="styles.css">
	  </head>
	  ```

# Bootstrap
- Commonly used framework
	- Originated from Twitter and was originaly called Twitter Blueprint.
	- Widely used now
- Standard styles for various components
	- Buttons
	- Forms
	- Icons
- Mobile first: highly responsive layout.

# Basic CSS
- two different names can share the same style
	- ```css
	  h1, h2{
		  color:red;
	  }
	  ```
- Making all even rows in a table to have a lightgray background.
	- ```css
	  tr:nth-child(even){
		  background-color:lightgray;
	  }
	  ```
	  - can also be done using tags and classes.
- A class is defined by putting a dot (`.`) before the class name to be defined.
	- ```html
	  <style>
		  .class1{
			  color:red;
		  }
	  </style>
	  <p class="class1">Red Color</p>
	  ```
- IDs are defined by putting a hash (`#`) before the name of the style for the ID.
	- ```html
	  <style>
		  #personal {
			  color:red;
		  }
	  </style>
	  <div id="personal">
			<p>Red Color</p>
	  </div>
	  ```