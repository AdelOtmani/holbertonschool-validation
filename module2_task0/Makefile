help:  ## Make help
	@sed -ne '/@sed/!s/## //p' Makefile
build:  ## Make build
	@go mod init github.com/AdelOtmani/awesome-api
	@go get github.com/gorilla/mux
	@go build

run: ## Make run
	@./awesome-api >./awesome.log 2>&1 &

stop: ## Make stop
	@kill "$(shell pgrep awesome-api)"

clean:  ## Make clean
	@rm -rf awesome-api
	@rm -rf awesome.log

test:  ## Make test
	@curl http://localhost:9999
	@curl http://localhost:9999/health
