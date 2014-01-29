Tangelo on Heroku
=================

[Tangelo](http://kitware.github.io/tangelo) is a web framework for rapid development of advanced visual applications.
[Heroku](http://heroku.com) is a fast and easy web app deployment system. Why not bring these two together?

First, make an account on [Heroku](http://heroku.com) and install the [Heroku Toolbelt](https://toolbelt.heroku.com/).
After that, it's a matter of opening a shell and typing the following:

    heroku login
    git clone https://github.com/jeffbaumes/tangelo-heroku.git
    cd tangelo-heroku
    heroku create
    git push heroku master
    heroku open

Congratulations, you have just deployed Tangelo to your own server on Heroku!
You should see the "Tangelo sunrise" and be able to click on the examples link to see some example applications.

To get your own environment set up to run Tangelo locally in the same way Heroku sees it,
run the following additional commands:

    sudo pip install virtualenv
    virtualenv venv --distribute
    source venv/bin/activate
    pip install tangelo
    export PORT=8080
    foreman start

Pointing your browser to [http://localhost:8080](http://localhost:8080) should show the same version of Tangelo's default setup.
