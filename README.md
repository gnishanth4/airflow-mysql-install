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

19

In your mysql command line do the following:

mysql> SHOW GLOBAL VARIABLES LIKE '%timestamp%';
+---------------------------------+-------+
| Variable_name                   | Value |
+---------------------------------+-------+
| explicit_defaults_for_timestamp | OFF   |
| log_timestamps                  | UTC   |
+---------------------------------+-------+
2 rows in set (0.01 sec)

mysql> SET GLOBAL explicit_defaults_for_timestamp = 1;
Query OK, 0 rows affected (0.00 sec)

mysql> SHOW GLOBAL VARIABLES LIKE '%timestamp%';
+---------------------------------+-------+
| Variable_name                   | Value |
+---------------------------------+-------+
| explicit_defaults_for_timestamp | ON    |
| log_timestamps                  | UTC   |
+---------------------------------+-------+
2 rows in set (0.00 sec)



