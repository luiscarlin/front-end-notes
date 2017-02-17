# Bower
- requires node and npm (comes with node)
- installs front-end dependencies (like jQuery, backbone, etc)

```bash
# install
npm install -g bower

# initialize bower app (generates bower.json)
# in $ROOT_PROJ/$APP_NAME
bower init

# dependencies added/ removed from json file and bower_components when using "--save"
bower install jquery angular backbone --save

# list everything installed
bower list

# uninstall packages and remove from bower.json file
bower uninstall jquery --save

# print relative paths to packages. You can use them for <scrpt> in html files
bower list --paths

# bower components should not be pushed to git repo
# to generate bower_components folder from json file
bower install
```
