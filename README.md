# linuxWebserverConfiguration

#### IP Address
52.25.200.150

#### SSH port
2200

#### URL 
ec2-52-25-200-150.us-west-2.compute.amazonaws.com/login 

*Head straight to login page via above url.  Still working out a bug in how the index page handles users who are not logged in yet*

#### packages installed
finger,
apache2,
libapache2-mod-wsgi,
postgresql,
git,
python-setuptools,
sqlalchemy,
flask,
python-psycopg2,
oauth2

### Configuration summary

- setup SSH access for virtual machine dev environment provided by Udacity
- dropped private key file to .ssh folder, granted owner read/write permissions and SSH'd into the instance
- created new user 'grader' with permission to sudo
- updated installed packages
- changed ssh port from 22 to 2200
- changed sshd_config to deny root login and allow user 'grader' to SSH
- generated SSH key pair to place in .ssh/authorized_keys folder
- configured ufw to allow connection to port 2200 (ssh), 80 (http) and 123 (ntp)
- enabled firewall
- set local timezone to UTC
- installed apache webserver and wsgi module
- installed git 
- installed python packages and setup directory structure for app
- installed, setup and activated a virtual environment (virtualenv)
- installed flask from within virtual environment
- setup config file for virtual host
- created wsgi file to point at the python script which will run the app
- cloned target app's git repository into virtual environment
- made repository inaccessible by using an .htaccess file specifying a 404 redirect on .git files
- installed postgresql and disabled remote connection
- created postgres user 'catalog' with sole permision to manage database
- logged in with 'catalog' user and created the catalog database
- ran database_setup.py to create neccessary tables
- logged onto google dev console and added public IP and AWS url to oauth2 credentials

App is now running at location listed above.

#### External Resources
- https://www.digitalocean.com/community/tutorials/how-to-deploy-a-flask-application-on-an-ubuntu-vps
- https://www.digitalocean.com/community/tutorials/how-to-secure-postgresql-on-an-ubuntu-vps
- http://askubuntu.com/questions/16650/create-a-new-ssh-user-on-ubuntu-server
- http://www.tutorialspoint.com/postgresql/
- https://github.com/elnobun/Linux-Server-Configuration
- Udacity forums
