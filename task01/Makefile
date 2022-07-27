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
	docker stop $(docker ps -qa);
	docker rm $(docker ps -qa);
	docker rmi -f $(docker images -qa);
	docker volume rm $(docker volume ls -q);
	docker network rm $(docker network ls -q) 2>/dev/null

ps:
	docker-compose -f ${SRC} ps

.PHONY: clean fclean all stop ps
