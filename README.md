# Flask web development 

## environment and get started
### python environment and virutual environment
- install python, prefer python3
- make new virtual environment
- install flask
- freeze the library dependencies

## "Hello World" flask application

### code first
```
from flask import Flask
app = Flask(__name__)

@app.route("/")
def index():
	return "Hello World"

### run the code
export flask app
` export FLASH_APP=app.py

` $flask run

(flask) ➜  flask git:(master) ✗ flask run
 * Environment: production
   WARNING: Do not use the development server in a production environment.
   Use a production WSGI server instead.
 * Debug mode: off
 * Running on http://127.0.0.1:5000/ (Press CTRL+C to quit)

OK, flask applicaiton is ready for testing now

### rendering the template with jinja

modify the app.py
add following:
'''
from flask import render_template

change the code from
=> return "Hello World" to
===> return render_template("index.html")
'''
make the directory templates in the current directory and add index.html into the templates:

```
<!DOCTYPE html>
<html lang='en'>
<body>
	<h1>Hello World</h1>
</body>
</html>

```

OK Hello world with templates
