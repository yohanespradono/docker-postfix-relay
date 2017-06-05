# Dockerized SMTP server#

SMTP server and SMTP relay host. Modified version of tecnativa/postfix-relay with additional MESSAGE_SIZE_LIMIT

## Run container

### SMTP relay via Gmail

    docker run -it -d --name smtp_relay \
           -e MAIL_RELAY_HOST='smtp.gmail.com' \
           -e MAIL_RELAY_PORT='587' \
           -e MAIL_RELAY_USER='your_gmail_addr' \
           -e MAIL_RELAY_PASS='your_gmail_pass' \
	   -e MESSAGE_SIZE_LIMIT=22020096 \
           tecnativa/postfix-relay

### Credit
tecnativa/postfix-relay