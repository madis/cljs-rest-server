## HTTP REST server on ClojureScript w/ hot reload

The title pretty much says it: a simple HTTP server with pure ClojureScript (minimal amount of standard Node.js libraries)

Used technologies and libraries:
1. [Reitit](https://github.com/metosin/reitit) for API endpoint routing
  - blog post with examples https://www.metosin.fi/blog/reitit/
2. [Macchiato](https://github.com/macchiato-framework/macchiato-core) ClojureScript micro framework (for http networking, minimal overhead)
  - docs: https://macchiato-framework.github.io/api/core/index.html
  - getting started: https://macchiato-framework.github.io/docs/getting-started
3. [shadow-cljs](https://shadow-cljs.github.io/docs/UsersGuide.html) for ClojureScript compilation
  - using `deps.edn` for dependency management
4. [Swagger UI](https://swagger.io/tools/swagger-ui/)

Bunch of the example code is based on this blog post https://dev.solita.fi/2020/05/26/clojurescript-web-serverwith-macchiato-shadowcljs-and-reitit.html by Heikki Hämäläinen.

## Usage

1. Start the build `clojure -A:shadow-cljs watch node-app`
2. Start the server `node ./out/node-app.js`

As hot reloading is implemented, after saving a file, shadow-cljs re-compiles the assets and runs associated hooks to stop & start again the server

Happy tinkering!
