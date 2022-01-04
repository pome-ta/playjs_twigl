# play.js の挙動

`index.js` を特別記述しなくても、`package.json`の`script:` で、node への指示ができてる


## start log

```
[ERR] `.bitly` not found.

Launching app... http://localhost:3001

[OK] development build
ℹ ｢wds｣: Project is running at http://localhost:3001/
ℹ ｢wds｣: webpack output is served from /js/
ℹ ｢wds｣: Content not from webpack is served from /private/var/mobile/Containers/Shared/AppGroup/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/File Provider Storage/Repositories/playjs_twigl/public
/private/var/mobile/Containers/Shared/AppGroup/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/File Provider Storage/Repositories/playjs_twigl/node_modules/opn/xdg-open:1
#!/bin/sh
^

SyntaxError: Invalid or unexpected token
    at wrapSafe (internal/modules/cjs/loader.js:1079:16)
    at Module._compile (internal/modules/cjs/loader.js:1138:23)
    at Object.Module._extensions..js (internal/modules/cjs/loader.js:1196:10)
    at Module.load (internal/modules/cjs/loader.js:1009:32)
    at Function.Module._load (internal/modules/cjs/loader.js:903:14)
    at Function.executeUserEntryPoint [as runMain] (internal/modules/run_main.js:74:12)
    at MessagePort.<anonymous> (internal/main/worker_thread.js:167:24)
    at MessagePort.emit (events.js:321:20)
    at MessagePort.onmessage (internal/worker/io.js:78:8)
ℹ ｢wdm｣: Hash: e954e0771f2eb092bb91
Version: webpack 4.46.0
Time: 3453ms
Built at: 01/04/2022 4:47:02 PM
    Asset      Size  Chunks             Chunk Names
script.js  3.72 MiB  script  [emitted]  script
Entrypoint script = script.js
[0] multi ../node_modules/webpack-dev-server/client?http://localhost:3001 ./script.js 40 bytes {script} [built]
[../node_modules/firebase/analytics/dist/index.esm.js] 68 bytes {script} [built]
[../node_modules/firebase/app/dist/index.cjs.js] 1.04 KiB {script} [built]
[../node_modules/firebase/database/dist/index.esm.js] 67 bytes {script} [built]
[../node_modules/promise-polyfill/src/index.js] 5.99 KiB {script} [built]
[../node_modules/webpack-dev-server/client/index.js?http://localhost:3001] ../node_modules/webpack-dev-server/client?http://localhost:3001 4.29 KiB {script} [built]
[../node_modules/webpack-dev-server/client/overlay.js] 3.52 KiB {script} [built]
[../node_modules/webpack-dev-server/client/socket.js] 1.53 KiB {script} [built]
[../node_modules/webpack-dev-server/client/utils/createSocketUrl.js] 2.91 KiB {script} [built]
[../node_modules/webpack-dev-server/client/utils/log.js] 964 bytes {script} [built]
[../node_modules/webpack-dev-server/client/utils/reloadApp.js] 1.59 KiB {script} [built]
[../node_modules/webpack-dev-server/client/utils/sendMessage.js] 402 bytes {script} [built]
[../node_modules/webpack-dev-server/node_modules/strip-ansi/index.js] 161 bytes {script} [built]
[../node_modules/webpack/hot sync ^\.\/log$] ../node_modules/webpack/hot sync nonrecursive ^\.\/log$ 170 bytes {script} [built]
[./script.js] 91.6 KiB {script} [built]
    + 44 hidden modules
ℹ ｢wdm｣: Compiled successfully.
```


## build log
 
```
[ERR] `.bitly` not found.

Launching app... http://localhost:3001

[OK] production build
Hash: b010b6a42bb8643c7918
Version: webpack 4.46.0
Time: 2873ms
Built at: 01/04/2022 4:45:49 PM
    Asset     Size  Chunks                    Chunk Names
script.js  370 KiB       0  [emitted]  [big]  script
Entrypoint script [big] = script.js
[16] ./script.js + 10 modules 301 KiB {0} [built]
     | ./script.js 91.6 KiB [built]
     | ./fragmen.js 39.3 KiB [built]
     | ./onomat.js 17.4 KiB [built]
     | ./music.js 7.82 KiB [built]
     | ./firedb.js 12.4 KiB [built]
     | ./shader_snippet/noise.glsl 8.65 KiB [built]
     |     + 5 hidden modules
    + 16 hidden modules

WARNING in asset size limit: The following asset(s) exceed the recommended size limit (244 KiB).
This can impact web performance.
Assets: 
  script.js (370 KiB)

WARNING in entrypoint size limit: The following entrypoint(s) combined asset size exceeds the recommended limit (244 KiB). This can impact web performance.
Entrypoints:
  script (370 KiB)
      script.js


WARNING in webpack performance recommendations: 
You can limit the size of your bundles by using import() or require.ensure to lazy load some parts of your application.
For more info visit https://webpack.js.org/guides/code-splitting/
```



## debug log

```
[ERR] `.bitly` not found.

Launching app... http://localhost:3001

[OK] development build
Hash: da2ab25102d00834ea8c
Version: webpack 4.46.0
Time: 3171ms
Built at: 01/04/2022 4:46:29 PM
    Asset      Size  Chunks             Chunk Names
script.js  2.85 MiB  script  [emitted]  script
Entrypoint script = script.js
[./firedb.js] 12.4 KiB {script} [built]
[./fragmen.js] 39.3 KiB {script} [built]
[./music.js] 7.82 KiB {script} [built]
[./onomat.js] 17.4 KiB {script} [built]
[./script.js] 91.6 KiB {script} [built]
[./shader_snippet/noise.glsl] 8.65 KiB {script} [built]
    + 21 hidden modules

```
