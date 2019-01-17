<img src="https://raw.githubusercontent.com/transitive-bullshit/functional-typescript/master/logo.png" alt="FTS Logo" width="150" />

# FTS "Hello World" Example

This is a simple example which shows how to generate an FTS `Definition`, create an `FTS.HttpHandler`, and start a basic http server that wraps a "Hello World" function.

In order to run this example, you must first build the top-level `functional-typescript` package locally.

Once you have a server running, you can invoke your type-safe function over HTTP:

```bash
$ curl -s http://localhost:3000?name=GET
Hello GET!

$ curl -s http://localhost:3000 -d 'name=POST'
Hello POST!
```

Note that in this example, we're generating the FTS Definition and serving it together, but in practice it is recommended that you generate these definitions during your build step, alongside your normal TS => JS compilation. These definitions should be viewed as json build artifacts that are _referenced_ at runtime in your server or serverless function.

## License

MIT © [Travis Fischer](https://transitivebullsh.it)