# api documentation for  [mysql2 (v1.2.0)](https://github.com/sidorares/node-mysql2#readme)  [![npm package](https://img.shields.io/npm/v/npmdoc-mysql2.svg?style=flat-square)](https://www.npmjs.org/package/npmdoc-mysql2) [![travis-ci.org build-status](https://api.travis-ci.org/npmdoc/node-npmdoc-mysql2.svg)](https://travis-ci.org/npmdoc/node-npmdoc-mysql2)
#### fast mysql driver. Implements core protocol, prepared statements, ssl and compression in native JS

[![NPM](https://nodei.co/npm/mysql2.png?downloads=true)](https://www.npmjs.com/package/mysql2)

[![apidoc](https://npmdoc.github.io/node-npmdoc-mysql2/build/screenCapture.buildNpmdoc.browser._2Fhome_2Ftravis_2Fbuild_2Fnpmdoc_2Fnode-npmdoc-mysql2_2Ftmp_2Fbuild_2Fapidoc.html.png)](https://npmdoc.github.io/node-npmdoc-mysql2/build/apidoc.html)

![npmPackageListing](https://npmdoc.github.io/node-npmdoc-mysql2/build/screenCapture.npmPackageListing.svg)

![npmPackageDependencyTree](https://npmdoc.github.io/node-npmdoc-mysql2/build/screenCapture.npmPackageDependencyTree.svg)



# package.json

```json

{
    "author": {
        "name": "Andrey Sidorov",
        "email": "sidorares@yandex.ru"
    },
    "bugs": {
        "url": "https://github.com/sidorares/node-mysql2/issues"
    },
    "dependencies": {
        "cardinal": "1.0.0",
        "denque": "^1.1.1",
        "generate-function": "^2.0.0",
        "iconv-lite": "^0.4.13",
        "long": "^3.2.0",
        "lru-cache": "^4.0.1",
        "named-placeholders": "1.1.1",
        "object-assign": "^4.1.1",
        "readable-stream": "2.2.2",
        "safe-buffer": "^5.0.1",
        "seq-queue": "0.0.5",
        "sqlstring": "^2.2.0"
    },
    "description": "fast mysql driver. Implements core protocol, prepared statements, ssl and compression in native JS",
    "devDependencies": {
        "assert-diff": "^1.0.1",
        "eslint": "3.15.0",
        "eslint-plugin-markdown": "^1.0.0-beta.2",
        "husky": "^0.13.0",
        "portfinder": "^1.0.10",
        "progress": "1.1.8",
        "urun": "0.0.8",
        "utest": "0.0.8"
    },
    "directories": {
        "example": "examples"
    },
    "dist": {
        "shasum": "3ac6a419a783a66aac8fd7eab8a71089a2612b79",
        "tarball": "https://registry.npmjs.org/mysql2/-/mysql2-1.2.0.tgz"
    },
    "engines": {
        "node": ">= 0.10"
    },
    "files": [
        "lib",
        "index.js",
        "promise.js"
    ],
    "gitHead": "c5c0c90000e72259381306d86f2c80ec9f4c38b1",
    "homepage": "https://github.com/sidorares/node-mysql2#readme",
    "keywords": [
        "mysql",
        "client",
        "server"
    ],
    "license": "MIT",
    "main": "index.js",
    "maintainers": [
        {
            "name": "iarna",
            "email": "me@re-becca.org"
        },
        {
            "name": "sidorares",
            "email": "sidorares@yandex.com"
        },
        {
            "name": "sushantdhiman",
            "email": "sushantdhiman@outlook.com"
        }
    ],
    "name": "mysql2",
    "optionalDependencies": {},
    "readme": "ERROR: No README data found!",
    "repository": {
        "type": "git",
        "url": "git+https://github.com/sidorares/node-mysql2.git"
    },
    "scripts": {
        "benchmark": "./benchmarks/run-unit.js",
        "lint": "npm run lint:docs && npm run lint:code",
        "lint:code": "eslint index.js promise.js 'lib/**/*.js' 'test/**/*.js'",
        "lint:docs": "eslint README.md Contributing.md 'documentation/**/*.md' examples/*.js",
        "precommit": "npm run lint",
        "test": "npm run lint && npm run test:raw",
        "test:raw": "node ./test/run.js && MYSQL_USE_COMPRESSION=1 node ./test/run.js"
    },
    "version": "1.2.0"
}
```



# <a name="apidoc.tableOfContents"></a>[table of contents](#apidoc.tableOfContents)

#### [module mysql2](#apidoc.module.mysql2)
1.  [function <span class="apidocSignatureSpan">mysql2.</span>Connection (opts)](#apidoc.element.mysql2.Connection)
1.  [function <span class="apidocSignatureSpan">mysql2.</span>connect (opts)](#apidoc.element.mysql2.connect)
1.  [function <span class="apidocSignatureSpan">mysql2.</span>connection_config (options)](#apidoc.element.mysql2.connection_config)
1.  [function <span class="apidocSignatureSpan">mysql2.</span>createConnection (opts)](#apidoc.element.mysql2.createConnection)
1.  [function <span class="apidocSignatureSpan">mysql2.</span>createConnectionPromise (opts)](#apidoc.element.mysql2.createConnectionPromise)
1.  [function <span class="apidocSignatureSpan">mysql2.</span>createPool (config)](#apidoc.element.mysql2.createPool)
1.  [function <span class="apidocSignatureSpan">mysql2.</span>createPoolCluster (config)](#apidoc.element.mysql2.createPoolCluster)
1.  [function <span class="apidocSignatureSpan">mysql2.</span>createPoolPromise (opts)](#apidoc.element.mysql2.createPoolPromise)
1.  [function <span class="apidocSignatureSpan">mysql2.</span>createServer (handler)](#apidoc.element.mysql2.createServer)
1.  [function <span class="apidocSignatureSpan">mysql2.</span>escape (val, stringifyObjects, timeZone)](#apidoc.element.mysql2.escape)
1.  [function <span class="apidocSignatureSpan">mysql2.</span>escapeId (val, forbidQualified)](#apidoc.element.mysql2.escapeId)
1.  [function <span class="apidocSignatureSpan">mysql2.</span>format (sql, values, stringifyObjects, timeZone)](#apidoc.element.mysql2.format)
1.  [function <span class="apidocSignatureSpan">mysql2.</span>packet_parser (onPacket, packetHeaderLength)](#apidoc.element.mysql2.packet_parser)
1.  [function <span class="apidocSignatureSpan">mysql2.</span>pool (options)](#apidoc.element.mysql2.pool)
1.  [function <span class="apidocSignatureSpan">mysql2.</span>pool_cluster (config)](#apidoc.element.mysql2.pool_cluster)
1.  [function <span class="apidocSignatureSpan">mysql2.</span>pool_connection (pool, options)](#apidoc.element.mysql2.pool_connection)
1.  [function <span class="apidocSignatureSpan">mysql2.</span>server ()](#apidoc.element.mysql2.server)
1.  object <span class="apidocSignatureSpan">mysql2.</span>CharsetToEncoding
1.  object <span class="apidocSignatureSpan">mysql2.</span>Charsets
1.  object <span class="apidocSignatureSpan">mysql2.</span>Connection.prototype
1.  object <span class="apidocSignatureSpan">mysql2.</span>Types
1.  object <span class="apidocSignatureSpan">mysql2.</span>auth_41
1.  object <span class="apidocSignatureSpan">mysql2.</span>compressed_protocol
1.  object <span class="apidocSignatureSpan">mysql2.</span>helpers
1.  object <span class="apidocSignatureSpan">mysql2.</span>packet_parser.prototype
1.  object <span class="apidocSignatureSpan">mysql2.</span>pool.prototype
1.  object <span class="apidocSignatureSpan">mysql2.</span>pool_cluster.prototype
1.  object <span class="apidocSignatureSpan">mysql2.</span>pool_connection.prototype
1.  object <span class="apidocSignatureSpan">mysql2.</span>promise
1.  object <span class="apidocSignatureSpan">mysql2.</span>server.prototype

#### [module mysql2.Connection](#apidoc.module.mysql2.Connection)
1.  [function <span class="apidocSignatureSpan">mysql2.</span>Connection (opts)](#apidoc.element.mysql2.Connection.Connection)
1.  [function <span class="apidocSignatureSpan">mysql2.Connection.</span>createQuery (sql, values, cb, config)](#apidoc.element.mysql2.Connection.createQuery)
1.  [function <span class="apidocSignatureSpan">mysql2.Connection.</span>statementKey (options)](#apidoc.element.mysql2.Connection.statementKey)
1.  [function <span class="apidocSignatureSpan">mysql2.Connection.</span>super_ ()](#apidoc.element.mysql2.Connection.super_)

#### [module mysql2.Connection.prototype](#apidoc.module.mysql2.Connection.prototype)
1.  [function <span class="apidocSignatureSpan">mysql2.Connection.prototype.</span>_addCommandClosedState (cmd)](#apidoc.element.mysql2.Connection.prototype._addCommandClosedState)
1.  [function <span class="apidocSignatureSpan">mysql2.Connection.prototype.</span>_binlogDump (opts, cb)](#apidoc.element.mysql2.Connection.prototype._binlogDump)
1.  [function <span class="apidocSignatureSpan">mysql2.Connection.prototype.</span>_bumpCompressedSequenceId (numPackets)](#apidoc.element.mysql2.Connection.prototype._bumpCompressedSequenceId)
1.  [function <span class="apidocSignatureSpan">mysql2.Connection.prototype.</span>_bumpSequenceId (numPackets)](#apidoc.element.mysql2.Connection.prototype._bumpSequenceId)
1.  [function <span class="apidocSignatureSpan">mysql2.Connection.prototype.</span>_handleFatalError (err)](#apidoc.element.mysql2.Connection.prototype._handleFatalError)
1.  [function <span class="apidocSignatureSpan">mysql2.Connection.prototype.</span>_handleNetworkError (err)](#apidoc.element.mysql2.Connection.prototype._handleNetworkError)
1.  [function <span class="apidocSignatureSpan">mysql2.Connection.prototype.</span>_handleTimeoutError ()](#apidoc.element.mysql2.Connection.prototype._handleTimeoutError)
1.  [function <span class="apidocSignatureSpan">mysql2.Connection.prototype.</span>_notifyError (err)](#apidoc.element.mysql2.Connection.prototype._notifyError)
1.  [function <span class="apidocSignatureSpan">mysql2.Connection.prototype.</span>_registerSlave (opts, cb)](#apidoc.element.mysql2.Connection.prototype._registerSlave)
1.  [function <span class="apidocSignatureSpan">mysql2.Connection.prototype.</span>_resetSequenceId ()](#apidoc.element.mysql2.Connection.prototype._resetSequenceId)
1.  [function <span class="apidocSignatureSpan">mysql2.Connection.prototype.</span>_resolveNamedPlaceholders (options)](#apidoc.element.mysql2.Connection.prototype._resolveNamedPlaceholders)
1.  [function <span class="apidocSignatureSpan">mysql2.Connection.prototype.</span>addCommand (cmd)](#apidoc.element.mysql2.Connection.prototype.addCommand)
1.  [function <span class="apidocSignatureSpan">mysql2.Connection.prototype.</span>beginTransaction (cb)](#apidoc.element.mysql2.Connection.prototype.beginTransaction)
1.  [function <span class="apidocSignatureSpan">mysql2.Connection.prototype.</span>changeUser (options, callback)](#apidoc.element.mysql2.Connection.prototype.changeUser)
1.  [function <span class="apidocSignatureSpan">mysql2.Connection.prototype.</span>close ()](#apidoc.element.mysql2.Connection.prototype.close)
1.  [function <span class="apidocSignatureSpan">mysql2.Connection.prototype.</span>commit (cb)](#apidoc.element.mysql2.Connection.prototype.commit)
1.  [function <span class="apidocSignatureSpan">mysql2.Connection.prototype.</span>connect (cb)](#apidoc.element.mysql2.Connection.prototype.connect)
1.  [function <span class="apidocSignatureSpan">mysql2.Connection.prototype.</span>createBinlogStream (opts)](#apidoc.element.mysql2.Connection.prototype.createBinlogStream)
1.  [function <span class="apidocSignatureSpan">mysql2.Connection.prototype.</span>destroy ()](#apidoc.element.mysql2.Connection.prototype.destroy)
1.  [function <span class="apidocSignatureSpan">mysql2.Connection.prototype.</span>end (callback)](#apidoc.element.mysql2.Connection.prototype.end)
1.  [function <span class="apidocSignatureSpan">mysql2.Connection.prototype.</span>escape (value)](#apidoc.element.mysql2.Connection.prototype.escape)
1.  [function <span class="apidocSignatureSpan">mysql2.Connection.prototype.</span>escapeId (value)](#apidoc.element.mysql2.Connection.prototype.escapeId)
1.  [function <span class="apidocSignatureSpan">mysql2.Connection.prototype.</span>execute (sql, values, cb)](#apidoc.element.mysql2.Connection.prototype.execute)
1.  [function <span class="apidocSignatureSpan">mysql2.Connection.prototype.</span>format (sql, values)](#apidoc.element.mysql2.Connection.prototype.format)
1.  [function <span class="apidocSignatureSpan">mysql2.Connection.prototype.</span>handlePacket (packet)](#apidoc.element.mysql2.Connection.prototype.handlePacket)
1.  [function <span class="apidocSignatureSpan">mysql2.Connection.prototype.</span>keyFromFields (fields, options)](#apidoc.element.mysql2.Connection.prototype.keyFromFields)
1.  [function <span class="apidocSignatureSpan">mysql2.Connection.prototype.</span>pause ()](#apidoc.element.mysql2.Connection.prototype.pause)
1.  [function <span class="apidocSignatureSpan">mysql2.Connection.prototype.</span>ping (cb)](#apidoc.element.mysql2.Connection.prototype.ping)
1.  [function <span class="apidocSignatureSpan">mysql2.Connection.prototype.</span>pipe ()](#apidoc.element.mysql2.Connection.prototype.pipe)
1.  [function <span class="apidocSignatureSpan">mysql2.Connection.prototype.</span>prepare (options, cb)](#apidoc.element.mysql2.Connection.prototype.prepare)
1.  [function <span class="apidocSignatureSpan">mysql2.Connection.prototype.</span>protocolError (message, code)](#apidoc.element.mysql2.Connection.prototype.protocolError)
1.  [function <span class="apidocSignatureSpan">mysql2.Connection.prototype.</span>query (sql, values, cb)](#apidoc.element.mysql2.Connection.prototype.query)
1.  [function <span class="apidocSignatureSpan">mysql2.Connection.prototype.</span>resume ()](#apidoc.element.mysql2.Connection.prototype.resume)
1.  [function <span class="apidocSignatureSpan">mysql2.Connection.prototype.</span>rollback (cb)](#apidoc.element.mysql2.Connection.prototype.rollback)
1.  [function <span class="apidocSignatureSpan">mysql2.Connection.prototype.</span>serverHandshake (args)](#apidoc.element.mysql2.Connection.prototype.serverHandshake)
1.  [function <span class="apidocSignatureSpan">mysql2.Connection.prototype.</span>startTLS (onSecure)](#apidoc.element.mysql2.Connection.prototype.startTLS)
1.  [function <span class="apidocSignatureSpan">mysql2.Connection.prototype.</span>unprepare (sql)](#apidoc.element.mysql2.Connection.prototype.unprepare)
1.  [function <span class="apidocSignatureSpan">mysql2.Connection.prototype.</span>write (buffer)](#apidoc.element.mysql2.Connection.prototype.write)
1.  [function <span class="apidocSignatureSpan">mysql2.Connection.prototype.</span>writeColumns (columns)](#apidoc.element.mysql2.Connection.prototype.writeColumns)
1.  [function <span class="apidocSignatureSpan">mysql2.Connection.prototype.</span>writeEof (warnings, statusFlags)](#apidoc.element.mysql2.Connection.prototype.writeEof)
1.  [function <span class="apidocSignatureSpan">mysql2.Connection.prototype.</span>writeError (args)](#apidoc.element.mysql2.Connection.prototype.writeError)
1.  [function <span class="apidocSignatureSpan">mysql2.Connection.prototype.</span>writeOk (args)](#apidoc.element.mysql2.Connection.prototype.writeOk)
1.  [function <span class="apidocSignatureSpan">mysql2.Connection.prototype.</span>writePacket (packet)](#apidoc.element.mysql2.Connection.prototype.writePacket)
1.  [function <span class="apidocSignatureSpan">mysql2.Connection.prototype.</span>writeTextResult (rows, columns)](#apidoc.element.mysql2.Connection.prototype.writeTextResult)
1.  [function <span class="apidocSignatureSpan">mysql2.Connection.prototype.</span>writeTextRow (column)](#apidoc.element.mysql2.Connection.prototype.writeTextRow)

#### [module mysql2.auth_41](#apidoc.module.mysql2.auth_41)
1.  [function <span class="apidocSignatureSpan">mysql2.auth_41.</span>calculateToken (password, scramble1, scramble2)](#apidoc.element.mysql2.auth_41.calculateToken)
1.  [function <span class="apidocSignatureSpan">mysql2.auth_41.</span>calculateTokenFromPasswordSha (passwordSha, scramble1, scramble2)](#apidoc.element.mysql2.auth_41.calculateTokenFromPasswordSha)
1.  [function <span class="apidocSignatureSpan">mysql2.auth_41.</span>doubleSha1 (password)](#apidoc.element.mysql2.auth_41.doubleSha1)
1.  [function <span class="apidocSignatureSpan">mysql2.auth_41.</span>verifyToken (publicSeed1, publicSeed2, token, doubleSha)](#apidoc.element.mysql2.auth_41.verifyToken)

#### [module mysql2.compressed_protocol](#apidoc.module.mysql2.compressed_protocol)
1.  [function <span class="apidocSignatureSpan">mysql2.compressed_protocol.</span>enableCompression (connection)](#apidoc.element.mysql2.compressed_protocol.enableCompression)

#### [module mysql2.connection_config](#apidoc.module.mysql2.connection_config)
1.  [function <span class="apidocSignatureSpan">mysql2.</span>connection_config (options)](#apidoc.element.mysql2.connection_config.connection_config)
1.  [function <span class="apidocSignatureSpan">mysql2.connection_config.</span>getCharsetNumber (charset)](#apidoc.element.mysql2.connection_config.getCharsetNumber)
1.  [function <span class="apidocSignatureSpan">mysql2.connection_config.</span>getDefaultFlags (options)](#apidoc.element.mysql2.connection_config.getDefaultFlags)
1.  [function <span class="apidocSignatureSpan">mysql2.connection_config.</span>getSSLProfile (name)](#apidoc.element.mysql2.connection_config.getSSLProfile)
1.  [function <span class="apidocSignatureSpan">mysql2.connection_config.</span>mergeFlags (default_flags, user_flags)](#apidoc.element.mysql2.connection_config.mergeFlags)
1.  [function <span class="apidocSignatureSpan">mysql2.connection_config.</span>parseUrl (url)](#apidoc.element.mysql2.connection_config.parseUrl)

#### [module mysql2.helpers](#apidoc.module.mysql2.helpers)
1.  [function <span class="apidocSignatureSpan">mysql2.helpers.</span>srcEscape (str)](#apidoc.element.mysql2.helpers.srcEscape)

#### [module mysql2.packet_parser](#apidoc.module.mysql2.packet_parser)
1.  [function <span class="apidocSignatureSpan">mysql2.</span>packet_parser (onPacket, packetHeaderLength)](#apidoc.element.mysql2.packet_parser.packet_parser)

#### [module mysql2.packet_parser.prototype](#apidoc.module.mysql2.packet_parser.prototype)
1.  [function <span class="apidocSignatureSpan">mysql2.packet_parser.prototype.</span>_flushLargePacket4 ()](#apidoc.element.mysql2.packet_parser.prototype._flushLargePacket4)
1.  [function <span class="apidocSignatureSpan">mysql2.packet_parser.prototype.</span>_flushLargePacket7 ()](#apidoc.element.mysql2.packet_parser.prototype._flushLargePacket7)
1.  [function <span class="apidocSignatureSpan">mysql2.packet_parser.prototype.</span>executeHeader2 (chunk)](#apidoc.element.mysql2.packet_parser.prototype.executeHeader2)
1.  [function <span class="apidocSignatureSpan">mysql2.packet_parser.prototype.</span>executeHeader3 (chunk)](#apidoc.element.mysql2.packet_parser.prototype.executeHeader3)
1.  [function <span class="apidocSignatureSpan">mysql2.packet_parser.prototype.</span>executePayload (chunk)](#apidoc.element.mysql2.packet_parser.prototype.executePayload)
1.  [function <span class="apidocSignatureSpan">mysql2.packet_parser.prototype.</span>executeStart (chunk)](#apidoc.element.mysql2.packet_parser.prototype.executeStart)

#### [module mysql2.pool](#apidoc.module.mysql2.pool)
1.  [function <span class="apidocSignatureSpan">mysql2.</span>pool (options)](#apidoc.element.mysql2.pool.pool)
1.  [function <span class="apidocSignatureSpan">mysql2.pool.</span>super_ ()](#apidoc.element.mysql2.pool.super_)

#### [module mysql2.pool.prototype](#apidoc.module.mysql2.pool.prototype)
1.  [function <span class="apidocSignatureSpan">mysql2.pool.prototype.</span>_removeConnection (connection)](#apidoc.element.mysql2.pool.prototype._removeConnection)
1.  [function <span class="apidocSignatureSpan">mysql2.pool.prototype.</span>end (cb)](#apidoc.element.mysql2.pool.prototype.end)
1.  [function <span class="apidocSignatureSpan">mysql2.pool.prototype.</span>escape (value)](#apidoc.element.mysql2.pool.prototype.escape)
1.  [function <span class="apidocSignatureSpan">mysql2.pool.prototype.</span>escapeId (value)](#apidoc.element.mysql2.pool.prototype.escapeId)
1.  [function <span class="apidocSignatureSpan">mysql2.pool.prototype.</span>execute (sql, values, cb)](#apidoc.element.mysql2.pool.prototype.execute)
1.  [function <span class="apidocSignatureSpan">mysql2.pool.prototype.</span>getConnection (cb)](#apidoc.element.mysql2.pool.prototype.getConnection)
1.  [function <span class="apidocSignatureSpan">mysql2.pool.prototype.</span>query (sql, values, cb)](#apidoc.element.mysql2.pool.prototype.query)
1.  [function <span class="apidocSignatureSpan">mysql2.pool.prototype.</span>releaseConnection (connection)](#apidoc.element.mysql2.pool.prototype.releaseConnection)

#### [module mysql2.pool_cluster](#apidoc.module.mysql2.pool_cluster)
1.  [function <span class="apidocSignatureSpan">mysql2.</span>pool_cluster (config)](#apidoc.element.mysql2.pool_cluster.pool_cluster)
1.  [function <span class="apidocSignatureSpan">mysql2.pool_cluster.</span>super_ ()](#apidoc.element.mysql2.pool_cluster.super_)

#### [module mysql2.pool_cluster.prototype](#apidoc.module.mysql2.pool_cluster.prototype)
1.  [function <span class="apidocSignatureSpan">mysql2.pool_cluster.prototype.</span>_clearFindCaches ()](#apidoc.element.mysql2.pool_cluster.prototype._clearFindCaches)
1.  [function <span class="apidocSignatureSpan">mysql2.pool_cluster.prototype.</span>_decreaseErrorCount (node)](#apidoc.element.mysql2.pool_cluster.prototype._decreaseErrorCount)
1.  [function <span class="apidocSignatureSpan">mysql2.pool_cluster.prototype.</span>_findNodeIds (pattern)](#apidoc.element.mysql2.pool_cluster.prototype._findNodeIds)
1.  [function <span class="apidocSignatureSpan">mysql2.pool_cluster.prototype.</span>_getConnection (node, cb)](#apidoc.element.mysql2.pool_cluster.prototype._getConnection)
1.  [function <span class="apidocSignatureSpan">mysql2.pool_cluster.prototype.</span>_getNode (id)](#apidoc.element.mysql2.pool_cluster.prototype._getNode)
1.  [function <span class="apidocSignatureSpan">mysql2.pool_cluster.prototype.</span>_increaseErrorCount (node)](#apidoc.element.mysql2.pool_cluster.prototype._increaseErrorCount)
1.  [function <span class="apidocSignatureSpan">mysql2.pool_cluster.prototype.</span>add (id, config)](#apidoc.element.mysql2.pool_cluster.prototype.add)
1.  [function <span class="apidocSignatureSpan">mysql2.pool_cluster.prototype.</span>end ()](#apidoc.element.mysql2.pool_cluster.prototype.end)
1.  [function <span class="apidocSignatureSpan">mysql2.pool_cluster.prototype.</span>getConnection (pattern, selector, cb)](#apidoc.element.mysql2.pool_cluster.prototype.getConnection)
1.  [function <span class="apidocSignatureSpan">mysql2.pool_cluster.prototype.</span>of (pattern, selector)](#apidoc.element.mysql2.pool_cluster.prototype.of)

#### [module mysql2.pool_connection](#apidoc.module.mysql2.pool_connection)
1.  [function <span class="apidocSignatureSpan">mysql2.</span>pool_connection (pool, options)](#apidoc.element.mysql2.pool_connection.pool_connection)
1.  [function <span class="apidocSignatureSpan">mysql2.pool_connection.</span>statementKey (options)](#apidoc.element.mysql2.pool_connection.statementKey)
1.  [function <span class="apidocSignatureSpan">mysql2.pool_connection.</span>super_ (opts)](#apidoc.element.mysql2.pool_connection.super_)

#### [module mysql2.pool_connection.prototype](#apidoc.module.mysql2.pool_connection.prototype)
1.  [function <span class="apidocSignatureSpan">mysql2.pool_connection.prototype.</span>_realEnd (callback)](#apidoc.element.mysql2.pool_connection.prototype._realEnd)
1.  [function <span class="apidocSignatureSpan">mysql2.pool_connection.prototype.</span>_removeFromPool ()](#apidoc.element.mysql2.pool_connection.prototype._removeFromPool)
1.  [function <span class="apidocSignatureSpan">mysql2.pool_connection.prototype.</span>destroy ()](#apidoc.element.mysql2.pool_connection.prototype.destroy)
1.  [function <span class="apidocSignatureSpan">mysql2.pool_connection.prototype.</span>end ()](#apidoc.element.mysql2.pool_connection.prototype.end)
1.  [function <span class="apidocSignatureSpan">mysql2.pool_connection.prototype.</span>release ()](#apidoc.element.mysql2.pool_connection.prototype.release)

#### [module mysql2.promise](#apidoc.module.mysql2.promise)
1.  [function <span class="apidocSignatureSpan">mysql2.promise.</span>createConnection (opts)](#apidoc.element.mysql2.promise.createConnection)
1.  [function <span class="apidocSignatureSpan">mysql2.promise.</span>createPool (opts)](#apidoc.element.mysql2.promise.createPool)

#### [module mysql2.server](#apidoc.module.mysql2.server)
1.  [function <span class="apidocSignatureSpan">mysql2.</span>server ()](#apidoc.element.mysql2.server.server)
1.  [function <span class="apidocSignatureSpan">mysql2.server.</span>super_ ()](#apidoc.element.mysql2.server.super_)

#### [module mysql2.server.prototype](#apidoc.module.mysql2.server.prototype)
1.  [function <span class="apidocSignatureSpan">mysql2.server.prototype.</span>_handleConnection (socket)](#apidoc.element.mysql2.server.prototype._handleConnection)
1.  [function <span class="apidocSignatureSpan">mysql2.server.prototype.</span>close (cb)](#apidoc.element.mysql2.server.prototype.close)
1.  [function <span class="apidocSignatureSpan">mysql2.server.prototype.</span>listen (port, host, backlog, callback)](#apidoc.element.mysql2.server.prototype.listen)



# <a name="apidoc.module.mysql2"></a>[module mysql2](#apidoc.module.mysql2)

#### <a name="apidoc.element.mysql2.Connection"></a>[function <span class="apidocSignatureSpan">mysql2.</span>Connection (opts)](#apidoc.element.mysql2.Connection)
- description and source-code
```javascript
function Connection(opts)
{
  EventEmitter.call(this);
  this.config = opts.config;

  // TODO: fill defaults
  // if no params, connect to /var/lib/mysql/mysql.sock ( /tmp/mysql.sock on OSX )
  // if host is given, connect to host:3306

  // TODO: use '/usr/local/mysql/bin/mysql_config --socket' output? as default socketPath
  // if there is no host/port and no socketPath parameters?

  if (!opts.config.stream) {
    if (opts.config.socketPath) {
      this.stream = Net.connect(opts.config.socketPath);
    } else {
      this.stream = Net.connect(opts.config.port, opts.config.host);
    }
  } else {
    // if stream is a function, treat it as "stream agent / factory"
    if (typeof opts.config.stream == 'function') {
      this.stream = opts.config.stream(opts);
    } else {
      this.stream = opts.config.stream;
    }
  }
  this._internalId = _connectionId++;

  this._commands = new Queue();
  this._command = null;

  this._paused = false;
  this._paused_packets = new Queue();

  this._statements = LRU({
    max: this.config.maxPreparedStatements,
    dispose: function (key, statement) { statement.close(); }
  });

  // TODO: make it lru cache
  // https://github.com/mercadolibre/node-simple-lru-cache
  // or https://github.com/rsms/js-lru
  // or https://github.com/monsur/jscache
  // or https://github.com/isaacs/node-lru-cache
  //
  // key is field.name + ':' + field.columnType + ':' field.flags + '/'
  this.textProtocolParsers = {};

  // TODO: not sure if cache should be separate (same key as with textProtocolParsers)
  // or part of prepared statements cache (key is sql query)
  this.binaryProtocolParsers = {};

  this.serverCapabilityFlags = 0;
  this.authorized = false;

  var connection = this;

  this.sequenceId = 0;
  this.compressedSequenceId = 0;

  this.threadId = null;
  this._handshakePacket = null;
  this._fatalError = null;
  this._protocolError = null;
  this._outOfOrderPackets = [];

  this.clientEncoding = CharsetToEncoding[this.config.charsetNumber];

  this.stream.once('error', connection._handleNetworkError.bind(this));

  // see https://gist.github.com/khoomeister/4985691#use-that-instead-of-bind
  this.packetParser = new PacketParser(function (p) {
    connection.handlePacket(p);
  });

  this.stream.on('data', function (data) {
    if (connection.connectTimeout) {
      Timers.clearTimeout(connection.connectTimeout);
      connection.connectTimeout = null;
    }
    connection.packetParser.execute(data);
  });

  this.stream.on('end', function () {
    // we need to set this flag everywhere where we want connection to close
    if (connection._closing) {
      return;
    }

    if (!connection._protocolError) { // no particular error message before disconnect
      connection._protocolError = new Error('Connection lost: The server closed the connection.');
      connection._protocolError.fatal = true;
      connection._protocolError.code = 'PROTOCOL_CONNECTION_LOST';
    }

    connection._notifyError(connection._protocolError);
  });
  var handshakeCommand;
  if (!this.config.isServer) {
    handshakeCommand = new Commands.ClientHandshake(this.config.clientFlags);
    handshakeCommand.on('end', function () {
      connection._handshakePacket = handshakeCommand.handshake;
      connection.threadId = handshakeCommand.handshake.connectionId;
      connection.emit('connect', handshakeCommand.handshake);
    });
    handshakeCommand.on('error', function (err) {
      connection._notifyError(err);
    });
    this.addCommand(handshakeCommand);
  }

  // in case there was no initiall handshake but we need to read sting, assume it utf-8
  // most common example: "Too many connections" error ( packet is sent immediately on connection attempt, we don't know server
encoding yet)
  // will be overwrittedn with actial encoding value as soon as server handshake packet is received
  this.serverEncoding = 'utf8';

  if (this.config.connectTimeout) {
    var timeoutHandler = this._handleTimeoutError.bind(this);
    this.connectTimeout = Timers.setTimeout(timeoutHandler, this.config.connectTimeout);
  }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mysql2.connect"></a>[function <span class="apidocSignatureSpan">mysql2.</span>connect (opts)](#apidoc.element.mysql2.connect)
- description and source-code
```javascript
connect = function (opts) {
  return new Connection({config: new ConnectionConfig(opts)});
}
```
- example usage
```shell
...
  }

  if (this.config.connectionLimit === 0 || this._allConnections.length < this.config.connectionLimit) {
connection = new PoolConnection(this, {config: this.config.connectionConfig});

this._allConnections.push(connection);

return connection.connect(function (err) {
  if (this._closed) {
    return cb(new Error('Pool is closed.'));
  }
  if (err) {
    return cb(err);
  }
...
```

#### <a name="apidoc.element.mysql2.connection_config"></a>[function <span class="apidocSignatureSpan">mysql2.</span>connection_config (options)](#apidoc.element.mysql2.connection_config)
- description and source-code
```javascript
function ConnectionConfig(options) {
  if (typeof options === 'string') {
    options = ConnectionConfig.parseUrl(options);
  }

  this.isServer = options.isServer;
  this.stream = options.stream;

  this.host = options.host || 'localhost';
  this.port = options.port || 3306;
  this.localAddress = options.localAddress;
  this.socketPath = options.socketPath;
  this.user = options.user || undefined;
  this.password = options.password || undefined;
  this.passwordSha1 = options.passwordSha1 || undefined;
  this.database = options.database;
  this.connectTimeout = (options.connectTimeout === undefined)
    ? (10 * 1000)
    : options.connectTimeout;
  this.insecureAuth = options.insecureAuth || false;
  this.supportBigNumbers = options.supportBigNumbers || false;
  this.bigNumberStrings = options.bigNumberStrings || false;
  this.decimalNumbers = options.decimalNumbers || false;
  this.dateStrings = options.dateStrings || false;
  this.debug = options.debug;
  this.trace = options.trace !== false;
  this.stringifyObjects = options.stringifyObjects || false;
  this.timezone = options.timezone || 'local';
  this.queryFormat = options.queryFormat;
  this.pool = options.pool || undefined;
  this.ssl = (typeof options.ssl === 'string')
    ? ConnectionConfig.getSSLProfile(options.ssl)
    : (options.ssl || false);
  this.multipleStatements = options.multipleStatements || false;
  this.rowsAsArray = options.rowsAsArray || false;
  this.namedPlaceholders = options.namedPlaceholders || false;
  this.nestTables = (options.nestTables === undefined) ? undefined : options.nestTables;
  this.typeCast = (options.typeCast === undefined)
    ? true
    : options.typeCast;

  if (this.timezone[0] == ' ') {
    // "+" is a url encoded char for space so it
    // gets translated to space when giving a
    // connection string..
    this.timezone = '+' + this.timezone.substr(1);
  }

  if (this.ssl) {
    // Default rejectUnauthorized to true
    this.ssl.rejectUnauthorized = this.ssl.rejectUnauthorized !== false;
  }

  this.maxPacketSize = 0;
  this.charsetNumber = (options.charset)
    ? ConnectionConfig.getCharsetNumber(options.charset)
    : options.charsetNumber || Charsets.UTF8MB4_UNICODE_CI;

  this.compress = options.compress || false;

  this.authSwitchHandler = options.authSwitchHandler;

  this.clientFlags = ConnectionConfig.mergeFlags(ConnectionConfig.getDefaultFlags(options),
                                                 options.flags || '');

  this.connectAttributes = options.connectAttributes;
  this.maxPreparedStatements = options.maxPreparedStatements || 16000;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mysql2.createConnection"></a>[function <span class="apidocSignatureSpan">mysql2.</span>createConnection (opts)](#apidoc.element.mysql2.createConnection)
- description and source-code
```javascript
createConnection = function (opts) {
  return new Connection({config: new ConnectionConfig(opts)});
}
```
- example usage
```shell
...
## First Query

'''js
// get the client
var mysql = require('mysql2');

// create the connection to database
var connection = mysql.createConnection({host:'localhost', user: 'root', database: 'test'});

// simple query
connection.query('SELECT * FROM 'table' WHERE 'name' = "Page" AND 'age' > 45', function (err, results, fields) {
  console.log(results); // results contains rows returned by server
  console.log(fields); // fields contains extra meta data about results, if available
});
...
```

#### <a name="apidoc.element.mysql2.createConnectionPromise"></a>[function <span class="apidocSignatureSpan">mysql2.</span>createConnectionPromise (opts)](#apidoc.element.mysql2.createConnectionPromise)
- description and source-code
```javascript
function createConnection(opts) {
  var coreConnection = core.createConnection(opts);
  var Promise = opts.Promise || global.Promise;
  if (!Promise) {
    throw new Error('no Promise implementation available.' +
      'Use promise-enabled node version or pass userland Promise' +
      ' implementation as parameter, for example: { Promise: require(\'es6-promise\').Promise }');
  }
  return new Promise(function (resolve, reject) {
    coreConnection.once('connect', function (connectParams) {
      resolve(new PromiseConnection(coreConnection, Promise));
    });
    coreConnection.once('error', reject);
  });
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mysql2.createPool"></a>[function <span class="apidocSignatureSpan">mysql2.</span>createPool (config)](#apidoc.element.mysql2.createPool)
- description and source-code
```javascript
createPool = function (config) {
  var PoolConfig = require('./lib/pool_config.js');
  var Pool = require('./lib/pool.js');
  return new Pool({config: new PoolConfig(config)});
}
```
- example usage
```shell
...
  c.end(function () {
    resolve();
  });
});
};

function createPool (opts) {
var corePool = core.createPool(opts);
var Promise = opts.Promise || global.Promise || require('es6-promise');

var promisePool = {
  getConnection: function () {
    return new Promise(function (resolve, reject) {
      corePool.getConnection(function (err, coreConnection) {
        if (err) {
...
```

#### <a name="apidoc.element.mysql2.createPoolCluster"></a>[function <span class="apidocSignatureSpan">mysql2.</span>createPoolCluster (config)](#apidoc.element.mysql2.createPoolCluster)
- description and source-code
```javascript
createPoolCluster = function (config) {
  var PoolCluster = require('./lib/pool_cluster.js');
  return new PoolCluster(config);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mysql2.createPoolPromise"></a>[function <span class="apidocSignatureSpan">mysql2.</span>createPoolPromise (opts)](#apidoc.element.mysql2.createPoolPromise)
- description and source-code
```javascript
function createPool(opts) {
  var corePool = core.createPool(opts);
  var Promise = opts.Promise || global.Promise || require('es6-promise');

  var promisePool = {
    getConnection: function () {
      return new Promise(function (resolve, reject) {
        corePool.getConnection(function (err, coreConnection) {
          if (err) {
            reject(err);
          } else {
            resolve(new PromiseConnection(coreConnection, Promise));
          }
        });
      });
    },

    query: function (sql, args) {
      return new Promise(function (resolve, reject) {
        var done = makeDoneCb(resolve, reject);
        if (args) {
          corePool.query(sql, args, done);
        } else {
          corePool.query(sql, done);
        }
      });
    },

    execute: function (sql, values) {
      return new Promise(function (resolve, reject) {
        corePool.execute(sql, values, makeDoneCb(resolve, reject));
      });
    },

    end: function () {
      return new Promise(function (resolve, reject) {
        corePool.end(function (err) {
          if (err) {
            reject(err);
          } else {
            resolve();
          }
        });
      });
    }
  };

  return promisePool;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mysql2.createServer"></a>[function <span class="apidocSignatureSpan">mysql2.</span>createServer (handler)](#apidoc.element.mysql2.createServer)
- description and source-code
```javascript
createServer = function (handler) {
  var Server = require('./lib/server.js');
  var s = new Server();
  if (handler) {
    s.on('connection', handler);
  }
  return s;
}
```
- example usage
```shell
...
var ConnectionConfig = require('./connection_config');

// TODO: inherit Server from net.Server
function Server ()
{
EventEmitter.call(this);
this.connections = [];
this._server = net.createServer(this._handleConnection.bind(this));
}
util.inherits(Server, EventEmitter);

Server.prototype._handleConnection = function (socket) {
var connectionConfig = new ConnectionConfig({stream: socket, isServer: true});
var connection = new Connection({config: connectionConfig});
this.emit('connection', connection);
...
```

#### <a name="apidoc.element.mysql2.escape"></a>[function <span class="apidocSignatureSpan">mysql2.</span>escape (val, stringifyObjects, timeZone)](#apidoc.element.mysql2.escape)
- description and source-code
```javascript
function escape(val, stringifyObjects, timeZone) {
  if (val === undefined || val === null) {
    return 'NULL';
  }

  switch (typeof val) {
    case 'boolean': return (val) ? 'true' : 'false';
    case 'number': return val+'';
    case 'object':
      if (val instanceof Date) {
        return SqlString.dateToString(val, timeZone || 'local');
      } else if (Array.isArray(val)) {
        return SqlString.arrayToList(val, timeZone);
      } else if (Buffer.isBuffer(val)) {
        return SqlString.bufferToString(val);
      } else if (stringifyObjects) {
        return escapeString(val.toString());
      } else {
        return SqlString.objectToValues(val, timeZone);
      }
    default: return escapeString(val);
  }
}
```
- example usage
```shell
...
  // Remove connection from free connections
  spliceConnection(this._freeConnections, connection);

  this.releaseConnection(connection);
};

Pool.prototype.escape = function (value) {
  return mysql.escape(value, this.config.connectionConfig.stringifyObjects, this.config.connectionConfig.timezone);
};

Pool.prototype.escapeId = function escapeId (value) {
  return mysql.escapeId(value, false);
};

function spliceConnection (queue, connection) {
...
```

#### <a name="apidoc.element.mysql2.escapeId"></a>[function <span class="apidocSignatureSpan">mysql2.</span>escapeId (val, forbidQualified)](#apidoc.element.mysql2.escapeId)
- description and source-code
```javascript
function escapeId(val, forbidQualified) {
  if (Array.isArray(val)) {
    var sql = '';

    for (var i = 0; i < val.length; i++) {
      sql += (i === 0 ? '' : ', ') + SqlString.escapeId(val[i], forbidQualified);
    }

    return sql;
  }

  if (forbidQualified) {
    return ''' + String(val).replace(/'/g, '''') + ''';
  }

  return ''' + String(val).replace(/'/g, '''').replace(/\./g, ''.'') + ''';
}
```
- example usage
```shell
...
};

Pool.prototype.escape = function (value) {
return mysql.escape(value, this.config.connectionConfig.stringifyObjects, this.config.connectionConfig.timezone);
};

Pool.prototype.escapeId = function escapeId (value) {
return mysql.escapeId(value, false);
};

function spliceConnection (queue, connection) {
var len = queue.length;
if (len) {
  if (queue.get(len - 1) === connection) {
    queue.pop();
...
```

#### <a name="apidoc.element.mysql2.format"></a>[function <span class="apidocSignatureSpan">mysql2.</span>format (sql, values, stringifyObjects, timeZone)](#apidoc.element.mysql2.format)
- description and source-code
```javascript
function format(sql, values, stringifyObjects, timeZone) {
  if (values == null) {
    return sql;
  }

  if (!(values instanceof Array || Array.isArray(values))) {
    values = [values];
  }

  var chunkIndex        = 0;
  var placeholdersRegex = /\?\??/g;
  var result            = '';
  var valuesIndex       = 0;
  var match;

  while (valuesIndex < values.length && (match = placeholdersRegex.exec(sql))) {
    var value = match[0] === '??'
        ? SqlString.escapeId(values[valuesIndex])
        : SqlString.escape(values[valuesIndex], stringifyObjects, timeZone);

    result += sql.slice(chunkIndex, match.index) + value;
    chunkIndex = placeholdersRegex.lastIndex;
    valuesIndex++;
  }

  if (chunkIndex === 0) {
    // Nothing was replaced
    return sql;
  }

  if (chunkIndex < sql.length) {
    return result + sql.slice(chunkIndex);
  }

  return result;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mysql2.packet_parser"></a>[function <span class="apidocSignatureSpan">mysql2.</span>packet_parser (onPacket, packetHeaderLength)](#apidoc.element.mysql2.packet_parser)
- description and source-code
```javascript
function PacketParser(onPacket, packetHeaderLength)
{
  // 4 for normal packets, 7 for comprssed protocol packets
  if (typeof packetHeaderLength == 'undefined') {
    packetHeaderLength = 4;
  }
  // array of last payload chunks
  // only used when current payload is not complete
  this.buffer = [];
  // total length of chunks on buffer
  this.bufferLength = 0;
  this.packetHeaderLength = packetHeaderLength;

  // incomplete header state: number of header bytes received
  this.headerLen = 0;

  // expected payload length
  this.length = 0;

  this.largePacketParts = [];
  this.firstPacketSequenceId = 0;

  this.onPacket = onPacket;
  this.execute = PacketParser.prototype.executeStart;
  this._flushLargePacket = packetHeaderLength == 7 ?
    this._flushLargePacket7 : this._flushLargePacket4;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mysql2.pool"></a>[function <span class="apidocSignatureSpan">mysql2.</span>pool (options)](#apidoc.element.mysql2.pool)
- description and source-code
```javascript
function Pool(options) {
  EventEmitter.call(this);
  this.config = options.config;
  this.config.connectionConfig.pool = this;

  this._allConnections = new Queue();
  this._freeConnections = new Queue();
  this._connectionQueue = new Queue();
  this._closed = false;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mysql2.pool_cluster"></a>[function <span class="apidocSignatureSpan">mysql2.</span>pool_cluster (config)](#apidoc.element.mysql2.pool_cluster)
- description and source-code
```javascript
function PoolCluster(config) {
  EventEmitter.call(this);

  config = config || {};
  this._canRetry = typeof config.canRetry === 'undefined' ? true : config.canRetry;
  this._removeNodeErrorCount = config.removeNodeErrorCount || 5;
  this._defaultSelector = config.defaultSelector || 'RR';

  this._closed = false;
  this._lastId = 0;
  this._nodes = {};
  this._serviceableNodeIds = [];
  this._namespaces = {};
  this._findCaches = {};
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mysql2.pool_connection"></a>[function <span class="apidocSignatureSpan">mysql2.</span>pool_connection (pool, options)](#apidoc.element.mysql2.pool_connection)
- description and source-code
```javascript
function PoolConnection(pool, options) {
  Connection.call(this, options);
  this._pool = pool;

  // When a fatal error occurs the connection's protocol ends, which will cause
  // the connection to end as well, thus we only need to watch for the end event
  // and we will be notified of disconnects.
  var connection = this;
  this.on('end', function (err) { this._removeFromPool(); });
  this.on('error', function (err) { this._removeFromPool(); });
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mysql2.server"></a>[function <span class="apidocSignatureSpan">mysql2.</span>server ()](#apidoc.element.mysql2.server)
- description and source-code
```javascript
function Server()
{
  EventEmitter.call(this);
  this.connections = [];
  this._server = net.createServer(this._handleConnection.bind(this));
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.mysql2.Connection"></a>[module mysql2.Connection](#apidoc.module.mysql2.Connection)

#### <a name="apidoc.element.mysql2.Connection.Connection"></a>[function <span class="apidocSignatureSpan">mysql2.</span>Connection (opts)](#apidoc.element.mysql2.Connection.Connection)
- description and source-code
```javascript
function Connection(opts)
{
  EventEmitter.call(this);
  this.config = opts.config;

  // TODO: fill defaults
  // if no params, connect to /var/lib/mysql/mysql.sock ( /tmp/mysql.sock on OSX )
  // if host is given, connect to host:3306

  // TODO: use '/usr/local/mysql/bin/mysql_config --socket' output? as default socketPath
  // if there is no host/port and no socketPath parameters?

  if (!opts.config.stream) {
    if (opts.config.socketPath) {
      this.stream = Net.connect(opts.config.socketPath);
    } else {
      this.stream = Net.connect(opts.config.port, opts.config.host);
    }
  } else {
    // if stream is a function, treat it as "stream agent / factory"
    if (typeof opts.config.stream == 'function') {
      this.stream = opts.config.stream(opts);
    } else {
      this.stream = opts.config.stream;
    }
  }
  this._internalId = _connectionId++;

  this._commands = new Queue();
  this._command = null;

  this._paused = false;
  this._paused_packets = new Queue();

  this._statements = LRU({
    max: this.config.maxPreparedStatements,
    dispose: function (key, statement) { statement.close(); }
  });

  // TODO: make it lru cache
  // https://github.com/mercadolibre/node-simple-lru-cache
  // or https://github.com/rsms/js-lru
  // or https://github.com/monsur/jscache
  // or https://github.com/isaacs/node-lru-cache
  //
  // key is field.name + ':' + field.columnType + ':' field.flags + '/'
  this.textProtocolParsers = {};

  // TODO: not sure if cache should be separate (same key as with textProtocolParsers)
  // or part of prepared statements cache (key is sql query)
  this.binaryProtocolParsers = {};

  this.serverCapabilityFlags = 0;
  this.authorized = false;

  var connection = this;

  this.sequenceId = 0;
  this.compressedSequenceId = 0;

  this.threadId = null;
  this._handshakePacket = null;
  this._fatalError = null;
  this._protocolError = null;
  this._outOfOrderPackets = [];

  this.clientEncoding = CharsetToEncoding[this.config.charsetNumber];

  this.stream.once('error', connection._handleNetworkError.bind(this));

  // see https://gist.github.com/khoomeister/4985691#use-that-instead-of-bind
  this.packetParser = new PacketParser(function (p) {
    connection.handlePacket(p);
  });

  this.stream.on('data', function (data) {
    if (connection.connectTimeout) {
      Timers.clearTimeout(connection.connectTimeout);
      connection.connectTimeout = null;
    }
    connection.packetParser.execute(data);
  });

  this.stream.on('end', function () {
    // we need to set this flag everywhere where we want connection to close
    if (connection._closing) {
      return;
    }

    if (!connection._protocolError) { // no particular error message before disconnect
      connection._protocolError = new Error('Connection lost: The server closed the connection.');
      connection._protocolError.fatal = true;
      connection._protocolError.code = 'PROTOCOL_CONNECTION_LOST';
    }

    connection._notifyError(connection._protocolError);
  });
  var handshakeCommand;
  if (!this.config.isServer) {
    handshakeCommand = new Commands.ClientHandshake(this.config.clientFlags);
    handshakeCommand.on('end', function () {
      connection._handshakePacket = handshakeCommand.handshake;
      connection.threadId = handshakeCommand.handshake.connectionId;
      connection.emit('connect', handshakeCommand.handshake);
    });
    handshakeCommand.on('error', function (err) {
      connection._notifyError(err);
    });
    this.addCommand(handshakeCommand);
  }

  // in case there was no initiall handshake but we need to read sting, assume it utf-8
  // most common example: "Too many connections" error ( packet is sent immediately on connection attempt, we don't know server
encoding yet)
  // will be overwrittedn with actial encoding value as soon as server handshake packet is received
  this.serverEncoding = 'utf8';

  if (this.config.connectTimeout) {
    var timeoutHandler = this._handleTimeoutError.bind(this);
    this.connectTimeout = Timers.setTimeout(timeoutHandler, this.config.connectTimeout);
  }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mysql2.Connection.createQuery"></a>[function <span class="apidocSignatureSpan">mysql2.Connection.</span>createQuery (sql, values, cb, config)](#apidoc.element.mysql2.Connection.createQuery)
- description and source-code
```javascript
function createQuery(sql, values, cb, config) {
  var options = {
    rowsAsArray: config.rowsAsArray
  };
  if (typeof sql === 'object') {
    // query(options, cb)
    options = sql;
    if (typeof values === 'function') {
      cb = values;
    } else if (values !== undefined) {
      options.values = values;
    }
  } else if (typeof values === 'function') {
    // query(sql, cb)
    cb = values;
    options.sql = sql;
    options.values = undefined;
  } else {
    // query(sql, values, cb)
    options.sql = sql;
    options.values = values;
  }
  return new Commands.Query(options, cb);
}
```
- example usage
```shell
...
for (var i = 0; i < this._allConnections.length; i++) {
  connection = this._allConnections.get(i);
  connection._realEnd(endCB);
}
};

Pool.prototype.query = function (sql, values, cb) {
var cmdQuery = Connection.createQuery(sql, values, cb, this.config.connectionConfig);
cmdQuery.namedPlaceholders = this.config.connectionConfig.namedPlaceholders;

this.getConnection(function (err, conn) {
  if (err) {
    if (typeof cmdQuery.onResult === 'function') {
      cmdQuery.onResult(err);
    } else {
...
```

#### <a name="apidoc.element.mysql2.Connection.statementKey"></a>[function <span class="apidocSignatureSpan">mysql2.Connection.</span>statementKey (options)](#apidoc.element.mysql2.Connection.statementKey)
- description and source-code
```javascript
statementKey = function (options) {
  return (typeof options.nestTables) +
    '/' + options.nestTables + '/' + options.rowsAsArray + options.sql;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mysql2.Connection.super_"></a>[function <span class="apidocSignatureSpan">mysql2.Connection.</span>super_ ()](#apidoc.element.mysql2.Connection.super_)
- description and source-code
```javascript
function EventEmitter() {
  EventEmitter.init.call(this);
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.mysql2.Connection.prototype"></a>[module mysql2.Connection.prototype](#apidoc.module.mysql2.Connection.prototype)

#### <a name="apidoc.element.mysql2.Connection.prototype._addCommandClosedState"></a>[function <span class="apidocSignatureSpan">mysql2.Connection.prototype.</span>_addCommandClosedState (cmd)](#apidoc.element.mysql2.Connection.prototype._addCommandClosedState)
- description and source-code
```javascript
_addCommandClosedState = function (cmd) {
  var err = new Error('Can\'t add new command when connection is in closed state');
  err.fatal = true;
  if (cmd.onResult) {
    cmd.onResult(err);
  } else {
    this.emit('error', err);
  }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mysql2.Connection.prototype._binlogDump"></a>[function <span class="apidocSignatureSpan">mysql2.Connection.prototype.</span>_binlogDump (opts, cb)](#apidoc.element.mysql2.Connection.prototype._binlogDump)
- description and source-code
```javascript
function binlogDump(opts, cb) {
  return this.addCommand(new Commands.BinlogDump(opts, cb));
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mysql2.Connection.prototype._bumpCompressedSequenceId"></a>[function <span class="apidocSignatureSpan">mysql2.Connection.prototype.</span>_bumpCompressedSequenceId (numPackets)](#apidoc.element.mysql2.Connection.prototype._bumpCompressedSequenceId)
- description and source-code
```javascript
_bumpCompressedSequenceId = function (numPackets) {
  this.compressedSequenceId += numPackets;
  this.compressedSequenceId %= 256;
}
```
- example usage
```shell
...
if (deflatedLength !== 0) {
  connection.inflateQueue.push(function (task) {
    zlib.inflate(body, function (err, data) {
      if (err) {
        connection._handleNetworkError(err);
        return;
      }
      connection._bumpCompressedSequenceId(packet.numPackets);
      connection._inflatedPacketsParser.execute(data);
      task.done();
    });
  });
} else {
  connection.inflateQueue.push(function (task) {
    connection._bumpCompressedSequenceId(packet.numPackets);
...
```

#### <a name="apidoc.element.mysql2.Connection.prototype._bumpSequenceId"></a>[function <span class="apidocSignatureSpan">mysql2.Connection.prototype.</span>_bumpSequenceId (numPackets)](#apidoc.element.mysql2.Connection.prototype._bumpSequenceId)
- description and source-code
```javascript
_bumpSequenceId = function (numPackets) {
  this.sequenceId += numPackets;
  this.sequenceId %= 256;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mysql2.Connection.prototype._handleFatalError"></a>[function <span class="apidocSignatureSpan">mysql2.Connection.prototype.</span>_handleFatalError (err)](#apidoc.element.mysql2.Connection.prototype._handleFatalError)
- description and source-code
```javascript
_handleFatalError = function (err) {
  var connection = this;
  err.fatal = true;
  // stop receiving packets
  connection.stream.removeAllListeners('data');
  connection.addCommand = connection._addCommandClosedState;
  connection.write = function () {
    connection.emit('error', new Error('Can\'t write in closed state'));
  };
  connection._notifyError(err);
  connection._fatalError = err;
}
```
- example usage
```shell
...
  // seqqueue is used here because zlib async execution is routed via thread pool
  // internally and when we have multiple compressed packets arriving we need
  // to assemble uncompressed result sequentially
  (function (seqId) {
    connection.deflateQueue.push(function (task) {
      zlib.deflate(buffer, function (err, compressed) {
if (err) {
  connection._handleFatalError(err);
  return;
}
var compressedLength = compressed.length;

if (compressedLength < packetLen) {
  compressHeader.writeUInt8(compressedLength & 0xff, 0);
  compressHeader.writeUInt16LE(compressedLength >> 8, 1);
...
```

#### <a name="apidoc.element.mysql2.Connection.prototype._handleNetworkError"></a>[function <span class="apidocSignatureSpan">mysql2.Connection.prototype.</span>_handleNetworkError (err)](#apidoc.element.mysql2.Connection.prototype._handleNetworkError)
- description and source-code
```javascript
_handleNetworkError = function (err) {
  this._handleFatalError(err);
}
```
- example usage
```shell
...
var body = packet.readBuffer();


if (deflatedLength !== 0) {
  connection.inflateQueue.push(function (task) {
    zlib.inflate(body, function (err, data) {
      if (err) {
        connection._handleNetworkError(err);
        return;
      }
      connection._bumpCompressedSequenceId(packet.numPackets);
      connection._inflatedPacketsParser.execute(data);
      task.done();
    });
  });
...
```

#### <a name="apidoc.element.mysql2.Connection.prototype._handleTimeoutError"></a>[function <span class="apidocSignatureSpan">mysql2.Connection.prototype.</span>_handleTimeoutError ()](#apidoc.element.mysql2.Connection.prototype._handleTimeoutError)
- description and source-code
```javascript
_handleTimeoutError = function () {
  if (this.connectTimeout) {
    Timers.clearTimeout(this.connectTimeout);
    this.connectTimeout = null;
  }

  this.stream.destroy && this.stream.destroy();

  var err = new Error('connect ETIMEDOUT');
  err.errorno = 'ETIMEDOUT';
  err.code = 'ETIMEDOUT';
  err.syscall = 'connect';

  this._handleNetworkError(err);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mysql2.Connection.prototype._notifyError"></a>[function <span class="apidocSignatureSpan">mysql2.Connection.prototype.</span>_notifyError (err)](#apidoc.element.mysql2.Connection.prototype._notifyError)
- description and source-code
```javascript
_notifyError = function (err) {
  var connection = this;

  // prevent from emitting 'PROTOCOL_CONNECTION_LOST' after EPIPE or ECONNRESET
  if (connection._fatalError) {
    return;
  }

  var command;

  // if there is no active command, notify connection
  // if there are commands and all of them have callbacks, pass error via callback
  var bubbleErrorToConnection = !connection._command;
  if (connection._command && connection._command.onResult) {
    connection._command.onResult(err);
    connection._command = null;
  } else {
    bubbleErrorToConnection = true;
  }
  while ((command = connection._commands.shift())) {
    if (command.onResult) {
      command.onResult(err);
    } else {
      bubbleErrorToConnection = true;
    }
  }
  // notify connection if some comands in the queue did not have callbacks
  // or if this is pool connection ( so it can be removed from pool )
  if (bubbleErrorToConnection || connection._pool) {
    connection.emit('error', err);
  }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mysql2.Connection.prototype._registerSlave"></a>[function <span class="apidocSignatureSpan">mysql2.Connection.prototype.</span>_registerSlave (opts, cb)](#apidoc.element.mysql2.Connection.prototype._registerSlave)
- description and source-code
```javascript
function registerSlave(opts, cb) {
  return this.addCommand(new Commands.RegisterSlave(opts, cb));
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mysql2.Connection.prototype._resetSequenceId"></a>[function <span class="apidocSignatureSpan">mysql2.Connection.prototype.</span>_resetSequenceId ()](#apidoc.element.mysql2.Connection.prototype._resetSequenceId)
- description and source-code
```javascript
_resetSequenceId = function () {
  this.sequenceId = 0;
  this.compressedSequenceId = 0;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mysql2.Connection.prototype._resolveNamedPlaceholders"></a>[function <span class="apidocSignatureSpan">mysql2.Connection.prototype.</span>_resolveNamedPlaceholders (options)](#apidoc.element.mysql2.Connection.prototype._resolveNamedPlaceholders)
- description and source-code
```javascript
_resolveNamedPlaceholders = function (options) {
  var unnamed;
  if (this.config.namedPlaceholders || options.namedPlaceholders) {
    if (convertNamedPlaceholders === null) {
      convertNamedPlaceholders = require('named-placeholders')();
    }
    unnamed = convertNamedPlaceholders(options.sql, options.values);
    options.sql = unnamed[0];
    options.values = unnamed[1];
  }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mysql2.Connection.prototype.addCommand"></a>[function <span class="apidocSignatureSpan">mysql2.Connection.prototype.</span>addCommand (cmd)](#apidoc.element.mysql2.Connection.prototype.addCommand)
- description and source-code
```javascript
addCommand = function (cmd) {

  // this.compressedSequenceId = 0;
  // this.sequenceId = 0;

  if (this.config.debug) {
    console.log('Add command: ' + arguments.callee.caller.name);
    cmd._commandName = arguments.callee.caller.name;
  }
  if (!this._command) {
    this._command = cmd;
    this.handlePacket();
  } else {
    this._commands.push(cmd);
  }
  return cmd;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mysql2.Connection.prototype.beginTransaction"></a>[function <span class="apidocSignatureSpan">mysql2.Connection.prototype.</span>beginTransaction (cb)](#apidoc.element.mysql2.Connection.prototype.beginTransaction)
- description and source-code
```javascript
beginTransaction = function (cb) {
  return this.query('START TRANSACTION', cb);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mysql2.Connection.prototype.changeUser"></a>[function <span class="apidocSignatureSpan">mysql2.Connection.prototype.</span>changeUser (options, callback)](#apidoc.element.mysql2.Connection.prototype.changeUser)
- description and source-code
```javascript
function changeUser(options, callback) {
  if (!callback && typeof options === 'function') {
    callback = options;
    options = {};
  }

  var charsetNumber = (options.charset) ? ConnectionConfig.getCharsetNumber(options.charset) : this.config.charsetNumber;

  return this.addCommand(new Commands.ChangeUser({
    user          : options.user || this.config.user,
    password      : options.password || this.config.password,
    passwordSha1  : options.passwordSha1 || this.config.passwordSha1,
    database      : options.database || this.config.database,
    timeout       : options.timeout,
    charsetNumber : charsetNumber,
    currentConfig : this.config
  }, function (err) {
    if (err) {
      err.fatal = true;
    }

    if (callback) {
      callback(err);
    }
  }));
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mysql2.Connection.prototype.close"></a>[function <span class="apidocSignatureSpan">mysql2.Connection.prototype.</span>close ()](#apidoc.element.mysql2.Connection.prototype.close)
- description and source-code
```javascript
close = function () {
  this._closing = true;
  this.stream.end();
  var connection = this;
  connection.addCommand = connection._addCommandClosedState;
}
```
- example usage
```shell
...
Server.prototype.listen = function (port, host, backlog, callback) {
  this._port = port;
  this._server.listen.apply(this._server, arguments);
  return this;
};

Server.prototype.close = function (cb) {
  this._server.close(cb);
};

module.exports = Server;
...
```

#### <a name="apidoc.element.mysql2.Connection.prototype.commit"></a>[function <span class="apidocSignatureSpan">mysql2.Connection.prototype.</span>commit (cb)](#apidoc.element.mysql2.Connection.prototype.commit)
- description and source-code
```javascript
commit = function (cb) {
  return this.query('COMMIT', cb);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mysql2.Connection.prototype.connect"></a>[function <span class="apidocSignatureSpan">mysql2.Connection.prototype.</span>connect (cb)](#apidoc.element.mysql2.Connection.prototype.connect)
- description and source-code
```javascript
connect = function (cb) {
  if (!cb) {
    return;
  }
  var connectCalled = 0;

  function callbackOnce (isErrorHandler) {
    return function (param) {
      if (!connectCalled) {
        if (isErrorHandler) {
          cb(param);
        } else {
          cb(null, param);
        }
      }
      connectCalled = 1;
    };
  }
  this.once('error', callbackOnce(true));
  this.once('connect', callbackOnce(false));
}
```
- example usage
```shell
...
  }

  if (this.config.connectionLimit === 0 || this._allConnections.length < this.config.connectionLimit) {
connection = new PoolConnection(this, {config: this.config.connectionConfig});

this._allConnections.push(connection);

return connection.connect(function (err) {
  if (this._closed) {
    return cb(new Error('Pool is closed.'));
  }
  if (err) {
    return cb(err);
  }
...
```

#### <a name="apidoc.element.mysql2.Connection.prototype.createBinlogStream"></a>[function <span class="apidocSignatureSpan">mysql2.Connection.prototype.</span>createBinlogStream (opts)](#apidoc.element.mysql2.Connection.prototype.createBinlogStream)
- description and source-code
```javascript
createBinlogStream = function (opts) {
  // TODO: create proper stream class
  // TODO: use through2
  var test = 1;
  var Readable = require('stream').Readable;
  var stream = new Readable({objectMode: true});
  stream._read = function () {
    return {
      data: test++
    };
  };
  var connection = this;
  connection._registerSlave(opts, function (err) {
    var dumpCmd = connection._binlogDump(opts);
    dumpCmd.on('event', function (ev) {
      stream.push(ev);
    });
    dumpCmd.on('eof', function () {
      stream.push(null);
      // if non-blocking, then close stream to prevent errors
      if (opts.flags && (opts.flags & 0x01)) {
        connection.close();
      }
    });
    // TODO: pipe errors as well
  });
  return stream;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mysql2.Connection.prototype.destroy"></a>[function <span class="apidocSignatureSpan">mysql2.Connection.prototype.</span>destroy ()](#apidoc.element.mysql2.Connection.prototype.destroy)
- description and source-code
```javascript
destroy = function () {
  this.close();
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mysql2.Connection.prototype.end"></a>[function <span class="apidocSignatureSpan">mysql2.Connection.prototype.</span>end (callback)](#apidoc.element.mysql2.Connection.prototype.end)
- description and source-code
```javascript
end = function (callback) {
  var connection = this;

  if (this.config.isServer) {
    connection._closing = true;
    var quitCmd = new EventEmitter();
    setImmediate(function () {
      connection.stream.end();
      quitCmd.emit('end');
    });
    return quitCmd;
  }

  // trigger error if more commands enqueued after end command
  var quitCmd = this.addCommand(new Commands.Quit(callback));
  connection.addCommand = connection._addCommandClosedState;
  return quitCmd;
}
```
- example usage
```shell
...
if (this._closed) {
  return;
}

this._closed = true;

for (var id in this._nodes) {
  this._nodes[id].pool.end();
}
};

PoolCluster.prototype._findNodeIds = function (pattern) {
if (typeof this._findCaches[pattern] !== 'undefined') {
  return this._findCaches[pattern];
}
...
```

#### <a name="apidoc.element.mysql2.Connection.prototype.escape"></a>[function <span class="apidocSignatureSpan">mysql2.Connection.prototype.</span>escape (value)](#apidoc.element.mysql2.Connection.prototype.escape)
- description and source-code
```javascript
escape = function (value) {
  return SqlString.escape(value, false, this.config.timezone);
}
```
- example usage
```shell
...
  // Remove connection from free connections
  spliceConnection(this._freeConnections, connection);

  this.releaseConnection(connection);
};

Pool.prototype.escape = function (value) {
  return mysql.escape(value, this.config.connectionConfig.stringifyObjects, this.config.connectionConfig.timezone);
};

Pool.prototype.escapeId = function escapeId (value) {
  return mysql.escapeId(value, false);
};

function spliceConnection (queue, connection) {
...
```

#### <a name="apidoc.element.mysql2.Connection.prototype.escapeId"></a>[function <span class="apidocSignatureSpan">mysql2.Connection.prototype.</span>escapeId (value)](#apidoc.element.mysql2.Connection.prototype.escapeId)
- description and source-code
```javascript
function escapeId(value) {
  return SqlString.escapeId(value, false);
}
```
- example usage
```shell
...
};

Pool.prototype.escape = function (value) {
return mysql.escape(value, this.config.connectionConfig.stringifyObjects, this.config.connectionConfig.timezone);
};

Pool.prototype.escapeId = function escapeId (value) {
return mysql.escapeId(value, false);
};

function spliceConnection (queue, connection) {
var len = queue.length;
if (len) {
  if (queue.get(len - 1) === connection) {
    queue.pop();
...
```

#### <a name="apidoc.element.mysql2.Connection.prototype.execute"></a>[function <span class="apidocSignatureSpan">mysql2.Connection.prototype.</span>execute (sql, values, cb)](#apidoc.element.mysql2.Connection.prototype.execute)
- description and source-code
```javascript
function execute(sql, values, cb) {
  var options = {};
  if (typeof sql === 'object') {
    // execute(options, cb)
    options = sql;
    if (typeof values === 'function') {
      cb = values;
    } else {
      options.values = options.values || values;
    }
  } else if (typeof values === 'function') {
    // execute(sql, cb)
    cb = values;
    options.sql = sql;
    options.values = undefined;
  } else {
    // execute(sql, values, cb)
    options.sql = sql;
    options.values = values;
  }
  this._resolveNamedPlaceholders(options);

  var executeCommand = new Commands.Execute(options, cb);
  var prepareCommand = new Commands.Prepare(options, function (err, stmt) {
    if (err) {
      // skip execute command if prepare failed, we have main
      // combined callback here
      executeCommand.start = function () { return null; };

      if (cb) {
        cb(err);
      } else {
        executeCommand.emit('error', err);
      }
      return;
    }

    executeCommand.statement = stmt;
  });

  this.addCommand(prepareCommand);
  this.addCommand(executeCommand);
  return executeCommand;
}
```
- example usage
```shell
...
// get the client
var mysql = require('mysql2');

// create the connection to database
var connection = mysql.createConnection({host:'localhost', user: 'root', database: 'test'});

// execute will internally call prepare and query
connection.execute('SELECT * FROM 'table' WHERE 'name' = ? AND 'age' > ?', ['Rick C-137', 53], function (err, results, fields) {
  console.log(results); // results contains rows returned by server
  console.log(fields); // fields contains extra meta data about results, if available

  // If you execute same statement again, it will be picked form a LRU cache
  // which will save query preparation time and give better performance
});
'''
...
```

#### <a name="apidoc.element.mysql2.Connection.prototype.format"></a>[function <span class="apidocSignatureSpan">mysql2.Connection.prototype.</span>format (sql, values)](#apidoc.element.mysql2.Connection.prototype.format)
- description and source-code
```javascript
format = function (sql, values) {
  if (typeof this.config.queryFormat == 'function') {
    return this.config.queryFormat.call(this, sql, values, this.config.timezone);
  }
  var opts = {
    sql: sql,
    values: values
  };
  this._resolveNamedPlaceholders(opts);
  return SqlString.format(opts.sql, opts.values, this.config.stringifyObjects, this.config.timezone);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mysql2.Connection.prototype.handlePacket"></a>[function <span class="apidocSignatureSpan">mysql2.Connection.prototype.</span>handlePacket (packet)](#apidoc.element.mysql2.Connection.prototype.handlePacket)
- description and source-code
```javascript
handlePacket = function (packet) {
  if (this._paused) {
    this._paused_packets.push(packet);
    return;
  }
  if (packet) {
    if (this.sequenceId !== packet.sequenceId) {
      console.error('Warning: got packets out of order. Expected ' +
        this.sequenceId + ' but received ' + packet.sequenceId);
    }
    this._bumpSequenceId(packet.numPackets);
  }

  if (this.config.debug) {
    if (packet) {
      console.log(' raw: ' + packet.buffer.slice(packet.offset, packet.offset + packet.length()).toString('hex'));
      console.trace();
      var commandName = this._command ? this._command._commandName : '(no command)';
      var stateName = this._command ? this._command.stateName() : '(no command)';
      console.log(this._internalId + ' ' + this.connectionId + ' ==> ' + commandName + '#' + stateName + '(' + [packet.sequenceId
, packet.type(), packet.length()].join(',') + ')');
    }
  }
  if (!this._command) {
    this.protocolError('Unexpected packet while no commands in the queue', 'PROTOCOL_UNEXPECTED_PACKET');
    this.close();
    return;
  }

  var done = this._command.execute(packet, this);
  if (done) {

    this._command = this._commands.shift();
    if (this._command) {
      this.sequenceId = 0;
      this.compressedSequenceId = 0;
      this.handlePacket();
    }
  }
}
```
- example usage
```shell
...

function enableCompression (connection) {
connection._lastWrittenPacketId = 0;
connection._lastReceivedPacketId = 0;

connection._handleCompressedPacket = handleCompressedPacket;
connection._inflatedPacketsParser = new PacketParser(function (p) {
  connection.handlePacket(p);
}, 4);
connection._inflatedPacketsParser._lastPacket = 0;
connection.packetParser = new PacketParser(function (packet) {
  connection._handleCompressedPacket(packet);
}, 7);

connection.writeUncompressed = connection.write;
...
```

#### <a name="apidoc.element.mysql2.Connection.prototype.keyFromFields"></a>[function <span class="apidocSignatureSpan">mysql2.Connection.prototype.</span>keyFromFields (fields, options)](#apidoc.element.mysql2.Connection.prototype.keyFromFields)
- description and source-code
```javascript
function keyFromFields(fields, options) {
  var res = (typeof options.nestTables) + '/' + options.nestTables + '/' + options.rowsAsArray
    + options.supportBigNumbers + '/' + options.bigNumberStrings + '/' + typeof options.typeCast;
  for (var i = 0; i < fields.length; ++i) {
    res += '/' + fields[i].name + ':' + fields[i].columnType + ':' + fields[i].flags;
  }
  return res;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mysql2.Connection.prototype.pause"></a>[function <span class="apidocSignatureSpan">mysql2.Connection.prototype.</span>pause ()](#apidoc.element.mysql2.Connection.prototype.pause)
- description and source-code
```javascript
function pause() {
  this._paused = true;
  this.stream.pause();
}
```
- example usage
```shell
...

stream._read = function () {
  connectionStream.resume();
};

this.on('result', function (row, i) {
  if (!stream.push(row)) {
    connectionStream.pause();
  }
  stream.emit('result', row, i);  // replicate old emitter
});

this.on('error', function (err) {
  stream.emit('error', err);  // Pass on any errors
});
...
```

#### <a name="apidoc.element.mysql2.Connection.prototype.ping"></a>[function <span class="apidocSignatureSpan">mysql2.Connection.prototype.</span>ping (cb)](#apidoc.element.mysql2.Connection.prototype.ping)
- description and source-code
```javascript
function ping(cb) {
  return this.addCommand(new Commands.Ping(cb));
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mysql2.Connection.prototype.pipe"></a>[function <span class="apidocSignatureSpan">mysql2.Connection.prototype.</span>pipe ()](#apidoc.element.mysql2.Connection.prototype.pipe)
- description and source-code
```javascript
pipe = function () {
  var connection = this;
  if (this.stream instanceof Net.Stream) {
    this.stream.ondata = function (data, start, end) {
      connection.packetParser.execute(data, start, end);
    };
  } else {
    this.stream.on('data', function (data) {
      connection.packetParser.execute(data.parent, data.offset, data.offset + data.length);
    });
  }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mysql2.Connection.prototype.prepare"></a>[function <span class="apidocSignatureSpan">mysql2.Connection.prototype.</span>prepare (options, cb)](#apidoc.element.mysql2.Connection.prototype.prepare)
- description and source-code
```javascript
function prepare(options, cb) {
  if (typeof options == 'string') {
    options = {sql: options};
  }
  return this.addCommand(new Commands.Prepare(options, cb));
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mysql2.Connection.prototype.protocolError"></a>[function <span class="apidocSignatureSpan">mysql2.Connection.prototype.</span>protocolError (message, code)](#apidoc.element.mysql2.Connection.prototype.protocolError)
- description and source-code
```javascript
protocolError = function (message, code) {
  var err = new Error(message);
  err.fatal = true;
  err.code = code || 'PROTOCOL_ERROR';
  this.emit('error', err);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mysql2.Connection.prototype.query"></a>[function <span class="apidocSignatureSpan">mysql2.Connection.prototype.</span>query (sql, values, cb)](#apidoc.element.mysql2.Connection.prototype.query)
- description and source-code
```javascript
function query(sql, values, cb) {
  var cmdQuery;
  if (sql.constructor == Commands.Query) {
    cmdQuery = sql;
  } else {
    cmdQuery = Connection.createQuery(sql, values, cb, this.config);
  }
  this._resolveNamedPlaceholders(cmdQuery);
  var rawSql = this.format(cmdQuery.sql, cmdQuery.values || []);
  cmdQuery.sql = rawSql;
  return this.addCommand(cmdQuery);
}
```
- example usage
```shell
...
// get the client
var mysql = require('mysql2');

// create the connection to database
var connection = mysql.createConnection({host:'localhost', user: 'root', database: 'test'});

// simple query
connection.query('SELECT * FROM 'table' WHERE 'name' = "Page" AND 'age' > 45', function (err, results, fields) {
console.log(results); // results contains rows returned by server
console.log(fields); // fields contains extra meta data about results, if available
});

// with placeholder
connection.query('SELECT * FROM 'table' WHERE 'name' = ? AND 'age' > ?', ['Page', 45], function (err, results) {
console.log(results);
...
```

#### <a name="apidoc.element.mysql2.Connection.prototype.resume"></a>[function <span class="apidocSignatureSpan">mysql2.Connection.prototype.</span>resume ()](#apidoc.element.mysql2.Connection.prototype.resume)
- description and source-code
```javascript
function resume() {
  var packet;
  this._paused = false;
  while ((packet = this._paused_packets.shift())) {
    this.handlePacket(packet);
    // don't resume if packet hander paused connection
    if (this._paused) {
      return;
    }
  }
  this.stream.resume();
}
```
- example usage
```shell
...
var stream;

options = options || {};
options.objectMode = true;
stream = new Readable(options),

stream._read = function () {
  connectionStream.resume();
};

this.on('result', function (row, i) {
  if (!stream.push(row)) {
    connectionStream.pause();
  }
  stream.emit('result', row, i);  // replicate old emitter
...
```

#### <a name="apidoc.element.mysql2.Connection.prototype.rollback"></a>[function <span class="apidocSignatureSpan">mysql2.Connection.prototype.</span>rollback (cb)](#apidoc.element.mysql2.Connection.prototype.rollback)
- description and source-code
```javascript
rollback = function (cb) {
  return this.query('ROLLBACK', cb);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mysql2.Connection.prototype.serverHandshake"></a>[function <span class="apidocSignatureSpan">mysql2.Connection.prototype.</span>serverHandshake (args)](#apidoc.element.mysql2.Connection.prototype.serverHandshake)
- description and source-code
```javascript
function serverHandshake(args) {
  this.serverConfig = args;
  this.serverConfig.encoding = CharsetToEncoding[this.serverConfig.characterSet];
  return this.addCommand(new Commands.ServerHandshake(args));
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mysql2.Connection.prototype.startTLS"></a>[function <span class="apidocSignatureSpan">mysql2.Connection.prototype.</span>startTLS (onSecure)](#apidoc.element.mysql2.Connection.prototype.startTLS)
- description and source-code
```javascript
function _startTLS(onSecure) {
  if (this.config.debug) {
    console.log('Upgrading connection to TLS');
  }
  var connection = this;
  var stream = this.stream;
  var secureContext = Tls.createSecureContext({
    ca         : this.config.ssl.ca,
    cert       : this.config.ssl.cert,
    ciphers    : this.config.ssl.ciphers,
    key        : this.config.ssl.key,
    passphrase : this.config.ssl.passphrase
  });

  var rejectUnauthorized = this.config.ssl.rejectUnauthorized;
  var secureEstablished = false;
  var secureSocket = new Tls.TLSSocket(connection.stream, {
    rejectUnauthorized : rejectUnauthorized,
    requestCert        : true,
    secureContext      : secureContext,
    isServer           : false
  });

  // error handler for secure socket
  secureSocket.on('_tlsError', function (err) {
    if (secureEstablished) {
      connection._handleNetworkError(err);
    } else {
      onSecure(err);
    }
  });

  secureSocket.on('secure', function () {
    secureEstablished = true;
    onSecure(rejectUnauthorized ? this.ssl.verifyError() : null);
  });
  secureSocket.on('data', function (data) {
    connection.packetParser.execute(data);
  });
  connection.write = function (buffer) {
    secureSocket.write(buffer);
  };
  // start TLS communications
  secureSocket._start();
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mysql2.Connection.prototype.unprepare"></a>[function <span class="apidocSignatureSpan">mysql2.Connection.prototype.</span>unprepare (sql)](#apidoc.element.mysql2.Connection.prototype.unprepare)
- description and source-code
```javascript
function unprepare(sql) {
  var options = {};
  if (typeof sql === 'object') {
    options = sql;
  } else {
    options.sql = sql;
  }
  var key = Connection.statementKey(options);
  var stmt = this._statements.get(key);
  if (stmt) {
    this._statements.del(key);
    stmt.close();
  }
  return stmt;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mysql2.Connection.prototype.write"></a>[function <span class="apidocSignatureSpan">mysql2.Connection.prototype.</span>write (buffer)](#apidoc.element.mysql2.Connection.prototype.write)
- description and source-code
```javascript
write = function (buffer) {
  var connection = this;
  this.stream.write(buffer, function (err) {
    if (err) {
      connection._handleNetworkError(err);
    }
  });
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mysql2.Connection.prototype.writeColumns"></a>[function <span class="apidocSignatureSpan">mysql2.Connection.prototype.</span>writeColumns (columns)](#apidoc.element.mysql2.Connection.prototype.writeColumns)
- description and source-code
```javascript
writeColumns = function (columns) {
  var connection = this;
  this.writePacket(Packets.ResultSetHeader.toPacket(columns.length));
  columns.forEach(function (column) {
    connection.writePacket(Packets.ColumnDefinition.toPacket(column, connection.serverConfig.encoding));
  });
  this.writeEof();
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mysql2.Connection.prototype.writeEof"></a>[function <span class="apidocSignatureSpan">mysql2.Connection.prototype.</span>writeEof (warnings, statusFlags)](#apidoc.element.mysql2.Connection.prototype.writeEof)
- description and source-code
```javascript
writeEof = function (warnings, statusFlags) {
  this.writePacket(Packets.EOF.toPacket(warnings, statusFlags));
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mysql2.Connection.prototype.writeError"></a>[function <span class="apidocSignatureSpan">mysql2.Connection.prototype.</span>writeError (args)](#apidoc.element.mysql2.Connection.prototype.writeError)
- description and source-code
```javascript
writeError = function (args) {
  // if we want to send error before initial hello was sent, use default encoding
  var encoding = this.serverConfig ? this.serverConfig.encoding : 'cesu8';
  this.writePacket(Packets.Error.toPacket(args, this.serverConfig.encoding));
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mysql2.Connection.prototype.writeOk"></a>[function <span class="apidocSignatureSpan">mysql2.Connection.prototype.</span>writeOk (args)](#apidoc.element.mysql2.Connection.prototype.writeOk)
- description and source-code
```javascript
writeOk = function (args) {
  if (!args) {
    args = {affectedRows: 0};
  }
  this.writePacket(Packets.OK.toPacket(args, this.serverConfig.encoding));
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mysql2.Connection.prototype.writePacket"></a>[function <span class="apidocSignatureSpan">mysql2.Connection.prototype.</span>writePacket (packet)](#apidoc.element.mysql2.Connection.prototype.writePacket)
- description and source-code
```javascript
writePacket = function (packet) {
  var MAX_PACKET_LENGTH = 16777215;
  var length = packet.length();
  var chunk, offset, header;

  if (length < MAX_PACKET_LENGTH) {
    packet.writeHeader(this.sequenceId);
    if (this.config.debug) {
      console.log(this._internalId + ' ' + this.connectionId + ' <== ' + this._command._commandName + '#' + this._command.stateName
() + '(' + [this.sequenceId, packet._name, packet.length()].join(',') + ')');
      console.log(this._internalId + ' ' + this.connectionId + ' <== ' + packet.buffer.toString('hex'));
    }
    this._bumpSequenceId(1);
    this.write(packet.buffer);
  } else {
    if (this.config.debug) {
      console.log(this._internalId + ' ' + this.connectionId + ' <== Writing large packet, raw content not written:');
      console.log(this._internalId + ' ' + this.connectionId + ' <== ' + this._command._commandName + '#' + this._command.stateName
() + '(' + [this.sequenceId, packet._name, packet.length()].join(',') + ')');
    }
    for (offset = 4; offset < 4 + length; offset += MAX_PACKET_LENGTH) {
      chunk = packet.buffer.slice(offset, offset + MAX_PACKET_LENGTH);
      if (chunk.length === MAX_PACKET_LENGTH) {
        header = Buffer.from([0xff, 0xff, 0xff, this.sequenceId]);
      } else {
        header = Buffer.from([chunk.length & 0xff, (chunk.length >> 8) & 0xff, (chunk.length >> 16) & 0xff, this.sequenceId]);
      }
      this._bumpSequenceId(1);
      this.write(header);
      this.write(chunk);
    }
  }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mysql2.Connection.prototype.writeTextResult"></a>[function <span class="apidocSignatureSpan">mysql2.Connection.prototype.</span>writeTextResult (rows, columns)](#apidoc.element.mysql2.Connection.prototype.writeTextResult)
- description and source-code
```javascript
writeTextResult = function (rows, columns) {
  var connection = this;
  connection.writeColumns(columns);
  rows.forEach(function (row) {
    var arrayRow = new Array(columns.length);
    columns.forEach(function (column) {
      arrayRow.push(row[column.name]);
    });
    connection.writeTextRow(arrayRow);
  });
  connection.writeEof();
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mysql2.Connection.prototype.writeTextRow"></a>[function <span class="apidocSignatureSpan">mysql2.Connection.prototype.</span>writeTextRow (column)](#apidoc.element.mysql2.Connection.prototype.writeTextRow)
- description and source-code
```javascript
writeTextRow = function (column) {
  this.writePacket(Packets.TextRow.toPacket(column, this.serverConfig.encoding));
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.mysql2.auth_41"></a>[module mysql2.auth_41](#apidoc.module.mysql2.auth_41)

#### <a name="apidoc.element.mysql2.auth_41.calculateToken"></a>[function <span class="apidocSignatureSpan">mysql2.auth_41.</span>calculateToken (password, scramble1, scramble2)](#apidoc.element.mysql2.auth_41.calculateToken)
- description and source-code
```javascript
function token(password, scramble1, scramble2) {
  // TODO: use buffers (not sure why strings here)
  if (!password) {
    return Buffer.alloc(0);
  }
  var stage1 = sha1(password);
  return module.exports.calculateTokenFromPasswordSha(stage1, scramble1, scramble2);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mysql2.auth_41.calculateTokenFromPasswordSha"></a>[function <span class="apidocSignatureSpan">mysql2.auth_41.</span>calculateTokenFromPasswordSha (passwordSha, scramble1, scramble2)](#apidoc.element.mysql2.auth_41.calculateTokenFromPasswordSha)
- description and source-code
```javascript
calculateTokenFromPasswordSha = function (passwordSha, scramble1, scramble2) {
  var stage2 = sha1(passwordSha);
  var stage3 = sha1(scramble1, scramble2, stage2);
  return xor(stage3, passwordSha);
}
```
- example usage
```shell
...

function token (password, scramble1, scramble2) {
  // TODO: use buffers (not sure why strings here)
  if (!password) {
    return Buffer.alloc(0);
  }
  var stage1 = sha1(password);
  return module.exports.calculateTokenFromPasswordSha(stage1, scramble1, scramble2);
}

module.exports.calculateTokenFromPasswordSha = function (passwordSha, scramble1, scramble2) {
  var stage2 = sha1(passwordSha);
  var stage3 = sha1(scramble1, scramble2, stage2);
  return xor(stage3, passwordSha);
};
...
```

#### <a name="apidoc.element.mysql2.auth_41.doubleSha1"></a>[function <span class="apidocSignatureSpan">mysql2.auth_41.</span>doubleSha1 (password)](#apidoc.element.mysql2.auth_41.doubleSha1)
- description and source-code
```javascript
doubleSha1 = function (password) {
  return sha1(sha1(password));
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mysql2.auth_41.verifyToken"></a>[function <span class="apidocSignatureSpan">mysql2.auth_41.</span>verifyToken (publicSeed1, publicSeed2, token, doubleSha)](#apidoc.element.mysql2.auth_41.verifyToken)
- description and source-code
```javascript
verifyToken = function (publicSeed1, publicSeed2, token, doubleSha) {
  var hashStage1 = xor(token, sha1(publicSeed1, publicSeed2, doubleSha));
  var candidateHash2 = sha1(hashStage1);
  // TODO better way to compare buffers?
  return candidateHash2.toString('hex') == doubleSha.toString('hex');
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.mysql2.compressed_protocol"></a>[module mysql2.compressed_protocol](#apidoc.module.mysql2.compressed_protocol)

#### <a name="apidoc.element.mysql2.compressed_protocol.enableCompression"></a>[function <span class="apidocSignatureSpan">mysql2.compressed_protocol.</span>enableCompression (connection)](#apidoc.element.mysql2.compressed_protocol.enableCompression)
- description and source-code
```javascript
function enableCompression(connection) {
  connection._lastWrittenPacketId = 0;
  connection._lastReceivedPacketId = 0;

  connection._handleCompressedPacket = handleCompressedPacket;
  connection._inflatedPacketsParser = new PacketParser(function (p) {
    connection.handlePacket(p);
  }, 4);
  connection._inflatedPacketsParser._lastPacket = 0;
  connection.packetParser = new PacketParser(function (packet) {
    connection._handleCompressedPacket(packet);
  }, 7);

  connection.writeUncompressed = connection.write;
  connection.write = writeCompressed;

  var seqqueue = require('seq-queue');
  connection.inflateQueue = seqqueue.createQueue();
  connection.deflateQueue = seqqueue.createQueue();
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.mysql2.connection_config"></a>[module mysql2.connection_config](#apidoc.module.mysql2.connection_config)

#### <a name="apidoc.element.mysql2.connection_config.connection_config"></a>[function <span class="apidocSignatureSpan">mysql2.</span>connection_config (options)](#apidoc.element.mysql2.connection_config.connection_config)
- description and source-code
```javascript
function ConnectionConfig(options) {
  if (typeof options === 'string') {
    options = ConnectionConfig.parseUrl(options);
  }

  this.isServer = options.isServer;
  this.stream = options.stream;

  this.host = options.host || 'localhost';
  this.port = options.port || 3306;
  this.localAddress = options.localAddress;
  this.socketPath = options.socketPath;
  this.user = options.user || undefined;
  this.password = options.password || undefined;
  this.passwordSha1 = options.passwordSha1 || undefined;
  this.database = options.database;
  this.connectTimeout = (options.connectTimeout === undefined)
    ? (10 * 1000)
    : options.connectTimeout;
  this.insecureAuth = options.insecureAuth || false;
  this.supportBigNumbers = options.supportBigNumbers || false;
  this.bigNumberStrings = options.bigNumberStrings || false;
  this.decimalNumbers = options.decimalNumbers || false;
  this.dateStrings = options.dateStrings || false;
  this.debug = options.debug;
  this.trace = options.trace !== false;
  this.stringifyObjects = options.stringifyObjects || false;
  this.timezone = options.timezone || 'local';
  this.queryFormat = options.queryFormat;
  this.pool = options.pool || undefined;
  this.ssl = (typeof options.ssl === 'string')
    ? ConnectionConfig.getSSLProfile(options.ssl)
    : (options.ssl || false);
  this.multipleStatements = options.multipleStatements || false;
  this.rowsAsArray = options.rowsAsArray || false;
  this.namedPlaceholders = options.namedPlaceholders || false;
  this.nestTables = (options.nestTables === undefined) ? undefined : options.nestTables;
  this.typeCast = (options.typeCast === undefined)
    ? true
    : options.typeCast;

  if (this.timezone[0] == ' ') {
    // "+" is a url encoded char for space so it
    // gets translated to space when giving a
    // connection string..
    this.timezone = '+' + this.timezone.substr(1);
  }

  if (this.ssl) {
    // Default rejectUnauthorized to true
    this.ssl.rejectUnauthorized = this.ssl.rejectUnauthorized !== false;
  }

  this.maxPacketSize = 0;
  this.charsetNumber = (options.charset)
    ? ConnectionConfig.getCharsetNumber(options.charset)
    : options.charsetNumber || Charsets.UTF8MB4_UNICODE_CI;

  this.compress = options.compress || false;

  this.authSwitchHandler = options.authSwitchHandler;

  this.clientFlags = ConnectionConfig.mergeFlags(ConnectionConfig.getDefaultFlags(options),
                                                 options.flags || '');

  this.connectAttributes = options.connectAttributes;
  this.maxPreparedStatements = options.maxPreparedStatements || 16000;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mysql2.connection_config.getCharsetNumber"></a>[function <span class="apidocSignatureSpan">mysql2.connection_config.</span>getCharsetNumber (charset)](#apidoc.element.mysql2.connection_config.getCharsetNumber)
- description and source-code
```javascript
function getCharsetNumber(charset) {
  var num = Charsets[charset.toUpperCase()];

  if (num === undefined) {
    throw new TypeError('Unknown charset \'' + charset + '\'');
  }

  return num;
}
```
- example usage
```shell
...
if (this.ssl) {
  // Default rejectUnauthorized to true
  this.ssl.rejectUnauthorized = this.ssl.rejectUnauthorized !== false;
}

this.maxPacketSize = 0;
this.charsetNumber = (options.charset)
  ? ConnectionConfig.getCharsetNumber(options.charset)
  : options.charsetNumber || Charsets.UTF8MB4_UNICODE_CI;

this.compress = options.compress || false;

this.authSwitchHandler = options.authSwitchHandler;

this.clientFlags = ConnectionConfig.mergeFlags(ConnectionConfig.getDefaultFlags(options),
...
```

#### <a name="apidoc.element.mysql2.connection_config.getDefaultFlags"></a>[function <span class="apidocSignatureSpan">mysql2.connection_config.</span>getDefaultFlags (options)](#apidoc.element.mysql2.connection_config.getDefaultFlags)
- description and source-code
```javascript
getDefaultFlags = function (options) {
  var defaultFlags = ['LONG_PASSWORD', 'FOUND_ROWS', 'LONG_FLAG',
    'CONNECT_WITH_DB', 'ODBC', 'LOCAL_FILES',
    'IGNORE_SPACE', 'PROTOCOL_41', 'IGNORE_SIGPIPE',
    'TRANSACTIONS', 'RESERVED', 'SECURE_CONNECTION',
    'MULTI_RESULTS', 'TRANSACTIONS', 'SESSION_TRACK'];

  if (options && options.multipleStatements) {
    defaultFlags.push('MULTI_STATEMENTS');
  }

  if (options && options.authSwitchHandler) {
    defaultFlags.push('PLUGIN_AUTH');
    defaultFlags.push('PLUGIN_AUTH_LENENC_CLIENT_DATA');
  }

  if (options && options.connectAttributes) {
    defaultFlags.push('CONNECT_ATTRS');
  }

  return defaultFlags;
}
```
- example usage
```shell
...
    ? ConnectionConfig.getCharsetNumber(options.charset)
    : options.charsetNumber || Charsets.UTF8MB4_UNICODE_CI;

  this.compress = options.compress || false;

  this.authSwitchHandler = options.authSwitchHandler;

  this.clientFlags = ConnectionConfig.mergeFlags(ConnectionConfig.getDefaultFlags(options),
                                                 options.flags || '');

  this.connectAttributes = options.connectAttributes;
  this.maxPreparedStatements = options.maxPreparedStatements || 16000;
}

ConnectionConfig.mergeFlags = function (default_flags, user_flags) {
...
```

#### <a name="apidoc.element.mysql2.connection_config.getSSLProfile"></a>[function <span class="apidocSignatureSpan">mysql2.connection_config.</span>getSSLProfile (name)](#apidoc.element.mysql2.connection_config.getSSLProfile)
- description and source-code
```javascript
function getSSLProfile(name) {
  if (!SSLProfiles) {
    SSLProfiles = require('./constants/ssl_profiles.js');
  }

  var ssl = SSLProfiles[name];

  if (ssl === undefined) {
    throw new TypeError('Unknown SSL profile \'' + name + '\'');
  }

  return ssl;
}
```
- example usage
```shell
...
this.debug = options.debug;
this.trace = options.trace !== false;
this.stringifyObjects = options.stringifyObjects || false;
this.timezone = options.timezone || 'local';
this.queryFormat = options.queryFormat;
this.pool = options.pool || undefined;
this.ssl = (typeof options.ssl === 'string')
  ? ConnectionConfig.getSSLProfile(options.ssl)
  : (options.ssl || false);
this.multipleStatements = options.multipleStatements || false;
this.rowsAsArray = options.rowsAsArray || false;
this.namedPlaceholders = options.namedPlaceholders || false;
this.nestTables = (options.nestTables === undefined) ? undefined : options.nestTables;
this.typeCast = (options.typeCast === undefined)
  ? true
...
```

#### <a name="apidoc.element.mysql2.connection_config.mergeFlags"></a>[function <span class="apidocSignatureSpan">mysql2.connection_config.</span>mergeFlags (default_flags, user_flags)](#apidoc.element.mysql2.connection_config.mergeFlags)
- description and source-code
```javascript
mergeFlags = function (default_flags, user_flags) {
  var flags = 0x0, i;

  user_flags = (user_flags || '').toUpperCase().split(/\s*,+\s*/);

  // add default flags unless "blacklisted"
  for (i in default_flags) {
    if (user_flags.indexOf('-' + default_flags[i]) >= 0) {
      continue;
    }

    flags |= ClientConstants[default_flags[i]] || 0x0;
  }
  // add user flags unless already already added
  for (i in user_flags) {
    if (user_flags[i][0] == '-') {
      continue;
    }

    if (default_flags.indexOf(user_flags[i]) >= 0) {
      continue;
    }

    flags |= ClientConstants[user_flags[i]] || 0x0;
  }

  return flags;
}
```
- example usage
```shell
...
    ? ConnectionConfig.getCharsetNumber(options.charset)
    : options.charsetNumber || Charsets.UTF8MB4_UNICODE_CI;

  this.compress = options.compress || false;

  this.authSwitchHandler = options.authSwitchHandler;

  this.clientFlags = ConnectionConfig.mergeFlags(ConnectionConfig.getDefaultFlags(options),
                                                 options.flags || '');

  this.connectAttributes = options.connectAttributes;
  this.maxPreparedStatements = options.maxPreparedStatements || 16000;
}

ConnectionConfig.mergeFlags = function (default_flags, user_flags) {
...
```

#### <a name="apidoc.element.mysql2.connection_config.parseUrl"></a>[function <span class="apidocSignatureSpan">mysql2.connection_config.</span>parseUrl (url)](#apidoc.element.mysql2.connection_config.parseUrl)
- description and source-code
```javascript
parseUrl = function (url) {
  url = urlParse(url, true);

  var options = {
    host     : url.hostname,
    port     : url.port,
    database : url.pathname.substr(1)
  };

  if (url.auth) {
    var auth = url.auth.split(':');
    options.user = auth[0];
    options.password = auth[1];
  }

  if (url.query) {
    for (var key in url.query) {
      var value = url.query[key];

      try {
        // Try to parse this as a JSON expression first
        options[key] = JSON.parse(value);
      } catch (err) {
        // Otherwise assume it is a plain string
        options[key] = value;
      }
    }
  }

  return options;
}
```
- example usage
```shell
...
var ClientConstants = require('./constants/client');
var Charsets = require('./constants/charsets');
var SSLProfiles = null;

module.exports = ConnectionConfig;
function ConnectionConfig (options) {
if (typeof options === 'string') {
  options = ConnectionConfig.parseUrl(options);
}

this.isServer = options.isServer;
this.stream = options.stream;

this.host = options.host || 'localhost';
this.port = options.port || 3306;
...
```



# <a name="apidoc.module.mysql2.helpers"></a>[module mysql2.helpers](#apidoc.module.mysql2.helpers)

#### <a name="apidoc.element.mysql2.helpers.srcEscape"></a>[function <span class="apidocSignatureSpan">mysql2.helpers.</span>srcEscape (str)](#apidoc.element.mysql2.helpers.srcEscape)
- description and source-code
```javascript
function srcEscape(str) {
  var a = {};
  a[str] = 1;
  return JSON.stringify(a).slice(1, -3);
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.mysql2.packet_parser"></a>[module mysql2.packet_parser](#apidoc.module.mysql2.packet_parser)

#### <a name="apidoc.element.mysql2.packet_parser.packet_parser"></a>[function <span class="apidocSignatureSpan">mysql2.</span>packet_parser (onPacket, packetHeaderLength)](#apidoc.element.mysql2.packet_parser.packet_parser)
- description and source-code
```javascript
function PacketParser(onPacket, packetHeaderLength)
{
  // 4 for normal packets, 7 for comprssed protocol packets
  if (typeof packetHeaderLength == 'undefined') {
    packetHeaderLength = 4;
  }
  // array of last payload chunks
  // only used when current payload is not complete
  this.buffer = [];
  // total length of chunks on buffer
  this.bufferLength = 0;
  this.packetHeaderLength = packetHeaderLength;

  // incomplete header state: number of header bytes received
  this.headerLen = 0;

  // expected payload length
  this.length = 0;

  this.largePacketParts = [];
  this.firstPacketSequenceId = 0;

  this.onPacket = onPacket;
  this.execute = PacketParser.prototype.executeStart;
  this._flushLargePacket = packetHeaderLength == 7 ?
    this._flushLargePacket7 : this._flushLargePacket4;
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.mysql2.packet_parser.prototype"></a>[module mysql2.packet_parser.prototype](#apidoc.module.mysql2.packet_parser.prototype)

#### <a name="apidoc.element.mysql2.packet_parser.prototype._flushLargePacket4"></a>[function <span class="apidocSignatureSpan">mysql2.packet_parser.prototype.</span>_flushLargePacket4 ()](#apidoc.element.mysql2.packet_parser.prototype._flushLargePacket4)
- description and source-code
```javascript
function _flushLargePacket() {
  var numPackets = this.largePacketParts.length;
  this.largePacketParts.unshift(Buffer.from([0, 0, 0, 0])); // insert header
  var body = Buffer.concat(this.largePacketParts);
  var packet = new Packet(this.firstPacketSequenceId, body, 0, body.length);
  this.largePacketParts.length = 0;
  packet.numPackets = numPackets;
  this.onPacket(packet);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mysql2.packet_parser.prototype._flushLargePacket7"></a>[function <span class="apidocSignatureSpan">mysql2.packet_parser.prototype.</span>_flushLargePacket7 ()](#apidoc.element.mysql2.packet_parser.prototype._flushLargePacket7)
- description and source-code
```javascript
function _flushLargePacket() {
  var numPackets = this.largePacketParts.length;
  this.largePacketParts.unshift(Buffer.from([0, 0, 0, 0, 0, 0, 0])); // insert header
  var body = Buffer.concat(this.largePacketParts);
  this.largePacketParts.length = 0;
  var packet = new Packet(this.firstPacketSequenceId, body, 0, body.length);
  packet.numPackets = numPackets;
  this.onPacket(packet);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mysql2.packet_parser.prototype.executeHeader2"></a>[function <span class="apidocSignatureSpan">mysql2.packet_parser.prototype.</span>executeHeader2 (chunk)](#apidoc.element.mysql2.packet_parser.prototype.executeHeader2)
- description and source-code
```javascript
function executeHeader2(chunk) {
  this.length += chunk[0] << 8;
  if (chunk.length > 1) {
    this.length += chunk[1] << 16;
    this.execute = PacketParser.prototype.executePayload;
    return this.executePayload(chunk.slice(2));
  } else {
    this.execute = PacketParser.prototype.executeHeader3;
  }
  return null;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mysql2.packet_parser.prototype.executeHeader3"></a>[function <span class="apidocSignatureSpan">mysql2.packet_parser.prototype.</span>executeHeader3 (chunk)](#apidoc.element.mysql2.packet_parser.prototype.executeHeader3)
- description and source-code
```javascript
function executeHeader3(chunk) {
  this.length += chunk[0] << 16;
  this.execute = PacketParser.prototype.executePayload;
  return this.executePayload(chunk.slice(1));
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mysql2.packet_parser.prototype.executePayload"></a>[function <span class="apidocSignatureSpan">mysql2.packet_parser.prototype.</span>executePayload (chunk)](#apidoc.element.mysql2.packet_parser.prototype.executePayload)
- description and source-code
```javascript
function executePayload(chunk) {

  var start = 0;
  var end = chunk.length;
  var remainingPayload = this.length - this.bufferLength + this.packetHeaderLength - 3;

  if (end - start >= remainingPayload) { // last chunk for payload
    var payload = Buffer.allocUnsafe(this.length + this.packetHeaderLength);
    var offset = 3;
    for (var i = 0; i < this.buffer.length; ++i) {
      this.buffer[i].copy(payload, offset);
      offset += this.buffer[i].length;
    }
    chunk.copy(payload, offset, start, start + remainingPayload);
    var sequenceId = payload[3];
    if (this.length < MAX_PACKET_LENGTH && this.largePacketParts.length === 0) {
      this.onPacket(new Packet(sequenceId, payload, 0, this.length + this.packetHeaderLength));
    } else {
      // first large packet - remember it's id
      if (this.largePacketParts.length === 0) {
        this.firstPacketSequenceId = sequenceId;
      }
      this.largePacketParts.push(payload.slice(this.packetHeaderLength, this.packetHeaderLength + this.length));
      if (this.length < MAX_PACKET_LENGTH) {
        this._flushLargePacket();
      }
    }
    this.buffer = [];
    this.bufferLength = 0;
    this.execute = PacketParser.prototype.executeStart;
    start += remainingPayload;
    if (end - start > 0) {
      return this.execute(chunk.slice(start, end));
    }
  } else {
    this.buffer.push(chunk);
    this.bufferLength += chunk.length;
  }
  return null;
}
```
- example usage
```shell
...
};

PacketParser.prototype.executeHeader2 = function executeHeader2 (chunk) {
  this.length += chunk[0] << 8;
  if (chunk.length > 1) {
    this.length += chunk[1] << 16;
    this.execute = PacketParser.prototype.executePayload;
    return this.executePayload(chunk.slice(2));
  } else {
    this.execute = PacketParser.prototype.executeHeader3;
  }
  return null;
};

PacketParser.prototype.executeHeader3 = function executeHeader3 (chunk) {
...
```

#### <a name="apidoc.element.mysql2.packet_parser.prototype.executeStart"></a>[function <span class="apidocSignatureSpan">mysql2.packet_parser.prototype.</span>executeStart (chunk)](#apidoc.element.mysql2.packet_parser.prototype.executeStart)
- description and source-code
```javascript
function executeStart(chunk) {
  var start = 0;
  var end = chunk.length;

  while (end - start >= 3) {
    this.length = readPacketLength(chunk, start);
    if (end - start >= this.length + this.packetHeaderLength) { // at least one full packet
      var sequenceId = chunk[start + 3];
      if (this.length < MAX_PACKET_LENGTH && this.largePacketParts.length === 0) {
        this.onPacket(new Packet(sequenceId, chunk, start, start + this.packetHeaderLength + this.length));
      } else {
        // first large packet - remember it's id
        if (this.largePacketParts.length === 0) {
          this.firstPacketSequenceId = sequenceId;
        }
        this.largePacketParts.push(chunk.slice(start + this.packetHeaderLength, start + this.packetHeaderLength + this.length));
        if (this.length < MAX_PACKET_LENGTH) {
          this._flushLargePacket();
        }
      }
      start += this.packetHeaderLength + this.length;
    } else { // payload is incomplete
      this.buffer = [chunk.slice(start + 3, end)];
      this.bufferLength = end - start - 3;
      this.execute = PacketParser.prototype.executePayload;
      return;
    }
  }
  if (end - start > 0) { // there is start of length header, but it's not full 3 bytes
    this.headerLen = end - start; // 1 or 2 bytes
    this.length = chunk[start];
    if (this.headerLen == 2) {
      this.length = chunk[start] + (chunk[start + 1] << 8);
      this.execute = PacketParser.prototype.executeHeader3;
    } else {
      this.execute = PacketParser.prototype.executeHeader2;
    }
  }
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.mysql2.pool"></a>[module mysql2.pool](#apidoc.module.mysql2.pool)

#### <a name="apidoc.element.mysql2.pool.pool"></a>[function <span class="apidocSignatureSpan">mysql2.</span>pool (options)](#apidoc.element.mysql2.pool.pool)
- description and source-code
```javascript
function Pool(options) {
  EventEmitter.call(this);
  this.config = options.config;
  this.config.connectionConfig.pool = this;

  this._allConnections = new Queue();
  this._freeConnections = new Queue();
  this._connectionQueue = new Queue();
  this._closed = false;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mysql2.pool.super_"></a>[function <span class="apidocSignatureSpan">mysql2.pool.</span>super_ ()](#apidoc.element.mysql2.pool.super_)
- description and source-code
```javascript
function EventEmitter() {
  EventEmitter.init.call(this);
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.mysql2.pool.prototype"></a>[module mysql2.pool.prototype](#apidoc.module.mysql2.pool.prototype)

#### <a name="apidoc.element.mysql2.pool.prototype._removeConnection"></a>[function <span class="apidocSignatureSpan">mysql2.pool.prototype.</span>_removeConnection (connection)](#apidoc.element.mysql2.pool.prototype._removeConnection)
- description and source-code
```javascript
_removeConnection = function (connection) {

  // Remove connection from all connections
  spliceConnection(this._allConnections, connection);

  // Remove connection from free connections
  spliceConnection(this._freeConnections, connection);

  this.releaseConnection(connection);
}
```
- example usage
```shell
...
  if (!this._pool || this._pool._closed) {
    return;
  }

  var pool = this._pool;
  this._pool = null;

  pool._removeConnection(this);
};
...
```

#### <a name="apidoc.element.mysql2.pool.prototype.end"></a>[function <span class="apidocSignatureSpan">mysql2.pool.prototype.</span>end (cb)](#apidoc.element.mysql2.pool.prototype.end)
- description and source-code
```javascript
end = function (cb) {
  this._closed = true;

  if (typeof cb != 'function') {
    cb = function (err) {
      if (err) {
        throw err;
      }
    };
  }

  var calledBack = false;
  var closedConnections = 0;
  var connection;

  var endCB = function (err) {
    if (calledBack) {
      return;
    }

    if (err || ++closedConnections >= this._allConnections.length) {
      calledBack = true;
      cb(err);
      return;
    }
  }.bind(this);

  if (this._allConnections.length === 0) {
    endCB();
    return;
  }

  for (var i = 0; i < this._allConnections.length; i++) {
    connection = this._allConnections.get(i);
    connection._realEnd(endCB);
  }
}
```
- example usage
```shell
...
if (this._closed) {
  return;
}

this._closed = true;

for (var id in this._nodes) {
  this._nodes[id].pool.end();
}
};

PoolCluster.prototype._findNodeIds = function (pattern) {
if (typeof this._findCaches[pattern] !== 'undefined') {
  return this._findCaches[pattern];
}
...
```

#### <a name="apidoc.element.mysql2.pool.prototype.escape"></a>[function <span class="apidocSignatureSpan">mysql2.pool.prototype.</span>escape (value)](#apidoc.element.mysql2.pool.prototype.escape)
- description and source-code
```javascript
escape = function (value) {
  return mysql.escape(value, this.config.connectionConfig.stringifyObjects, this.config.connectionConfig.timezone);
}
```
- example usage
```shell
...
  // Remove connection from free connections
  spliceConnection(this._freeConnections, connection);

  this.releaseConnection(connection);
};

Pool.prototype.escape = function (value) {
  return mysql.escape(value, this.config.connectionConfig.stringifyObjects, this.config.connectionConfig.timezone);
};

Pool.prototype.escapeId = function escapeId (value) {
  return mysql.escapeId(value, false);
};

function spliceConnection (queue, connection) {
...
```

#### <a name="apidoc.element.mysql2.pool.prototype.escapeId"></a>[function <span class="apidocSignatureSpan">mysql2.pool.prototype.</span>escapeId (value)](#apidoc.element.mysql2.pool.prototype.escapeId)
- description and source-code
```javascript
function escapeId(value) {
  return mysql.escapeId(value, false);
}
```
- example usage
```shell
...
};

Pool.prototype.escape = function (value) {
return mysql.escape(value, this.config.connectionConfig.stringifyObjects, this.config.connectionConfig.timezone);
};

Pool.prototype.escapeId = function escapeId (value) {
return mysql.escapeId(value, false);
};

function spliceConnection (queue, connection) {
var len = queue.length;
if (len) {
  if (queue.get(len - 1) === connection) {
    queue.pop();
...
```

#### <a name="apidoc.element.mysql2.pool.prototype.execute"></a>[function <span class="apidocSignatureSpan">mysql2.pool.prototype.</span>execute (sql, values, cb)](#apidoc.element.mysql2.pool.prototype.execute)
- description and source-code
```javascript
execute = function (sql, values, cb) {
  var useNamedPlaceholders = this.config.connectionConfig.namedPlaceholders;

  this.getConnection(function (err, conn) {
    if (err) {
      return cb(err);
    }

    conn.config.namedPlaceholders = useNamedPlaceholders;
    return conn.execute(sql, values, function () {
      conn.release();
      cb.apply(this, arguments);
    });
  });
}
```
- example usage
```shell
...
// get the client
var mysql = require('mysql2');

// create the connection to database
var connection = mysql.createConnection({host:'localhost', user: 'root', database: 'test'});

// execute will internally call prepare and query
connection.execute('SELECT * FROM 'table' WHERE 'name' = ? AND 'age' > ?', ['Rick C-137', 53], function (err, results, fields) {
  console.log(results); // results contains rows returned by server
  console.log(fields); // fields contains extra meta data about results, if available

  // If you execute same statement again, it will be picked form a LRU cache
  // which will save query preparation time and give better performance
});
'''
...
```

#### <a name="apidoc.element.mysql2.pool.prototype.getConnection"></a>[function <span class="apidocSignatureSpan">mysql2.pool.prototype.</span>getConnection (cb)](#apidoc.element.mysql2.pool.prototype.getConnection)
- description and source-code
```javascript
getConnection = function (cb) {
  if (this._closed) {
    return process.nextTick(function () {
      return cb(new Error('Pool is closed.'));
    });
  }

  var connection;

  if (this._freeConnections.length > 0) {
    connection = this._freeConnections.shift();

    return process.nextTick(function () {
      return cb(null, connection);
    });
  }

  if (this.config.connectionLimit === 0 || this._allConnections.length < this.config.connectionLimit) {
    connection = new PoolConnection(this, {config: this.config.connectionConfig});

    this._allConnections.push(connection);

    return connection.connect(function (err) {
      if (this._closed) {
        return cb(new Error('Pool is closed.'));
      }
      if (err) {
        return cb(err);
      }

      this.emit('connection', connection);
      return cb(null, connection);
    }.bind(this));
  }

  if (!this.config.waitForConnections) {
    return process.nextTick(function () {
      return cb(new Error('No connections available.'));
    });
  }

  if (this.config.queueLimit && this._connectionQueue.length >= this.config.queueLimit) {
    return cb(new Error('Queue limit reached.'));
  }

  this.emit('enqueue');
  return this._connectionQueue.push(cb);
}
```
- example usage
```shell
...
}
};

Pool.prototype.query = function (sql, values, cb) {
var cmdQuery = Connection.createQuery(sql, values, cb, this.config.connectionConfig);
cmdQuery.namedPlaceholders = this.config.connectionConfig.namedPlaceholders;

this.getConnection(function (err, conn) {
  if (err) {
    if (typeof cmdQuery.onResult === 'function') {
      cmdQuery.onResult(err);
    } else {
      cmdQuery.emit('error', err);
    }
    return;
...
```

#### <a name="apidoc.element.mysql2.pool.prototype.query"></a>[function <span class="apidocSignatureSpan">mysql2.pool.prototype.</span>query (sql, values, cb)](#apidoc.element.mysql2.pool.prototype.query)
- description and source-code
```javascript
query = function (sql, values, cb) {
  var cmdQuery = Connection.createQuery(sql, values, cb, this.config.connectionConfig);
  cmdQuery.namedPlaceholders = this.config.connectionConfig.namedPlaceholders;

  this.getConnection(function (err, conn) {
    if (err) {
      if (typeof cmdQuery.onResult === 'function') {
        cmdQuery.onResult(err);
      } else {
        cmdQuery.emit('error', err);
      }
      return;
    }

    conn.query(cmdQuery).once('end', function () {
      conn.release();
    });
  });
  return cmdQuery;
}
```
- example usage
```shell
...
// get the client
var mysql = require('mysql2');

// create the connection to database
var connection = mysql.createConnection({host:'localhost', user: 'root', database: 'test'});

// simple query
connection.query('SELECT * FROM 'table' WHERE 'name' = "Page" AND 'age' > 45', function (err, results, fields) {
console.log(results); // results contains rows returned by server
console.log(fields); // fields contains extra meta data about results, if available
});

// with placeholder
connection.query('SELECT * FROM 'table' WHERE 'name' = ? AND 'age' > ?', ['Page', 45], function (err, results) {
console.log(results);
...
```

#### <a name="apidoc.element.mysql2.pool.prototype.releaseConnection"></a>[function <span class="apidocSignatureSpan">mysql2.pool.prototype.</span>releaseConnection (connection)](#apidoc.element.mysql2.pool.prototype.releaseConnection)
- description and source-code
```javascript
releaseConnection = function (connection) {
  var cb;

  if (!connection._pool) {
    // The connection has been removed from the pool and is no longer good.
    if (this._connectionQueue.length) {
      cb = this._connectionQueue.shift();

      process.nextTick(this.getConnection.bind(this, cb));
    }
  } else if (this._connectionQueue.length) {
    cb = this._connectionQueue.shift();

    process.nextTick(cb.bind(null, null, connection));
  } else {
    this._freeConnections.push(connection);
  }
}
```
- example usage
```shell
...

  // Remove connection from all connections
  spliceConnection(this._allConnections, connection);

  // Remove connection from free connections
  spliceConnection(this._freeConnections, connection);

  this.releaseConnection(connection);
};

Pool.prototype.escape = function (value) {
  return mysql.escape(value, this.config.connectionConfig.stringifyObjects, this.config.connectionConfig.timezone);
};

Pool.prototype.escapeId = function escapeId (value) {
...
```



# <a name="apidoc.module.mysql2.pool_cluster"></a>[module mysql2.pool_cluster](#apidoc.module.mysql2.pool_cluster)

#### <a name="apidoc.element.mysql2.pool_cluster.pool_cluster"></a>[function <span class="apidocSignatureSpan">mysql2.</span>pool_cluster (config)](#apidoc.element.mysql2.pool_cluster.pool_cluster)
- description and source-code
```javascript
function PoolCluster(config) {
  EventEmitter.call(this);

  config = config || {};
  this._canRetry = typeof config.canRetry === 'undefined' ? true : config.canRetry;
  this._removeNodeErrorCount = config.removeNodeErrorCount || 5;
  this._defaultSelector = config.defaultSelector || 'RR';

  this._closed = false;
  this._lastId = 0;
  this._nodes = {};
  this._serviceableNodeIds = [];
  this._namespaces = {};
  this._findCaches = {};
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mysql2.pool_cluster.super_"></a>[function <span class="apidocSignatureSpan">mysql2.pool_cluster.</span>super_ ()](#apidoc.element.mysql2.pool_cluster.super_)
- description and source-code
```javascript
function EventEmitter() {
  EventEmitter.init.call(this);
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.mysql2.pool_cluster.prototype"></a>[module mysql2.pool_cluster.prototype](#apidoc.module.mysql2.pool_cluster.prototype)

#### <a name="apidoc.element.mysql2.pool_cluster.prototype._clearFindCaches"></a>[function <span class="apidocSignatureSpan">mysql2.pool_cluster.prototype.</span>_clearFindCaches ()](#apidoc.element.mysql2.pool_cluster.prototype._clearFindCaches)
- description and source-code
```javascript
_clearFindCaches = function () {
  this._findCaches = {};
}
```
- example usage
```shell
...
    id: id,
    errorCount: 0,
    pool: new Pool({config: new PoolConfig(config)})
  };

  this._serviceableNodeIds.push(id);

  this._clearFindCaches();
}
};

PoolCluster.prototype.getConnection = function (pattern, selector, cb) {
var namespace;
if (typeof pattern === 'function') {
  cb = pattern;
...
```

#### <a name="apidoc.element.mysql2.pool_cluster.prototype._decreaseErrorCount"></a>[function <span class="apidocSignatureSpan">mysql2.pool_cluster.prototype.</span>_decreaseErrorCount (node)](#apidoc.element.mysql2.pool_cluster.prototype._decreaseErrorCount)
- description and source-code
```javascript
_decreaseErrorCount = function (node) {
  if (node.errorCount > 0) {
    --node.errorCount;
  }
}
```
- example usage
```shell
...
      if (self._canRetry) {
        console.warn('[Error] PoolCluster : ' + err);
        return cb(null, 'retry');
      } else {
        return cb(err);
      }
    } else {
      self._decreaseErrorCount(node);
    }

    connection._clusterId = node.id;

    return cb(null, connection);
  });
};
...
```

#### <a name="apidoc.element.mysql2.pool_cluster.prototype._findNodeIds"></a>[function <span class="apidocSignatureSpan">mysql2.pool_cluster.prototype.</span>_findNodeIds (pattern)](#apidoc.element.mysql2.pool_cluster.prototype._findNodeIds)
- description and source-code
```javascript
_findNodeIds = function (pattern) {
  if (typeof this._findCaches[pattern] !== 'undefined') {
    return this._findCaches[pattern];
  }

  var foundNodeIds;

  if (pattern === '*') { // all
    foundNodeIds = this._serviceableNodeIds;
  } else if (this._serviceableNodeIds.indexOf(pattern) != -1) { // one
    foundNodeIds = [pattern];
  } else { // wild matching
    var keyword = pattern.substring(pattern.length - 1, 0);

    foundNodeIds = this._serviceableNodeIds.filter(function (id) {
      return id.indexOf(keyword) === 0;
    });
  }

  this._findCaches[pattern] = foundNodeIds;

  return foundNodeIds;
}
```
- example usage
```shell
...
  }

  return cb(null, connection);
}.bind(this));
};

PoolNamespace.prototype._getClusterNode = function () {
var foundNodeIds = this._cluster._findNodeIds(this._pattern);

if (foundNodeIds.length === 0) {
  return null;
}

var nodeId = (foundNodeIds.length === 1) ? foundNodeIds[0] : this._selector(foundNodeIds);
...
```

#### <a name="apidoc.element.mysql2.pool_cluster.prototype._getConnection"></a>[function <span class="apidocSignatureSpan">mysql2.pool_cluster.prototype.</span>_getConnection (node, cb)](#apidoc.element.mysql2.pool_cluster.prototype._getConnection)
- description and source-code
```javascript
_getConnection = function (node, cb) {
  var self = this;

  node.pool.getConnection(function (err, connection) {
    if (err) {
      self._increaseErrorCount(node);

      if (self._canRetry) {
        console.warn('[Error] PoolCluster : ' + err);
        return cb(null, 'retry');
      } else {
        return cb(err);
      }
    } else {
      self._decreaseErrorCount(node);
    }

    connection._clusterId = node.id;

    return cb(null, connection);
  });
}
```
- example usage
```shell
...
PoolNamespace.prototype.getConnection = function (cb) {
  var clusterNode = this._getClusterNode();

  if (clusterNode === null) {
return cb(new Error('Pool does Not exists.'));
  }

  return this._cluster._getConnection(clusterNode, function (err, connection) {
if (err) {
  return cb(err);
}

if (connection === 'retry') {
  return this.getConnection(cb);
}
...
```

#### <a name="apidoc.element.mysql2.pool_cluster.prototype._getNode"></a>[function <span class="apidocSignatureSpan">mysql2.pool_cluster.prototype.</span>_getNode (id)](#apidoc.element.mysql2.pool_cluster.prototype._getNode)
- description and source-code
```javascript
_getNode = function (id) {
  return this._nodes[id] || null;
}
```
- example usage
```shell
...

  if (foundNodeIds.length === 0) {
    return null;
  }

  var nodeId = (foundNodeIds.length === 1) ? foundNodeIds[0] : this._selector(foundNodeIds);

  return this._cluster._getNode(nodeId);
};

/**
 * Selector
 */
var Selector = {};
...
```

#### <a name="apidoc.element.mysql2.pool_cluster.prototype._increaseErrorCount"></a>[function <span class="apidocSignatureSpan">mysql2.pool_cluster.prototype.</span>_increaseErrorCount (node)](#apidoc.element.mysql2.pool_cluster.prototype._increaseErrorCount)
- description and source-code
```javascript
_increaseErrorCount = function (node) {
  if (++node.errorCount >= this._removeNodeErrorCount) {
    var index = this._serviceableNodeIds.indexOf(node.id);
    if (index !== -1) {
      this._serviceableNodeIds.splice(index, 1);
      delete this._nodes[node.id];

      this._clearFindCaches();

      node.pool.end();

      this.emit('remove', node.id);
    }
  }
}
```
- example usage
```shell
...
};

PoolCluster.prototype._getConnection = function (node, cb) {
  var self = this;

  node.pool.getConnection(function (err, connection) {
    if (err) {
self._increaseErrorCount(node);

if (self._canRetry) {
  console.warn('[Error] PoolCluster : ' + err);
  return cb(null, 'retry');
} else {
  return cb(err);
}
...
```

#### <a name="apidoc.element.mysql2.pool_cluster.prototype.add"></a>[function <span class="apidocSignatureSpan">mysql2.pool_cluster.prototype.</span>add (id, config)](#apidoc.element.mysql2.pool_cluster.prototype.add)
- description and source-code
```javascript
add = function (id, config) {
  if (typeof id === 'object') {
    config = id;
    id = 'CLUSTER::' + (++this._lastId);
  }

  if (typeof this._nodes[id] === 'undefined') {
    this._nodes[id] = {
      id: id,
      errorCount: 0,
      pool: new Pool({config: new PoolConfig(config)})
    };

    this._serviceableNodeIds.push(id);

    this._clearFindCaches();
  }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mysql2.pool_cluster.prototype.end"></a>[function <span class="apidocSignatureSpan">mysql2.pool_cluster.prototype.</span>end ()](#apidoc.element.mysql2.pool_cluster.prototype.end)
- description and source-code
```javascript
end = function () {
  if (this._closed) {
    return;
  }

  this._closed = true;

  for (var id in this._nodes) {
    this._nodes[id].pool.end();
  }
}
```
- example usage
```shell
...
if (this._closed) {
  return;
}

this._closed = true;

for (var id in this._nodes) {
  this._nodes[id].pool.end();
}
};

PoolCluster.prototype._findNodeIds = function (pattern) {
if (typeof this._findCaches[pattern] !== 'undefined') {
  return this._findCaches[pattern];
}
...
```

#### <a name="apidoc.element.mysql2.pool_cluster.prototype.getConnection"></a>[function <span class="apidocSignatureSpan">mysql2.pool_cluster.prototype.</span>getConnection (pattern, selector, cb)](#apidoc.element.mysql2.pool_cluster.prototype.getConnection)
- description and source-code
```javascript
getConnection = function (pattern, selector, cb) {
  var namespace;
  if (typeof pattern === 'function') {
    cb = pattern;
    namespace = this.of();
  } else {
    if (typeof selector === 'function') {
      cb = selector;
      selector = this._defaultSelector;
    }

    namespace = this.of(pattern, selector);
  }

  namespace.getConnection(cb);
}
```
- example usage
```shell
...
}
};

Pool.prototype.query = function (sql, values, cb) {
var cmdQuery = Connection.createQuery(sql, values, cb, this.config.connectionConfig);
cmdQuery.namedPlaceholders = this.config.connectionConfig.namedPlaceholders;

this.getConnection(function (err, conn) {
  if (err) {
    if (typeof cmdQuery.onResult === 'function') {
      cmdQuery.onResult(err);
    } else {
      cmdQuery.emit('error', err);
    }
    return;
...
```

#### <a name="apidoc.element.mysql2.pool_cluster.prototype.of"></a>[function <span class="apidocSignatureSpan">mysql2.pool_cluster.prototype.</span>of (pattern, selector)](#apidoc.element.mysql2.pool_cluster.prototype.of)
- description and source-code
```javascript
of = function (pattern, selector) {
  pattern = pattern || '*';

  selector = selector || this._defaultSelector;
  selector = selector.toUpperCase();
  if (typeof Selector[selector] === 'undefined') {
    selector = this._defaultSelector;
  }

  var key = pattern + selector;

  if (typeof this._namespaces[key] === 'undefined') {
    this._namespaces[key] = new PoolNamespace(this, pattern, selector);
  }

  return this._namespaces[key];
}
```
- example usage
```shell
...
  }
};

PoolCluster.prototype.getConnection = function (pattern, selector, cb) {
  var namespace;
  if (typeof pattern === 'function') {
cb = pattern;
namespace = this.of();
  } else {
if (typeof selector === 'function') {
  cb = selector;
  selector = this._defaultSelector;
}

namespace = this.of(pattern, selector);
...
```



# <a name="apidoc.module.mysql2.pool_connection"></a>[module mysql2.pool_connection](#apidoc.module.mysql2.pool_connection)

#### <a name="apidoc.element.mysql2.pool_connection.pool_connection"></a>[function <span class="apidocSignatureSpan">mysql2.</span>pool_connection (pool, options)](#apidoc.element.mysql2.pool_connection.pool_connection)
- description and source-code
```javascript
function PoolConnection(pool, options) {
  Connection.call(this, options);
  this._pool = pool;

  // When a fatal error occurs the connection's protocol ends, which will cause
  // the connection to end as well, thus we only need to watch for the end event
  // and we will be notified of disconnects.
  var connection = this;
  this.on('end', function (err) { this._removeFromPool(); });
  this.on('error', function (err) { this._removeFromPool(); });
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mysql2.pool_connection.statementKey"></a>[function <span class="apidocSignatureSpan">mysql2.pool_connection.</span>statementKey (options)](#apidoc.element.mysql2.pool_connection.statementKey)
- description and source-code
```javascript
statementKey = function (options) {
  return (typeof options.nestTables) +
    '/' + options.nestTables + '/' + options.rowsAsArray + options.sql;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mysql2.pool_connection.super_"></a>[function <span class="apidocSignatureSpan">mysql2.pool_connection.</span>super_ (opts)](#apidoc.element.mysql2.pool_connection.super_)
- description and source-code
```javascript
function Connection(opts)
{
  EventEmitter.call(this);
  this.config = opts.config;

  // TODO: fill defaults
  // if no params, connect to /var/lib/mysql/mysql.sock ( /tmp/mysql.sock on OSX )
  // if host is given, connect to host:3306

  // TODO: use '/usr/local/mysql/bin/mysql_config --socket' output? as default socketPath
  // if there is no host/port and no socketPath parameters?

  if (!opts.config.stream) {
    if (opts.config.socketPath) {
      this.stream = Net.connect(opts.config.socketPath);
    } else {
      this.stream = Net.connect(opts.config.port, opts.config.host);
    }
  } else {
    // if stream is a function, treat it as "stream agent / factory"
    if (typeof opts.config.stream == 'function') {
      this.stream = opts.config.stream(opts);
    } else {
      this.stream = opts.config.stream;
    }
  }
  this._internalId = _connectionId++;

  this._commands = new Queue();
  this._command = null;

  this._paused = false;
  this._paused_packets = new Queue();

  this._statements = LRU({
    max: this.config.maxPreparedStatements,
    dispose: function (key, statement) { statement.close(); }
  });

  // TODO: make it lru cache
  // https://github.com/mercadolibre/node-simple-lru-cache
  // or https://github.com/rsms/js-lru
  // or https://github.com/monsur/jscache
  // or https://github.com/isaacs/node-lru-cache
  //
  // key is field.name + ':' + field.columnType + ':' field.flags + '/'
  this.textProtocolParsers = {};

  // TODO: not sure if cache should be separate (same key as with textProtocolParsers)
  // or part of prepared statements cache (key is sql query)
  this.binaryProtocolParsers = {};

  this.serverCapabilityFlags = 0;
  this.authorized = false;

  var connection = this;

  this.sequenceId = 0;
  this.compressedSequenceId = 0;

  this.threadId = null;
  this._handshakePacket = null;
  this._fatalError = null;
  this._protocolError = null;
  this._outOfOrderPackets = [];

  this.clientEncoding = CharsetToEncoding[this.config.charsetNumber];

  this.stream.once('error', connection._handleNetworkError.bind(this));

  // see https://gist.github.com/khoomeister/4985691#use-that-instead-of-bind
  this.packetParser = new PacketParser(function (p) {
    connection.handlePacket(p);
  });

  this.stream.on('data', function (data) {
    if (connection.connectTimeout) {
      Timers.clearTimeout(connection.connectTimeout);
      connection.connectTimeout = null;
    }
    connection.packetParser.execute(data);
  });

  this.stream.on('end', function () {
    // we need to set this flag everywhere where we want connection to close
    if (connection._closing) {
      return;
    }

    if (!connection._protocolError) { // no particular error message before disconnect
      connection._protocolError = new Error('Connection lost: The server closed the connection.');
      connection._protocolError.fatal = true;
      connection._protocolError.code = 'PROTOCOL_CONNECTION_LOST';
    }

    connection._notifyError(connection._protocolError);
  });
  var handshakeCommand;
  if (!this.config.isServer) {
    handshakeCommand = new Commands.ClientHandshake(this.config.clientFlags);
    handshakeCommand.on('end', function () {
      connection._handshakePacket = handshakeCommand.handshake;
      connection.threadId = handshakeCommand.handshake.connectionId;
      connection.emit('connect', handshakeCommand.handshake);
    });
    handshakeCommand.on('error', function (err) {
      connection._notifyError(err);
    });
    this.addCommand(handshakeCommand);
  }

  // in case there was no initiall handshake but we need to read sting, assume it utf-8
  // most common example: "Too many connections" error ( packet is sent immediately on connection attempt, we don't know server
encoding yet)
  // will be overwrittedn with actial encoding value as soon as server handshake packet is received
  this.serverEncoding = 'utf8';

  if (this.config.connectTimeout) {
    var timeoutHandler = this._handleTimeoutError.bind(this);
    this.connectTimeout = Timers.setTimeout(timeoutHandler, this.config.connectTimeout);
  }
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.mysql2.pool_connection.prototype"></a>[module mysql2.pool_connection.prototype](#apidoc.module.mysql2.pool_connection.prototype)

#### <a name="apidoc.element.mysql2.pool_connection.prototype._realEnd"></a>[function <span class="apidocSignatureSpan">mysql2.pool_connection.prototype.</span>_realEnd (callback)](#apidoc.element.mysql2.pool_connection.prototype._realEnd)
- description and source-code
```javascript
_realEnd = function (callback) {
  var connection = this;

  if (this.config.isServer) {
    connection._closing = true;
    var quitCmd = new EventEmitter();
    setImmediate(function () {
      connection.stream.end();
      quitCmd.emit('end');
    });
    return quitCmd;
  }

  // trigger error if more commands enqueued after end command
  var quitCmd = this.addCommand(new Commands.Quit(callback));
  connection.addCommand = connection._addCommandClosedState;
  return quitCmd;
}
```
- example usage
```shell
...
if (this._allConnections.length === 0) {
  endCB();
  return;
}

for (var i = 0; i < this._allConnections.length; i++) {
  connection = this._allConnections.get(i);
  connection._realEnd(endCB);
}
};

Pool.prototype.query = function (sql, values, cb) {
var cmdQuery = Connection.createQuery(sql, values, cb, this.config.connectionConfig);
cmdQuery.namedPlaceholders = this.config.connectionConfig.namedPlaceholders;
...
```

#### <a name="apidoc.element.mysql2.pool_connection.prototype._removeFromPool"></a>[function <span class="apidocSignatureSpan">mysql2.pool_connection.prototype.</span>_removeFromPool ()](#apidoc.element.mysql2.pool_connection.prototype._removeFromPool)
- description and source-code
```javascript
_removeFromPool = function () {
  if (!this._pool || this._pool._closed) {
    return;
  }

  var pool = this._pool;
  this._pool = null;

  pool._removeConnection(this);
}
```
- example usage
```shell
...
Connection.call(this, options);
this._pool = pool;

// When a fatal error occurs the connection's protocol ends, which will cause
// the connection to end as well, thus we only need to watch for the end event
// and we will be notified of disconnects.
var connection = this;
this.on('end', function (err) { this._removeFromPool(); });
this.on('error', function (err) { this._removeFromPool(); });
}

PoolConnection.prototype.release = function () {
if (!this._pool || this._pool._closed) {
  return;
}
...
```

#### <a name="apidoc.element.mysql2.pool_connection.prototype.destroy"></a>[function <span class="apidocSignatureSpan">mysql2.pool_connection.prototype.</span>destroy ()](#apidoc.element.mysql2.pool_connection.prototype.destroy)
- description and source-code
```javascript
destroy = function () {
  this._removeFromPool();
  return Connection.prototype.destroy.apply(this, arguments);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mysql2.pool_connection.prototype.end"></a>[function <span class="apidocSignatureSpan">mysql2.pool_connection.prototype.</span>end ()](#apidoc.element.mysql2.pool_connection.prototype.end)
- description and source-code
```javascript
end = function () {
  console.warn('Calling conn.end() to release a pooled connection is '
              + 'deprecated. In next version calling conn.end() will be '
              + 'restored to default conn.end() behavior. Use '
              + 'conn.release() instead.'
              );
  this.release();
}
```
- example usage
```shell
...
if (this._closed) {
  return;
}

this._closed = true;

for (var id in this._nodes) {
  this._nodes[id].pool.end();
}
};

PoolCluster.prototype._findNodeIds = function (pattern) {
if (typeof this._findCaches[pattern] !== 'undefined') {
  return this._findCaches[pattern];
}
...
```

#### <a name="apidoc.element.mysql2.pool_connection.prototype.release"></a>[function <span class="apidocSignatureSpan">mysql2.pool_connection.prototype.</span>release ()](#apidoc.element.mysql2.pool_connection.prototype.release)
- description and source-code
```javascript
release = function () {
  if (!this._pool || this._pool._closed) {
    return;
  }
  this._pool.releaseConnection(this);
}
```
- example usage
```shell
...
    } else {
      cmdQuery.emit('error', err);
    }
    return;
  }

  conn.query(cmdQuery).once('end', function () {
    conn.release();
  });
});
return cmdQuery;
};

Pool.prototype.execute = function (sql, values, cb) {
var useNamedPlaceholders = this.config.connectionConfig.namedPlaceholders;
...
```



# <a name="apidoc.module.mysql2.promise"></a>[module mysql2.promise](#apidoc.module.mysql2.promise)

#### <a name="apidoc.element.mysql2.promise.createConnection"></a>[function <span class="apidocSignatureSpan">mysql2.promise.</span>createConnection (opts)](#apidoc.element.mysql2.promise.createConnection)
- description and source-code
```javascript
function createConnection(opts) {
  var coreConnection = core.createConnection(opts);
  var Promise = opts.Promise || global.Promise;
  if (!Promise) {
    throw new Error('no Promise implementation available.' +
      'Use promise-enabled node version or pass userland Promise' +
      ' implementation as parameter, for example: { Promise: require(\'es6-promise\').Promise }');
  }
  return new Promise(function (resolve, reject) {
    coreConnection.once('connect', function (connectParams) {
      resolve(new PromiseConnection(coreConnection, Promise));
    });
    coreConnection.once('error', reject);
  });
}
```
- example usage
```shell
...
## First Query

'''js
// get the client
var mysql = require('mysql2');

// create the connection to database
var connection = mysql.createConnection({host:'localhost', user: 'root', database: 'test'});

// simple query
connection.query('SELECT * FROM 'table' WHERE 'name' = "Page" AND 'age' > 45', function (err, results, fields) {
  console.log(results); // results contains rows returned by server
  console.log(fields); // fields contains extra meta data about results, if available
});
...
```

#### <a name="apidoc.element.mysql2.promise.createPool"></a>[function <span class="apidocSignatureSpan">mysql2.promise.</span>createPool (opts)](#apidoc.element.mysql2.promise.createPool)
- description and source-code
```javascript
function createPool(opts) {
  var corePool = core.createPool(opts);
  var Promise = opts.Promise || global.Promise || require('es6-promise');

  var promisePool = {
    getConnection: function () {
      return new Promise(function (resolve, reject) {
        corePool.getConnection(function (err, coreConnection) {
          if (err) {
            reject(err);
          } else {
            resolve(new PromiseConnection(coreConnection, Promise));
          }
        });
      });
    },

    query: function (sql, args) {
      return new Promise(function (resolve, reject) {
        var done = makeDoneCb(resolve, reject);
        if (args) {
          corePool.query(sql, args, done);
        } else {
          corePool.query(sql, done);
        }
      });
    },

    execute: function (sql, values) {
      return new Promise(function (resolve, reject) {
        corePool.execute(sql, values, makeDoneCb(resolve, reject));
      });
    },

    end: function () {
      return new Promise(function (resolve, reject) {
        corePool.end(function (err) {
          if (err) {
            reject(err);
          } else {
            resolve();
          }
        });
      });
    }
  };

  return promisePool;
}
```
- example usage
```shell
...
  c.end(function () {
    resolve();
  });
});
};

function createPool (opts) {
var corePool = core.createPool(opts);
var Promise = opts.Promise || global.Promise || require('es6-promise');

var promisePool = {
  getConnection: function () {
    return new Promise(function (resolve, reject) {
      corePool.getConnection(function (err, coreConnection) {
        if (err) {
...
```



# <a name="apidoc.module.mysql2.server"></a>[module mysql2.server](#apidoc.module.mysql2.server)

#### <a name="apidoc.element.mysql2.server.server"></a>[function <span class="apidocSignatureSpan">mysql2.</span>server ()](#apidoc.element.mysql2.server.server)
- description and source-code
```javascript
function Server()
{
  EventEmitter.call(this);
  this.connections = [];
  this._server = net.createServer(this._handleConnection.bind(this));
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mysql2.server.super_"></a>[function <span class="apidocSignatureSpan">mysql2.server.</span>super_ ()](#apidoc.element.mysql2.server.super_)
- description and source-code
```javascript
function EventEmitter() {
  EventEmitter.init.call(this);
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.mysql2.server.prototype"></a>[module mysql2.server.prototype](#apidoc.module.mysql2.server.prototype)

#### <a name="apidoc.element.mysql2.server.prototype._handleConnection"></a>[function <span class="apidocSignatureSpan">mysql2.server.prototype.</span>_handleConnection (socket)](#apidoc.element.mysql2.server.prototype._handleConnection)
- description and source-code
```javascript
_handleConnection = function (socket) {
  var connectionConfig = new ConnectionConfig({stream: socket, isServer: true});
  var connection = new Connection({config: connectionConfig});
  this.emit('connection', connection);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mysql2.server.prototype.close"></a>[function <span class="apidocSignatureSpan">mysql2.server.prototype.</span>close (cb)](#apidoc.element.mysql2.server.prototype.close)
- description and source-code
```javascript
close = function (cb) {
  this._server.close(cb);
}
```
- example usage
```shell
...
Server.prototype.listen = function (port, host, backlog, callback) {
  this._port = port;
  this._server.listen.apply(this._server, arguments);
  return this;
};

Server.prototype.close = function (cb) {
  this._server.close(cb);
};

module.exports = Server;
...
```

#### <a name="apidoc.element.mysql2.server.prototype.listen"></a>[function <span class="apidocSignatureSpan">mysql2.server.prototype.</span>listen (port, host, backlog, callback)](#apidoc.element.mysql2.server.prototype.listen)
- description and source-code
```javascript
listen = function (port, host, backlog, callback) {
  this._port = port;
  this._server.listen.apply(this._server, arguments);
  return this;
}
```
- example usage
```shell
n/a
```



# misc
- this document was created with [utility2](https://github.com/kaizhu256/node-utility2)
