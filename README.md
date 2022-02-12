# Odoo Installation for Developing <img src="https://mms.businesswire.com/media/20191217005513/en/763363/22/Odoo_LP-logo.jpg" alt="Odoo" height="40" style="vertical-align:top; margin:4px">

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
  - git clone https://github.com/odoo/odoo.git -b 14.0 --depth=1
  - pip3 install -r ~/odoo_dev/odoo/requirements.txt
  - pip3 install num2words phonenumbers psycopg2-binary watchdog xlwt
  
 Start teh Odoo server instance:-
  - cd odoo_dev/odoo
  - ./odoo-bin 
  - ./odoo-bin -h
  - ./odoo-bin --config=<odoo.conf path>  --http-port = <new port>
 
 Initializing a new Odoo database:-
  - sudo su -c "createuser -s $USER" postgres <b>#Create db superuser</b>
  - ./odoo-bin -d testdb
  - createdb MyDB
  - createdb --template = MyDB MyDB2
  - psql -l
  - dropdb MyDB2
  


# PostgreSQL Installation <img src="https://github.com/devicons/devicon/blob/master/icons/postgresql/postgresql-original.svg" alt="Postgresql" height="40" style="vertical-align:top; margin:4px">
  - sudo apt update
  - sudo apt list postgresql*
  - sudo apt list postgresql
  - sudo systemctl stop postgresql
  - sudo systemctl disable postgresql
  - sudo systemctl start postgresql
  - sudo systemctl enable postgresql
  - sudo systemctl status postgresql
  - --------------------------------------------
 ## CREATE USER:
 https://kb.objectrocket.com/postgresql/how-to-create-a-role-in-postgres-1454#:~:text=To%20create%20a%20role%20in%20Postgres%2C%20use%20the%20CREATE%20ROLE,by%20the%20new%20role%20name.&text=CREATE%20ROLE%20new_role%3B,CREATE%20ROLE%20statement%20in%20PostgreSQL.&text=The%20only%20information%20we%20see,it%20has%20no%20login%20privileges.
  -  sudo -i -u postgres
  -  psql
  -  \l
  - CREATE ROLE superuser WITH SUPERUSER CREATEDB CREATEROLE LOGIN ENCRYPTED PASSWORD '1234';
  - \du
  - \l <list of databases>
  - \c <database name>  ## Connect Database
  - \q <exit from anything>
  -\d or \dt+ <Show all tables in database>
 
 # Delete Database  
  - psql -U username -h localhost -d postgres -c "DROP DATABASE  <db name>;"

# PgAdmin4 Installation <img src="https://www.ktexperts.com/wp-content/uploads/2019/07/pgadmin4.png" alt="PgAdmin4" height="40" style="vertical-align:top; margin:4px">

  - sudo apt update 
  - sudo nano /etc/apt/sources.list.d/pgdg.list
  - deb http://apt.postgresql.org/pub/repos/apt/ focal-pgdg main
  - wget --quiet -O - https://www.postgresql.org/media/keys/ACCC4CF8.asc | sudo apt-key add -
  - sudo apt-get update
  - sudo apt install pgadmin4 pgadmin4-apache2
  - sudo a2enmod rewrite
  - sudo systemctl restart apache2
  
