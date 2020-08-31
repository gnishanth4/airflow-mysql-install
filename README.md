# airflow-mysql-install

Install Ansible for ubuntu
--------------------------

sudo apt-get update -y

sudo apt-add-repository ppa:ansible/ansible

sudo apt-get update -y

sudo apt-get install ansible -y

sudo ansible --version




Install these packages
----------------------

pip install werkzeug==0.16.0

apt install python-mysqldb


#Clone the Githubrepo 
---------------------

git clone https://github.com/gnishanth4/airflow-mysql-install.git

cd airflow-mysql-install

ansible-galaxy install -r requirements.yml

ansible-playbook airflow-mysql-playbook.yml

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






