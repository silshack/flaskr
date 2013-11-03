
Code for the Flaskr blogging platform, an example written with [Flask](http://flask.pocoo.org/) by Armin Ronacher

## Instructions

1 - Install Flask

```
pip install Flask
```

2 - Run Flaskr

```
python flaskr.py
```

3 - Log in

Username: admin
Password: default

And/or edit these variables in `flaskr.py`.

4 - Hackity Hack

In general:
* Edit `templates/layout.html` to change the way the site's pages look
* Add routes (pages) by editing `flaskr.py` and adding the appropriate templates
* Edit `static/style.css` to change the site's styling if desired

In specific:

* Create `templates/about.html` to be something like this:

```
{% extends "layout.html" %}
{% block body %}
  <h2>About</h2>
  <p>Here's a little about me</p>
{% endblock %}
```
* Add a route for your about page in `flaskr.py`:

```
@app.route('/about')
def about():
    return render_template('about.html')

```
* Add a link to your `templates/layout.html`:
```
...
  <h1>Flaskr</h1>
  <div class=metanav>
  ## Add this line:
    <a href="{{ url_for('about') }}">about</a>
  {% if not session.logged_in %}
...
```

### Original documentation:

                         / Flaskr /

                 a minimal blog application


    ~ What is Flaskr?

      A sqlite powered thumble blog application

    ~ How do I use it?

      1. edit the configuration in the flaskr.py file or
         export an FLASKR_SETTINGS environment variable
         pointing to a configuration file.

      2. now you can run the flaskr.py file with your
         python interpreter and the application will
         greet you on http://localhost:5000/
	
    ~ Is it tested?

      You betcha.  Run the `flaskr_tests.py` file to see
      the tests pass.
