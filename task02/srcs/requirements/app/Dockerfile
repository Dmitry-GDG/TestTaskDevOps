FROM debian:buster

RUN apt-get -y update && \
    apt-get -y install git nodejs npm && \
	git clone https://github.com/skidding/flatris.git /node_app && \
	cd /node_app && \
    npm build

CMD supervisord
