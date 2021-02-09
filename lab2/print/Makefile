all: lab2.pdf

lab2.html: ../README.md Makefile
	podman run -it --rm \
		-v $(dir $(shell pwd)):/data:z \
		pandoc/core \
		-s -t html5 --self-contained \
		-c print/github-pandoc.css \
		-o print/lab2.html \
		README.md

lab2.pdf: lab2.html
	podman run -it --rm \
		-v $(dir $(shell pwd)):/data:z \
		surnet/alpine-wkhtmltopdf:3.12-0.12.6-small \
		/data/print/lab2.html \
		/data/print/lab2.pdf

clean:
	-rm lab2.html
	-rm lab2.pdf
