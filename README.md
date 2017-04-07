# api documentation for  [grunt-rev (v0.1.0)](https://github.com/cbas/grunt-rev)  [![npm package](https://img.shields.io/npm/v/npmdoc-grunt-rev.svg?style=flat-square)](https://www.npmjs.org/package/npmdoc-grunt-rev) [![travis-ci.org build-status](https://api.travis-ci.org/npmdoc/node-npmdoc-grunt-rev.svg)](https://travis-ci.org/npmdoc/node-npmdoc-grunt-rev)
#### Static file asset revisioning through content hashing

[![NPM](https://nodei.co/npm/grunt-rev.png?downloads=true)](https://www.npmjs.com/package/grunt-rev)

[![apidoc](https://npmdoc.github.io/node-npmdoc-grunt-rev/build/screenCapture.buildNpmdoc.browser._2Fhome_2Ftravis_2Fbuild_2Fnpmdoc_2Fnode-npmdoc-grunt-rev_2Ftmp_2Fbuild_2Fapidoc.html.png)](https://npmdoc.github.io/node-npmdoc-grunt-rev/build/apidoc.html)

![npmPackageListing](https://npmdoc.github.io/node-npmdoc-grunt-rev/build/screenCapture.npmPackageListing.svg)

![npmPackageDependencyTree](https://npmdoc.github.io/node-npmdoc-grunt-rev/build/screenCapture.npmPackageDependencyTree.svg)



# package.json

```json

{
    "author": {
        "name": "Sebastiaan Deckers",
        "email": "seb@ninja.sg",
        "url": "http://ninja.sg"
    },
    "bugs": {
        "url": "https://github.com/cbas/grunt-rev/issues"
    },
    "dependencies": {},
    "description": "Static file asset revisioning through content hashing",
    "devDependencies": {
        "grunt": "0.4.0rc6",
        "grunt-contrib-clean": "0.4.0rc6",
        "grunt-contrib-copy": "0.4.0",
        "grunt-contrib-jshint": "0.1.1rc6",
        "grunt-contrib-nodeunit": "0.1.2rc6"
    },
    "directories": {},
    "dist": {
        "shasum": "b32427e7d842345839709343a58c387361694947",
        "tarball": "https://registry.npmjs.org/grunt-rev/-/grunt-rev-0.1.0.tgz"
    },
    "engines": {
        "node": ">= 0.8.0"
    },
    "homepage": "https://github.com/cbas/grunt-rev",
    "keywords": [
        "gruntplugin"
    ],
    "licenses": [
        {
            "type": "MIT",
            "url": "https://github.com/cbas/grunt-rev/blob/master/LICENSE-MIT"
        }
    ],
    "main": "Gruntfile.js",
    "maintainers": [
        {
            "name": "seb",
            "email": "seb@ninja.sg"
        }
    ],
    "name": "grunt-rev",
    "optionalDependencies": {},
    "readme": "# grunt-rev [![Build Status](https://travis-ci.org/cbas/grunt-rev.png)](https://travis-ci.org/cbas/grunt-rev)\n\n> Static file asset revisioning through content hashing\n\n## Getting Started\n_If you haven't used [grunt][] before, be sure to check out the [Getting Started][] guide._\n\nFrom the same directory as your project's [Gruntfile][Getting Started] and [package.json][], install this plugin with the following command:\n\n'''bash\nnpm install grunt-rev --save-dev\n'''\n\nOnce that's done, add this line to your project's Gruntfile:\n\n'''js\ngrunt.loadNpmTasks('grunt-rev');\n'''\n\nIf the plugin has been installed correctly, running 'grunt --help' at the command line should list the newly-installed plugin's task or tasks. In addition, the plugin should be listed in package.json as a 'devDependency', which ensures that it will be installed whenever the 'npm install' command is run.\n\n[grunt]: http://gruntjs.com/\n[Getting Started]: https://github.com/gruntjs/grunt/blob/devel/docs/getting_started.md\n[package.json]: https://npmjs.org/doc/json.html\n\n## The \"rev\" task\n\nUse the **rev** task together with [yeoman/grunt-usemin](https://github.com/yeoman/grunt-usemin) for cache busting of static files in your app. This allows them to be cached forever by the browser.\n\n### Overview\nIn your project's Gruntfile, add a section named 'rev' to the data object passed into 'grunt.initConfig()'.\n\n'''js\ngrunt.initConfig({\n  rev: {\n    options: {\n      algorithm: 'md5',\n      length: 8\n    },\n    assets: {\n      files: [{\n        src: [\n          'img/**/*.{jpg,jpeg,gif,png}',\n          'fonts/**/*.{eot,svg,ttf,woff}'\n        ]\n      }]\n    }\n  },\n})\n'''\n\n### Options\n\n#### options.algorithm\nType: 'String'\nDefault value: ''md5''\n\n'algorithm' is dependent on the available algorithms supported by the version of OpenSSL on the platform. Examples are ''sha1'', ''md5'', ''sha256'', ''sha512'', etc. On recent releases, 'openssl list-message-digest-algorithms' will display the available digest algorithms.\n\n#### options.length\nType: 'Number'\nDefault value: '8'\n\nThe number of characters of the file content hash to prefix the file name with.\n\n### Usage Examples\n\n#### Basic Asset Revving\nThis will rename 'app.js' and 'app.css' with an 8 character long hash prefix. For example 'js/9becff3a.app.js' and 'css/ae35dd05.app.css'. The hash value depends on the file contents.\n\n'''js\ngrunt.initConfig({\n  rev: {\n    files: {\n      src: ['scripts/app.js', 'css/app.css']\n    }\n  }\n})\n'''\n\n#### Custom Options\nChange the algorithm or length to style the generated asset file names. Note that the 'usemin' companion task requires at least one anycase hexadecimal character to prefix the file name.\n\n'''js\ngrunt.initConfig({\n  rev: {\n    options: {\n      algorithm: 'sha1',\n      length: 4\n    },\n    files: {\n      src: ['**/*.{js,css,png,jpg}']\n    }\n  }\n})\n'''\n\n## Contributing\nIn lieu of a formal styleguide, take care to maintain the existing coding style. Add unit tests for any new or changed functionality. Lint and test your code using [grunt][].\n\n## Release History\n_(Nothing yet)_\n",
    "readmeFilename": "README.md",
    "repository": {
        "type": "git",
        "url": "git://github.com/cbas/grunt-rev.git"
    },
    "scripts": {
        "test": "grunt test"
    },
    "version": "0.1.0"
}
```



# <a name="apidoc.tableOfContents"></a>[table of contents](#apidoc.tableOfContents)

#### [module grunt-rev](#apidoc.module.grunt-rev)



# <a name="apidoc.module.grunt-rev"></a>[module grunt-rev](#apidoc.module.grunt-rev)



# misc
- this document was created with [utility2](https://github.com/kaizhu256/node-utility2)
