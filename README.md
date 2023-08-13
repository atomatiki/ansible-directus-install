# ansible-directus-install-roles

Install directus with docker in a remote linux {ubuntu} machine using ansible.
 - We are using traefik as a webserver

## Usage 
fork the repository to your account
add a actions secret `SSH_PRIVATE_KEY` containing a private key to connect with your server

Make sure you know the values below, the click run workflow under tab `Actions` > `workfows` > `Configure Directus` and fill in the correct values and click run.

```
directus_domain = <your domain name i.e directus.mywebsite.com> 
directus_db_connection_string = <database string i.e postgresql://admin:password@postgis/>
docker_network = traefik_network
TARGET_HOST = <server-ip i.e 0.0.0>
SSH_PORT = 22
SSH_USER = <ssh-user i.e root>
SSH_USER_HOME_DIR = <ssh-uer-dir i.e /root >
```
Here is the structure of the directus_db_connection_string example value `postgresql://admin:password@postgis/` 

`postgresql` = The type of database management system you are connecting to, which in this case is PostgreSQL.

`admin:password` = The username and password respectively, it is used for authenticating to the PostgreSQL database.

`postgis`: The hostname or IP address of the machine where your PostgreSQL database is hosted. It's named "postgis" in this case. The actual hostname or IP address would depend on your specific setup.

Note : Optional you can define the database you want to connect to by writing it's name after the / i.e  `postgresql://admin:password@postgis/database` Here `database` is the database which will be used. MAKE SURE THIS EXISTS in your database management system since if it does not you will get an error trying visit your domain, you can then just go create the database you stated.
