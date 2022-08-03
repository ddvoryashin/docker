-- запуск контейнера
docker run -p 10000:8888 jupyter/scipy-notebook:807999a41207

-- зайти внутрь контейнера
docker exec -it d38191085aba bash

-- копировать файл в контейнер с локальной машины
docker cp wine.data 56cb3c1cc08c:/home/jovyan/wine.data

-- запуск контейнера с volume
docker run -v /Users/dvorasindmitrij/Desktop/docker:/home/jovyan -p 10000:8888 jupyter/scipy-notebook:807999a41207

-- запуск контейнера из Dockerfile
docker build -t ds_container .
docker run -v /Users/dvorasindmitrij/Desktop/docker:/home/jovyan -p 10000:8888 ds_container

-- docker compose
-- создать файл docker-compose.yml, указать порты и Dockerfile, а затем
docker compose up