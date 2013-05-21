Sample Web Application using Python and Flask
=============

[![Code Now](https://friendco.de/widgets/image/codenow?url=https%3A%2F%2Fgithub.com%2FFriendCode%2Fpython-flask-sample.git)](https://friendco.de/widgets/url/codenow?url=https%3A%2F%2Fgithub.com%2FFriendCode%2Fpython-flask-sample.git)


A complete sample application in python using flask which 
can run on FriendCode and Heroku.

## Important
 * Requires a **Procfile** to run on **FriendCode** and **Heroku**
 * Like Heroku the port must be fetch from an environment variable called **PORT** (`process.env.PORT` in NodeJs)
 * FriendCode's runtime is in many ways similar to (and compatible with) Heroku's, so be aware of that

## Example :

    import os
    from flask import Flask

    app = Flask(__name__)

    @app.route('/')
    def hello():
        return 'Hello World!'

    if __name__ == '__main__':
        # Bind to PORT if defined, otherwise default to 5000.
        port = int(os.environ.get('PORT', 5000))
        app.run(host='0.0.0.0', port=port)

Happy coding !