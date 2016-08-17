FROM        alpine
MAINTAINER  Gonkulator Labs <github.com/gonkulator>
COPY        setup.yml /etc/ansible/
COPY        entrypoint.sh /usr/bin/entrypoint
RUN         chmod a+x /usr/bin/entrypoint && \
#test
            apk add --update gcc python-dev libffi-dev python py-pip bash openssh-client openssl bash py-crypto ncurses && \
	    apk add gcc git libffi-dev musl-dev openssl-dev perl py-pip python python-dev sshpass && \
            pip install --upgrade ansible && mkdir -p /etc/ansible
VOLUME      /keys
CMD         /usr/bin/entrypoint
