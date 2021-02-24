# LDFLAGS="-L${CONDA_PREFIX}/lib ${LDFLAGS}"
CC=gcc
CXX=g++


.PHONY: build-parser
build-parser:
	bison parser.y

.PHONY: build-lexer
build-lexer:
	flex scanner.lex


.PHONY: combine-lexer-parser
combine-lexer-parser:
	$(CXX) lex.yy.c -lfl -v


.PHONY: compile-source
compile-source:
	./a.out source.ect


.PHONY: all
all: build-parser build-lexer combine-lexer-parser compile-source
