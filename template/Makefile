#
# Vars
#

BIN = ./node_modules/.bin
.DEFAULT_GOAL := all

#
# Tasks
#

test: node_modules
	@node test/*

validate: node_modules
	@standard

all: validate test

init:
	@git init
	@git add .
	@git commit -am "FIRST"
	@hub create joshrtay/{{basename}} -d "{{description}}"
	@travis enable
	@git push -u origin master

#
# Phony
#

.PHONY: test validate all init
