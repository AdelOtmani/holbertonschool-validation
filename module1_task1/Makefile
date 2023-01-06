build: 
	hugo
clean:
	rm -rf dist/
post:
	hugo new posts/$(POST_NAME).md
	sed -i 's#title: "Who are we"#' Makefile
	