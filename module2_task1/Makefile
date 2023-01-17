help:  ## Make help
	@sed -ne '/@sed/!s/## //p' Makefile

lint:  ## Make lint
	@golangci-lint run

build:  ## Make build
	@make lint >/dev/null 2>&1 go build || exit -1

run: ## Make run
	@./awesome-api >./awesome.log 2>&1 &

stop: ## Make stop
	@kill "$(shell pgrep awesome-api)" >/dev/null &

clean:  ## Make clean
	@make stop
	@rm -rf awesome-api
	@rm -rf awesome.log

test:  ## Make test
	@curl http://localhost:9999
	@curl http://localhost:9999/health


