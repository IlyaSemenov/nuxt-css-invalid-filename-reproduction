## Steps to reproduce

Using Node 10.15.3 and yarn 1.22.5:

```
yarn
yarn nuxt build
```

## Actual result

```
Hash: c574ad6ea5fd6a34f912
Version: webpack 4.46.0
Time: 12258ms
Built at: 02/03/2021 12:03:26 AM
                                                                                                                    Asset       Size  Chunks                         Chunk Names
                                                                                           ../server/client.manifest.json   8.53 KiB          [emitted]
                                                                                                               04e9088.js  291 bytes       5  [emitted] [immutable]  pages/test2
                                                                                                               080808d.js  291 bytes       6  [emitted] [immutable]  pages/test2/index
                                                                                                               17d82ba.js    161 KiB       2  [emitted] [immutable]  commons/app
                                                                                                               42a7899.js  291 bytes       3  [emitted] [immutable]  pages/123456789_123456789_123456789_123456789x
                                                                                                               6913260.js   4.08 KiB       8  [emitted] [immutable]  runtime
                                                                                                               754663d.js  291 bytes       7  [emitted] [immutable]  pages/test2/test
                                                                                                               9e2551e.js  334 bytes       0  [emitted] [immutable]  pages/123456789_123456789_123456789_123456789x/pages/test1/test/pages/test2/pages/test2/index/pages//6b37dd43
                                                                                                                 LICENSES  390 bytes          [emitted]
                                                                                                          app.7a3f40f.css  942 bytes       1  [emitted] [immutable]  app
                                                                                                               ba5ac79.js   46.5 KiB       1  [emitted] [immutable]  app
                                                                                                               cbf7ac1.js  291 bytes       4  [emitted] [immutable]  pages/test1/test
pages/123456789_123456789_123456789_123456789x/pages/test1/test/pages/test2/pages/test2/index/pages//6b37dd43.c67c3ba.css    119 KiB       0  [emitted] [immutable]  pages/123456789_123456789_123456789_123456789x/pages/test1/test/pages/test2/pages/test2/index/pages//6b37dd43
 + 2 hidden assets
Entrypoint app = 6913260.js 17d82ba.js app.7a3f40f.css ba5ac79.js

Hash: fead869ff49d7189264d
Version: webpack 4.46.0
Time: 3121ms
Built at: 02/03/2021 12:03:29 AM
                                            Asset       Size  Chunks             Chunk Names
pages/123456789_123456789_123456789_123456789x.js    142 KiB       1  [emitted]  pages/123456789_123456789_123456789_123456789x
                              pages/test1/test.js    142 KiB       2  [emitted]  pages/test1/test
                                   pages/test2.js    142 KiB       3  [emitted]  pages/test2
                             pages/test2/index.js    142 KiB       4  [emitted]  pages/test2/index
                              pages/test2/test.js    142 KiB       5  [emitted]  pages/test2/test
                                        server.js   68.6 KiB       0  [emitted]  app
                             server.manifest.json  747 bytes          [emitted]
 + 6 hidden assets
Entrypoint app = server.js server.js.map
```

Note the invalid filename near `pages//6b37dd43.c67c3ba.css` (double slash).

## Expected result

Valid filenames.
