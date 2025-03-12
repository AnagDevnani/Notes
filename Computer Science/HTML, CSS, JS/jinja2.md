Jinja2 is a templating engine in Python for HTML.

It uses syntax similiar to the default template functionality in Python,
```python
#Default templating in Python
Template = "{name}"
print(Template.format(name="Anag"))
#o/p: Anag
```

There also exist specifiers for the template variables.
Example:
- if the templated variable is a number, we can give a specifier to show sign based on positive, negative etc.
- Note: specifiers are usually given after a colon(`:`), example `template = "{a:+}"`
	- ```python
		#sample code for specifiers
		template1 = "a = {a}, b = {b}"
		template2 = "a ={a:+}, b = {b:+}"
		print(template1.format(a=5,b=-7))#o/p 1
		print(template2.format(a=5,b=-7))#o/p 2
		#o/p 1: a = 5, b = -7
		#o/p 2: a = +5, b = -7
	  ```
	  - Another specfier is `:d` and `:x` for printing the decimal and hexadecimal values of a number respectively.
	 
# Jinja2 Introduction (finally)
- First we have to import template from jinja2 by:
- The syntax is similiar to the default templating engine of python but is slight different
```python
from jinja2 import Template
temp = "Hello {{ name }} "
#note we use double curly brackets instead of single
def main():
	template = Template(temp) #we create a template object
	print(template.render(name = "Anag"))
```

- jinja2 also allows us to create loops inside the template by specifying the loop in `{% insert_loop_here %}`
- ```python3
  ...
  template = """
  {% for row in list %}
  <tr>
  <td>{{ row[value] }}</td>
  </tr>
  {% endfor %}
  """
  ...
# Generating HTML output using jinja2
