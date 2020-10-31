## Steps to reproduce

Using Node 10.15.3 and yarn 1.22.5:

```
yarn
yarn nuxt build
```

## Actual result

```
Hash: 3e90303d1ef396b70bb2
Version: webpack 4.44.2
Time: 8785ms
Built at: 10/31/2020 3:31:46 PM
                                                                                                                    Asset       Size  Chunks                         Chunk Names
                                                                                           ../server/client.manifest.json   8.59 KiB          [emitted]
                                                                                                               0365909.js  291 bytes       3  [emitted] [immutable]  pages/123456789_123456789_123456789_123456789_
                                                                                                               3b59a57.js  291 bytes       7  [emitted] [immutable]  pages/test2/test
                                                                                                               3c5f1d6.js  291 bytes       5  [emitted] [immutable]  pages/test2
                                                                                                               7a0387b.js  291 bytes       4  [emitted] [immutable]  pages/test1/test
                                                                                                               8d52d82.js  291 bytes       6  [emitted] [immutable]  pages/test2/index
                                                                                                               9697a60.js   3.47 KiB       8  [emitted] [immutable]  runtime
                                                                                                                 LICENSES  389 bytes          [emitted]
                                                                                                          app.f8816a1.css  942 bytes       1  [emitted] [immutable]  app
                                                                                                               b0e005c.js    155 KiB       2  [emitted] [immutable]  commons/app
                                                                                                               ba6e3ea.js   45.2 KiB       1  [emitted] [immutable]  app
                                                                                                               fc7a588.js  336 bytes       0  [emitted] [immutable]  pages/123456789_123456789_123456789_123456789_/pages/test1/test/pages/test2/pages/test2/index/pages//6c0ffc7c
pages/123456789_123456789_123456789_123456789_/pages/test1/test/pages/test2/pages/test2/index/pages//6c0ffc7c.c67c3ba.css    119 KiB       0  [emitted] [immutable]  pages/123456789_123456789_123456789_123456789_/pages/test1/test/pages/test2/pages/test2/index/pages//6c0ffc7c
 + 2 hidden assets
Entrypoint app = 9697a60.js b0e005c.js app.f8816a1.css ba6e3ea.js

Hash: a5e29db0b41075160f15
Version: webpack 4.44.2
Time: 1675ms
Built at: 10/31/2020 3:31:47 PM
                                            Asset       Size  Chunks             Chunk Names
pages/123456789_123456789_123456789_123456789_.js   5.15 KiB       1  [emitted]  pages/123456789_123456789_123456789_123456789_
                              pages/test1/test.js   4.79 KiB       2  [emitted]  pages/test1/test
                                   pages/test2.js   4.77 KiB       3  [emitted]  pages/test2
                             pages/test2/index.js    4.8 KiB       4  [emitted]  pages/test2/index
                              pages/test2/test.js   4.79 KiB       5  [emitted]  pages/test2/test
                                        server.js     66 KiB       0  [emitted]  app
                             server.manifest.json  747 bytes          [emitted]
 + 6 hidden assets
Entrypoint app = server.js server.js.map
```

Note the invalid filename near `...pages//6c0ffc7c.c67c3ba.css` (double slash).

## Expected result

Valid filenames.
