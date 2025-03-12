- first we import the Flask class from the flask module
- then we define a variable to be an Object of Flask.
- then execute the `run()` method of the Flask object.
- Optionally, we can also set debug mode to be on by putting `Object.debug = True` before the `run()` method is executed.
- We define where to serve the app by using: `app.route("/")` where `/` implies to serve it at the base root.
- An example program would like something like:
	- ```python
	  from flask import Flask
	  app = Flask(__name__)
	  @app.route("/")
	  def hello_world():
		  return """
		  <!DOCTYPE html>
		  <html>
			  <head>
				  <meta charset="UTF-8"/>
			  </head>
			  <body>
				  Hello World
			  </body>
		  </html>
		  """
		if __name__ == "__main__":
		  app.debug = True
		  app.run()

	  ```