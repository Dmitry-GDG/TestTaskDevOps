NAME = infra

SRC = ./srcs/docker-compose.yml

all : ${NAME}

${NAME}:
	docker-compose -f ${SRC} build --parallel
	docker-compose -f ${SRC} up -d

re : fclean all

stop : 
	docker-compose -f ${SRC} down

clean :
	docker-compose -f ${SRC} down --rmi all

fclean : clean
	docker system prune -f
	sudo chmod 777 ${HOME}/jenkins_compose
	sudo rm -rf ${HOME}/jenkins_compose

ps:
	docker-compose -f ${SRC} ps

.PHONY: clean fclean all stop ps
