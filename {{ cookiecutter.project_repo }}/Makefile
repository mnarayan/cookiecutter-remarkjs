BIND_ADDRESS ?= 127.0.0.1
PORT ?= 8000
GITHUB_REPO ?= mnarayan/{{ cookiecutter.project_repo }}

.DEFAULT_GOAL := help

.PHONY: help clean link serve

help:
	@grep -E '^[a-zA-Z_-]+:.*?## .*$$' $(MAKEFILE_LIST) | sort | awk 'BEGIN {FS = ":.*?## "}; {printf "\033[36m%-30s\033[0m %s\n", $$1, $$2}'

#clean: ## Clean all links


node_modules:
	npm install

#link: ## Link to any needed resources


serve: ## Serve the slides
	@echo "Serving slides at http://$(BIND_ADDRESS):$(PORT)/"
	@echo "Quit the server with CONTROL-C."
	@python -m http.server --bind $(BIND_ADDRESS) $(PORT)

pages: ## Push to github
	@echo "Pushing slides to git@github.com:$(GITHUB_REPO) gh-pages"
	@git push origin gh-pages
