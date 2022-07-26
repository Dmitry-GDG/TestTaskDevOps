## 1. infra

На виртуальной машине с Linux развернуть контейнеры в docker:

- Jenkins

- Bitbucket

- Nexus

По возможности использовать docker-compose

```zsh
	make
	docker ps
	make ps
	docker logs -f имя_контейнера
	docker stop имя_контейнера
	docker rm -r имя_контейнера
```
### To test:

- Jenkins: localhost:8080 (for password go via terminal docker logs jenkins | less)

- Bitbucket: localhost:7990

- Nexus: curl http://localhost:8081/

