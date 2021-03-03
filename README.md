# Odoo-Installation-for-Developing

 Installing Odoo system dependencies:-
  - sudo apt update
  - sudo apt upgrade
  - sudo apt install git
  - sudo apt install python3-dev python3-pip
  - sudo apt install build-essential libxslt-dev libzip-dev libldap2-dev libsasl2-dev libssl-dev
  - sudo apt install npm
  - sudo ln -s /usr/bin/nodejs/usr/bin/node # node runs Node.js
  - sudo npm install -g less less-plugin-clean-css
 
 Installing Odoo from source:-
  - mkdir odoo_dev
  - cd odoo_dev
  - git clone https://github.com/odoo/odoo.git -b 12.0 --depth=1
  - pip3 install -r ~/odoo_dev/odoo/requirements.txt
  - pip3 install num2words phonenumbers psycopg2-binary watchdog xlwt
  
 Start teh Odoo server instance:-
  - cd odoo_dev/odoo
  - ./odoo-bin 
  - ./odoo-bin -h
  - ./odoo-bin --config=<odoo.conf path>  --http-port = <new port>
 
 Initializing a new Odoo database:-
  - sudo su -c "createuser -s $USER" postgres <b>Create db superuser</b>
  - ./odoo-bin -d testdb
  - createdb MyDB
  - createdb --template = MyDB MyDB2
  - psql -l
  - dropdb MyDB2
  


# PostgreSQL-Installation
  -  
  
# PgAdmin4-Installation


