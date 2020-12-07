## Steps to reproduce

Using Node 10.15.3 and yarn 1.22.5:

```
yarn
yarn nuxt build
```

## Actual result

```
Hash: 41cabe28221b0ff75ecd
Version: webpack 4.44.2
Time: 15317ms
Built at: 12/07/2020 2:43:39 PM
                                                                                                                    Asset       Size  Chunks                         Chunk Names
                                                                                           ../server/client.manifest.json   8.43 KiB          [emitted]
                                                                                                               3111a34.js  334 bytes       0  [emitted] [immutable]  pages/123456789_123456789_123456789_123456789x/pages/test1/test/pages/test2/pages/test2/index/pages//6b37dd43
                                                                                                               3f88aec.js  291 bytes       5  [emitted] [immutable]  pages/test2
                                                                                                               40f8a86.js   45.4 KiB       1  [emitted] [immutable]  app
                                                                                                               49d5d73.js  291 bytes       6  [emitted] [immutable]  pages/test2/index
                                                                                                               8391b26.js    155 KiB       2  [emitted] [immutable]  commons/app
                                                                                                               98d2390.js  291 bytes       7  [emitted] [immutable]  pages/test2/test
                                                                                                                 LICENSES  390 bytes          [emitted]
                                                                                                          app.f8816a1.css  942 bytes       1  [emitted] [immutable]  app
                                                                                                               c39ec97.js  291 bytes       3  [emitted] [immutable]  pages/123456789_123456789_123456789_123456789x
                                                                                                               cb2859f.js   4.08 KiB       8  [emitted] [immutable]  runtime
                                                                                                               ee5817a.js  291 bytes       4  [emitted] [immutable]  pages/test1/test
pages/123456789_123456789_123456789_123456789x/pages/test1/test/pages/test2/pages/test2/index/pages//6b37dd43.c67c3ba.css    119 KiB       0  [emitted] [immutable]  pages/123456789_123456789_123456789_123456789x/pages/test1/test/pages/test2/pages/test2/index/pages//6b37dd43
 + 2 hidden assets
Entrypoint app = cb2859f.js 8391b26.js app.f8816a1.css 40f8a86.js

Hash: e4880bdbb08aae8a47c4
Version: webpack 4.44.2
Time: 4957ms
Built at: 12/07/2020 2:43:44 PM
                                            Asset       Size  Chunks             Chunk Names
pages/123456789_123456789_123456789_123456789x.js    142 KiB       1  [emitted]  pages/123456789_123456789_123456789_123456789x
                              pages/test1/test.js    142 KiB       2  [emitted]  pages/test1/test
                                   pages/test2.js    142 KiB       3  [emitted]  pages/test2
                             pages/test2/index.js    142 KiB       4  [emitted]  pages/test2/index
                              pages/test2/test.js    142 KiB       5  [emitted]  pages/test2/test
                                        server.js   67.1 KiB       0  [emitted]  app
                             server.manifest.json  747 bytes          [emitted]
 + 6 hidden assets
Entrypoint app = server.js server.js.map
```

Note the invalid filename near `pages//6b37dd43.c67c3ba.css` (double slash).

## Expected result

Valid filenames.
