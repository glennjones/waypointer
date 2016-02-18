# waypointer

## IN DEVELOPMENT - API NOT STABLE

A HAPI plug-in that provides a template framework for OpenAPI (aka swagger).

````bash
$ npm install waypointer
```

``` javascript
const Inert = require('inert');
const Vision = require('vision');
const HapiSwagger = require('hapi-swagger');
const Waypointer = require('waypointer');

let server = new Hapi.Server();
server.connection({
    host: 'localhost',
    port: 3007
});

server.register([
    Inert,
    Vision,
    HapiSwagger,
    Waypointer], (err) => {

        server.route(Routes);

        server.start((err) => {
            if (err) {
                console.log(err);
            } else {
                console.log('Server running at:', server.info.uri);
            }
        });
    });
```




## Lab test
The project has integration and unit tests. To run the test within the project type one of the following commands.
```bash
$ lab
$ lab -r html -o coverage.html
$ lab -r html -o coverage.html --lint
$ lab -r console -o stdout -r html -o coverage.html --lint
```

## Issues
If you find any issue please file here on github and I will try and fix them.