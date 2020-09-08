.PHONY: all say_hello generategrammar generatelexer generate clean

all: say_hello generategrammar generatelexer generate


CC = gcc

LINKERFLAG = -lfl

say_hello:
		@echo "Make Started"

generategrammar:
		@echo "Creating Yacc Compiled Object..."
		yacc -d parser.y
		@echo "Compiled Successfully"


generatelexer:
		@echo "Creating Lexer Compiled Object..."
		lex lexer.l
		@echo "Compiled Successfully"

generate:
		@echo "Creating Final Compiled Binary..."
		${CC} -g -o myASTGenerator lex.yy.c y.tab.c ${LINKERFLAG}
		rm y.tab.c y.tab.h lex.yy.c

clean:
		@echo "Cleaning up..."
		rm myASTGenerato