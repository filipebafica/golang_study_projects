APP_IMAGE = golang_study_projects_1_webserver
APP_CONTAINER = golang_study_projects_1_webserver

all: build

build:
	docker compose build

up:
	docker compose up -d

down:
	docker compose down

clean: SHELL := /bin/bash
clean:
	@if [[ $$(docker images $(APP_IMAGE) | wc -l) > 1 ]]; then\
		docker rmi $(APP_IMAGE);\
	fi

app:
	docker exec -it $(APP_CONTAINER) bash