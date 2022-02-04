# Alloy Proxy

A node.js proxy that features URL encoding, and amazing compatablity!

# How to install and use:

`git clone https://github.com/titaniumnetwork-dev/alloyproxy.git`

`cd alloyproxy`

`npm install`

`npm start`

The default place for the proxy when its started is `https://localhost:443` but feel free to change it in config.json!

# How the proxy works:

The proxy works by using node-fetch (Basically Window.fetch ported to Node-js). 
Basically what the app is doing is node-fetch is sending the request to the server then
the app sends the response back to the server with the modifactions made to the attributes and elements.

When a attribute is rewritten, depending on the contents inside. It will turn:

`href="/assets/js/main.js"` into `href="/fetch/websiteURL/assets/js/main.js"`.

A porition of its rewriting is in client-side JS so `Element.setAttribute`, `window.fetch()`, XMLHttpRequest, and more are rewritten.

# Extra information:

If your gonna have an external website redirect to this proxy. Then we recommend you have the value base64 encoded and redirected to `/alloy?url=` then value.

# Known websites that work

- Google Search

- Discord

- LittleBigSnake

- Surviv.io

- Youtube

- Y8

- 1v1.LOL

- Old Reddit

and plenty more!

# Known issues that need to be fixed

- Better POST body parsing instead of using body-parser.

- Cookie header rewriting

# Updates to come in the future

- Full URL encoding / encryption mode

- Websocket proxing
