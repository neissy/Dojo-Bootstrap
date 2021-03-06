# Dojo-Bootstrap

An implementation of the excellent [Twitter Bootstrap](http://twitter.github.com/bootstrap/) framework using the [Dojo Toolkit](http://dojotoolkit.org). This project replaces the Twitter Bootstrap Javascript components with AMD-compatible Dojo modules. Tested with Dojo 1.8 and Twitter Bootstrap 2.1.

## Quick Start

+ `git clone git://github.com/xsokev/Dojo-Bootstrap.git`
+ `git submodule init`
+ `git submodule update`
+ Point your browser to test/index.html
+ Add [dojo sdk](https://github.com/dojo) under the vendor folder or add a symbolic link to the dojo sdk under the vendor folder

## Integration

See examples in tests/test_*.html

### In Brief

    <!DOCTYPE html>
    <html>
        <head>
            <meta charset="utf-8">
            <title>Dojo-Bootstrap</title>
            <meta name="viewport" content="width=device-width, initial-scale=1.0">
            <link rel="stylesheet" href="path/to/bootstrap/styles.css">
        </head>
    
        <body>
            <button type="button" id="loading-button" class="btn btn-primary"
                data-dojo-type="bootstrap/Button" data-dojo-props="loadingText: 'Loading...'">Load</button>
        
            <script>
                var dojoConfig = {
                    async: 1,
                    parseOnLoad: true,
                    packages: [
                        { name: "bootstrap", location: "path/to/Dojo-Bootstrap" }
                    ]
                };
            </script>
        
            <script type="text/javascript" src="path/to/dojo/dojo/dojo.js"></script>
    
            <script>
                require(["bootstrap/Button"], function (Button) {

                });
            </script>
        </body>
    </html>

## Useful resources

+ [Dojo-Bootstrap Website with examples for all the modules](http://dojobootstrap.com)
+ [Dojo Reference Guide (latest release version)](http://dojotoolkit.org/reference-guide/)
+ [Dojo Reference Guide (Dojo trunk)](http://livedocs.dojotoolkit.org/)
+ [Twitter Bootstrap](http://twitter.github.com/bootstrap/)

## License

Dojo Bootstrap is licensed under the [Apache License 2.0](http://www.apache.org/licenses/LICENSE-2.0)
