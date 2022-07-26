NAME = infra

SRC = ./srcs/docker-compose.yml

all : ${NAME}

${NAME}:
	mkdir -p ${HOME}/nexus-data
	chmod 777 ${HOME}/nexus-data
	docker-compose -f ${SRC} build --parallel
	docker-compose -f ${SRC} up -d

re : fclean all

stop : 
	docker-compose -f ${SRC} down

clean :
	sudo rm -rf ${HOME}/nexus-data/*
	docker-compose -f ${SRC} down --rmi all

fclean : clean
	docker system prune -f

ps:
	docker-compose -f srcs/docker-compose.yml ps

.PHONY: clean fclean all stop ps
