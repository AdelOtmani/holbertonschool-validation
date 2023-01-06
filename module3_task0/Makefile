help:  ## Make help
	@sed -ne '/@sed/!s/## //p' Makefile
build:  ## Make build
	@hugo
clean:  ## Make clean
	@rm -rf dist/
post:  ## Make post
	@hugo new posts/$(POST_NAME).md
	@sed -i 's#title: ".*"#title: "$(POST_TITLE)"#g' content/posts/$(POST_NAME).md
