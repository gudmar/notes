# Deploying an angular page in github repository:
[source](https://angular.io/guide/deployment)
* git remote add origin https://github.com/username/project-name.git
* git branch -M main    // moves master to main, so now master is named main, like in github
* git push -u origin main
* git checkout -b gh-pages
* ng build --output-path docs --base-href /project-name/  // creates an output in docs folder with base href set to /project-name/
* Copy index.html to the same docs folder, and rename it to 404.html
* git push origin gh-pages
* may merge gh-pages on git to master, not necesary
* Go to project in github / settings / pages and in source section, select branch name (main or gh-pages) and
/docs/ folder and save
* Now in blue box there is a link to ready page
* <b>NOTE</b> that in case a project contains a README.md file this file will be served as default. To change this default behavoir <b>Jekyll</b> has to be turned off by placing a .nojekyll empty file in 
main project folder!

## Note
* No child folders named with route name should be added
* No ./ in index or to 404 html added


* NO gh-pages branch can be merged to master !!!. Need to checkout to other branch from this one to do the trick. 
