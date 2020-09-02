# airflow-mysql-install

Install Ansible for ubuntu
--------------------------

sudo apt-get update -y

sudo apt-get install python3

sudo apt-get install python3-pip

pip3 install ansible



Install these packages
----------------------

pip3 install werkzeug==0.16.0

apt install python-mysqldb

pip3 install apache-airflow[s3]


#Clone the Githubrepo 
---------------------

git clone https://github.com/gnishanth4/airflow-mysql-install.git

cd airflow-mysql-install

ansible-galaxy install -r requirements.yml

ansible-playbook airflow-mysql-playbook.yml

Set default python version to python3 in ubuntu
-----------------------------------------------

A simple safe way would be to use an alias. Place this into ~/.bashrc file: if you have gedit editor use

vi  ~/.bashrc

Go into the bashrc file and then at the top of the bashrc file make the following change.

alias python=python3

After adding the above in the file. run the below command

source ~/.bashrc


Install Ansible with python 3.x version
----------------------------------------

pip3 install ansible

Upgrading the MYSQl Database when new version of airflow is deployed
--------------------------------------------------------------------

login into mysql 

mysql -u root -p

In your mysql command line do the following:

mysql> SHOW GLOBAL VARIABLES LIKE '%timestamp%';

mysql> SET GLOBAL explicit_defaults_for_timestamp = 1;

mysql> SHOW GLOBAL VARIABLES LIKE '%timestamp%';


Downgrading the MYSQL DB
------------------------
mysql -u root -p 

mysql> SELECT * FROM alembic_version;

To solve your problem simply use the command:

DROP TABLE alembic_version;

Starting And Checking the Status of Aiflow 
----------------------------

sudo systemctl start airflow-webserver.service

sudo systemctl start airflow-scheduler.service

sudo systemctl status airflow-webserver.service

sudo systemctl status airflow-scheduler.service

check the last 10 log entries for a particular unit you can type

sudo journalctl -u your-service.service -n 10

To see the 10 last log entries for both services you can type:

sudo journalctl -u airflow-webserver.service -u airflow-scheduler.service -n 10









