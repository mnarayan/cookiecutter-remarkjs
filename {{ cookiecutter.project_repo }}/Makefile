BIND_ADDRESS ?= 127.0.0.1
PORT ?= 8000
GITHUB_REPO ?= {{ cookiecutter.github_account }}/{{ cookiecutter.project_repo }}

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

new-gh-pages: ## Create gh-pages branch
	@echo "Initializing git"
	@git init
	@echo "Adding remote git@github.com:$(GITHUB_REPO)"
	@git remote add origin git@github.com:$(GITHUB_REPO)
	@echo "Creating gh-pages branch"
	@git checkout -b  gh-pages
	@echo "Adding files to gh-pages"
	@git add slides.md slides.css index.html 
	@git commit -m "Adding default files from cookiecutter template in {{ cookiecutter.project_repo }}"

update-gh-pages: ## Update existing gh-pages branch
	@echo "Initializing git"
	@git init
	@echo "Adding remote git@github.com:$(GITHUB_REPO)"
	@git remote add origin git@github.com:$(GITHUB_REPO)
	@echo "Creating gh-pages branch"
	@git checkout -b  gh-pages
	@echo "Adding files to gh-pages"
	@git add slides.md slides.css index.html 
	@git commit -m "Adding default files from cookiecutter template in {{ cookiecutter.project_repo }}"
	@echo "Fetching existing gh-pages"
	@git fetch origin gh-pages
	@echo "Checking origin/gh-pages"
	@git checkout origin/gh-pages
	@git checkout -b rebase-gh-pages
	@git checkout gh-pages slides.md slides.css index.html
	@git commit -m "Updating gh-pages with latest files from cookiecutter template in {{ cookiecutter.project_repo }}"
    
    
pages: ## Push to github
	@echo "Pushing slides to git@github.com:$(GITHUB_REPO) gh-pages"
	@git push origin gh-pages
