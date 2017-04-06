# api documentation for  [forever-service (v0.5.9)](https://github.com/zapty/forever-service)  [![npm package](https://img.shields.io/npm/v/npmdoc-forever-service.svg?style=flat-square)](https://www.npmjs.org/package/npmdoc-forever-service) [![travis-ci.org build-status](https://api.travis-ci.org/npmdoc/node-npmdoc-forever-service.svg)](https://travis-ci.org/npmdoc/node-npmdoc-forever-service)
#### Provision node script as a service via forever, allowing it to automatically start on boot, working across various Linux distros and OS

[![NPM](https://nodei.co/npm/forever-service.png?downloads=true)](https://www.npmjs.com/package/forever-service)

[![apidoc](https://npmdoc.github.io/node-npmdoc-forever-service/build/screenCapture.buildNpmdoc.browser._2Fhome_2Ftravis_2Fbuild_2Fnpmdoc_2Fnode-npmdoc-forever-service_2Ftmp_2Fbuild_2Fapidoc.html.png)](https://npmdoc.github.io/node-npmdoc-forever-service/build/apidoc.html)

![npmPackageListing](https://npmdoc.github.io/node-npmdoc-forever-service/build/screenCapture.npmPackageListing.svg)

![npmPackageDependencyTree](https://npmdoc.github.io/node-npmdoc-forever-service/build/screenCapture.npmPackageDependencyTree.svg)



# package.json

```json

{
    "author": {
        "name": "Arvind Agarwal"
    },
    "bin": {
        "forever-service": "./bin/forever-service",
        "get-forever-config": "./bin/get-forever-config"
    },
    "bugs": {
        "url": "https://github.com/zapty/forever-service/issues"
    },
    "dependencies": {
        "async": "~0.9.0",
        "commander": "~2.3.0",
        "shelljs": "~0.3.0",
        "swig": "~1.4.2",
        "walker": "~1.0.6"
    },
    "description": "Provision node script as a service via forever, allowing it to automatically start on boot, working across various Linux distros and OS",
    "devDependencies": {
        "fs-extra": "^0.30.0",
        "mocha": "*",
        "should": "*"
    },
    "directories": {},
    "dist": {
        "shasum": "437302400aea09b9a2f0a2aa22ec737610cec75d",
        "tarball": "https://registry.npmjs.org/forever-service/-/forever-service-0.5.9.tgz"
    },
    "homepage": "https://github.com/zapty/forever-service",
    "keywords": [
        "forever",
        "nodejs",
        "aws",
        "amazon",
        "linux",
        "initd",
        "service",
        "logrotate",
        "reboot",
        "start",
        "service",
        "amazon linux",
        "centos",
        "redhat",
        "debian",
        "raspbian",
        "ubuntu",
        "busenlabs"
    ],
    "main": "lib/api.js",
    "maintainers": [
        {
            "name": "zapty",
            "email": "arvind@zapty.com"
        }
    ],
    "name": "forever-service",
    "optionalDependencies": {},
    "preferGlobal": "true",
    "readme": "ERROR: No README data found!",
    "repository": {
        "type": "git",
        "url": "git+https://github.com/zapty/forever-service.git"
    },
    "scripts": {
        "test": "mocha test/*.js"
    },
    "version": "0.5.9"
}
```



# <a name="apidoc.tableOfContents"></a>[table of contents](#apidoc.tableOfContents)

#### [module forever-service](#apidoc.module.forever-service)
1.  object <span class="apidocSignatureSpan">forever-service.</span>installer
1.  object <span class="apidocSignatureSpan">forever-service.</span>platforms
1.  object <span class="apidocSignatureSpan">forever-service.</span>scriptBuilder

#### [module forever-service.installer](#apidoc.module.forever-service.installer)
1.  [function <span class="apidocSignatureSpan">forever-service.installer.</span>delete (ctx, callback)](#apidoc.element.forever-service.installer.delete)
1.  [function <span class="apidocSignatureSpan">forever-service.installer.</span>install (ctx, callback)](#apidoc.element.forever-service.installer.install)
1.  [function <span class="apidocSignatureSpan">forever-service.installer.</span>splitEnvVariables (envVars)](#apidoc.element.forever-service.installer.splitEnvVariables)
1.  [function <span class="apidocSignatureSpan">forever-service.installer.</span>validateScriptName (scriptname)](#apidoc.element.forever-service.installer.validateScriptName)

#### [module forever-service.scriptBuilder](#apidoc.module.forever-service.scriptBuilder)
1.  [function <span class="apidocSignatureSpan">forever-service.scriptBuilder.</span>gen (ctx, callback)](#apidoc.element.forever-service.scriptBuilder.gen)



# <a name="apidoc.module.forever-service"></a>[module forever-service](#apidoc.module.forever-service)



# <a name="apidoc.module.forever-service.installer"></a>[module forever-service.installer](#apidoc.module.forever-service.installer)

#### <a name="apidoc.element.forever-service.installer.delete"></a>[function <span class="apidocSignatureSpan">forever-service.installer.</span>delete (ctx, callback)](#apidoc.element.forever-service.installer.delete)
- description and source-code
```javascript
delete = function (ctx, callback){
	scriptBuilder.gen(ctx, function(err, scripts){
		if(err) return callback(err);

		ctx.installer.delete(ctx, scripts, callback);
	});
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.forever-service.installer.install"></a>[function <span class="apidocSignatureSpan">forever-service.installer.</span>install (ctx, callback)](#apidoc.element.forever-service.installer.install)
- description and source-code
```javascript
install = function (ctx, callback){
	scriptBuilder.gen(ctx, function(err, scripts){
		if(err) return callback(err);

		ctx.installer.install(ctx, scripts, callback);
	});
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.forever-service.installer.splitEnvVariables"></a>[function <span class="apidocSignatureSpan">forever-service.installer.</span>splitEnvVariables (envVars)](#apidoc.element.forever-service.installer.splitEnvVariables)
- description and source-code
```javascript
splitEnvVariables = function (envVars){
	//Split at space, but ignore space inside quotes..
	return envVars.match(/(?:[^\s"']+|["'][^"']*["'])+/g);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.forever-service.installer.validateScriptName"></a>[function <span class="apidocSignatureSpan">forever-service.installer.</span>validateScriptName (scriptname)](#apidoc.element.forever-service.installer.validateScriptName)
- description and source-code
```javascript
validateScriptName = function (scriptname){
	if(scriptname && scriptname[0] === path.sep)
		return fs.existsSync(scriptname);
	else
		return fs.existsSync( process.cwd()+'/'+scriptname );
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.forever-service.scriptBuilder"></a>[module forever-service.scriptBuilder](#apidoc.module.forever-service.scriptBuilder)

#### <a name="apidoc.element.forever-service.scriptBuilder.gen"></a>[function <span class="apidocSignatureSpan">forever-service.scriptBuilder.</span>gen (ctx, callback)](#apidoc.element.forever-service.scriptBuilder.gen)
- description and source-code
```javascript
gen = function (ctx, callback){

	if(!ctx) throw "context missing";
	if(!ctx.platform) throw "platform missing";
	if(!callback && typeof(callback) !== "function") throw "callback missing";

	ctx.cwd = process.cwd();
	ctx.cli = process.argv.join(' ');
	var templateDir =  path.normalize( __dirname + '/..' ) +'/templates/'+ctx.platform;
	var filledTemplates = {};

	fs.exists(templateDir, function(exists){
		if(!exists) throw "platform "+ctx.platform+" not found";
		fs.readdir(templateDir, function(err, files){
			async.each(files,
				function(file, callback){
					if(file.match(/.template$/g)){
						genFile(ctx, templateDir, file, function(err, output){
							if(err) throw err;
							filledTemplates[output.file.replace('.template','')] = output.out;
							callback();
						});
					} else callback();
				},
				function(err){
					callback(err, filledTemplates);
				}
			);
		});
	});
}
```
- example usage
```shell
n/a
```



# misc
- this document was created with [utility2](https://github.com/kaizhu256/node-utility2)
