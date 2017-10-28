# angular
Angular Info, Samples and Stuff

## angular-cli

## angular-cli offline (no internet)
How I work with angular-cli on a computer that does not have internet access.
This is helpful for corportate, secure environments and during travel.

_STEPS_

You will need to perform these steps on a computer that has internet access.
After that you will be able to transfer some folders to your offline computer.

*Online Computer*

1. Install (www.nodejs.com)[www.nodejs.com] "LTS" version
2. Install (cli.angular.io)[cli.angular.io]
```
>npm install -g @angular/cli
>ng new myapp
// after npm install completes successfully
>cd myapp
>ng server
// make sure app was installed and runs correctly
```
3. Find your npm_cache folders (windows: %appdata%\Roaming\npm_cache)
4. zip npm_cache folder and name it npm_cache.zip

*Offline Computer*
1. Install (www.nodejs.com)[www.nodejs.com] "LTS" version
2. extract npm_cache.zip contents into your npm_cache folder (windows: %appdata%\Roaming\npm_cache)
3. configure npm to use your local npm_cache folder
```
>npm config set cache PATH_TO_CACHE_FOLDER
>npm config set cache min 999999999
>npm config shrinkwrap false
```
4. Install Angular-CLI from cache
```
>npm install -g @angular/cli
```
