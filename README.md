# ECE5260: Graph-Based Data Science for Networked Systems

This is the repository for [ECE5260 (Spring 22)](http://sinegit.github.io/ECE5260). 
## Workflow

### Maintaining the `master` branch

1. Clone the `master` branch of this repository
```bash
git clone -b master https://github.com/sinegit/sinegit.github.io.git
```
2. Install the dependencies specified in the Gemfile
```bash
bundle install
```
3. Build the website
```bash
bundle exec jekyll build
```
This will create the destination directory `_site/` and build the site into it.

4. Add file contents to the index
```bash
git add -A
```
5. Commit the changes
```bash
git commit -m "Your message"
```
6. Push the commit to the `master` branch
```bash
git push origin master
```

### Maintaining the `gh-pages` branch

The GitHub Pages site will be built from the `gh-pages` branch. Thus we need to push the `_site` folder to the `gh-pages` branch

1. Change the current working directory to the `_site` directory
```bash
cd _site/
```
2. Tell GitHub Pages that there is no need to build (GitHub can build Jekyll site directly from the source, the `master` branch, if it contains only supported plugins. We utilize some unsupported plugins.)
```bash
touch .nojekyll
```
3. Add our repository
```bash
git remote add origin https://github.com/sinegit/sinegit.github.io.git
```
4. Switch to the `gh-pages` branch
```bash
git checkout -b gh-pages
```
5. Add file contents to the index
```bash
git add -A
```
6. Commit the changes
```bash
git commit -m "Your message"
```
7. Push the commit to the `gh-pages` branch
```bash
git push origin gh-pages
```

## Run the page locally using Jekyll

To run locally:
```bash
bundle exec jekyll serve
```