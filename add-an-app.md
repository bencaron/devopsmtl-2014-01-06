# Add a simple application

Following on Dokku [installation exemple](https://github.com/progrium/dokku#deploy-an-app), lets install a [simple Nodejs application](https://github.com/heroku/node-js-sample):

## Clone the code

```bash
 ~/src/ ⮀ git clone https://github.com/heroku/node-js-sample
Cloning into 'node-js-sample'...
remote: Reusing existing pack: 313, done.
remote: Total 313 (delta 0), reused 0 (delta 0)
Receiving objects: 100% (313/313), 200.76 KiB, done.
Resolving deltas: 100% (15/15), done.
 ~/src/ ⮀ cd node-js-sample

## Add a remote

```bash
~/src/node-js-sample ⮀ ⭠ master  ⮀ git remote add myvm dokku@exemple.com:node
```

## Push the code to this remote

```bash
 ~/src/node-js-sample ⮀ ⭠ master  ⮀ git push myvm master
Counting objects: 313, done.
Delta compression using up to 4 threads.
Compressing objects: 100% (270/270), done.
Writing objects: 100% (313/313), 200.76 KiB, done.
Total 313 (delta 15), reused 313 (delta 15)
-----> Building node ...
       Node.js app detected
-----> Resolving engine versions
       Using Node.js version: 0.10.21
       Using npm version: 1.3.11
-----> Fetching Node.js binaries
-----> Vendoring node into slug
-----> Installing dependencies with npm
       npm http GET https://registry.npmjs.org/express
       npm http 200 https://registry.npmjs.org/express
       npm http GET https://registry.npmjs.org/express/-/express-3.3.8.tgz
       npm http 200 https://registry.npmjs.org/express/-/express-3.3.8.tgz
       npm http GET https://registry.npmjs.org/connect/2.8.8
       npm http GET https://registry.npmjs.org/commander/1.2.0
       npm http GET https://registry.npmjs.org/range-parser/0.0.4
       npm http GET https://registry.npmjs.org/mkdirp/0.3.5
       npm http GET https://registry.npmjs.org/cookie/0.1.0
       npm http GET https://registry.npmjs.org/buffer-crc32/0.2.1
       npm http GET https://registry.npmjs.org/fresh/0.2.0
       npm http GET https://registry.npmjs.org/methods/0.0.1
       npm http GET https://registry.npmjs.org/send/0.1.4
       npm http GET https://registry.npmjs.org/cookie-signature/1.0.1
       npm http GET https://registry.npmjs.org/debug
       npm http 200 https://registry.npmjs.org/range-parser/0.0.4
       npm http GET https://registry.npmjs.org/range-parser/-/range-parser-0.0.4.tgz
       npm http 200 https://registry.npmjs.org/connect/2.8.8
       npm http GET https://registry.npmjs.org/connect/-/connect-2.8.8.tgz
       npm http 200 https://registry.npmjs.org/commander/1.2.0
       npm http 200 https://registry.npmjs.org/mkdirp/0.3.5
       npm http 200 https://registry.npmjs.org/cookie/0.1.0
       npm http GET https://registry.npmjs.org/commander/-/commander-1.2.0.tgz
       npm http GET https://registry.npmjs.org/mkdirp/-/mkdirp-0.3.5.tgz
       npm http GET https://registry.npmjs.org/cookie/-/cookie-0.1.0.tgz
       npm http 200 https://registry.npmjs.org/buffer-crc32/0.2.1
       npm http GET https://registry.npmjs.org/buffer-crc32/-/buffer-crc32-0.2.1.tgz
       npm http 200 https://registry.npmjs.org/fresh/0.2.0
       npm http 200 https://registry.npmjs.org/methods/0.0.1
       npm http 200 https://registry.npmjs.org/send/0.1.4
       npm http 200 https://registry.npmjs.org/cookie-signature/1.0.1
       npm http 200 https://registry.npmjs.org/range-parser/-/range-parser-0.0.4.tgz
       npm http GET https://registry.npmjs.org/fresh/-/fresh-0.2.0.tgz
       npm http 200 https://registry.npmjs.org/debug
       npm http 200 https://registry.npmjs.org/buffer-crc32/-/buffer-crc32-0.2.1.tgz
       npm http GET https://registry.npmjs.org/methods/-/methods-0.0.1.tgz
       npm http GET https://registry.npmjs.org/send/-/send-0.1.4.tgz
       npm http GET https://registry.npmjs.org/cookie-signature/-/cookie-signature-1.0.1.tgz
       npm http 200 https://registry.npmjs.org/commander/-/commander-1.2.0.tgz
       npm http GET https://registry.npmjs.org/debug/-/debug-0.7.4.tgz
       npm http 200 https://registry.npmjs.org/fresh/-/fresh-0.2.0.tgz
       npm http 200 https://registry.npmjs.org/mkdirp/-/mkdirp-0.3.5.tgz
       npm http 200 https://registry.npmjs.org/cookie/-/cookie-0.1.0.tgz
       npm http 200 https://registry.npmjs.org/methods/-/methods-0.0.1.tgz
       npm http 200 https://registry.npmjs.org/send/-/send-0.1.4.tgz
       npm http 200 https://registry.npmjs.org/cookie-signature/-/cookie-signature-1.0.1.tgz
       npm http 200 https://registry.npmjs.org/debug/-/debug-0.7.4.tgz
       npm http 200 https://registry.npmjs.org/connect/-/connect-2.8.8.tgz
       npm http GET https://registry.npmjs.org/mime
       npm http GET https://registry.npmjs.org/keypress
       npm http GET https://registry.npmjs.org/qs/0.6.5
       npm http GET https://registry.npmjs.org/formidable/1.0.14
       npm http GET https://registry.npmjs.org/bytes/0.2.0
       npm http GET https://registry.npmjs.org/pause/0.0.1
       npm http GET https://registry.npmjs.org/uid2/0.0.2
       npm http 200 https://registry.npmjs.org/mime
       npm http 200 https://registry.npmjs.org/keypress
       npm http GET https://registry.npmjs.org/mime/-/mime-1.2.11.tgz
       npm http GET https://registry.npmjs.org/keypress/-/keypress-0.1.0.tgz
       npm http 200 https://registry.npmjs.org/pause/0.0.1
       npm http 200 https://registry.npmjs.org/uid2/0.0.2
       npm http GET https://registry.npmjs.org/pause/-/pause-0.0.1.tgz
       npm http GET https://registry.npmjs.org/uid2/-/uid2-0.0.2.tgz
       npm http 200 https://registry.npmjs.org/bytes/0.2.0
       npm http 200 https://registry.npmjs.org/qs/0.6.5
       npm http GET https://registry.npmjs.org/bytes/-/bytes-0.2.0.tgz
       npm http GET https://registry.npmjs.org/qs/-/qs-0.6.5.tgz
       npm http 200 https://registry.npmjs.org/keypress/-/keypress-0.1.0.tgz
       npm http 200 https://registry.npmjs.org/formidable/1.0.14
       npm http GET https://registry.npmjs.org/formidable/-/formidable-1.0.14.tgz
       npm http 200 https://registry.npmjs.org/mime/-/mime-1.2.11.tgz
       npm http 200 https://registry.npmjs.org/qs/-/qs-0.6.5.tgz
       npm http 200 https://registry.npmjs.org/formidable/-/formidable-1.0.14.tgz
       npm http 200 https://registry.npmjs.org/pause/-/pause-0.0.1.tgz
       npm http 200 https://registry.npmjs.org/uid2/-/uid2-0.0.2.tgz
       npm http 200 https://registry.npmjs.org/bytes/-/bytes-0.2.0.tgz
       express@3.3.8 node_modules/express
       ├── methods@0.0.1
       ├── range-parser@0.0.4
       ├── cookie-signature@1.0.1
       ├── fresh@0.2.0
       ├── debug@0.7.4
       ├── buffer-crc32@0.2.1
       ├── cookie@0.1.0
       ├── mkdirp@0.3.5
       ├── commander@1.2.0 (keypress@0.1.0)
       ├── send@0.1.4 (mime@1.2.11)
       └── connect@2.8.8 (uid2@0.0.2, pause@0.0.1, qs@0.6.5, bytes@0.2.0, formidable@1.0.14)
       express@3.3.8 /build/app/node_modules/express
       connect@2.8.8 /build/app/node_modules/express/node_modules/connect
       qs@0.6.5 /build/app/node_modules/express/node_modules/connect/node_modules/qs
       formidable@1.0.14 /build/app/node_modules/express/node_modules/connect/node_modules/formidable
       cookie-signature@1.0.1 /build/app/node_modules/express/node_modules/cookie-signature
       buffer-crc32@0.2.1 /build/app/node_modules/express/node_modules/buffer-crc32
       cookie@0.1.0 /build/app/node_modules/express/node_modules/cookie
       send@0.1.4 /build/app/node_modules/express/node_modules/send
       debug@0.7.4 /build/app/node_modules/express/node_modules/debug
       mime@1.2.11 /build/app/node_modules/express/node_modules/send/node_modules/mime
       fresh@0.2.0 /build/app/node_modules/express/node_modules/fresh
       range-parser@0.0.4 /build/app/node_modules/express/node_modules/range-parser
       bytes@0.2.0 /build/app/node_modules/express/node_modules/connect/node_modules/bytes
       pause@0.0.1 /build/app/node_modules/express/node_modules/connect/node_modules/pause
       uid2@0.0.2 /build/app/node_modules/express/node_modules/connect/node_modules/uid2
       methods@0.0.1 /build/app/node_modules/express/node_modules/methods
       commander@1.2.0 /build/app/node_modules/express/node_modules/commander
       keypress@0.1.0 /build/app/node_modules/express/node_modules/commander/node_modules/keypress
       mkdirp@0.3.5 /build/app/node_modules/express/node_modules/mkdirp
       Dependencies installed
-----> Building runtime environment
-----> Discovering process types
       Procfile declares types -> web
-----> Releasing node ...
-----> Deploying node ...
-----> Cleaning up ...
=====> Application deployed:
       http://node.exemple.com

To dokku@exemple.com:node
 * [new branch]      master -> master
```

## Docker side...

You now have a new container:

```bash
root@vagrant:/vagrant# docker ps
CONTAINER ID        IMAGE               COMMAND                CREATED             STATUS              PORTS                     NAMES
dc510d3af595        app/node:latest     /bin/bash -c /start    14 minutes ago      Up 14 minutes       0.0.0.0:49154->5000/tcp   prickly_albattani
```

## Browser side:

