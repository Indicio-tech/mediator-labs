all: lab1.pdf

lab1.html: ../README.md Makefile
	podman run -it --rm \
		-v $(dir $(shell pwd)):/data:z \
		pandoc/core \
		-s -t html5 --self-contained \
		-c print/github-pandoc.css \
		-o print/lab1.html \
		README.md

lab1.pdf: lab1.html
	podman run -it --rm \
		-v $(dir $(shell pwd)):/data:z \
		surnet/alpine-wkhtmltopdf:3.12-0.12.6-small \
		/data/print/lab1.html \
		/data/print/lab1.pdf

clean:
	-rm lab1.html
	-rm lab1.pdf
