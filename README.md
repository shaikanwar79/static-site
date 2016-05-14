# Static-Site
[![Build Status](https://travis-ci.org/redbrick/static-site.svg?branch=master)](https://travis-ci.org/redbrick/static-site)

A Static Site for [redbrick](http://redbrick.dcu.ie) generated with [hexo](hexo.io) using a theme
based off [tranquilpeak](https://github.com/LouisBarranqueiro/hexo-theme-tranquilpeak)
Documentation for hexo can be found [here](hexo.io/docs/) and the themes documentaion can be
found in
[themes/tranquilpeak/docs](https://github.com/redbrick/static-site/tree/master/themes/tranquilpeak/docs)

Demo at [butlerx site](http://redbrick.dcu.ie/~butlerx/demo)

## Requirements

1. **Node** : v0.10.35 or higher. Download [Node](https://nodejs.org/download/)
2. **Hexo CLI** : v0.1.4 or higher. Run `npm install hexo-cli -g`
3. **Grunt CLI** : v0.1.13 or higher. Run `npm install grunt-cli -g`
4. **Bower** : v1.4.1 or higher. Run `npm install bower -g`
5. **ESLint** : v2.3.0 or higher. Run `npm install eslint -g`
6. **ESLint config Google** : v0.4.0 or higher. Run `npm install eslint eslint-config-google -g`

## Setup

Inside the main repo run `./setup` this is a bash script that will install all the dependencies.

It will run `npm install from the main folder and inside the theme folder(theme/tranquilpeak) it'll
  - Run `npm install` to install all NPM dependencies
  - Run `bower install` to install all Bower dependencies

## Generate
- To demo the site run `hexo server`. This will create a server that runs on localhost:4000
- To generate HTML to be deployed 
  1. Set `url` & `root` in _config.yaml
  2. Run `hexo generate` - The generated site will be located in the public directory
- To deploy: 
  1. Edit the `deploy` section in _config.yaml 
  2. Run `hexo deploy`
    - Alternatively, you can run `hexo generate --deploy`

## Development
- To generate new posts 
  - Run `hexo new posts [title]` This will create a new post in source/_post/[title].md
- To generate new pages:
  - Run `hexo new page [title]` this will create a new page in source/[title]/index.md
- To edit the sidebar:
  - Edit theme/tranquilpeak/_config.yaml - this is where all the theme configuration is controlled from.

### CSS and Templates
- You can edit the css for the theme in theme/tranquilpeak/source/_css  
- You can edit the templates in theme/tranquilpeak/layout  
- If you edit the theme it will need to be regenerated. This is done by running `grunt buildProd` from theme/tranquilpeak