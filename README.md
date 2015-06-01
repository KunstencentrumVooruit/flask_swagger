# flask_swagger

## Setup

```
sudo apt-get install virtualenv
virtualenv testapp
cd testapp
bin/pip install flask-restplus
wget https://raw.githubusercontent.com/KunstencentrumVooruit/flask_swagger/master/template.py
chmod 775 template.py
mv template.py app.py
./app.py
```

http://localhost:5003/apiv1/sensoren/swagger

# uitleg over framework setup

Doel:
* elke applicatie in eigen container en listening port (virtualenv)
* nginx als remote proxy op poort 80
* automatic deployment via webinterface, github en fabric (2do)

## VIRTUALENV

> virtualenv test

Maakt directory 'test' aan, met daarin volledige python omgeving
* naamgeving: app.py
* #!bin/python ipv #!/usr/bin/python
* installeren van libraries: bin/pip install .... (geen sudo nodig)
* resultaat: containeromgeving voor app die via github naar server kan worden gedeployed

## SWAGGER

* Elke app documenteren via swagger (zie voorbeeld.py), zodat wijzelf en andere ontwikkelaars zien wat beschikbaar is, en zelfstandig kunnen ontwikkelen op basis van de documentatie
* flask-restplus: http://flask-restplus.readthedocs.org/en/latest/quickstart.html
* zie template.py 

## DEPLOYMENT
* via fabric (2do)
* 
