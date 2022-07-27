NAME = infra

SRC = ./srcs/docker-compose.yml

all : ${NAME}

${NAME}:
#	mkdir -p ${HOME}/sonatype-work/nexus3/log
#	mkdir -p ${HOME}/sonatype-work/nexus3/tmp
#	chmod 777 ${HOME}/sonatype-work/nexus3/log
#	chmod 777 ${HOME}/sonatype-work/nexus3/tmp
	docker-compose -f ${SRC} build --parallel
	docker-compose -f ${SRC} up -d

re : fclean all

stop : 
	docker-compose -f ${SRC} down

clean :
#	sudo rm -rf ${HOME}/sonatype-work/*
	docker-compose -f ${SRC} down --rmi all

fclean : clean
	docker system prune -f

ps:
	docker-compose -f srcs/docker-compose.yml ps

.PHONY: clean fclean all stop ps
