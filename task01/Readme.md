## 1. infra

На виртуальной машине с Linux развернуть контейнеры в docker:

- Jenkins

- Bitbucket

- Nexus

По возможности использовать docker-compose

```zsh
	sudo apt-get update -y && sudo apt-get upgrade -y
	make
	docker ps
	make ps
	docker logs -f имя_контейнера
	docker stop имя_контейнера
	docker rm -r имя_контейнера
```
### To test:

- Jenkins: 
```
	localhost:8080 
	(for password go via terminal docker logs jenkins | less)
```

- Bitbucket: 
```
	localhost:7990
```

- Nexus:
```
	localhost:8081 
	(for password go via terminal sudo docker exec -it nexus cat /nexus-data/admin.password)
```
