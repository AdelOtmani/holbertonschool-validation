help:  ## Make help
	@sed -ne '/@sed/!s/## //p' Makefile

lint:  ## Make lint
	@golangci-lint run

build:  ## Make build
	@make lint &
	@go mod init github.com/AdelOtmani/awesome-api
	@go get github.com/gorilla/mux
	@go build

run: ## Make run
	@./awesome-api >./awesome.log 2>&1 &

stop: ## Make stop
	@kill "$(shell pgrep awesome-api)" >/dev/null 2>&1 &

clean:  ## Make clean
	@make stop
	@rm -rf awesome-api
	@rm -rf awesome.log

test:  ## Make test
	@curl http://localhost:9999
	@curl http://localhost:9999/health


