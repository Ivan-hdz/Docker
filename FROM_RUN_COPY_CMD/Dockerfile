FROM debian
RUN apt-get update -y && apt-get install -y \ 
	git \
	python3 \
	vim
COPY ./Hello.py /home/Hello_World.py
CMD ["echo", "Hello World"]
