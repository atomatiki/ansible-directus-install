# ansible-directus-install-roles

Install directus with docker in a remote linux {ubuntu} machine using ansible
We are using traefik as a webserver

## Usage 
fork the repository to your account
add a actions secret `SSH_DEVEOPS_KEY` containing a private key to connect with your server

Make sure you know the values below, the click run workflow under `Actions` > `workfows` ? `Configure Directus` and fill in the correct values and click run.

directus_domain = <your domain name>
directus_db_connection_string = <database string>
docker_network = traefik_network
TARGET_HOST = <server-ip>
SSH_PORT = 22
SSH_USER = <ssh-user>
SSH_USER_HOME_DIR = <ssh-uer-dir>
