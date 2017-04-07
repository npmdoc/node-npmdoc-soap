# api documentation for  [soap (v0.19.0)](https://github.com/milewise/node-soap#readme)  [![npm package](https://img.shields.io/npm/v/npmdoc-soap.svg?style=flat-square)](https://www.npmjs.org/package/npmdoc-soap) [![travis-ci.org build-status](https://api.travis-ci.org/npmdoc/node-npmdoc-soap.svg)](https://travis-ci.org/npmdoc/node-npmdoc-soap)
#### A minimal node SOAP client

[![NPM](https://nodei.co/npm/soap.png?downloads=true)](https://www.npmjs.com/package/soap)

[![apidoc](https://npmdoc.github.io/node-npmdoc-soap/build/screenCapture.buildNpmdoc.browser.%2Fhome%2Ftravis%2Fbuild%2Fnpmdoc%2Fnode-npmdoc-soap%2Ftmp%2Fbuild%2Fapidoc.html.png)](https://npmdoc.github.io/node-npmdoc-soap/build/apidoc.html)

![npmPackageListing](https://npmdoc.github.io/node-npmdoc-soap/build/screenCapture.npmPackageListing.svg)

![npmPackageDependencyTree](https://npmdoc.github.io/node-npmdoc-soap/build/screenCapture.npmPackageDependencyTree.svg)



# package.json

```json

{
    "author": {
        "name": "Vinay Pulim",
        "email": "v@pulim.com"
    },
    "bugs": {
        "url": "https://github.com/milewise/node-soap/issues"
    },
    "dependencies": {
        "compress": "^0.99.0",
        "concat-stream": "^1.5.1",
        "debug": "~0.7.4",
        "ejs": "~2.5.5",
        "finalhandler": "^0.5.0",
        "lodash": "^3.10.1",
        "optional": "^0.1.3",
        "request": ">=2.9.0",
        "sax": ">=0.6",
        "selectn": "^0.9.6",
        "serve-static": "^1.11.1",
        "strip-bom": "~0.3.1",
        "ursa": "0.8.5 || >=0.9.4",
        "uuid": "^3.0.1",
        "xml-crypto": "~0.8.0"
    },
    "description": "A minimal node SOAP client",
    "devDependencies": {
        "body-parser": "^1.15.2",
        "colors": "^1.1.2",
        "coveralls": "^2.11.6",
        "diff": "^2.2.1",
        "doctoc": "^1.0.0",
        "duplexer": "~0.1.1",
        "express": "^4.14.0",
        "glob": "~3.2.8",
        "istanbul": "^0.4.1",
        "jshint": "2.3.0",
        "mocha": "~1.17.0",
        "readable-stream": "~2.0.2",
        "semver": "~5.0.3",
        "should": "~3.3.0",
        "sinon": "^1.17.5",
        "timekeeper": "~0.0.4"
    },
    "directories": {
        "lib": "./lib"
    },
    "dist": {
        "shasum": "e80d1ac07d43d2259869d5ca70f41499abf5f34e",
        "tarball": "https://registry.npmjs.org/soap/-/soap-0.19.0.tgz"
    },
    "engines": {
        "node": ">=0.10.0"
    },
    "gitHead": "bd762cc3a822fa699ad8bbceff753d58e5b2dafe",
    "homepage": "https://github.com/milewise/node-soap#readme",
    "keywords": [
        "soap"
    ],
    "license": "MIT",
    "main": "./index.js",
    "maintainers": [
        {
            "name": "vpulim",
            "email": "v@pulim.com"
        },
        {
            "name": "aaron",
            "email": "aaron.heckmann+github@gmail.com"
        },
        {
            "name": "jsdevel",
            "email": "js.developer.undefined@gmail.com"
        },
        {
            "name": "herom",
            "email": "h.romirer@gmail.com"
        }
    ],
    "name": "soap",
    "optionalDependencies": {
        "ursa": "0.8.5 || >=0.9.4"
    },
    "readme": "ERROR: No README data found!",
    "repository": {
        "type": "git",
        "url": "git+https://github.com/milewise/node-soap.git"
    },
    "scripts": {
        "cover": "istanbul cover _mocha -- --timeout 10000 test/*-test.js test/security/*.js",
        "coveralls": "cat ./coverage/lcov.info | ./node_modules/coveralls/bin/coveralls.js -v",
        "pretest": "jshint index.js lib test",
        "test": "mocha --timeout 10000 test/*-test.js test/security/*.js",
        "toc": "doctoc Readme.md --github --maxlevel 3"
    },
    "version": "0.19.0"
}
```



# <a name="apidoc.tableOfContents"></a>[table of contents](#apidoc.tableOfContents)

#### [module soap](#apidoc.module.soap)
1.  [function <span class="apidocSignatureSpan">soap.</span>BasicAuthSecurity (username, password, defaults)](#apidoc.element.soap.BasicAuthSecurity)
1.  [function <span class="apidocSignatureSpan">soap.</span>BearerSecurity (token, defaults)](#apidoc.element.soap.BearerSecurity)
1.  [function <span class="apidocSignatureSpan">soap.</span>Client (wsdl, endpoint, options)](#apidoc.element.soap.Client)
1.  [function <span class="apidocSignatureSpan">soap.</span>ClientSSLSecurity (key, cert, ca, defaults)](#apidoc.element.soap.ClientSSLSecurity)
1.  [function <span class="apidocSignatureSpan">soap.</span>ClientSSLSecurityPFX (pfx, passphrase, defaults)](#apidoc.element.soap.ClientSSLSecurityPFX)
1.  [function <span class="apidocSignatureSpan">soap.</span>HttpClient (options)](#apidoc.element.soap.HttpClient)
1.  [function <span class="apidocSignatureSpan">soap.</span>Server (server, path, services, wsdl, options)](#apidoc.element.soap.Server)
1.  [function <span class="apidocSignatureSpan">soap.</span>WSDL (definition, uri, options)](#apidoc.element.soap.WSDL)
1.  [function <span class="apidocSignatureSpan">soap.</span>WSSecurity (username, password, options)](#apidoc.element.soap.WSSecurity)
1.  [function <span class="apidocSignatureSpan">soap.</span>WSSecurityCert (privatePEM, publicP12PEM, password, encoding)](#apidoc.element.soap.WSSecurityCert)
1.  [function <span class="apidocSignatureSpan">soap.</span>createClient (url, options, callback, endpoint)](#apidoc.element.soap.createClient)
1.  [function <span class="apidocSignatureSpan">soap.</span>listen (server, pathOrOptions, services, xml)](#apidoc.element.soap.listen)
1.  [function <span class="apidocSignatureSpan">soap.</span>nscontext ()](#apidoc.element.soap.nscontext)
1.  [function <span class="apidocSignatureSpan">soap.</span>passwordDigest (nonce, created, password)](#apidoc.element.soap.passwordDigest)
1.  object <span class="apidocSignatureSpan">soap.</span>BasicAuthSecurity.prototype
1.  object <span class="apidocSignatureSpan">soap.</span>BearerSecurity.prototype
1.  object <span class="apidocSignatureSpan">soap.</span>Client.prototype
1.  object <span class="apidocSignatureSpan">soap.</span>ClientSSLSecurity.prototype
1.  object <span class="apidocSignatureSpan">soap.</span>ClientSSLSecurityPFX.prototype
1.  object <span class="apidocSignatureSpan">soap.</span>HttpClient.prototype
1.  object <span class="apidocSignatureSpan">soap.</span>Server.prototype
1.  object <span class="apidocSignatureSpan">soap.</span>WSDL.prototype
1.  object <span class="apidocSignatureSpan">soap.</span>WSSecurity.prototype
1.  object <span class="apidocSignatureSpan">soap.</span>WSSecurityCert.prototype
1.  object <span class="apidocSignatureSpan">soap.</span>client
1.  object <span class="apidocSignatureSpan">soap.</span>nscontext.prototype
1.  object <span class="apidocSignatureSpan">soap.</span>security
1.  object <span class="apidocSignatureSpan">soap.</span>server
1.  object <span class="apidocSignatureSpan">soap.</span>soap_stub
1.  object <span class="apidocSignatureSpan">soap.</span>utils
1.  object <span class="apidocSignatureSpan">soap.</span>wsdl

#### [module soap.BasicAuthSecurity](#apidoc.module.soap.BasicAuthSecurity)
1.  [function <span class="apidocSignatureSpan">soap.</span>BasicAuthSecurity (username, password, defaults)](#apidoc.element.soap.BasicAuthSecurity.BasicAuthSecurity)

#### [module soap.BasicAuthSecurity.prototype](#apidoc.module.soap.BasicAuthSecurity.prototype)
1.  [function <span class="apidocSignatureSpan">soap.BasicAuthSecurity.prototype.</span>addHeaders (headers)](#apidoc.element.soap.BasicAuthSecurity.prototype.addHeaders)
1.  [function <span class="apidocSignatureSpan">soap.BasicAuthSecurity.prototype.</span>addOptions (options)](#apidoc.element.soap.BasicAuthSecurity.prototype.addOptions)
1.  [function <span class="apidocSignatureSpan">soap.BasicAuthSecurity.prototype.</span>toXML ()](#apidoc.element.soap.BasicAuthSecurity.prototype.toXML)

#### [module soap.BearerSecurity](#apidoc.module.soap.BearerSecurity)
1.  [function <span class="apidocSignatureSpan">soap.</span>BearerSecurity (token, defaults)](#apidoc.element.soap.BearerSecurity.BearerSecurity)

#### [module soap.BearerSecurity.prototype](#apidoc.module.soap.BearerSecurity.prototype)
1.  [function <span class="apidocSignatureSpan">soap.BearerSecurity.prototype.</span>addHeaders (headers)](#apidoc.element.soap.BearerSecurity.prototype.addHeaders)
1.  [function <span class="apidocSignatureSpan">soap.BearerSecurity.prototype.</span>addOptions (options)](#apidoc.element.soap.BearerSecurity.prototype.addOptions)
1.  [function <span class="apidocSignatureSpan">soap.BearerSecurity.prototype.</span>toXML ()](#apidoc.element.soap.BearerSecurity.prototype.toXML)

#### [module soap.Client](#apidoc.module.soap.Client)
1.  [function <span class="apidocSignatureSpan">soap.</span>Client (wsdl, endpoint, options)](#apidoc.element.soap.Client.Client)
1.  [function <span class="apidocSignatureSpan">soap.Client.</span>super_ ()](#apidoc.element.soap.Client.super_)

#### [module soap.Client.prototype](#apidoc.module.soap.Client.prototype)
1.  [function <span class="apidocSignatureSpan">soap.Client.prototype.</span>_defineMethod (method, location)](#apidoc.element.soap.Client.prototype._defineMethod)
1.  [function <span class="apidocSignatureSpan">soap.Client.prototype.</span>_definePort (port, endpoint)](#apidoc.element.soap.Client.prototype._definePort)
1.  [function <span class="apidocSignatureSpan">soap.Client.prototype.</span>_defineService (service, endpoint)](#apidoc.element.soap.Client.prototype._defineService)
1.  [function <span class="apidocSignatureSpan">soap.Client.prototype.</span>_getArgsScheme (methodName)](#apidoc.element.soap.Client.prototype._getArgsScheme)
1.  [function <span class="apidocSignatureSpan">soap.Client.prototype.</span>_initializeOptions (options)](#apidoc.element.soap.Client.prototype._initializeOptions)
1.  [function <span class="apidocSignatureSpan">soap.Client.prototype.</span>_initializeServices (endpoint)](#apidoc.element.soap.Client.prototype._initializeServices)
1.  [function <span class="apidocSignatureSpan">soap.Client.prototype.</span>_invoke (method, args, location, callback, options, extraHeaders)](#apidoc.element.soap.Client.prototype._invoke)
1.  [function <span class="apidocSignatureSpan">soap.Client.prototype.</span>_isSequenceRequired (methodName)](#apidoc.element.soap.Client.prototype._isSequenceRequired)
1.  [function <span class="apidocSignatureSpan">soap.Client.prototype.</span>_setSequenceArgs (argsScheme, args)](#apidoc.element.soap.Client.prototype._setSequenceArgs)
1.  [function <span class="apidocSignatureSpan">soap.Client.prototype.</span>addBodyAttribute (bodyAttribute, name, namespace, xmlns)](#apidoc.element.soap.Client.prototype.addBodyAttribute)
1.  [function <span class="apidocSignatureSpan">soap.Client.prototype.</span>addHttpHeader (name, value)](#apidoc.element.soap.Client.prototype.addHttpHeader)
1.  [function <span class="apidocSignatureSpan">soap.Client.prototype.</span>addSoapHeader (soapHeader, name, namespace, xmlns)](#apidoc.element.soap.Client.prototype.addSoapHeader)
1.  [function <span class="apidocSignatureSpan">soap.Client.prototype.</span>changeSoapHeader (index, soapHeader, name, namespace, xmlns)](#apidoc.element.soap.Client.prototype.changeSoapHeader)
1.  [function <span class="apidocSignatureSpan">soap.Client.prototype.</span>clearBodyAttributes ()](#apidoc.element.soap.Client.prototype.clearBodyAttributes)
1.  [function <span class="apidocSignatureSpan">soap.Client.prototype.</span>clearHttpHeaders ()](#apidoc.element.soap.Client.prototype.clearHttpHeaders)
1.  [function <span class="apidocSignatureSpan">soap.Client.prototype.</span>clearSoapHeaders ()](#apidoc.element.soap.Client.prototype.clearSoapHeaders)
1.  [function <span class="apidocSignatureSpan">soap.Client.prototype.</span>describe ()](#apidoc.element.soap.Client.prototype.describe)
1.  [function <span class="apidocSignatureSpan">soap.Client.prototype.</span>getBodyAttributes ()](#apidoc.element.soap.Client.prototype.getBodyAttributes)
1.  [function <span class="apidocSignatureSpan">soap.Client.prototype.</span>getHttpHeaders ()](#apidoc.element.soap.Client.prototype.getHttpHeaders)
1.  [function <span class="apidocSignatureSpan">soap.Client.prototype.</span>getSoapHeaders ()](#apidoc.element.soap.Client.prototype.getSoapHeaders)
1.  [function <span class="apidocSignatureSpan">soap.Client.prototype.</span>setEndpoint (endpoint)](#apidoc.element.soap.Client.prototype.setEndpoint)
1.  [function <span class="apidocSignatureSpan">soap.Client.prototype.</span>setSOAPAction (SOAPAction)](#apidoc.element.soap.Client.prototype.setSOAPAction)
1.  [function <span class="apidocSignatureSpan">soap.Client.prototype.</span>setSecurity (security)](#apidoc.element.soap.Client.prototype.setSecurity)

#### [module soap.ClientSSLSecurity](#apidoc.module.soap.ClientSSLSecurity)
1.  [function <span class="apidocSignatureSpan">soap.</span>ClientSSLSecurity (key, cert, ca, defaults)](#apidoc.element.soap.ClientSSLSecurity.ClientSSLSecurity)

#### [module soap.ClientSSLSecurity.prototype](#apidoc.module.soap.ClientSSLSecurity.prototype)
1.  [function <span class="apidocSignatureSpan">soap.ClientSSLSecurity.prototype.</span>addOptions (options)](#apidoc.element.soap.ClientSSLSecurity.prototype.addOptions)
1.  [function <span class="apidocSignatureSpan">soap.ClientSSLSecurity.prototype.</span>toXML (headers)](#apidoc.element.soap.ClientSSLSecurity.prototype.toXML)

#### [module soap.ClientSSLSecurityPFX](#apidoc.module.soap.ClientSSLSecurityPFX)
1.  [function <span class="apidocSignatureSpan">soap.</span>ClientSSLSecurityPFX (pfx, passphrase, defaults)](#apidoc.element.soap.ClientSSLSecurityPFX.ClientSSLSecurityPFX)

#### [module soap.ClientSSLSecurityPFX.prototype](#apidoc.module.soap.ClientSSLSecurityPFX.prototype)
1.  [function <span class="apidocSignatureSpan">soap.ClientSSLSecurityPFX.prototype.</span>addOptions (options)](#apidoc.element.soap.ClientSSLSecurityPFX.prototype.addOptions)
1.  [function <span class="apidocSignatureSpan">soap.ClientSSLSecurityPFX.prototype.</span>toXML (headers)](#apidoc.element.soap.ClientSSLSecurityPFX.prototype.toXML)

#### [module soap.HttpClient](#apidoc.module.soap.HttpClient)
1.  [function <span class="apidocSignatureSpan">soap.</span>HttpClient (options)](#apidoc.element.soap.HttpClient.HttpClient)

#### [module soap.HttpClient.prototype](#apidoc.module.soap.HttpClient.prototype)
1.  [function <span class="apidocSignatureSpan">soap.HttpClient.prototype.</span>buildRequest (rurl, data, exheaders, exoptions)](#apidoc.element.soap.HttpClient.prototype.buildRequest)
1.  [function <span class="apidocSignatureSpan">soap.HttpClient.prototype.</span>handleResponse (req, res, body)](#apidoc.element.soap.HttpClient.prototype.handleResponse)
1.  [function <span class="apidocSignatureSpan">soap.HttpClient.prototype.</span>request (rurl, data, callback, exheaders, exoptions)](#apidoc.element.soap.HttpClient.prototype.request)
1.  [function <span class="apidocSignatureSpan">soap.HttpClient.prototype.</span>requestStream (rurl, data, exheaders, exoptions)](#apidoc.element.soap.HttpClient.prototype.requestStream)

#### [module soap.Server](#apidoc.module.soap.Server)
1.  [function <span class="apidocSignatureSpan">soap.</span>Server (server, path, services, wsdl, options)](#apidoc.element.soap.Server.Server)
1.  [function <span class="apidocSignatureSpan">soap.Server.</span>super_ ()](#apidoc.element.soap.Server.super_)

#### [module soap.Server.prototype](#apidoc.module.soap.Server.prototype)
1.  [function <span class="apidocSignatureSpan">soap.Server.prototype.</span>_envelope (body, includeTimestamp)](#apidoc.element.soap.Server.prototype._envelope)
1.  [function <span class="apidocSignatureSpan">soap.Server.prototype.</span>_executeMethod (options, req, callback, includeTimestamp)](#apidoc.element.soap.Server.prototype._executeMethod)
1.  [function <span class="apidocSignatureSpan">soap.Server.prototype.</span>_initializeOptions (options)](#apidoc.element.soap.Server.prototype._initializeOptions)
1.  [function <span class="apidocSignatureSpan">soap.Server.prototype.</span>_process (input, req, callback)](#apidoc.element.soap.Server.prototype._process)
1.  [function <span class="apidocSignatureSpan">soap.Server.prototype.</span>_processRequestXml (req, res, xml)](#apidoc.element.soap.Server.prototype._processRequestXml)
1.  [function <span class="apidocSignatureSpan">soap.Server.prototype.</span>_requestListener (req, res)](#apidoc.element.soap.Server.prototype._requestListener)
1.  [function <span class="apidocSignatureSpan">soap.Server.prototype.</span>_sendError (soapFault, callback, includeTimestamp)](#apidoc.element.soap.Server.prototype._sendError)
1.  [function <span class="apidocSignatureSpan">soap.Server.prototype.</span>addSoapHeader (soapHeader, name, namespace, xmlns)](#apidoc.element.soap.Server.prototype.addSoapHeader)
1.  [function <span class="apidocSignatureSpan">soap.Server.prototype.</span>changeSoapHeader (index, soapHeader, name, namespace, xmlns)](#apidoc.element.soap.Server.prototype.changeSoapHeader)
1.  [function <span class="apidocSignatureSpan">soap.Server.prototype.</span>clearSoapHeaders ()](#apidoc.element.soap.Server.prototype.clearSoapHeaders)
1.  [function <span class="apidocSignatureSpan">soap.Server.prototype.</span>getSoapHeaders ()](#apidoc.element.soap.Server.prototype.getSoapHeaders)

#### [module soap.WSDL](#apidoc.module.soap.WSDL)
1.  [function <span class="apidocSignatureSpan">soap.</span>WSDL (definition, uri, options)](#apidoc.element.soap.WSDL.WSDL)

#### [module soap.WSDL.prototype](#apidoc.module.soap.WSDL.prototype)
1.  boolean <span class="apidocSignatureSpan">soap.WSDL.prototype.</span>ignoreBaseNameSpaces
1.  [function <span class="apidocSignatureSpan">soap.WSDL.prototype.</span>_fromServices (services)](#apidoc.element.soap.WSDL.prototype._fromServices)
1.  [function <span class="apidocSignatureSpan">soap.WSDL.prototype.</span>_fromXML (xml)](#apidoc.element.soap.WSDL.prototype._fromXML)
1.  [function <span class="apidocSignatureSpan">soap.WSDL.prototype.</span>_initializeOptions (options)](#apidoc.element.soap.WSDL.prototype._initializeOptions)
1.  [function <span class="apidocSignatureSpan">soap.WSDL.prototype.</span>_parse (xml)](#apidoc.element.soap.WSDL.prototype._parse)
1.  [function <span class="apidocSignatureSpan">soap.WSDL.prototype.</span>_processNextInclude (includes, callback)](#apidoc.element.soap.WSDL.prototype._processNextInclude)
1.  [function <span class="apidocSignatureSpan">soap.WSDL.prototype.</span>_splitQName (nsName)](#apidoc.element.soap.WSDL.prototype._splitQName)
1.  [function <span class="apidocSignatureSpan">soap.WSDL.prototype.</span>_xmlnsMap ()](#apidoc.element.soap.WSDL.prototype._xmlnsMap)
1.  [function <span class="apidocSignatureSpan">soap.WSDL.prototype.</span>describeServices ()](#apidoc.element.soap.WSDL.prototype.describeServices)
1.  [function <span class="apidocSignatureSpan">soap.WSDL.prototype.</span>filterOutIgnoredNameSpace (ns)](#apidoc.element.soap.WSDL.prototype.filterOutIgnoredNameSpace)
1.  [function <span class="apidocSignatureSpan">soap.WSDL.prototype.</span>findChildSchemaObject (parameterTypeObj, childName)](#apidoc.element.soap.WSDL.prototype.findChildSchemaObject)
1.  [function <span class="apidocSignatureSpan">soap.WSDL.prototype.</span>findSchemaObject (nsURI, qname)](#apidoc.element.soap.WSDL.prototype.findSchemaObject)
1.  [function <span class="apidocSignatureSpan">soap.WSDL.prototype.</span>findSchemaType (name, nsURI)](#apidoc.element.soap.WSDL.prototype.findSchemaType)
1.  [function <span class="apidocSignatureSpan">soap.WSDL.prototype.</span>isIgnoredNameSpace (ns)](#apidoc.element.soap.WSDL.prototype.isIgnoredNameSpace)
1.  [function <span class="apidocSignatureSpan">soap.WSDL.prototype.</span>objectToDocumentXML (name, params, nsPrefix, nsURI, type)](#apidoc.element.soap.WSDL.prototype.objectToDocumentXML)
1.  [function <span class="apidocSignatureSpan">soap.WSDL.prototype.</span>objectToRpcXML (name, params, nsPrefix, nsURI, isParts)](#apidoc.element.soap.WSDL.prototype.objectToRpcXML)
1.  [function <span class="apidocSignatureSpan">soap.WSDL.prototype.</span>objectToXML (obj, name, nsPrefix, nsURI, isFirst, xmlnsAttr, schemaObject, nsContext)](#apidoc.element.soap.WSDL.prototype.objectToXML)
1.  [function <span class="apidocSignatureSpan">soap.WSDL.prototype.</span>onReady (callback)](#apidoc.element.soap.WSDL.prototype.onReady)
1.  [function <span class="apidocSignatureSpan">soap.WSDL.prototype.</span>processAttributes (child, nsContext)](#apidoc.element.soap.WSDL.prototype.processAttributes)
1.  [function <span class="apidocSignatureSpan">soap.WSDL.prototype.</span>processIncludes (callback)](#apidoc.element.soap.WSDL.prototype.processIncludes)
1.  [function <span class="apidocSignatureSpan">soap.WSDL.prototype.</span>toXML ()](#apidoc.element.soap.WSDL.prototype.toXML)
1.  [function <span class="apidocSignatureSpan">soap.WSDL.prototype.</span>xmlToObject (xml, callback)](#apidoc.element.soap.WSDL.prototype.xmlToObject)
1.  object <span class="apidocSignatureSpan">soap.WSDL.prototype.</span>ignoredNamespaces
1.  string <span class="apidocSignatureSpan">soap.WSDL.prototype.</span>valueKey
1.  string <span class="apidocSignatureSpan">soap.WSDL.prototype.</span>xmlKey

#### [module soap.WSSecurity](#apidoc.module.soap.WSSecurity)
1.  [function <span class="apidocSignatureSpan">soap.</span>WSSecurity (username, password, options)](#apidoc.element.soap.WSSecurity.WSSecurity)

#### [module soap.WSSecurity.prototype](#apidoc.module.soap.WSSecurity.prototype)
1.  [function <span class="apidocSignatureSpan">soap.WSSecurity.prototype.</span>toXML ()](#apidoc.element.soap.WSSecurity.prototype.toXML)

#### [module soap.WSSecurityCert](#apidoc.module.soap.WSSecurityCert)
1.  [function <span class="apidocSignatureSpan">soap.</span>WSSecurityCert (privatePEM, publicP12PEM, password, encoding)](#apidoc.element.soap.WSSecurityCert.WSSecurityCert)

#### [module soap.WSSecurityCert.prototype](#apidoc.module.soap.WSSecurityCert.prototype)
1.  [function <span class="apidocSignatureSpan">soap.WSSecurityCert.prototype.</span>postProcess (xml, envelopeKey)](#apidoc.element.soap.WSSecurityCert.prototype.postProcess)

#### [module soap.client](#apidoc.module.soap.client)
1.  [function <span class="apidocSignatureSpan">soap.client.</span>Client (wsdl, endpoint, options)](#apidoc.element.soap.client.Client)

#### [module soap.nscontext](#apidoc.module.soap.nscontext)
1.  [function <span class="apidocSignatureSpan">soap.</span>nscontext ()](#apidoc.element.soap.nscontext.nscontext)

#### [module soap.nscontext.prototype](#apidoc.module.soap.nscontext.prototype)
1.  [function <span class="apidocSignatureSpan">soap.nscontext.prototype.</span>addNamespace (prefix, nsUri, localOnly)](#apidoc.element.soap.nscontext.prototype.addNamespace)
1.  [function <span class="apidocSignatureSpan">soap.nscontext.prototype.</span>declareNamespace (prefix, nsUri)](#apidoc.element.soap.nscontext.prototype.declareNamespace)
1.  [function <span class="apidocSignatureSpan">soap.nscontext.prototype.</span>getNamespaceURI (prefix, localOnly)](#apidoc.element.soap.nscontext.prototype.getNamespaceURI)
1.  [function <span class="apidocSignatureSpan">soap.nscontext.prototype.</span>getPrefix (nsUri, localOnly)](#apidoc.element.soap.nscontext.prototype.getPrefix)
1.  [function <span class="apidocSignatureSpan">soap.nscontext.prototype.</span>popContext ()](#apidoc.element.soap.nscontext.prototype.popContext)
1.  [function <span class="apidocSignatureSpan">soap.nscontext.prototype.</span>pushContext ()](#apidoc.element.soap.nscontext.prototype.pushContext)
1.  [function <span class="apidocSignatureSpan">soap.nscontext.prototype.</span>registerNamespace (nsUri)](#apidoc.element.soap.nscontext.prototype.registerNamespace)

#### [module soap.security](#apidoc.module.soap.security)
1.  [function <span class="apidocSignatureSpan">soap.security.</span>BasicAuthSecurity (username, password, defaults)](#apidoc.element.soap.security.BasicAuthSecurity)
1.  [function <span class="apidocSignatureSpan">soap.security.</span>BearerSecurity (token, defaults)](#apidoc.element.soap.security.BearerSecurity)
1.  [function <span class="apidocSignatureSpan">soap.security.</span>ClientSSLSecurity (key, cert, ca, defaults)](#apidoc.element.soap.security.ClientSSLSecurity)
1.  [function <span class="apidocSignatureSpan">soap.security.</span>ClientSSLSecurityPFX (pfx, passphrase, defaults)](#apidoc.element.soap.security.ClientSSLSecurityPFX)
1.  [function <span class="apidocSignatureSpan">soap.security.</span>WSSecurity (username, password, options)](#apidoc.element.soap.security.WSSecurity)
1.  [function <span class="apidocSignatureSpan">soap.security.</span>WSSecurityCert (privatePEM, publicP12PEM, password, encoding)](#apidoc.element.soap.security.WSSecurityCert)

#### [module soap.server](#apidoc.module.soap.server)
1.  [function <span class="apidocSignatureSpan">soap.server.</span>Server (server, path, services, wsdl, options)](#apidoc.element.soap.server.Server)

#### [module soap.soap_stub](#apidoc.module.soap.soap_stub)
1.  boolean <span class="apidocSignatureSpan">soap.soap_stub.</span>errOnCreateClient
1.  [function <span class="apidocSignatureSpan">soap.soap_stub.</span>createClient (wsdlUrl, options, cb)](#apidoc.element.soap.soap_stub.createClient)
1.  [function <span class="apidocSignatureSpan">soap.soap_stub.</span>createErroringStub (err)](#apidoc.element.soap.soap_stub.createErroringStub)
1.  [function <span class="apidocSignatureSpan">soap.soap_stub.</span>createRespondingStub (object, body)](#apidoc.element.soap.soap_stub.createRespondingStub)
1.  [function <span class="apidocSignatureSpan">soap.soap_stub.</span>getStub (aliasOrWsdlUrl)](#apidoc.element.soap.soap_stub.getStub)
1.  [function <span class="apidocSignatureSpan">soap.soap_stub.</span>registerClient (alias, urlToWsdl, clientStub)](#apidoc.element.soap.soap_stub.registerClient)
1.  [function <span class="apidocSignatureSpan">soap.soap_stub.</span>reset ()](#apidoc.element.soap.soap_stub.reset)
1.  object <span class="apidocSignatureSpan">soap.soap_stub.</span>security

#### [module soap.utils](#apidoc.module.soap.utils)
1.  [function <span class="apidocSignatureSpan">soap.utils.</span>findPrefix (xmlnsMapping, nsURI)](#apidoc.element.soap.utils.findPrefix)
1.  [function <span class="apidocSignatureSpan">soap.utils.</span>passwordDigest (nonce, created, password)](#apidoc.element.soap.utils.passwordDigest)
1.  string <span class="apidocSignatureSpan">soap.utils.</span>TNS_PREFIX

#### [module soap.wsdl](#apidoc.module.soap.wsdl)
1.  [function <span class="apidocSignatureSpan">soap.wsdl.</span>WSDL (definition, uri, options)](#apidoc.element.soap.wsdl.WSDL)
1.  [function <span class="apidocSignatureSpan">soap.wsdl.</span>open_wsdl (uri, options, callback)](#apidoc.element.soap.wsdl.open_wsdl)



# <a name="apidoc.module.soap"></a>[module soap](#apidoc.module.soap)

#### <a name="apidoc.element.soap.BasicAuthSecurity"></a>[function <span class="apidocSignatureSpan">soap.</span>BasicAuthSecurity (username, password, defaults)](#apidoc.element.soap.BasicAuthSecurity)
- description and source-code
```javascript
function BasicAuthSecurity(username, password, defaults) {
  this._username = username;
  this._password = password;
  this.defaults = {};
  _.merge(this.defaults, defaults);
}
```
- example usage
```shell
...
as well.  The interface is quite simple. Each protocol defines 2 methods:
* 'addOptions' - a method that accepts an options arg that is eventually passed directly to 'request'
* 'toXML' - a method that returns a string of XML.

### BasicAuthSecurity

''' javascript
  client.setSecurity(new soap.BasicAuthSecurity('username', 'password'));
'''

### BearerSecurity

''' javascript
  client.setSecurity(new soap.BearerSecurity('token'));
'''
...
```

#### <a name="apidoc.element.soap.BearerSecurity"></a>[function <span class="apidocSignatureSpan">soap.</span>BearerSecurity (token, defaults)](#apidoc.element.soap.BearerSecurity)
- description and source-code
```javascript
function BearerSecurity(token, defaults) {
	this._token = token;
	this.defaults = {};
	_.merge(this.defaults, defaults);
}
```
- example usage
```shell
...
''' javascript
  client.setSecurity(new soap.BasicAuthSecurity('username', 'password'));
'''

### BearerSecurity

''' javascript
  client.setSecurity(new soap.BearerSecurity('token'));
'''

### ClientSSLSecurity

_Note_: If you run into issues using this protocol, consider passing these options
as default request options to the constructor:
* 'rejectUnauthorized: false'
...
```

#### <a name="apidoc.element.soap.Client"></a>[function <span class="apidocSignatureSpan">soap.</span>Client (wsdl, endpoint, options)](#apidoc.element.soap.Client)
- description and source-code
```javascript
Client = function (wsdl, endpoint, options) {
  events.EventEmitter.call(this);
  options = options || {};
  this.wsdl = wsdl;
  this._initializeOptions(options);
  this._initializeServices(endpoint);
  this.httpClient = options.httpClient || new HttpClient(options);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.soap.ClientSSLSecurity"></a>[function <span class="apidocSignatureSpan">soap.</span>ClientSSLSecurity (key, cert, ca, defaults)](#apidoc.element.soap.ClientSSLSecurity)
- description and source-code
```javascript
function ClientSSLSecurity(key, cert, ca, defaults) {
  if (key) {
    if(Buffer.isBuffer(key)) {
      this.key = key;
    } else if (typeof key === 'string') {
      this.key = fs.readFileSync(key);
    } else {
      throw new Error('key should be a buffer or a string!');
    }
  }

  if (cert) {
    if(Buffer.isBuffer(cert)) {
      this.cert = cert;
    } else if (typeof cert === 'string') {
      this.cert = fs.readFileSync(cert);
    } else {
      throw new Error('cert should be a buffer or a string!');
    }
  }

  if (ca) {
    if(Buffer.isBuffer(ca) || Array.isArray(ca)) {
      this.ca = ca;
    } else if (typeof ca === 'string') {
      this.ca = fs.readFileSync(ca);
    } else {
      defaults = ca;
      this.ca = null;
    }
  }

  this.defaults = {};
  _.merge(this.defaults, defaults);
}
```
- example usage
```shell
...
_Note_: If you run into issues using this protocol, consider passing these options
as default request options to the constructor:
* 'rejectUnauthorized: false'
* 'strictSSL: false'
* 'secureOptions: constants.SSL_OP_NO_TLSv1_2' (this is likely needed for node >= 10.0)

''' javascript
  client.setSecurity(new soap.ClientSSLSecurity(
    '/path/to/key'
    , '/path/to/cert'
    , {/*default request options*/}
  ));
'''

### WSSecurity
...
```

#### <a name="apidoc.element.soap.ClientSSLSecurityPFX"></a>[function <span class="apidocSignatureSpan">soap.</span>ClientSSLSecurityPFX (pfx, passphrase, defaults)](#apidoc.element.soap.ClientSSLSecurityPFX)
- description and source-code
```javascript
function ClientSSLSecurityPFX(pfx, passphrase, defaults) {
  if (typeof passphrase === 'object') {
    defaults = passphrase;
  }
  if (pfx) {
    if (Buffer.isBuffer(pfx)) {
      this.pfx = pfx;
    } else if (typeof pfx === 'string') {
      this.pfx = fs.readFileSync(pfx);
    } else {
      throw new Error('supplied pfx file should be a buffer or a file location');
    }
  }

  if (passphrase) {
    if (typeof passphrase === 'string') {
      this.passphrase = passphrase;
    }
  }
  this.defaults = {};
  _.merge(this.defaults, defaults);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.soap.HttpClient"></a>[function <span class="apidocSignatureSpan">soap.</span>HttpClient (options)](#apidoc.element.soap.HttpClient)
- description and source-code
```javascript
function HttpClient(options) {
  options = options || {};
  this._request = options.request || req;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.soap.Server"></a>[function <span class="apidocSignatureSpan">soap.</span>Server (server, path, services, wsdl, options)](#apidoc.element.soap.Server)
- description and source-code
```javascript
Server = function (server, path, services, wsdl, options) {
  var self = this;

  events.EventEmitter.call(this);

  options = options || {};
  this.path = path;
  this.services = services;
  this.wsdl = wsdl;
  this.suppressStack = options && options.suppressStack;

  if (path[path.length - 1] !== '/')
    path += '/';
  wsdl.onReady(function (err) {
    if (typeof server.route === 'function' && typeof server.use === 'function') {
      //handle only the required URL path for express server
      server.route(path).all(function (req, res, next) {
        if (typeof self.authorizeConnection === 'function') {
          if (!self.authorizeConnection(req)) {
            res.end();
            return;
          }
        }
        self._requestListener(req, res);
      });
    } else {
      var listeners = server.listeners('request').slice();
      server.removeAllListeners('request');
      server.addListener('request', function (req, res) {
        if (typeof self.authorizeConnection === 'function') {
          if (!self.authorizeConnection(req)) {
            res.end();
            return;
          }
        }
        var reqPath = url.parse(req.url).pathname;
        if (reqPath[reqPath.length - 1] !== '/') {
          reqPath += '/';
        }
        if (path === reqPath) {
          self._requestListener(req, res);
        } else {
          for (var i = 0, len = listeners.length; i < len; i++) {
            listeners[i].call(this, req, res);
          }
        }
      });
    }
  });

  this._initializeOptions(options);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.soap.WSDL"></a>[function <span class="apidocSignatureSpan">soap.</span>WSDL (definition, uri, options)](#apidoc.element.soap.WSDL)
- description and source-code
```javascript
WSDL = function (definition, uri, options) {
  var self = this,
      fromFunc;

  this.uri = uri;
  this.callback = function() {
  };
  this._includesWsdl = [];

  // initialize WSDL cache
  this.WSDL_CACHE = (options || {}).WSDL_CACHE || {};

  this._initializeOptions(options);

  if (typeof definition === 'string') {
    definition = stripBom(definition);
    fromFunc = this._fromXML;
  }
  else if (typeof definition === 'object') {
    fromFunc = this._fromServices;
  }
  else {
    throw new Error('WSDL constructor takes either an XML string or service definition');
  }

  process.nextTick(function() {
    try {
      fromFunc.call(self, definition);
    } catch (e) {
      return self.callback(e.message);
    }

    self.processIncludes(function(err) {
      var name;
      if (err) {
        return self.callback(err);
      }

      self.definitions.deleteFixedAttrs();
      var services = self.services = self.definitions.services;
      if (services) {
        for (name in services) {
          services[name].postProcess(self.definitions);
        }
      }
      var complexTypes = self.definitions.complexTypes;
      if (complexTypes) {
        for (name in complexTypes) {
          complexTypes[name].deleteFixedAttrs();
        }
      }

      // for document style, for every binding, prepare input message element name to (methodName, output message element name)
mapping
      var bindings = self.definitions.bindings;
      for (var bindingName in bindings) {
        var binding = bindings[bindingName];
        if (typeof binding.style === 'undefined') {
          binding.style = 'document';
        }
        if (binding.style !== 'document')
          continue;
        var methods = binding.methods;
        var topEls = binding.topElements = {};
        for (var methodName in methods) {
          if (methods[methodName].input) {
            var inputName = methods[methodName].input.$name;
            var outputName="";
            if(methods[methodName].output )
              outputName = methods[methodName].output.$name;
            topEls[inputName] = {"methodName": methodName, "outputName": outputName};
          }
        }
      }

      // prepare soap envelope xmlns definition string
      self.xmlnsInEnvelope = self._xmlnsMap();

      self.callback(err, self);
    });

  });
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.soap.WSSecurity"></a>[function <span class="apidocSignatureSpan">soap.</span>WSSecurity (username, password, options)](#apidoc.element.soap.WSSecurity)
- description and source-code
```javascript
function WSSecurity(username, password, options) {
  options = options || {};
  this._username = username;
  this._password = password;
  //must account for backward compatibility for passwordType String param as well as object options defaults: passwordType = 'PasswordText
', hasTimeStamp = true
  if (typeof options === 'string') {
    this._passwordType = options ? options : 'PasswordText';
    options = {};
  } else {
    this._passwordType = options.passwordType ? options.passwordType : 'PasswordText';
  }

  if (validPasswordTypes.indexOf(this._passwordType) === -1) {
    this._passwordType = 'PasswordText';
  }

  this._hasTimeStamp = options.hasTimeStamp || typeof options.hasTimeStamp === 'boolean' ? !!options.hasTimeStamp : true;
  /*jshint eqnull:true */
  if (options.hasNonce != null) {
    this._hasNonce = !!options.hasNonce;
  }
  this._hasTokenCreated = options.hasTokenCreated || typeof options.hasTokenCreated === 'boolean' ? !!options.hasTokenCreated :
true;
  if (options.actor != null) {
    this._actor = options.actor;
  }
  if (options.mustUnderstand != null) {
    this._mustUnderstand = !!options.mustUnderstand;
  }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.soap.WSSecurityCert"></a>[function <span class="apidocSignatureSpan">soap.</span>WSSecurityCert (privatePEM, publicP12PEM, password, encoding)](#apidoc.element.soap.WSSecurityCert)
- description and source-code
```javascript
function WSSecurityCert(privatePEM, publicP12PEM, password, encoding) {
  if (!ursa) {
    throw new Error('Module ursa must be installed to use WSSecurityCert');
  }
  this.privateKey = ursa.createPrivateKey(privatePEM, password, encoding);
  this.publicP12PEM = publicP12PEM.toString().replace('-----BEGIN CERTIFICATE-----', '').replace('-----END CERTIFICATE-----', '').
replace(/(\r\n|\n|\r)/gm, '');

  this.signer = new SignedXml();
  this.signer.signingKey = this.privateKey.toPrivatePem();
  this.x509Id = "x509-" + generateId();

  var _this = this;
  this.signer.keyInfoProvider = {};
  this.signer.keyInfoProvider.getKeyInfo = function (key) {
    return wsseSecurityTokenTemplate({ x509Id: _this.x509Id });
  };
}
```
- example usage
```shell
...

WS-Security X509 Certificate support.

''' javascript
  var privateKey = fs.readFileSync(privateKeyPath);
  var publicKey = fs.readFileSync(publicKeyPath);
  var password = ''; // optional password
  var wsSecurity = new soap.WSSecurityCert(privateKey, publicKey, password, 'utf8');
  client.setSecurity(wsSecurity);
'''

_Note_: Optional dependency 'ursa' is required to be installed successfully when WSSecurityCert is used.

## Handling XML Attributes, Value and XML (wsdlOptions).
Sometimes it is necessary to override the default behaviour of 'node-soap' in order to deal with the special requirements
...
```

#### <a name="apidoc.element.soap.createClient"></a>[function <span class="apidocSignatureSpan">soap.</span>createClient (url, options, callback, endpoint)](#apidoc.element.soap.createClient)
- description and source-code
```javascript
function createClient(url, options, callback, endpoint) {
  if (typeof options === 'function') {
    endpoint = callback;
    callback = options;
    options = {};
  }
  endpoint = options.endpoint || endpoint;
  _requestWSDL(url, options, function(err, wsdl) {
    callback(err, wsdl && new Client(wsdl, endpoint, options));
  });
}
```
- example usage
```shell
...
<!-- DON'T EDIT THIS SECTION, INSTEAD RE-RUN doctoc TO UPDATE -->


- [Features:](#features)
- [Install](#install)
- [Where can I file an issue?](#where-can-i-file-an-issue)
- [Module](#module)
- [soap.createClient(url[, options], callback) - create a new SOAP client from a WSDL url. Also supports a local filesystem path
.](#soapcreateclienturl-options-callback---create-a-new-soap-client-from-a-wsdl-url-also-supports-a-local-filesystem-path)
- [soap.listen(*server*, *path*, *services*, *wsdl*) - create a new SOAP server that listens on *path* and provides *services*.](#
soaplistenserver-path-services-wsdl---create-a-new-soap-server-that-listens-on-path-and-provides-services)
- [Options](#options)
- [Server Logging](#server-logging)
- [Server Events](#server-events)
- [SOAP Fault](#soap-fault)
- [Server security example using PasswordDigest](#server-security-example-using-passworddigest)
- [Server connection authorization](#server-connection-authorization)
...
```

#### <a name="apidoc.element.soap.listen"></a>[function <span class="apidocSignatureSpan">soap.</span>listen (server, pathOrOptions, services, xml)](#apidoc.element.soap.listen)
- description and source-code
```javascript
function listen(server, pathOrOptions, services, xml) {
  var options = {},
    path = pathOrOptions,
    uri = null;

  if (typeof pathOrOptions === 'object') {
    options = pathOrOptions;
    path = options.path;
    services = options.services;
    xml = options.xml;
    uri = options.uri;
  }

  var wsdl = new WSDL(xml || services, uri, options);
  return new Server(server, path, services, wsdl, options);
}
```
- example usage
```shell
...


- [Features:](#features)
- [Install](#install)
- [Where can I file an issue?](#where-can-i-file-an-issue)
- [Module](#module)
  - [soap.createClient(url[, options], callback) - create a new SOAP client from a WSDL url. Also supports a local filesystem path
.](#soapcreateclienturl-options-callback---create-a-new-soap-client-from-a-wsdl-url-also-supports-a-local-filesystem-path)
  - [soap.listen(*server*, *path*, *services*, *wsdl*) - create a new SOAP server that listens on *path* and provides *services*.](#
soaplistenserver-path-services-wsdl---create-a-new-soap-server-that-listens-on-path-and-provides-services)
  - [Options](#options)
  - [Server Logging](#server-logging)
  - [Server Events](#server-events)
  - [SOAP Fault](#soap-fault)
  - [Server security example using PasswordDigest](#server-security-example-using-passworddigest)
  - [Server connection authorization](#server-connection-authorization)
- [SOAP Headers](#soap-headers)
...
```

#### <a name="apidoc.element.soap.nscontext"></a>[function <span class="apidocSignatureSpan">soap.</span>nscontext ()](#apidoc.element.soap.nscontext)
- description and source-code
```javascript
function NamespaceContext() {
  if (!(this instanceof NamespaceContext)) {
    return new NamespaceContext();
  }
  this.scopes = [];
  this.pushContext();
  this.prefixCount = 0;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.soap.passwordDigest"></a>[function <span class="apidocSignatureSpan">soap.</span>passwordDigest (nonce, created, password)](#apidoc.element.soap.passwordDigest)
- description and source-code
```javascript
function passwordDigest(nonce, created, password) {
  // digest = base64 ( sha1 ( nonce + created + password ) )
  var pwHash = crypto.createHash('sha1');
  var rawNonce = new Buffer(nonce || '', 'base64').toString('binary');
  pwHash.update(rawNonce + created + password);
  return pwHash.digest('base64');
}
```
- example usage
```shell
...

''' javascript
  server = soap.listen(...)
  server.authenticate = function(security) {
    var created, nonce, password, user, token;
    token = security.UsernameToken, user = token.Username,
            password = token.Password, nonce = token.Nonce, created = token.Created;
    return user === 'user' && password === soap.passwordDigest(nonce, created, 'password');
  };
'''

### Server connection authorization

The 'server.authorizeConnection' method is called prior to the soap service method.
If the method is defined and returns 'false' then the incoming connection is
...
```



# <a name="apidoc.module.soap.BasicAuthSecurity"></a>[module soap.BasicAuthSecurity](#apidoc.module.soap.BasicAuthSecurity)

#### <a name="apidoc.element.soap.BasicAuthSecurity.BasicAuthSecurity"></a>[function <span class="apidocSignatureSpan">soap.</span>BasicAuthSecurity (username, password, defaults)](#apidoc.element.soap.BasicAuthSecurity.BasicAuthSecurity)
- description and source-code
```javascript
function BasicAuthSecurity(username, password, defaults) {
  this._username = username;
  this._password = password;
  this.defaults = {};
  _.merge(this.defaults, defaults);
}
```
- example usage
```shell
...
as well.  The interface is quite simple. Each protocol defines 2 methods:
* 'addOptions' - a method that accepts an options arg that is eventually passed directly to 'request'
* 'toXML' - a method that returns a string of XML.

### BasicAuthSecurity

''' javascript
  client.setSecurity(new soap.BasicAuthSecurity('username', 'password'));
'''

### BearerSecurity

''' javascript
  client.setSecurity(new soap.BearerSecurity('token'));
'''
...
```



# <a name="apidoc.module.soap.BasicAuthSecurity.prototype"></a>[module soap.BasicAuthSecurity.prototype](#apidoc.module.soap.BasicAuthSecurity.prototype)

#### <a name="apidoc.element.soap.BasicAuthSecurity.prototype.addHeaders"></a>[function <span class="apidocSignatureSpan">soap.BasicAuthSecurity.prototype.</span>addHeaders (headers)](#apidoc.element.soap.BasicAuthSecurity.prototype.addHeaders)
- description and source-code
```javascript
addHeaders = function (headers) {
  headers.Authorization = 'Basic ' + new Buffer((this._username + ':' + this._password) || '').toString('base64');
}
```
- example usage
```shell
...

//Add extra headers
for (var header in this.httpHeaders ) { headers[header] = this.httpHeaders[header];  }
for (var attr in extraHeaders) { headers[attr] = extraHeaders[attr]; }

// Allow the security object to add headers
if (self.security && self.security.addHeaders)
  self.security.addHeaders(headers);
if (self.security && self.security.addOptions)
  self.security.addOptions(options);

if ((style === 'rpc')&& ( ( input.parts || input.name==="element" ) || args === null) ) {
  assert.ok(!style || style === 'rpc', 'invalid message definition for document style binding');
  message = self.wsdl.objectToRpcXML(name, args, alias, ns,(input.name!=="element" ));
  (method.inputSoap === 'encoded') && (encoding = 'soap:encodingStyle="http://schemas.xmlsoap.org/soap/encoding/" ');
...
```

#### <a name="apidoc.element.soap.BasicAuthSecurity.prototype.addOptions"></a>[function <span class="apidocSignatureSpan">soap.BasicAuthSecurity.prototype.</span>addOptions (options)](#apidoc.element.soap.BasicAuthSecurity.prototype.addOptions)
- description and source-code
```javascript
addOptions = function (options) {
  _.merge(options, this.defaults);
}
```
- example usage
```shell
...
for (var header in this.httpHeaders ) { headers[header] = this.httpHeaders[header];  }
for (var attr in extraHeaders) { headers[attr] = extraHeaders[attr]; }

// Allow the security object to add headers
if (self.security && self.security.addHeaders)
  self.security.addHeaders(headers);
if (self.security && self.security.addOptions)
  self.security.addOptions(options);

if ((style === 'rpc')&& ( ( input.parts || input.name==="element" ) || args === null) ) {
  assert.ok(!style || style === 'rpc', 'invalid message definition for document style binding');
  message = self.wsdl.objectToRpcXML(name, args, alias, ns,(input.name!=="element" ));
  (method.inputSoap === 'encoded') && (encoding = 'soap:encodingStyle="http://schemas.xmlsoap.org/soap/encoding/" ');
} else {
  assert.ok(!style || style === 'document', 'invalid message definition for rpc style binding');
...
```

#### <a name="apidoc.element.soap.BasicAuthSecurity.prototype.toXML"></a>[function <span class="apidocSignatureSpan">soap.BasicAuthSecurity.prototype.</span>toXML ()](#apidoc.element.soap.BasicAuthSecurity.prototype.toXML)
- description and source-code
```javascript
toXML = function () {
  return '';
}
```
- example usage
```shell
...
"xmlns:xsi=\"http://www.w3.org/2001/XMLSchema-instance\" " +
encoding +
this.wsdl.xmlnsInEnvelope + '>' +
((self.soapHeaders || self.security) ?
  (
    "<" + envelopeKey + ":Header>" +
    (self.soapHeaders ? self.soapHeaders.join("\n") : "") +
    (self.security && !self.security.postProcess ? self.security.toXML() : "") +
    "</" + envelopeKey + ":Header>"
  )
  :
    ''
  ) +
"<" + envelopeKey + ":Body" +
(self.bodyAttributes ? self.bodyAttributes.join(' ') : '') +
...
```



# <a name="apidoc.module.soap.BearerSecurity"></a>[module soap.BearerSecurity](#apidoc.module.soap.BearerSecurity)

#### <a name="apidoc.element.soap.BearerSecurity.BearerSecurity"></a>[function <span class="apidocSignatureSpan">soap.</span>BearerSecurity (token, defaults)](#apidoc.element.soap.BearerSecurity.BearerSecurity)
- description and source-code
```javascript
function BearerSecurity(token, defaults) {
	this._token = token;
	this.defaults = {};
	_.merge(this.defaults, defaults);
}
```
- example usage
```shell
...
''' javascript
  client.setSecurity(new soap.BasicAuthSecurity('username', 'password'));
'''

### BearerSecurity

''' javascript
  client.setSecurity(new soap.BearerSecurity('token'));
'''

### ClientSSLSecurity

_Note_: If you run into issues using this protocol, consider passing these options
as default request options to the constructor:
* 'rejectUnauthorized: false'
...
```



# <a name="apidoc.module.soap.BearerSecurity.prototype"></a>[module soap.BearerSecurity.prototype](#apidoc.module.soap.BearerSecurity.prototype)

#### <a name="apidoc.element.soap.BearerSecurity.prototype.addHeaders"></a>[function <span class="apidocSignatureSpan">soap.BearerSecurity.prototype.</span>addHeaders (headers)](#apidoc.element.soap.BearerSecurity.prototype.addHeaders)
- description and source-code
```javascript
addHeaders = function (headers) {
	headers.Authorization = "Bearer " + this._token;
}
```
- example usage
```shell
...

//Add extra headers
for (var header in this.httpHeaders ) { headers[header] = this.httpHeaders[header];  }
for (var attr in extraHeaders) { headers[attr] = extraHeaders[attr]; }

// Allow the security object to add headers
if (self.security && self.security.addHeaders)
  self.security.addHeaders(headers);
if (self.security && self.security.addOptions)
  self.security.addOptions(options);

if ((style === 'rpc')&& ( ( input.parts || input.name==="element" ) || args === null) ) {
  assert.ok(!style || style === 'rpc', 'invalid message definition for document style binding');
  message = self.wsdl.objectToRpcXML(name, args, alias, ns,(input.name!=="element" ));
  (method.inputSoap === 'encoded') && (encoding = 'soap:encodingStyle="http://schemas.xmlsoap.org/soap/encoding/" ');
...
```

#### <a name="apidoc.element.soap.BearerSecurity.prototype.addOptions"></a>[function <span class="apidocSignatureSpan">soap.BearerSecurity.prototype.</span>addOptions (options)](#apidoc.element.soap.BearerSecurity.prototype.addOptions)
- description and source-code
```javascript
addOptions = function (options) {
  _.merge(options, this.defaults);
}
```
- example usage
```shell
...
for (var header in this.httpHeaders ) { headers[header] = this.httpHeaders[header];  }
for (var attr in extraHeaders) { headers[attr] = extraHeaders[attr]; }

// Allow the security object to add headers
if (self.security && self.security.addHeaders)
  self.security.addHeaders(headers);
if (self.security && self.security.addOptions)
  self.security.addOptions(options);

if ((style === 'rpc')&& ( ( input.parts || input.name==="element" ) || args === null) ) {
  assert.ok(!style || style === 'rpc', 'invalid message definition for document style binding');
  message = self.wsdl.objectToRpcXML(name, args, alias, ns,(input.name!=="element" ));
  (method.inputSoap === 'encoded') && (encoding = 'soap:encodingStyle="http://schemas.xmlsoap.org/soap/encoding/" ');
} else {
  assert.ok(!style || style === 'document', 'invalid message definition for rpc style binding');
...
```

#### <a name="apidoc.element.soap.BearerSecurity.prototype.toXML"></a>[function <span class="apidocSignatureSpan">soap.BearerSecurity.prototype.</span>toXML ()](#apidoc.element.soap.BearerSecurity.prototype.toXML)
- description and source-code
```javascript
toXML = function () {
	return '';
}
```
- example usage
```shell
...
"xmlns:xsi=\"http://www.w3.org/2001/XMLSchema-instance\" " +
encoding +
this.wsdl.xmlnsInEnvelope + '>' +
((self.soapHeaders || self.security) ?
  (
    "<" + envelopeKey + ":Header>" +
    (self.soapHeaders ? self.soapHeaders.join("\n") : "") +
    (self.security && !self.security.postProcess ? self.security.toXML() : "") +
    "</" + envelopeKey + ":Header>"
  )
  :
    ''
  ) +
"<" + envelopeKey + ":Body" +
(self.bodyAttributes ? self.bodyAttributes.join(' ') : '') +
...
```



# <a name="apidoc.module.soap.Client"></a>[module soap.Client](#apidoc.module.soap.Client)

#### <a name="apidoc.element.soap.Client.Client"></a>[function <span class="apidocSignatureSpan">soap.</span>Client (wsdl, endpoint, options)](#apidoc.element.soap.Client.Client)
- description and source-code
```javascript
Client = function (wsdl, endpoint, options) {
  events.EventEmitter.call(this);
  options = options || {};
  this.wsdl = wsdl;
  this._initializeOptions(options);
  this._initializeServices(endpoint);
  this.httpClient = options.httpClient || new HttpClient(options);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.soap.Client.super_"></a>[function <span class="apidocSignatureSpan">soap.Client.</span>super_ ()](#apidoc.element.soap.Client.super_)
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



# <a name="apidoc.module.soap.Client.prototype"></a>[module soap.Client.prototype](#apidoc.module.soap.Client.prototype)

#### <a name="apidoc.element.soap.Client.prototype._defineMethod"></a>[function <span class="apidocSignatureSpan">soap.Client.prototype.</span>_defineMethod (method, location)](#apidoc.element.soap.Client.prototype._defineMethod)
- description and source-code
```javascript
_defineMethod = function (method, location) {
  var self = this;
  var temp;
  return function(args, callback, options, extraHeaders) {
    if (typeof args === 'function') {
      callback = args;
      args = {};
    } else if (typeof options === 'function') {
      temp = callback;
      callback = options;
      options = temp;
    } else if (typeof extraHeaders === 'function') {
      temp = callback;
      callback = extraHeaders;
      extraHeaders = options;
      options = temp;
    }
    self._invoke(method, args, location, function(error, result, raw, soapHeader) {
      callback(error, result, raw, soapHeader);
    }, options, extraHeaders);
  };
}
```
- example usage
```shell
...

Client.prototype._definePort = function(port, endpoint) {
var location = endpoint,
  binding = port.binding,
  methods = binding.methods,
  def = {};
for (var name in methods) {
  def[name] = this._defineMethod(methods[name], location);
  this[name] = def[name];
}
return def;
};

Client.prototype._defineMethod = function(method, location) {
var self = this;
...
```

#### <a name="apidoc.element.soap.Client.prototype._definePort"></a>[function <span class="apidocSignatureSpan">soap.Client.prototype.</span>_definePort (port, endpoint)](#apidoc.element.soap.Client.prototype._definePort)
- description and source-code
```javascript
_definePort = function (port, endpoint) {
  var location = endpoint,
    binding = port.binding,
    methods = binding.methods,
    def = {};
  for (var name in methods) {
    def[name] = this._defineMethod(methods[name], location);
    this[name] = def[name];
  }
  return def;
}
```
- example usage
```shell
...
this.wsdl.options.forceSoap12Headers = !!options.forceSoap12Headers;
};

Client.prototype._defineService = function(service, endpoint) {
var ports = service.ports,
  def = {};
for (var name in ports) {
  def[name] = this._definePort(ports[name], endpoint ? endpoint : ports[name].location);
}
return def;
};

Client.prototype._definePort = function(port, endpoint) {
var location = endpoint,
  binding = port.binding,
...
```

#### <a name="apidoc.element.soap.Client.prototype._defineService"></a>[function <span class="apidocSignatureSpan">soap.Client.prototype.</span>_defineService (service, endpoint)](#apidoc.element.soap.Client.prototype._defineService)
- description and source-code
```javascript
_defineService = function (service, endpoint) {
  var ports = service.ports,
    def = {};
  for (var name in ports) {
    def[name] = this._definePort(ports[name], endpoint ? endpoint : ports[name].location);
  }
  return def;
}
```
- example usage
```shell
...
this.SOAPAction = SOAPAction;
};

Client.prototype._initializeServices = function(endpoint) {
var definitions = this.wsdl.definitions,
  services = definitions.services;
for (var name in services) {
  this[name] = this._defineService(services[name], endpoint);
}
};

Client.prototype._initializeOptions = function(options) {
this.streamAllowed = options.stream;
this.wsdl.options.attributesKey = options.attributesKey || 'attributes';
this.wsdl.options.envelopeKey = options.envelopeKey || 'soap';
...
```

#### <a name="apidoc.element.soap.Client.prototype._getArgsScheme"></a>[function <span class="apidocSignatureSpan">soap.Client.prototype.</span>_getArgsScheme (methodName)](#apidoc.element.soap.Client.prototype._getArgsScheme)
- description and source-code
```javascript
_getArgsScheme = function (methodName) {
  var methodRequestName = _.result(this.wsdl.definitions, 'messages.'+methodName+'.$name');
  var args = _.result(this.wsdl.definitions, 'messages.' + methodRequestName + '.parts');

  if(typeof args === 'undefined' && typeof _.pick(args, 'params') !== 'undefined') {
    return [];
  }
  if(Object.keys(args).length === 1) {
    return [];
  }

  return args;
}
```
- example usage
```shell
...
  alias = findPrefix(defs.xmlns, ns),
  headers = {
    "Content-Type": "text/xml; charset=utf-8"
  },
  xmlnsSoap = "xmlns:" + envelopeKey + "=\"http://schemas.xmlsoap.org/soap/envelope/\"";

if(this._isSequenceRequired(name)) {
  var argsScheme = this._getArgsScheme(name);
  if(argsScheme) {
    args = this._setSequenceArgs(argsScheme, args);
  }
}

if (this.wsdl.options.forceSoap12Headers) {
  headers["Content-Type"] = "application/soap+xml; charset=utf-8";
...
```

#### <a name="apidoc.element.soap.Client.prototype._initializeOptions"></a>[function <span class="apidocSignatureSpan">soap.Client.prototype.</span>_initializeOptions (options)](#apidoc.element.soap.Client.prototype._initializeOptions)
- description and source-code
```javascript
_initializeOptions = function (options) {
  this.streamAllowed = options.stream;
  this.wsdl.options.attributesKey = options.attributesKey || 'attributes';
  this.wsdl.options.envelopeKey = options.envelopeKey || 'soap';
  if(options.ignoredNamespaces !== undefined) {
    if(options.ignoredNamespaces.override !== undefined) {
      if(options.ignoredNamespaces.override === true) {
        if(options.ignoredNamespaces.namespaces !== undefined) {
          this.wsdl.options.ignoredNamespaces = options.ignoredNamespaces.namespaces;
        }
      }
    }
  }
  if(options.overrideRootElement !== undefined) {
    this.wsdl.options.overrideRootElement = options.overrideRootElement;
  }
  this.wsdl.options.forceSoap12Headers = !!options.forceSoap12Headers;
}
```
- example usage
```shell
...
concatStream = require('concat-stream'),
uuid = require('uuid');

var Client = function(wsdl, endpoint, options) {
events.EventEmitter.call(this);
options = options || {};
this.wsdl = wsdl;
this._initializeOptions(options);
this._initializeServices(endpoint);
this.httpClient = options.httpClient || new HttpClient(options);
};
util.inherits(Client, events.EventEmitter);

Client.prototype.addSoapHeader = function(soapHeader, name, namespace, xmlns) {
if (!this.soapHeaders) {
...
```

#### <a name="apidoc.element.soap.Client.prototype._initializeServices"></a>[function <span class="apidocSignatureSpan">soap.Client.prototype.</span>_initializeServices (endpoint)](#apidoc.element.soap.Client.prototype._initializeServices)
- description and source-code
```javascript
_initializeServices = function (endpoint) {
  var definitions = this.wsdl.definitions,
    services = definitions.services;
  for (var name in services) {
    this[name] = this._defineService(services[name], endpoint);
  }
}
```
- example usage
```shell
...
uuid = require('uuid');

var Client = function(wsdl, endpoint, options) {
events.EventEmitter.call(this);
options = options || {};
this.wsdl = wsdl;
this._initializeOptions(options);
this._initializeServices(endpoint);
this.httpClient = options.httpClient || new HttpClient(options);
};
util.inherits(Client, events.EventEmitter);

Client.prototype.addSoapHeader = function(soapHeader, name, namespace, xmlns) {
if (!this.soapHeaders) {
  this.soapHeaders = [];
...
```

#### <a name="apidoc.element.soap.Client.prototype._invoke"></a>[function <span class="apidocSignatureSpan">soap.Client.prototype.</span>_invoke (method, args, location, callback, options, extraHeaders)](#apidoc.element.soap.Client.prototype._invoke)
- description and source-code
```javascript
_invoke = function (method, args, location, callback, options, extraHeaders) {
  var self = this,
    name = method.$name,
    input = method.input,
    output = method.output,
    style = method.style,
    defs = this.wsdl.definitions,
    envelopeKey = this.wsdl.options.envelopeKey,
    ns = defs.$targetNamespace,
    encoding = '',
    message = '',
    xml = null,
    req = null,
    soapAction,
    alias = findPrefix(defs.xmlns, ns),
    headers = {
      "Content-Type": "text/xml; charset=utf-8"
    },
    xmlnsSoap = "xmlns:" + envelopeKey + "=\"http://schemas.xmlsoap.org/soap/envelope/\"";

  if(this._isSequenceRequired(name)) {
    var argsScheme = this._getArgsScheme(name);
    if(argsScheme) {
      args = this._setSequenceArgs(argsScheme, args);
    }
  }

  if (this.wsdl.options.forceSoap12Headers) {
    headers["Content-Type"] = "application/soap+xml; charset=utf-8";
    xmlnsSoap = "xmlns:" + envelopeKey + "=\"http://www.w3.org/2003/05/soap-envelope\"";
  }

  if (this.SOAPAction) {
    soapAction = this.SOAPAction;
  } else if (method.soapAction !== undefined && method.soapAction !== null) {
    soapAction = method.soapAction;
  } else {
    soapAction = ((ns.lastIndexOf("/") !== ns.length - 1) ? ns + "/" : ns) + name;
  }

  if (!this.wsdl.options.forceSoap12Headers) {
    headers.SOAPAction = '"' + soapAction + '"';
  }

  options = options || {};

  //Add extra headers
  for (var header in this.httpHeaders ) { headers[header] = this.httpHeaders[header];  }
  for (var attr in extraHeaders) { headers[attr] = extraHeaders[attr]; }

  // Allow the security object to add headers
  if (self.security && self.security.addHeaders)
    self.security.addHeaders(headers);
  if (self.security && self.security.addOptions)
    self.security.addOptions(options);

  if ((style === 'rpc')&& ( ( input.parts || input.name==="element" ) || args === null) ) {
    assert.ok(!style || style === 'rpc', 'invalid message definition for document style binding');
    message = self.wsdl.objectToRpcXML(name, args, alias, ns,(input.name!=="element" ));
    (method.inputSoap === 'encoded') && (encoding = 'soap:encodingStyle="http://schemas.xmlsoap.org/soap/encoding/" ');
  } else {
    assert.ok(!style || style === 'document', 'invalid message definition for rpc style binding');
    // pass 'input.$lookupType' if 'input.$type' could not be found
    message = self.wsdl.objectToDocumentXML(input.$name, args, input.targetNSAlias, input.targetNamespace, (input.$type || input
.$lookupType));
  }
  xml = "<?xml version=\"1.0\" encoding=\"utf-8\"?>" +
    "<" + envelopeKey + ":Envelope " +
    xmlnsSoap + " " +
    "xmlns:xsi=\"http://www.w3.org/2001/XMLSchema-instance\" " +
    encoding +
    this.wsdl.xmlnsInEnvelope + '>' +
    ((self.soapHeaders || self.security) ?
      (
        "<" + envelopeKey + ":Header>" +
        (self.soapHeaders ? self.soapHeaders.join("\n") : "") +
        (self.security && !self.security.postProcess ? self.security.toXML() : "") +
        "</" + envelopeKey + ":Header>"
      )
      :
        ''
      ) +
    "<" + envelopeKey + ":Body" +
    (self.bodyAttributes ? self.bodyAttributes.join(' ') : '') +
    (self.security && self.security.postProcess ? ' Id="_0"' : '') +
    ">" +
    message +
    "</" + envelopeKey + ":Body>" +
    "</" + envelopeKey + ":Envelope>";

  if(self.security && self.security.postProcess){
    xml = self.security.postProcess(xml, envelopeKey);
  }

  self.lastMessage = message;
  self.lastRequest = xml;
  self.lastEndpoint = location;

  var eid = options.exchangeId || uuid.v4();

  self.emit('message', message, eid);
  self.emit('request', xml, eid);

  var tryJSONparse = function(body) {
    try {
      return JSON.parse(body);
    }
    catch(err) {
      return undefined;
    }
  };

  if (this.streamAllowed && typeof self.httpClient.requestStream === 'function') {
    callback = _.once(callback);
    var startTime = Date.now();
    req = self.httpClient.requestStream(locat ...
```
- example usage
```shell
...
    options = temp;
  } else if (typeof extraHeaders === 'function') {
    temp = callback;
    callback = extraHeaders;
    extraHeaders = options;
    options = temp;
  }
  self._invoke(method, args, location, function(error, result, raw, soapHeader) {
    callback(error, result, raw, soapHeader);
  }, options, extraHeaders);
};
};

Client.prototype._isSequenceRequired = function(methodName) {
var tns = this.wsdl.definitions.$targetNamespace;
...
```

#### <a name="apidoc.element.soap.Client.prototype._isSequenceRequired"></a>[function <span class="apidocSignatureSpan">soap.Client.prototype.</span>_isSequenceRequired (methodName)](#apidoc.element.soap.Client.prototype._isSequenceRequired)
- description and source-code
```javascript
_isSequenceRequired = function (methodName) {
  var tns = this.wsdl.definitions.$targetNamespace;
  var methodRequestName = _.result(this.wsdl.definitions, 'messages.' + methodName + '.$name');
  var args = _.result(this.wsdl.definitions, 'messages.' + methodRequestName + '.parts');

  if(typeof args === 'undefined' && typeof _.pick(args, 'params') !== 'undefined') {
    return false;
  }
  if(Object.keys(args).length === 1) {
    return false;
  }

  var complexTypeName = _.result(this.wsdl.definitions, 'messages.' + methodRequestName + '.element.$name');
  var modeOfComplexType = _.result(
    this.wsdl.definitions,
    'schemas[\'' + tns + '\'].elements.' + complexTypeName + '.children[0].children[0].name');

  if(modeOfComplexType === 'sequence') {
    return true;
  }

  return false;
}
```
- example usage
```shell
...
  soapAction,
  alias = findPrefix(defs.xmlns, ns),
  headers = {
    "Content-Type": "text/xml; charset=utf-8"
  },
  xmlnsSoap = "xmlns:" + envelopeKey + "=\"http://schemas.xmlsoap.org/soap/envelope/\"";

if(this._isSequenceRequired(name)) {
  var argsScheme = this._getArgsScheme(name);
  if(argsScheme) {
    args = this._setSequenceArgs(argsScheme, args);
  }
}

if (this.wsdl.options.forceSoap12Headers) {
...
```

#### <a name="apidoc.element.soap.Client.prototype._setSequenceArgs"></a>[function <span class="apidocSignatureSpan">soap.Client.prototype.</span>_setSequenceArgs (argsScheme, args)](#apidoc.element.soap.Client.prototype._setSequenceArgs)
- description and source-code
```javascript
_setSequenceArgs = function (argsScheme, args) {
  var result = {};
  if(typeof argsScheme !== 'object') {
    return args;
  }
  for (var partIndex in argsScheme) {
    if(typeof args[partIndex] === 'undefined') {
      continue;
    }
    if(typeof argsScheme[partIndex] !== 'object') {
      result[partIndex] = args[partIndex];
    } else {
      result[partIndex] = this._setSequenceArgs(argsScheme[partIndex], args[partIndex]);
    }
  }
  return result;
}
```
- example usage
```shell
...
for (var partIndex in argsScheme) {
  if(typeof args[partIndex] === 'undefined') {
    continue;
  }
  if(typeof argsScheme[partIndex] !== 'object') {
    result[partIndex] = args[partIndex];
  } else {
    result[partIndex] = this._setSequenceArgs(argsScheme[partIndex], args[partIndex]);
  }
}
return result;
};

Client.prototype._getArgsScheme = function(methodName) {
var methodRequestName = _.result(this.wsdl.definitions, 'messages.'+methodName+'.$name');
...
```

#### <a name="apidoc.element.soap.Client.prototype.addBodyAttribute"></a>[function <span class="apidocSignatureSpan">soap.Client.prototype.</span>addBodyAttribute (bodyAttribute, name, namespace, xmlns)](#apidoc.element.soap.Client.prototype.addBodyAttribute)
- description and source-code
```javascript
addBodyAttribute = function (bodyAttribute, name, namespace, xmlns) {
  if (!this.bodyAttributes) {
    this.bodyAttributes = [];
  }
  if (typeof bodyAttribute === 'object') {
    var composition = '';
    Object.getOwnPropertyNames(bodyAttribute).forEach(function(prop, idx, array) {
      composition += ' ' + prop + '="' + bodyAttribute[prop] + '"';
    });
    bodyAttribute = composition;
  }
  if (bodyAttribute.substr(0, 1) !== ' ') bodyAttribute = ' ' + bodyAttribute;
  this.bodyAttributes.push(bodyAttribute);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.soap.Client.prototype.addHttpHeader"></a>[function <span class="apidocSignatureSpan">soap.Client.prototype.</span>addHttpHeader (name, value)](#apidoc.element.soap.Client.prototype.addHttpHeader)
- description and source-code
```javascript
addHttpHeader = function (name, value) {
  if (!this.httpHeaders) {
    this.httpHeaders = {};
  }
  this.httpHeaders[name] = value;
}
```
- example usage
```shell
...

#### Extra Headers (optional)

Object properties define extra HTTP headers to be sent on the request.

- Add custom User-Agent:
'''javascript
client.addHttpHeader('User-Agent', 'CustomUserAgent');
'''

#### Alternative method call using callback-last pattern

To align method call signature with node' standard callback-last patter and event allow promisification of method calls, the following
 method signatures are also supported:

'''javascript
...
```

#### <a name="apidoc.element.soap.Client.prototype.addSoapHeader"></a>[function <span class="apidocSignatureSpan">soap.Client.prototype.</span>addSoapHeader (soapHeader, name, namespace, xmlns)](#apidoc.element.soap.Client.prototype.addSoapHeader)
- description and source-code
```javascript
addSoapHeader = function (soapHeader, name, namespace, xmlns) {
  if (!this.soapHeaders) {
    this.soapHeaders = [];
  }
  if (typeof soapHeader === 'object') {
    soapHeader = this.wsdl.objectToXML(soapHeader, name, namespace, xmlns, true);
  }
  return this.soapHeaders.push(soapHeader) - 1;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.soap.Client.prototype.changeSoapHeader"></a>[function <span class="apidocSignatureSpan">soap.Client.prototype.</span>changeSoapHeader (index, soapHeader, name, namespace, xmlns)](#apidoc.element.soap.Client.prototype.changeSoapHeader)
- description and source-code
```javascript
changeSoapHeader = function (index, soapHeader, name, namespace, xmlns) {
  if (!this.soapHeaders) {
    this.soapHeaders = [];
  }
  if (typeof soapHeader === 'object') {
    soapHeader = this.wsdl.objectToXML(soapHeader, name, namespace, xmlns, true);
  }
  this.soapHeaders[index] = soapHeader;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.soap.Client.prototype.clearBodyAttributes"></a>[function <span class="apidocSignatureSpan">soap.Client.prototype.</span>clearBodyAttributes ()](#apidoc.element.soap.Client.prototype.clearBodyAttributes)
- description and source-code
```javascript
clearBodyAttributes = function () {
  this.bodyAttributes = null;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.soap.Client.prototype.clearHttpHeaders"></a>[function <span class="apidocSignatureSpan">soap.Client.prototype.</span>clearHttpHeaders ()](#apidoc.element.soap.Client.prototype.clearHttpHeaders)
- description and source-code
```javascript
clearHttpHeaders = function () {
  this.httpHeaders = {};
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.soap.Client.prototype.clearSoapHeaders"></a>[function <span class="apidocSignatureSpan">soap.Client.prototype.</span>clearSoapHeaders ()](#apidoc.element.soap.Client.prototype.clearSoapHeaders)
- description and source-code
```javascript
clearSoapHeaders = function () {
  this.soapHeaders = null;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.soap.Client.prototype.describe"></a>[function <span class="apidocSignatureSpan">soap.Client.prototype.</span>describe ()](#apidoc.element.soap.Client.prototype.describe)
- description and source-code
```javascript
describe = function () {
  var types = this.wsdl.definitions.types;
  return this.wsdl.describeServices();
}
```
- example usage
```shell
...
  - [SOAP Fault](#soap-fault)
  - [Server security example using PasswordDigest](#server-security-example-using-passworddigest)
  - [Server connection authorization](#server-connection-authorization)
- [SOAP Headers](#soap-headers)
  - [Received SOAP Headers](#received-soap-headers)
  - [Outgoing SOAP Headers](#outgoing-soap-headers)
- [Client](#client)
  - [Client.describe() - description of services, ports and methods as a JavaScript object](#clientdescribe---description-of-services
-ports-and-methods-as-a-javascript-object)
  - [Client.setSecurity(security) - use the specified security protocol](#clientsetsecuritysecurity---use-the-specified-security
-protocol)
  - [Client.*method*(args, callback) - call *method* on the SOAP service.](#clientmethodargs-callback---call-method-on-the-soap-
service)
  - [Client.*service*.*port*.*method*(args, callback[, options[, extraHeaders]]) - call a *method* using a specific *service* and
 *port*](#clientserviceportmethodargs-callback-options-extraheaders---call-a-method-using-a-specific-service-and-port)
  - [Client.*lastRequest* - the property that contains last full soap request for client logging](#clientlastrequest---the-property
-that-contains-last-full-soap-request-for-client-logging)
  - [Client.setEndpoint(url) - overwrite the SOAP service endpoint address](#clientsetendpointurl---overwrite-the-soap-service-endpoint
-address)
  - [Client Events](#client-events)
- [Security](#security)
...
```

#### <a name="apidoc.element.soap.Client.prototype.getBodyAttributes"></a>[function <span class="apidocSignatureSpan">soap.Client.prototype.</span>getBodyAttributes ()](#apidoc.element.soap.Client.prototype.getBodyAttributes)
- description and source-code
```javascript
getBodyAttributes = function () {
  return this.bodyAttributes;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.soap.Client.prototype.getHttpHeaders"></a>[function <span class="apidocSignatureSpan">soap.Client.prototype.</span>getHttpHeaders ()](#apidoc.element.soap.Client.prototype.getHttpHeaders)
- description and source-code
```javascript
getHttpHeaders = function () {
  return this.httpHeaders;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.soap.Client.prototype.getSoapHeaders"></a>[function <span class="apidocSignatureSpan">soap.Client.prototype.</span>getSoapHeaders ()](#apidoc.element.soap.Client.prototype.getSoapHeaders)
- description and source-code
```javascript
getSoapHeaders = function () {
  return this.soapHeaders;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.soap.Client.prototype.setEndpoint"></a>[function <span class="apidocSignatureSpan">soap.Client.prototype.</span>setEndpoint (endpoint)](#apidoc.element.soap.Client.prototype.setEndpoint)
- description and source-code
```javascript
setEndpoint = function (endpoint) {
  this.endpoint = endpoint;
  this._initializeServices(endpoint);
}
```
- example usage
```shell
...
- [Outgoing SOAP Headers](#outgoing-soap-headers)
- [Client](#client)
- [Client.describe() - description of services, ports and methods as a JavaScript object](#clientdescribe---description-of-services
-ports-and-methods-as-a-javascript-object)
- [Client.setSecurity(security) - use the specified security protocol](#clientsetsecuritysecurity---use-the-specified-security-protocol
)
- [Client.*method*(args, callback) - call *method* on the SOAP service.](#clientmethodargs-callback---call-method-on-the-soap-service
)
- [Client.*service*.*port*.*method*(args, callback[, options[, extraHeaders]]) - call a *method* using a specific *service* and *
port*](#clientserviceportmethodargs-callback-options-extraheaders---call-a-method-using-a-specific-service-and-port)
- [Client.*lastRequest* - the property that contains last full soap request for client logging](#clientlastrequest---the-property
-that-contains-last-full-soap-request-for-client-logging)
- [Client.setEndpoint(url) - overwrite the SOAP service endpoint address](#clientsetendpointurl---overwrite-the-soap-service-endpoint
-address)
- [Client Events](#client-events)
- [Security](#security)
- [BasicAuthSecurity](#basicauthsecurity)
- [BearerSecurity](#bearersecurity)
- [ClientSSLSecurity](#clientsslsecurity)
- [WSSecurity](#wssecurity)
- [WSSecurityCert](#wssecuritycert)
...
```

#### <a name="apidoc.element.soap.Client.prototype.setSOAPAction"></a>[function <span class="apidocSignatureSpan">soap.Client.prototype.</span>setSOAPAction (SOAPAction)](#apidoc.element.soap.Client.prototype.setSOAPAction)
- description and source-code
```javascript
setSOAPAction = function (SOAPAction) {
  this.SOAPAction = SOAPAction;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.soap.Client.prototype.setSecurity"></a>[function <span class="apidocSignatureSpan">soap.Client.prototype.</span>setSecurity (security)](#apidoc.element.soap.Client.prototype.setSecurity)
- description and source-code
```javascript
setSecurity = function (security) {
  this.security = security;
}
```
- example usage
```shell
...
- [Server security example using PasswordDigest](#server-security-example-using-passworddigest)
- [Server connection authorization](#server-connection-authorization)
- [SOAP Headers](#soap-headers)
- [Received SOAP Headers](#received-soap-headers)
- [Outgoing SOAP Headers](#outgoing-soap-headers)
- [Client](#client)
- [Client.describe() - description of services, ports and methods as a JavaScript object](#clientdescribe---description-of-services
-ports-and-methods-as-a-javascript-object)
- [Client.setSecurity(security) - use the specified security protocol](#clientsetsecuritysecurity---use-the-specified-security-protocol
)
- [Client.*method*(args, callback) - call *method* on the SOAP service.](#clientmethodargs-callback---call-method-on-the-soap-service
)
- [Client.*service*.*port*.*method*(args, callback[, options[, extraHeaders]]) - call a *method* using a specific *service* and *
port*](#clientserviceportmethodargs-callback-options-extraheaders---call-a-method-using-a-specific-service-and-port)
- [Client.*lastRequest* - the property that contains last full soap request for client logging](#clientlastrequest---the-property
-that-contains-last-full-soap-request-for-client-logging)
- [Client.setEndpoint(url) - overwrite the SOAP service endpoint address](#clientsetendpointurl---overwrite-the-soap-service-endpoint
-address)
- [Client Events](#client-events)
- [Security](#security)
- [BasicAuthSecurity](#basicauthsecurity)
...
```



# <a name="apidoc.module.soap.ClientSSLSecurity"></a>[module soap.ClientSSLSecurity](#apidoc.module.soap.ClientSSLSecurity)

#### <a name="apidoc.element.soap.ClientSSLSecurity.ClientSSLSecurity"></a>[function <span class="apidocSignatureSpan">soap.</span>ClientSSLSecurity (key, cert, ca, defaults)](#apidoc.element.soap.ClientSSLSecurity.ClientSSLSecurity)
- description and source-code
```javascript
function ClientSSLSecurity(key, cert, ca, defaults) {
  if (key) {
    if(Buffer.isBuffer(key)) {
      this.key = key;
    } else if (typeof key === 'string') {
      this.key = fs.readFileSync(key);
    } else {
      throw new Error('key should be a buffer or a string!');
    }
  }

  if (cert) {
    if(Buffer.isBuffer(cert)) {
      this.cert = cert;
    } else if (typeof cert === 'string') {
      this.cert = fs.readFileSync(cert);
    } else {
      throw new Error('cert should be a buffer or a string!');
    }
  }

  if (ca) {
    if(Buffer.isBuffer(ca) || Array.isArray(ca)) {
      this.ca = ca;
    } else if (typeof ca === 'string') {
      this.ca = fs.readFileSync(ca);
    } else {
      defaults = ca;
      this.ca = null;
    }
  }

  this.defaults = {};
  _.merge(this.defaults, defaults);
}
```
- example usage
```shell
...
_Note_: If you run into issues using this protocol, consider passing these options
as default request options to the constructor:
* 'rejectUnauthorized: false'
* 'strictSSL: false'
* 'secureOptions: constants.SSL_OP_NO_TLSv1_2' (this is likely needed for node >= 10.0)

''' javascript
  client.setSecurity(new soap.ClientSSLSecurity(
    '/path/to/key'
    , '/path/to/cert'
    , {/*default request options*/}
  ));
'''

### WSSecurity
...
```



# <a name="apidoc.module.soap.ClientSSLSecurity.prototype"></a>[module soap.ClientSSLSecurity.prototype](#apidoc.module.soap.ClientSSLSecurity.prototype)

#### <a name="apidoc.element.soap.ClientSSLSecurity.prototype.addOptions"></a>[function <span class="apidocSignatureSpan">soap.ClientSSLSecurity.prototype.</span>addOptions (options)](#apidoc.element.soap.ClientSSLSecurity.prototype.addOptions)
- description and source-code
```javascript
addOptions = function (options) {
  options.key = this.key;
  options.cert = this.cert;
  options.ca = this.ca;
  _.merge(options, this.defaults);
  options.agent = new https.Agent(options);
}
```
- example usage
```shell
...
for (var header in this.httpHeaders ) { headers[header] = this.httpHeaders[header];  }
for (var attr in extraHeaders) { headers[attr] = extraHeaders[attr]; }

// Allow the security object to add headers
if (self.security && self.security.addHeaders)
  self.security.addHeaders(headers);
if (self.security && self.security.addOptions)
  self.security.addOptions(options);

if ((style === 'rpc')&& ( ( input.parts || input.name==="element" ) || args === null) ) {
  assert.ok(!style || style === 'rpc', 'invalid message definition for document style binding');
  message = self.wsdl.objectToRpcXML(name, args, alias, ns,(input.name!=="element" ));
  (method.inputSoap === 'encoded') && (encoding = 'soap:encodingStyle="http://schemas.xmlsoap.org/soap/encoding/" ');
} else {
  assert.ok(!style || style === 'document', 'invalid message definition for rpc style binding');
...
```

#### <a name="apidoc.element.soap.ClientSSLSecurity.prototype.toXML"></a>[function <span class="apidocSignatureSpan">soap.ClientSSLSecurity.prototype.</span>toXML (headers)](#apidoc.element.soap.ClientSSLSecurity.prototype.toXML)
- description and source-code
```javascript
toXML = function (headers) {
  return '';
}
```
- example usage
```shell
...
"xmlns:xsi=\"http://www.w3.org/2001/XMLSchema-instance\" " +
encoding +
this.wsdl.xmlnsInEnvelope + '>' +
((self.soapHeaders || self.security) ?
  (
    "<" + envelopeKey + ":Header>" +
    (self.soapHeaders ? self.soapHeaders.join("\n") : "") +
    (self.security && !self.security.postProcess ? self.security.toXML() : "") +
    "</" + envelopeKey + ":Header>"
  )
  :
    ''
  ) +
"<" + envelopeKey + ":Body" +
(self.bodyAttributes ? self.bodyAttributes.join(' ') : '') +
...
```



# <a name="apidoc.module.soap.ClientSSLSecurityPFX"></a>[module soap.ClientSSLSecurityPFX](#apidoc.module.soap.ClientSSLSecurityPFX)

#### <a name="apidoc.element.soap.ClientSSLSecurityPFX.ClientSSLSecurityPFX"></a>[function <span class="apidocSignatureSpan">soap.</span>ClientSSLSecurityPFX (pfx, passphrase, defaults)](#apidoc.element.soap.ClientSSLSecurityPFX.ClientSSLSecurityPFX)
- description and source-code
```javascript
function ClientSSLSecurityPFX(pfx, passphrase, defaults) {
  if (typeof passphrase === 'object') {
    defaults = passphrase;
  }
  if (pfx) {
    if (Buffer.isBuffer(pfx)) {
      this.pfx = pfx;
    } else if (typeof pfx === 'string') {
      this.pfx = fs.readFileSync(pfx);
    } else {
      throw new Error('supplied pfx file should be a buffer or a file location');
    }
  }

  if (passphrase) {
    if (typeof passphrase === 'string') {
      this.passphrase = passphrase;
    }
  }
  this.defaults = {};
  _.merge(this.defaults, defaults);
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.soap.ClientSSLSecurityPFX.prototype"></a>[module soap.ClientSSLSecurityPFX.prototype](#apidoc.module.soap.ClientSSLSecurityPFX.prototype)

#### <a name="apidoc.element.soap.ClientSSLSecurityPFX.prototype.addOptions"></a>[function <span class="apidocSignatureSpan">soap.ClientSSLSecurityPFX.prototype.</span>addOptions (options)](#apidoc.element.soap.ClientSSLSecurityPFX.prototype.addOptions)
- description and source-code
```javascript
addOptions = function (options) {
  options.pfx = this.pfx;
  if (this.passphrase) {
    options.passphrase = this.passphrase;
  }
  _.merge(options, this.defaults);
  options.agent = new https.Agent(options);
}
```
- example usage
```shell
...
for (var header in this.httpHeaders ) { headers[header] = this.httpHeaders[header];  }
for (var attr in extraHeaders) { headers[attr] = extraHeaders[attr]; }

// Allow the security object to add headers
if (self.security && self.security.addHeaders)
  self.security.addHeaders(headers);
if (self.security && self.security.addOptions)
  self.security.addOptions(options);

if ((style === 'rpc')&& ( ( input.parts || input.name==="element" ) || args === null) ) {
  assert.ok(!style || style === 'rpc', 'invalid message definition for document style binding');
  message = self.wsdl.objectToRpcXML(name, args, alias, ns,(input.name!=="element" ));
  (method.inputSoap === 'encoded') && (encoding = 'soap:encodingStyle="http://schemas.xmlsoap.org/soap/encoding/" ');
} else {
  assert.ok(!style || style === 'document', 'invalid message definition for rpc style binding');
...
```

#### <a name="apidoc.element.soap.ClientSSLSecurityPFX.prototype.toXML"></a>[function <span class="apidocSignatureSpan">soap.ClientSSLSecurityPFX.prototype.</span>toXML (headers)](#apidoc.element.soap.ClientSSLSecurityPFX.prototype.toXML)
- description and source-code
```javascript
toXML = function (headers) {
  return '';
}
```
- example usage
```shell
...
"xmlns:xsi=\"http://www.w3.org/2001/XMLSchema-instance\" " +
encoding +
this.wsdl.xmlnsInEnvelope + '>' +
((self.soapHeaders || self.security) ?
  (
    "<" + envelopeKey + ":Header>" +
    (self.soapHeaders ? self.soapHeaders.join("\n") : "") +
    (self.security && !self.security.postProcess ? self.security.toXML() : "") +
    "</" + envelopeKey + ":Header>"
  )
  :
    ''
  ) +
"<" + envelopeKey + ":Body" +
(self.bodyAttributes ? self.bodyAttributes.join(' ') : '') +
...
```



# <a name="apidoc.module.soap.HttpClient"></a>[module soap.HttpClient](#apidoc.module.soap.HttpClient)

#### <a name="apidoc.element.soap.HttpClient.HttpClient"></a>[function <span class="apidocSignatureSpan">soap.</span>HttpClient (options)](#apidoc.element.soap.HttpClient.HttpClient)
- description and source-code
```javascript
function HttpClient(options) {
  options = options || {};
  this._request = options.request || req;
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.soap.HttpClient.prototype"></a>[module soap.HttpClient.prototype](#apidoc.module.soap.HttpClient.prototype)

#### <a name="apidoc.element.soap.HttpClient.prototype.buildRequest"></a>[function <span class="apidocSignatureSpan">soap.HttpClient.prototype.</span>buildRequest (rurl, data, exheaders, exoptions)](#apidoc.element.soap.HttpClient.prototype.buildRequest)
- description and source-code
```javascript
buildRequest = function (rurl, data, exheaders, exoptions) {
  var curl = url.parse(rurl);
  var secure = curl.protocol === 'https:';
  var host = curl.hostname;
  var port = parseInt(curl.port, 10);
  var path = [curl.pathname || '/', curl.search || '', curl.hash || ''].join('');
  var method = data ? 'POST' : 'GET';
  var headers = {
    'User-Agent': 'node-soap/' + VERSION,
    'Accept': 'text/html,application/xhtml+xml,application/xml,text/xml;q=0.9,*/*;q=0.8',
    'Accept-Encoding': 'none',
    'Accept-Charset': 'utf-8',
    'Connection': 'close',
    'Host': host + (isNaN(port) ? '' : ':' + port)
  };
  var attr;
  var header;
  var mergeOptions = ['headers'];

  if (typeof data === 'string') {
    headers['Content-Length'] = Buffer.byteLength(data, 'utf8');
    headers['Content-Type'] = 'application/x-www-form-urlencoded';
  }

  exheaders = exheaders || {};
  for (attr in exheaders) {
    headers[attr] = exheaders[attr];
  }

  var options = {
    uri: curl,
    method: method,
    headers: headers,
    followAllRedirects: true
  };


  options.body = data;


  exoptions = exoptions || {};
  for (attr in exoptions) {
    if (mergeOptions.indexOf(attr) !== -1) {
      for (header in exoptions[attr]) {
        options[attr][header] = exoptions[attr][header];
      }
    } else {
      options[attr] = exoptions[attr];
    }
  }
  debug('Http request: %j', options);
  return options;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.soap.HttpClient.prototype.handleResponse"></a>[function <span class="apidocSignatureSpan">soap.HttpClient.prototype.</span>handleResponse (req, res, body)](#apidoc.element.soap.HttpClient.prototype.handleResponse)
- description and source-code
```javascript
handleResponse = function (req, res, body) {
  debug('Http response body: %j', body);
  if (typeof body === 'string') {
    // Remove any extra characters that appear before or after the SOAP
    // envelope.
    var match =
      body.replace(/<!--[\s\S]*?-->/, "").match(/(?:<\?[^?]*\?>[\s]*)?<([^:]*):Envelope([\S\s]*)<\/\1:Envelope>/i);
    if (match) {
      body = match[0];
    }
  }
  return body;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.soap.HttpClient.prototype.request"></a>[function <span class="apidocSignatureSpan">soap.HttpClient.prototype.</span>request (rurl, data, callback, exheaders, exoptions)](#apidoc.element.soap.HttpClient.prototype.request)
- description and source-code
```javascript
request = function (rurl, data, callback, exheaders, exoptions) {
  var self = this;
  var options = self.buildRequest(rurl, data, exheaders, exoptions);
  var headers = options.headers;
  var req = self._request(options, function(err, res, body) {
    if (err) {
      return callback(err);
    }
    body = self.handleResponse(req, res, body);
    callback(null, res, body);
  });

  return req;
}
```
- example usage
```shell
...

    return finish(obj, '<stream>', response);
  });
});
return;
  }

  req = self.httpClient.request(location, xml, function(err, response, body) {
self.lastResponse = body;
self.lastResponseHeaders = response && response.headers;
self.lastElapsedTime = response && response.elapsedTime;
self.emit('response', body, response, eid);

if (err) {
  callback(err);
...
```

#### <a name="apidoc.element.soap.HttpClient.prototype.requestStream"></a>[function <span class="apidocSignatureSpan">soap.HttpClient.prototype.</span>requestStream (rurl, data, exheaders, exoptions)](#apidoc.element.soap.HttpClient.prototype.requestStream)
- description and source-code
```javascript
requestStream = function (rurl, data, exheaders, exoptions) {
  var self = this;
  var options = self.buildRequest(rurl, data, exheaders, exoptions);
  return self._request(options);
}
```
- example usage
```shell
...
    return undefined;
  }
};

if (this.streamAllowed && typeof self.httpClient.requestStream === 'function') {
  callback = _.once(callback);
  var startTime = Date.now();
  req = self.httpClient.requestStream(location, xml, headers, options, self);
  self.lastRequestHeaders = req.headers;
  var onError = function onError(err) {
    self.lastResponse = null;
    self.lastResponseHeaders = null;
    self.lastElapsedTime = null;
    self.emit('response', null, null, eid);
...
```



# <a name="apidoc.module.soap.Server"></a>[module soap.Server](#apidoc.module.soap.Server)

#### <a name="apidoc.element.soap.Server.Server"></a>[function <span class="apidocSignatureSpan">soap.</span>Server (server, path, services, wsdl, options)](#apidoc.element.soap.Server.Server)
- description and source-code
```javascript
Server = function (server, path, services, wsdl, options) {
  var self = this;

  events.EventEmitter.call(this);

  options = options || {};
  this.path = path;
  this.services = services;
  this.wsdl = wsdl;
  this.suppressStack = options && options.suppressStack;

  if (path[path.length - 1] !== '/')
    path += '/';
  wsdl.onReady(function (err) {
    if (typeof server.route === 'function' && typeof server.use === 'function') {
      //handle only the required URL path for express server
      server.route(path).all(function (req, res, next) {
        if (typeof self.authorizeConnection === 'function') {
          if (!self.authorizeConnection(req)) {
            res.end();
            return;
          }
        }
        self._requestListener(req, res);
      });
    } else {
      var listeners = server.listeners('request').slice();
      server.removeAllListeners('request');
      server.addListener('request', function (req, res) {
        if (typeof self.authorizeConnection === 'function') {
          if (!self.authorizeConnection(req)) {
            res.end();
            return;
          }
        }
        var reqPath = url.parse(req.url).pathname;
        if (reqPath[reqPath.length - 1] !== '/') {
          reqPath += '/';
        }
        if (path === reqPath) {
          self._requestListener(req, res);
        } else {
          for (var i = 0, len = listeners.length; i < len; i++) {
            listeners[i].call(this, req, res);
          }
        }
      });
    }
  });

  this._initializeOptions(options);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.soap.Server.super_"></a>[function <span class="apidocSignatureSpan">soap.Server.</span>super_ ()](#apidoc.element.soap.Server.super_)
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



# <a name="apidoc.module.soap.Server.prototype"></a>[module soap.Server.prototype](#apidoc.module.soap.Server.prototype)

#### <a name="apidoc.element.soap.Server.prototype._envelope"></a>[function <span class="apidocSignatureSpan">soap.Server.prototype.</span>_envelope (body, includeTimestamp)](#apidoc.element.soap.Server.prototype._envelope)
- description and source-code
```javascript
_envelope = function (body, includeTimestamp) {
  var defs = this.wsdl.definitions,
    ns = defs.$targetNamespace,
    encoding = '',
    alias = findPrefix(defs.xmlns, ns);
  var xml = "<?xml version=\"1.0\" encoding=\"utf-8\"?>" +
    "<soap:Envelope xmlns:soap=\"http://schemas.xmlsoap.org/soap/envelope/\" " +
    encoding +
    this.wsdl.xmlnsInEnvelope + '>';
  var headers = '';

  if (includeTimestamp) {
    var now = new Date();
    var created = getDateString(now);
    var expires = getDateString(new Date(now.getTime() + (1000 * 600)));

    headers += "<o:Security soap:mustUnderstand=\"1\" " +
      "xmlns:o=\"http://docs.oasis-open.org/wss/2004/01/oasis-200401-wss-wssecurity-secext-1.0.xsd\" " +
      "xmlns:u=\"http://docs.oasis-open.org/wss/2004/01/oasis-200401-wss-wssecurity-utility-1.0.xsd\">" +
      "    <u:Timestamp u:Id=\"_0\">" +
      "      <u:Created>" + created + "</u:Created>" +
      "      <u:Expires>" + expires + "</u:Expires>" +
      "    </u:Timestamp>" +
      "  </o:Security>\n";
  }

  if (this.soapHeaders) {
    headers += this.soapHeaders.join("\n");
  }

  if (headers !== '') {
    xml += "<soap:Header>" + headers + "</soap:Header>";
  }

  xml += "<soap:Body>" +
    body +
    "</soap:Body>" +
    "</soap:Envelope>";
  return xml;
}
```
- example usage
```shell
...
  args = options.args,
  style = options.style,
  handled = false;

try {
  method = this.services[serviceName][portName][methodName];
} catch (error) {
  return callback(this._envelope('', includeTimestamp));
}

function handleResult(error, result) {
  if (handled)
    return;
  handled = true;
...
```

#### <a name="apidoc.element.soap.Server.prototype._executeMethod"></a>[function <span class="apidocSignatureSpan">soap.Server.prototype.</span>_executeMethod (options, req, callback, includeTimestamp)](#apidoc.element.soap.Server.prototype._executeMethod)
- description and source-code
```javascript
_executeMethod = function (options, req, callback, includeTimestamp) {
  options = options || {};
  var self = this,
    method, body,
    serviceName = options.serviceName,
    portName = options.portName,
    methodName = options.methodName,
    outputName = options.outputName,
    args = options.args,
    style = options.style,
    handled = false;

  try {
    method = this.services[serviceName][portName][methodName];
  } catch (error) {
    return callback(this._envelope('', includeTimestamp));
  }

  function handleResult(error, result) {
    if (handled)
      return;
    handled = true;

    if (error && error.Fault !== undefined) {
      return self._sendError(error.Fault, callback, includeTimestamp);
    }
    else if (result === undefined) {
      // Backward compatibility to support one argument callback style
      result = error;
    }

    if (style === 'rpc') {
      body = self.wsdl.objectToRpcXML(outputName, result, '', self.wsdl.definitions.$targetNamespace);
    } else {
      var element = self.wsdl.definitions.services[serviceName].ports[portName].binding.methods[methodName].output;
      body = self.wsdl.objectToDocumentXML(outputName, result, element.targetNSAlias, element.targetNamespace);
    }
    callback(self._envelope(body, includeTimestamp));
  }

  if (!self.wsdl.definitions.services[serviceName].ports[portName].binding.methods[methodName].output) {
    // no output defined = one-way operation so return empty response
    handled = true;
    callback('');
  }

  var result = method(args, handleResult, options.headers, req);
  if (typeof result !== 'undefined') {
    handleResult(result);
  }
}
```
- example usage
```shell
...
    if (binding.style === 'rpc') {
methodName = Object.keys(body)[0];

self.emit('request', obj, methodName);
if (headers)
  self.emit('headers', headers, methodName);

self._executeMethod({
  serviceName: serviceName,
  portName: portName,
  methodName: methodName,
  outputName: methodName + 'Response',
  args: body[methodName],
  headers: headers,
  style: 'rpc'
...
```

#### <a name="apidoc.element.soap.Server.prototype._initializeOptions"></a>[function <span class="apidocSignatureSpan">soap.Server.prototype.</span>_initializeOptions (options)](#apidoc.element.soap.Server.prototype._initializeOptions)
- description and source-code
```javascript
_initializeOptions = function (options) {
  this.wsdl.options.attributesKey = options.attributesKey || 'attributes';
}
```
- example usage
```shell
...
concatStream = require('concat-stream'),
uuid = require('uuid');

var Client = function(wsdl, endpoint, options) {
events.EventEmitter.call(this);
options = options || {};
this.wsdl = wsdl;
this._initializeOptions(options);
this._initializeServices(endpoint);
this.httpClient = options.httpClient || new HttpClient(options);
};
util.inherits(Client, events.EventEmitter);

Client.prototype.addSoapHeader = function(soapHeader, name, namespace, xmlns) {
if (!this.soapHeaders) {
...
```

#### <a name="apidoc.element.soap.Server.prototype._process"></a>[function <span class="apidocSignatureSpan">soap.Server.prototype.</span>_process (input, req, callback)](#apidoc.element.soap.Server.prototype._process)
- description and source-code
```javascript
_process = function (input, req, callback) {
  var self = this,
    pathname = url.parse(req.url).pathname.replace(/\/$/, ''),
    obj = this.wsdl.xmlToObject(input),
    body = obj.Body,
    headers = obj.Header,
    bindings = this.wsdl.definitions.bindings, binding,
    method, methodName,
    serviceName, portName,
    includeTimestamp = obj.Header && obj.Header.Security && obj.Header.Security.Timestamp;

  if (typeof self.authenticate === 'function') {
    if (!obj.Header || !obj.Header.Security) {
      throw new Error('No security header');
    }
    if (!self.authenticate(obj.Header.Security)) {
      throw new Error('Invalid username or password');
    }
  }

  if (typeof self.log === 'function') {
    self.log("info", "Attempting to bind to " + pathname);
  }

  //Avoid Cannot convert undefined or null to object due to Object.keys(body)
  //and throw more meaningful error
  if (!body) {
    throw new Error('Failed to parse the SOAP Message body');
  }

  // use port.location and current url to find the right binding
  binding = (function (self) {
    var services = self.wsdl.definitions.services;
    var firstPort;
    var name;
    for (name in services) {
      serviceName = name;
      var service = services[serviceName];
      var ports = service.ports;
      for (name in ports) {
        portName = name;
        var port = ports[portName];
        var portPathname = url.parse(port.location).pathname.replace(/\/$/, '');

        if (typeof self.log === 'function') {
          self.log("info", "Trying " + portName + " from path " + portPathname);
        }

        if (portPathname === pathname)
          return port.binding;

        // The port path is almost always wrong for generated WSDLs
        if (!firstPort) {
          firstPort = port;
        }
      }
    }
    return !firstPort ? void 0 : firstPort.binding;
  })(this);

  if (!binding) {
    throw new Error('Failed to bind to WSDL');
  }

  try {
    if (binding.style === 'rpc') {
      methodName = Object.keys(body)[0];

      self.emit('request', obj, methodName);
      if (headers)
        self.emit('headers', headers, methodName);

      self._executeMethod({
        serviceName: serviceName,
        portName: portName,
        methodName: methodName,
        outputName: methodName + 'Response',
        args: body[methodName],
        headers: headers,
        style: 'rpc'
      }, req, callback);
    } else {
      var messageElemName = (Object.keys(body)[0] === 'attributes' ? Object.keys(body)[1] : Object.keys(body)[0]);
      var pair = binding.topElements[messageElemName];

      self.emit('request', obj, pair.methodName);
      if (headers)
        self.emit('headers', headers, pair.methodName);

      self._executeMethod({
        serviceName: serviceName,
        portName: portName,
        methodName: pair.methodName,
        outputName: pair.outputName,
        args: body[messageElemName],
        headers: headers,
        style: 'document'
      }, req, callback, includeTimestamp);
    }
  }
  catch (error) {
    if (error.Fault !== undefined) {
      return self._sendError(error.Fault, callback, includeTimestamp);
    }

    throw error;
  }
}
```
- example usage
```shell
...
var self = this;
var result;
var error;
try {
  if (typeof self.log === 'function') {
    self.log("received", xml);
  }
  self._process(xml, req, function (result, statusCode) {
    if (statusCode) {
      res.statusCode = statusCode;
    }
    res.write(result);
    res.end();
    if (typeof self.log === 'function') {
      self.log("replied", result);
...
```

#### <a name="apidoc.element.soap.Server.prototype._processRequestXml"></a>[function <span class="apidocSignatureSpan">soap.Server.prototype.</span>_processRequestXml (req, res, xml)](#apidoc.element.soap.Server.prototype._processRequestXml)
- description and source-code
```javascript
_processRequestXml = function (req, res, xml) {
  var self = this;
  var result;
  var error;
  try {
    if (typeof self.log === 'function') {
      self.log("received", xml);
    }
    self._process(xml, req, function (result, statusCode) {
      if (statusCode) {
        res.statusCode = statusCode;
      }
      res.write(result);
      res.end();
      if (typeof self.log === 'function') {
        self.log("replied", result);
      }
    });
  } catch (err) {
    if (err.Fault !== undefined) {
      return self._sendError(err.Fault, function (result, statusCode) {
        res.statusCode = statusCode || 500;
        res.write(result);
        res.end();
        if (typeof self.log === 'function') {
          self.log("error", err);
        }
      }, new Date().toISOString());
    } else {
      error = err.stack ? (self.suppressStack === true ? err.message : err.stack) : err;
      res.statusCode = 500;
      res.write(error);
      res.end();
      if (typeof self.log === 'function') {
        self.log("error", error);
      }
    }
  }
}
```
- example usage
```shell
...
} else {
  res.setHeader('Content-Type', "application/xml");
}

//request body is already provided by an express middleware
//in this case unzipping should also be done by the express middleware itself
if (req.body) {
  return self._processRequestXml(req, res, req.body.toString());
}

var chunks = [], gunzip;
if (compress && req.headers["content-encoding"] === "gzip") {
  gunzip = new compress.Gunzip();
  gunzip.init();
}
...
```

#### <a name="apidoc.element.soap.Server.prototype._requestListener"></a>[function <span class="apidocSignatureSpan">soap.Server.prototype.</span>_requestListener (req, res)](#apidoc.element.soap.Server.prototype._requestListener)
- description and source-code
```javascript
_requestListener = function (req, res) {
  var self = this;
  var reqParse = url.parse(req.url);
  var reqPath = reqParse.pathname;
  var reqQuery = reqParse.search;

  if (typeof self.log === 'function') {
    self.log("info", "Handling " + req.method + " on " + req.url);
  }

  if (req.method === 'GET') {
    if (reqQuery && reqQuery.toLowerCase() === '?wsdl') {
      if (typeof self.log === 'function') {
        self.log("info", "Wants the WSDL");
      }
      res.setHeader("Content-Type", "application/xml");
      res.write(self.wsdl.toXML());
    }
    res.end();
  } else if (req.method === 'POST') {
    if (typeof req.headers['content-type'] !== "undefined") {
      res.setHeader('Content-Type', req.headers['content-type']);
    } else {
      res.setHeader('Content-Type', "application/xml");
    }

    //request body is already provided by an express middleware
    //in this case unzipping should also be done by the express middleware itself
    if (req.body) {
      return self._processRequestXml(req, res, req.body.toString());
    }

    var chunks = [], gunzip;
    if (compress && req.headers["content-encoding"] === "gzip") {
      gunzip = new compress.Gunzip();
      gunzip.init();
    }
    req.on('data', function (chunk) {
      if (gunzip)
        chunk = gunzip.inflate(chunk, "binary");
      chunks.push(chunk);
    });
    req.on('end', function () {
      var xml = chunks.join('');
      var result;
      var error;
      if (gunzip) {
        gunzip.end();
        gunzip = null;
      }
      self._processRequestXml(req, res, xml);
    });
  }
  else {
    res.end();
  }
}
```
- example usage
```shell
...
  server.route(path).all(function (req, res, next) {
    if (typeof self.authorizeConnection === 'function') {
      if (!self.authorizeConnection(req)) {
        res.end();
        return;
      }
    }
    self._requestListener(req, res);
  });
} else {
  var listeners = server.listeners('request').slice();
  server.removeAllListeners('request');
  server.addListener('request', function (req, res) {
    if (typeof self.authorizeConnection === 'function') {
      if (!self.authorizeConnection(req)) {
...
```

#### <a name="apidoc.element.soap.Server.prototype._sendError"></a>[function <span class="apidocSignatureSpan">soap.Server.prototype.</span>_sendError (soapFault, callback, includeTimestamp)](#apidoc.element.soap.Server.prototype._sendError)
- description and source-code
```javascript
_sendError = function (soapFault, callback, includeTimestamp) {
  var self = this,
    fault;

  var statusCode;
  if (soapFault.statusCode) {
    statusCode = soapFault.statusCode;
    soapFault.statusCode = undefined;
  }

  if (soapFault.faultcode) {
    // Soap 1.1 error style
    // Root element will be prependend with the soap NS
    // It must match the NS defined in the Envelope (set by the _envelope method)
    fault = self.wsdl.objectToDocumentXML("soap:Fault", soapFault, undefined);
  }
  else {
    // Soap 1.2 error style.
    // 3rd param is the NS prepended to all elements
    // It must match the NS defined in the Envelope (set by the _envelope method)
    fault = self.wsdl.objectToDocumentXML("Fault", soapFault, "soap");
  }

  return callback(self._envelope(fault, includeTimestamp), statusCode);
}
```
- example usage
```shell
...
    res.end();
    if (typeof self.log === 'function') {
      self.log("replied", result);
    }
  });
} catch (err) {
  if (err.Fault !== undefined) {
    return self._sendError(err.Fault, function (result, statusCode) {
      res.statusCode = statusCode || 500;
      res.write(result);
      res.end();
      if (typeof self.log === 'function') {
        self.log("error", err);
      }
    }, new Date().toISOString());
...
```

#### <a name="apidoc.element.soap.Server.prototype.addSoapHeader"></a>[function <span class="apidocSignatureSpan">soap.Server.prototype.</span>addSoapHeader (soapHeader, name, namespace, xmlns)](#apidoc.element.soap.Server.prototype.addSoapHeader)
- description and source-code
```javascript
addSoapHeader = function (soapHeader, name, namespace, xmlns) {
  if (!this.soapHeaders) {
    this.soapHeaders = [];
  }
  if (typeof soapHeader === 'object') {
    soapHeader = this.wsdl.objectToXML(soapHeader, name, namespace, xmlns, true);
  }
  return this.soapHeaders.push(soapHeader) - 1;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.soap.Server.prototype.changeSoapHeader"></a>[function <span class="apidocSignatureSpan">soap.Server.prototype.</span>changeSoapHeader (index, soapHeader, name, namespace, xmlns)](#apidoc.element.soap.Server.prototype.changeSoapHeader)
- description and source-code
```javascript
changeSoapHeader = function (index, soapHeader, name, namespace, xmlns) {
  if (!this.soapHeaders) {
    this.soapHeaders = [];
  }
  if (typeof soapHeader === 'object') {
    soapHeader = this.wsdl.objectToXML(soapHeader, name, namespace, xmlns, true);
  }
  this.soapHeaders[index] = soapHeader;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.soap.Server.prototype.clearSoapHeaders"></a>[function <span class="apidocSignatureSpan">soap.Server.prototype.</span>clearSoapHeaders ()](#apidoc.element.soap.Server.prototype.clearSoapHeaders)
- description and source-code
```javascript
clearSoapHeaders = function () {
  this.soapHeaders = null;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.soap.Server.prototype.getSoapHeaders"></a>[function <span class="apidocSignatureSpan">soap.Server.prototype.</span>getSoapHeaders ()](#apidoc.element.soap.Server.prototype.getSoapHeaders)
- description and source-code
```javascript
getSoapHeaders = function () {
  return this.soapHeaders;
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.soap.WSDL"></a>[module soap.WSDL](#apidoc.module.soap.WSDL)

#### <a name="apidoc.element.soap.WSDL.WSDL"></a>[function <span class="apidocSignatureSpan">soap.</span>WSDL (definition, uri, options)](#apidoc.element.soap.WSDL.WSDL)
- description and source-code
```javascript
WSDL = function (definition, uri, options) {
  var self = this,
      fromFunc;

  this.uri = uri;
  this.callback = function() {
  };
  this._includesWsdl = [];

  // initialize WSDL cache
  this.WSDL_CACHE = (options || {}).WSDL_CACHE || {};

  this._initializeOptions(options);

  if (typeof definition === 'string') {
    definition = stripBom(definition);
    fromFunc = this._fromXML;
  }
  else if (typeof definition === 'object') {
    fromFunc = this._fromServices;
  }
  else {
    throw new Error('WSDL constructor takes either an XML string or service definition');
  }

  process.nextTick(function() {
    try {
      fromFunc.call(self, definition);
    } catch (e) {
      return self.callback(e.message);
    }

    self.processIncludes(function(err) {
      var name;
      if (err) {
        return self.callback(err);
      }

      self.definitions.deleteFixedAttrs();
      var services = self.services = self.definitions.services;
      if (services) {
        for (name in services) {
          services[name].postProcess(self.definitions);
        }
      }
      var complexTypes = self.definitions.complexTypes;
      if (complexTypes) {
        for (name in complexTypes) {
          complexTypes[name].deleteFixedAttrs();
        }
      }

      // for document style, for every binding, prepare input message element name to (methodName, output message element name)
mapping
      var bindings = self.definitions.bindings;
      for (var bindingName in bindings) {
        var binding = bindings[bindingName];
        if (typeof binding.style === 'undefined') {
          binding.style = 'document';
        }
        if (binding.style !== 'document')
          continue;
        var methods = binding.methods;
        var topEls = binding.topElements = {};
        for (var methodName in methods) {
          if (methods[methodName].input) {
            var inputName = methods[methodName].input.$name;
            var outputName="";
            if(methods[methodName].output )
              outputName = methods[methodName].output.$name;
            topEls[inputName] = {"methodName": methodName, "outputName": outputName};
          }
        }
      }

      // prepare soap envelope xmlns definition string
      self.xmlnsInEnvelope = self._xmlnsMap();

      self.callback(err, self);
    });

  });
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.soap.WSDL.prototype"></a>[module soap.WSDL.prototype](#apidoc.module.soap.WSDL.prototype)

#### <a name="apidoc.element.soap.WSDL.prototype._fromServices"></a>[function <span class="apidocSignatureSpan">soap.WSDL.prototype.</span>_fromServices (services)](#apidoc.element.soap.WSDL.prototype._fromServices)
- description and source-code
```javascript
_fromServices = function (services) {

}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.soap.WSDL.prototype._fromXML"></a>[function <span class="apidocSignatureSpan">soap.WSDL.prototype.</span>_fromXML (xml)](#apidoc.element.soap.WSDL.prototype._fromXML)
- description and source-code
```javascript
_fromXML = function (xml) {
  this.definitions = this._parse(xml);
  this.definitions.descriptions = {
    types:{}
  };
  this.xml = xml;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.soap.WSDL.prototype._initializeOptions"></a>[function <span class="apidocSignatureSpan">soap.WSDL.prototype.</span>_initializeOptions (options)](#apidoc.element.soap.WSDL.prototype._initializeOptions)
- description and source-code
```javascript
_initializeOptions = function (options) {
  this._originalIgnoredNamespaces = (options || {}).ignoredNamespaces;
  this.options = {};

  var ignoredNamespaces = options ? options.ignoredNamespaces : null;

  if (ignoredNamespaces &&
      (Array.isArray(ignoredNamespaces.namespaces) || typeof ignoredNamespaces.namespaces === 'string')) {
    if (ignoredNamespaces.override) {
      this.options.ignoredNamespaces = ignoredNamespaces.namespaces;
    } else {
      this.options.ignoredNamespaces = this.ignoredNamespaces.concat(ignoredNamespaces.namespaces);
    }
  } else {
    this.options.ignoredNamespaces = this.ignoredNamespaces;
  }

  this.options.valueKey = options.valueKey || this.valueKey;
  this.options.xmlKey = options.xmlKey || this.xmlKey;
  if (options.escapeXML !== undefined) {
    this.options.escapeXML = options.escapeXML;
  } else {
    this.options.escapeXML = true;
  }
  // Allow any request headers to keep passing through
  this.options.wsdl_headers = options.wsdl_headers;
  this.options.wsdl_options = options.wsdl_options;
  if (options.httpClient) {
    this.options.httpClient = options.httpClient;
  }

  // The supplied request-object should be passed through
  if (options.request) {
    this.options.request = options.request;
  }

  var ignoreBaseNameSpaces = options ? options.ignoreBaseNameSpaces : null;
  if (ignoreBaseNameSpaces !== null && typeof ignoreBaseNameSpaces !== 'undefined') {
    this.options.ignoreBaseNameSpaces = ignoreBaseNameSpaces;
  } else {
    this.options.ignoreBaseNameSpaces = this.ignoreBaseNameSpaces;
  }

  // Works only in client
  this.options.forceSoap12Headers = options.forceSoap12Headers;
  this.options.customDeserializer = options.customDeserializer;

  if (options.overrideRootElement !== undefined) {
    this.options.overrideRootElement = options.overrideRootElement;
  }
}
```
- example usage
```shell
...
concatStream = require('concat-stream'),
uuid = require('uuid');

var Client = function(wsdl, endpoint, options) {
events.EventEmitter.call(this);
options = options || {};
this.wsdl = wsdl;
this._initializeOptions(options);
this._initializeServices(endpoint);
this.httpClient = options.httpClient || new HttpClient(options);
};
util.inherits(Client, events.EventEmitter);

Client.prototype.addSoapHeader = function(soapHeader, name, namespace, xmlns) {
if (!this.soapHeaders) {
...
```

#### <a name="apidoc.element.soap.WSDL.prototype._parse"></a>[function <span class="apidocSignatureSpan">soap.WSDL.prototype.</span>_parse (xml)](#apidoc.element.soap.WSDL.prototype._parse)
- description and source-code
```javascript
_parse = function (xml) {
  var self = this,
    p = sax.parser(true),
    stack = [],
    root = null,
    types = null,
    schema = null,
      options = self.options;

  p.onopentag = function(node) {
    var nsName = node.name;
    var attrs  = node.attributes;

    var top = stack[stack.length - 1];
    var name;
    if (top) {
      try {
        top.startElement(stack, nsName, attrs, options);
      } catch (e) {
        if (self.options.strict) {
          throw e;
        } else {
          stack.push(new Element(nsName, attrs, options));
        }
      }
    } else {
      name = splitQName(nsName).name;
      if (name === 'definitions') {
        root = new DefinitionsElement(nsName, attrs, options);
        stack.push(root);
      } else if (name === 'schema') {
        // Shim a structure in here to allow the proper objects to be created when merging back.
        root = new DefinitionsElement('definitions', {}, {});
        types = new TypesElement('types', {}, {});
        schema = new SchemaElement(nsName, attrs, options);
        types.addChild(schema);
        root.addChild(types);
        stack.push(schema);
      } else {
        throw new Error('Unexpected root element of WSDL or include');
      }
    }
  };

  p.onclosetag = function(name) {
    var top = stack[stack.length - 1];
    assert(top, 'Unmatched close tag: ' + name);

    top.endElement(stack, name);
  };

  p.write(xml).close();

  return root;
}
```
- example usage
```shell
...

  p.write(xml).close();

  return root;
};

WSDL.prototype._fromXML = function(xml) {
  this.definitions = this._parse(xml);
  this.definitions.descriptions = {
    types:{}
  };
  this.xml = xml;
};

WSDL.prototype._fromServices = function(services) {
...
```

#### <a name="apidoc.element.soap.WSDL.prototype._processNextInclude"></a>[function <span class="apidocSignatureSpan">soap.WSDL.prototype.</span>_processNextInclude (includes, callback)](#apidoc.element.soap.WSDL.prototype._processNextInclude)
- description and source-code
```javascript
_processNextInclude = function (includes, callback) {
  var self = this,
    include = includes.shift(),
    options;

  if (!include)
    return callback();

  var includePath;
  if (!/^https?:/.test(self.uri) && !/^https?:/.test(include.location)) {
    includePath = path.resolve(path.dirname(self.uri), include.location);
  } else {
    includePath = url.resolve(self.uri||'', include.location);
  }

  options = _.assign({}, this.options);
  // follow supplied ignoredNamespaces option
  options.ignoredNamespaces = this._originalIgnoredNamespaces || this.options.ignoredNamespaces;
  options.WSDL_CACHE = this.WSDL_CACHE;

  open_wsdl_recursive(includePath, options, function(err, wsdl) {
    if (err) {
      return callback(err);
    }

    self._includesWsdl.push(wsdl);

    if (wsdl.definitions instanceof DefinitionsElement) {
      _.merge(self.definitions, wsdl.definitions, function(a,b) {
        return (a instanceof SchemaElement) ? a.merge(b) : undefined;
      });
    } else {
      self.definitions.schemas[include.namespace || wsdl.definitions.$targetNamespace] = deepMerge(self.definitions.schemas[include
.namespace || wsdl.definitions.$targetNamespace], wsdl.definitions);
    }
    self._processNextInclude(includes, function(err) {
      callback(err);
    });
  });
}
```
- example usage
```shell
...
  if (wsdl.definitions instanceof DefinitionsElement) {
    _.merge(self.definitions, wsdl.definitions, function(a,b) {
      return (a instanceof SchemaElement) ? a.merge(b) : undefined;
    });
  } else {
    self.definitions.schemas[include.namespace || wsdl.definitions.$targetNamespace] = deepMerge(self.definitions.schemas[include
.namespace || wsdl.definitions.$targetNamespace], wsdl.definitions);
  }
  self._processNextInclude(includes, function(err) {
    callback(err);
  });
});
};

WSDL.prototype.processIncludes = function(callback) {
var schemas = this.definitions.schemas,
...
```

#### <a name="apidoc.element.soap.WSDL.prototype._splitQName"></a>[function <span class="apidocSignatureSpan">soap.WSDL.prototype.</span>_splitQName (nsName)](#apidoc.element.soap.WSDL.prototype._splitQName)
- description and source-code
```javascript
function splitQName(nsName) {
  var i = typeof nsName === 'string' ? nsName.indexOf(':') : -1;
  return i < 0 ? {prefix: TNS_PREFIX, name: nsName} :
  {prefix: nsName.substring(0, i), name: nsName.substring(i + 1)};
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.soap.WSDL.prototype._xmlnsMap"></a>[function <span class="apidocSignatureSpan">soap.WSDL.prototype.</span>_xmlnsMap ()](#apidoc.element.soap.WSDL.prototype._xmlnsMap)
- description and source-code
```javascript
_xmlnsMap = function () {
  var xmlns = this.definitions.xmlns;
  var str = '';
  for (var alias in xmlns) {
    if (alias === '' || alias === TNS_PREFIX) {
      continue;
    }
    var ns = xmlns[alias];
    switch (ns) {
      case "http://xml.apache.org/xml-soap" : // apachesoap
      case "http://schemas.xmlsoap.org/wsdl/" : // wsdl
      case "http://schemas.xmlsoap.org/wsdl/soap/" : // wsdlsoap
      case "http://schemas.xmlsoap.org/wsdl/soap12/": // wsdlsoap12
      case "http://schemas.xmlsoap.org/soap/encoding/" : // soapenc
      case "http://www.w3.org/2001/XMLSchema" : // xsd
        continue;
    }
    if (~ns.indexOf('http://schemas.xmlsoap.org/')) {
      continue;
    }
    if (~ns.indexOf('http://www.w3.org/')) {
      continue;
    }
    if (~ns.indexOf('http://xml.apache.org/')) {
      continue;
    }
    str += ' xmlns:' + alias + '="' + ns + '"';
  }
  return str;
}
```
- example usage
```shell
...
              outputName = methods[methodName].output.$name;
            topEls[inputName] = {"methodName": methodName, "outputName": outputName};
          }
        }
      }

      // prepare soap envelope xmlns definition string
      self.xmlnsInEnvelope = self._xmlnsMap();

      self.callback(err, self);
    });

  });
};
...
```

#### <a name="apidoc.element.soap.WSDL.prototype.describeServices"></a>[function <span class="apidocSignatureSpan">soap.WSDL.prototype.</span>describeServices ()](#apidoc.element.soap.WSDL.prototype.describeServices)
- description and source-code
```javascript
describeServices = function () {
  var services = {};
  for (var name in this.services) {
    var service = this.services[name];
    services[name] = service.description(this.definitions);
  }
  return services;
}
```
- example usage
```shell
...
Client.prototype.setEndpoint = function(endpoint) {
  this.endpoint = endpoint;
  this._initializeServices(endpoint);
};

Client.prototype.describe = function() {
  var types = this.wsdl.definitions.types;
  return this.wsdl.describeServices();
};

Client.prototype.setSecurity = function(security) {
  this.security = security;
};

Client.prototype.setSOAPAction = function(SOAPAction) {
...
```

#### <a name="apidoc.element.soap.WSDL.prototype.filterOutIgnoredNameSpace"></a>[function <span class="apidocSignatureSpan">soap.WSDL.prototype.</span>filterOutIgnoredNameSpace (ns)](#apidoc.element.soap.WSDL.prototype.filterOutIgnoredNameSpace)
- description and source-code
```javascript
filterOutIgnoredNameSpace = function (ns) {
  var namespace = noColonNameSpace(ns);
  return this.isIgnoredNameSpace(namespace) ? '' : namespace;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.soap.WSDL.prototype.findChildSchemaObject"></a>[function <span class="apidocSignatureSpan">soap.WSDL.prototype.</span>findChildSchemaObject (parameterTypeObj, childName)](#apidoc.element.soap.WSDL.prototype.findChildSchemaObject)
- description and source-code
```javascript
findChildSchemaObject = function (parameterTypeObj, childName) {
  if (!parameterTypeObj || !childName) {
    return null;
  }
  var found = null,
      i = 0,
      child,
      ref;

  if (Array.isArray(parameterTypeObj.$lookupTypes) && parameterTypeObj.$lookupTypes.length) {
    var types = parameterTypeObj.$lookupTypes;

    for(i = 0; i < types.length; i++) {
      var typeObj = types[i];

      if(typeObj.$name === childName) {
        found = typeObj;
        break;
      }
    }
  }

  var object = parameterTypeObj;
  if (object.$name === childName && object.name === 'element') {
    return object;
  }
  if (object.$ref) {
    ref = splitQName(object.$ref);
    if (ref.name === childName) {
      return object;
    }
  }

  var childNsURI;
  if (object.$type) {
    var typeInfo = splitQName(object.$type);
    if (typeInfo.prefix === TNS_PREFIX) {
      childNsURI = parameterTypeObj.$targetNamespace;
    } else {
      childNsURI = this.definitions.xmlns[typeInfo.prefix];
    }
    var typeDef = this.findSchemaType(typeInfo.name, childNsURI);
    if (typeDef) {
      return this.findChildSchemaObject(typeDef, childName);
    }
  }

  if (object.children) {
    for (i = 0, child; child = object.children[i]; i++) {
      found = this.findChildSchemaObject(child, childName);
      if (found) {
        break;
      }

      if (child.$base) {
        var baseQName = splitQName(child.$base);
        var childNameSpace = baseQName.prefix === TNS_PREFIX ? '' : baseQName.prefix;
        childNsURI = this.definitions.xmlns[baseQName.prefix];

        var foundBase = this.findSchemaType(baseQName.name, childNsURI);

        if (foundBase) {
          found = this.findChildSchemaObject(foundBase, childName);

          if (found) {
            found.$baseNameSpace = childNameSpace;
            found.$type = childNameSpace + ':' + childName;
            break;
          }
        }
      }
    }

  }

  if (!found && object.$name === childName) {
    return object;
  }

  return found;
}
```
- example usage
```shell
...

      if (isFirst) {
value = self.objectToXML(child, name, nsPrefix, nsURI, false, null, schemaObject, nsContext);
      } else {

if (self.definitions.schemas) {
  if (schema) {
    var childSchemaObject = self.findChildSchemaObject(schemaObject, name);
    //find sub namespace if not a primitive
    if (childSchemaObject &&
      ((childSchemaObject.$type && (childSchemaObject.$type.indexOf('xsd:') === -1)) ||
      childSchemaObject.$ref || childSchemaObject.$name)) {
      /*if the base name space of the children is not in the ingoredSchemaNamspaces we use it.
       This is because in some services the child nodes do not need the baseNameSpace.
       */
...
```

#### <a name="apidoc.element.soap.WSDL.prototype.findSchemaObject"></a>[function <span class="apidocSignatureSpan">soap.WSDL.prototype.</span>findSchemaObject (nsURI, qname)](#apidoc.element.soap.WSDL.prototype.findSchemaObject)
- description and source-code
```javascript
findSchemaObject = function (nsURI, qname) {
  if (!nsURI || !qname) {
    return null;
  }

  var def = null;

  if (this.definitions.schemas) {
    var schema = this.definitions.schemas[nsURI];
    if (schema) {
      if (qname.indexOf(':') !== -1) {
        qname = qname.substring(qname.indexOf(':') + 1, qname.length);
      }

      // if the client passed an input element which has a '$lookupType' property instead of '$type'
      // the 'def' is found in 'schema.elements'.
      def = schema.complexTypes[qname] || schema.types[qname] || schema.elements[qname];
    }
  }

  return def;
}
```
- example usage
```shell
...
  var typeURI;
  if (type.prefix === TNS_PREFIX) {
    // In case of xsi:type = "MyType"
    typeURI = xmlns[type.prefix] || xmlns.xmlns;
  } else {
    typeURI = xmlns[type.prefix];
  }
  var typeDef = self.findSchemaObject(typeURI, type.name);
  if (typeDef) {
    xsiTypeSchema = typeDef.description(self.definitions);
  }
}

if (topSchema && topSchema[name + '[]']) {
  name = name + '[]';
...
```

#### <a name="apidoc.element.soap.WSDL.prototype.findSchemaType"></a>[function <span class="apidocSignatureSpan">soap.WSDL.prototype.</span>findSchemaType (name, nsURI)](#apidoc.element.soap.WSDL.prototype.findSchemaType)
- description and source-code
```javascript
findSchemaType = function (name, nsURI) {
  if (!this.definitions.schemas || !name || !nsURI) {
    return null;
  }

  var schema = this.definitions.schemas[nsURI];
  if (!schema || !schema.complexTypes) {
    return null;
  }

  return schema.complexTypes[name];
}
```
- example usage
```shell
...
  var typeURI = schema.xmlns[typePrefix] || self.definitions.xmlns[typePrefix];
  childNsURI = typeURI;
  if (typeURI !== 'http://www.w3.org/2001/XMLSchema' && typePrefix !== TNS_PREFIX) {
    // Add the prefix/namespace mapping, but not declare it
    nsContext.addNamespace(typePrefix, typeURI);
  }
  resolvedChildSchemaObject =
    self.findSchemaType(typeQName.name, typeURI) || childSchemaObject;
} else {
  resolvedChildSchemaObject =
    self.findSchemaObject(childNsURI, childName) || childSchemaObject;
}

if (childSchemaObject.$baseNameSpace && this.options.ignoreBaseNameSpaces) {
  childNsPrefix = nsPrefix;
...
```

#### <a name="apidoc.element.soap.WSDL.prototype.isIgnoredNameSpace"></a>[function <span class="apidocSignatureSpan">soap.WSDL.prototype.</span>isIgnoredNameSpace (ns)](#apidoc.element.soap.WSDL.prototype.isIgnoredNameSpace)
- description and source-code
```javascript
isIgnoredNameSpace = function (ns) {
  return this.options.ignoredNamespaces.indexOf(ns) > -1;
}
```
- example usage
```shell
...

WSDL.prototype.isIgnoredNameSpace = function(ns) {
 return this.options.ignoredNamespaces.indexOf(ns) > -1;
};

WSDL.prototype.filterOutIgnoredNameSpace = function(ns) {
 var namespace = noColonNameSpace(ns);
 return this.isIgnoredNameSpace(namespace) ? '' : namespace;
};



/**
* Convert an object to XML.  This is a recursive method as it calls itself.
*
...
```

#### <a name="apidoc.element.soap.WSDL.prototype.objectToDocumentXML"></a>[function <span class="apidocSignatureSpan">soap.WSDL.prototype.</span>objectToDocumentXML (name, params, nsPrefix, nsURI, type)](#apidoc.element.soap.WSDL.prototype.objectToDocumentXML)
- description and source-code
```javascript
objectToDocumentXML = function (name, params, nsPrefix, nsURI, type) {
  var args = {};
  args[name] = params;
  var parameterTypeObj = type ? this.findSchemaObject(nsURI, type) : null;
  return this.objectToXML(args, null, nsPrefix, nsURI, true, null, parameterTypeObj);
}
```
- example usage
```shell
...
if ((style === 'rpc')&& ( ( input.parts || input.name==="element" ) || args === null) ) {
  assert.ok(!style || style === 'rpc', 'invalid message definition for document style binding');
  message = self.wsdl.objectToRpcXML(name, args, alias, ns,(input.name!=="element" ));
  (method.inputSoap === 'encoded') && (encoding = 'soap:encodingStyle="http://schemas.xmlsoap.org/soap/encoding/" ');
} else {
  assert.ok(!style || style === 'document', 'invalid message definition for rpc style binding');
  // pass 'input.$lookupType' if 'input.$type' could not be found
  message = self.wsdl.objectToDocumentXML(input.$name, args, input.targetNSAlias, input.targetNamespace, (input.$type || input.$
lookupType));
}
xml = "<?xml version=\"1.0\" encoding=\"utf-8\"?>" +
  "<" + envelopeKey + ":Envelope " +
  xmlnsSoap + " " +
  "xmlns:xsi=\"http://www.w3.org/2001/XMLSchema-instance\" " +
  encoding +
  this.wsdl.xmlnsInEnvelope + '>' +
...
```

#### <a name="apidoc.element.soap.WSDL.prototype.objectToRpcXML"></a>[function <span class="apidocSignatureSpan">soap.WSDL.prototype.</span>objectToRpcXML (name, params, nsPrefix, nsURI, isParts)](#apidoc.element.soap.WSDL.prototype.objectToRpcXML)
- description and source-code
```javascript
objectToRpcXML = function (name, params, nsPrefix, nsURI, isParts) {
  var parts = [];
  var defs = this.definitions;
  var nsAttrName = '_xmlns';

  nsPrefix = nsPrefix || findPrefix(defs.xmlns, nsURI);

  nsURI = nsURI || defs.xmlns[nsPrefix];
  nsPrefix = nsPrefix === TNS_PREFIX ? '' : (nsPrefix + ':');

  parts.push(['<', nsPrefix, name, '>'].join(''));

  for (var key in params) {
    if (!params.hasOwnProperty(key)) {
      continue;
    }
    if (key !== nsAttrName) {
      var value = params[key];
      var prefixedKey = (isParts ? '' : nsPrefix) + key;
      parts.push(['<', prefixedKey, '>'].join(''));
      parts.push((typeof value === 'object') ? this.objectToXML(value, key, nsPrefix, nsURI) : xmlEscape(value));
      parts.push(['</', prefixedKey, '>'].join(''));
    }
  }
  parts.push(['</', nsPrefix, name, '>'].join(''));
  return parts.join('');
}
```
- example usage
```shell
...
if (self.security && self.security.addHeaders)
  self.security.addHeaders(headers);
if (self.security && self.security.addOptions)
  self.security.addOptions(options);

if ((style === 'rpc')&& ( ( input.parts || input.name==="element" ) || args === null) ) {
  assert.ok(!style || style === 'rpc', 'invalid message definition for document style binding');
  message = self.wsdl.objectToRpcXML(name, args, alias, ns,(input.name!=="element" ));
  (method.inputSoap === 'encoded') && (encoding = 'soap:encodingStyle="http://schemas.xmlsoap.org/soap/encoding/" ');
} else {
  assert.ok(!style || style === 'document', 'invalid message definition for rpc style binding');
  // pass 'input.$lookupType' if 'input.$type' could not be found
  message = self.wsdl.objectToDocumentXML(input.$name, args, input.targetNSAlias, input.targetNamespace, (input.$type || input.$
lookupType));
}
xml = "<?xml version=\"1.0\" encoding=\"utf-8\"?>" +
...
```

#### <a name="apidoc.element.soap.WSDL.prototype.objectToXML"></a>[function <span class="apidocSignatureSpan">soap.WSDL.prototype.</span>objectToXML (obj, name, nsPrefix, nsURI, isFirst, xmlnsAttr, schemaObject, nsContext)](#apidoc.element.soap.WSDL.prototype.objectToXML)
- description and source-code
```javascript
objectToXML = function (obj, name, nsPrefix, nsURI, isFirst, xmlnsAttr, schemaObject, nsContext) {
  var self = this;
  var schema = this.definitions.schemas[nsURI];

  var parentNsPrefix = nsPrefix ? nsPrefix.parent : undefined;
  if (typeof parentNsPrefix !== 'undefined') {
    //we got the parentNsPrefix for our array. setting the namespace-variable back to the current namespace string
    nsPrefix = nsPrefix.current;
  }

  parentNsPrefix = noColonNameSpace(parentNsPrefix);
  if (this.isIgnoredNameSpace(parentNsPrefix)) {
    parentNsPrefix = '';
  }

  var soapHeader = !schema;
  var qualified = schema && schema.$elementFormDefault === 'qualified';
  var parts = [];
  var prefixNamespace = (nsPrefix || qualified) && nsPrefix !== TNS_PREFIX;

  var xmlnsAttrib = '';
  if (nsURI && isFirst) {
    if(self.options.overrideRootElement && self.options.overrideRootElement.xmlnsAttributes) {
      self.options.overrideRootElement.xmlnsAttributes.forEach(function(attribute) {
        xmlnsAttrib += ' ' + attribute.name + '="' + attribute.value + '"';
      });
    } else {
      if (prefixNamespace && !this.isIgnoredNameSpace(nsPrefix)) {
        // resolve the prefix namespace
        xmlnsAttrib += ' xmlns:' + nsPrefix + '="' + nsURI + '"';
      }
      // only add default namespace if the schema elementFormDefault is qualified
      if (qualified || soapHeader) xmlnsAttrib += ' xmlns="' + nsURI + '"';
    }
  }

  if (!nsContext) {
    nsContext = new NamespaceContext();
    nsContext.declareNamespace(nsPrefix, nsURI);
  } else {
    nsContext.pushContext();
  }

  // explicitly use xmlns attribute if available
  if (xmlnsAttr && !(self.options.overrideRootElement && self.options.overrideRootElement.xmlnsAttributes)) {
    xmlnsAttrib = xmlnsAttr;
  }

  var ns = '';

  if (self.options.overrideRootElement && isFirst) {
    ns = self.options.overrideRootElement.namespace;
  } else if (prefixNamespace && (qualified || isFirst || soapHeader) && !this.isIgnoredNameSpace(nsPrefix)) {
    ns = nsPrefix;
  }

  var i, n;
  // start building out XML string.
  if (Array.isArray(obj)) {
    for (i = 0, n = obj.length; i < n; i++) {
      var item = obj[i];
      var arrayAttr = self.processAttributes(item, nsContext),
          correctOuterNsPrefix = parentNsPrefix || ns; //using the parent namespace prefix if given

      parts.push(['<', appendColon(correctOuterNsPrefix), name, arrayAttr, xmlnsAttrib, '>'].join(''));
      parts.push(self.objectToXML(item, name, nsPrefix, nsURI, false, null, schemaObject, nsContext));
      parts.push(['</', appendColon(correctOuterNsPrefix), name, '>'].join(''));
    }
  } else if (typeof obj === 'object') {
    for (name in obj) {
      if (!obj.hasOwnProperty(name)) continue;
      //don't process attributes as element
      if (name === self.options.attributesKey) {
        continue;
      }
      //Its the value of a xml object. Return it directly.
      if (name === self.options.xmlKey){
        nsContext.popContext();
        return obj[name];
      }
      //Its the value of an item. Return it directly.
      if (name === self.options.valueKey) {
        nsContext.popContext();
        return xmlEscape(obj[name]);
      }

      var child = obj[name];
      if (typeof child === 'undefined') {
        continue;
      }

      var attr = self.processAttributes(child, nsContext);

      var value = '';
      var nonSubNameSpace = '';
      var emptyNonSubNameSpace = false;

      var nameWithNsRegex = /^([^:]+):([^:]+)$/.exec(name);
      if (nameWithNsRegex) {
        nonSubNameSpace = nameWithNsRegex[1] + ':';
        name = nameWithNsRegex[2];
      } else if(name[0] === ':'){
        emptyNonSubNameSpace = true;
        name = name.substr(1);
      }

      if (isFirst) {
        value = self.objectToXML(child, name, nsPrefix, nsURI, false, null, schemaObject, nsContext);
      } else {

        if (self.definitions.schemas) {
          if (schema) {
            var childSchemaObject = sel ...
```
- example usage
```shell
...
util.inherits(Client, events.EventEmitter);

Client.prototype.addSoapHeader = function(soapHeader, name, namespace, xmlns) {
if (!this.soapHeaders) {
  this.soapHeaders = [];
}
if (typeof soapHeader === 'object') {
  soapHeader = this.wsdl.objectToXML(soapHeader, name, namespace, xmlns, true);
}
return this.soapHeaders.push(soapHeader) - 1;
};

Client.prototype.changeSoapHeader = function(index, soapHeader, name, namespace, xmlns) {
if (!this.soapHeaders) {
  this.soapHeaders = [];
...
```

#### <a name="apidoc.element.soap.WSDL.prototype.onReady"></a>[function <span class="apidocSignatureSpan">soap.WSDL.prototype.</span>onReady (callback)](#apidoc.element.soap.WSDL.prototype.onReady)
- description and source-code
```javascript
onReady = function (callback) {
  if (callback)
    this.callback = callback;
}
```
- example usage
```shell
...
this.path = path;
this.services = services;
this.wsdl = wsdl;
this.suppressStack = options && options.suppressStack;

if (path[path.length - 1] !== '/')
  path += '/';
wsdl.onReady(function (err) {
  if (typeof server.route === 'function' && typeof server.use === 'function') {
    //handle only the required URL path for express server
    server.route(path).all(function (req, res, next) {
      if (typeof self.authorizeConnection === 'function') {
        if (!self.authorizeConnection(req)) {
          res.end();
          return;
...
```

#### <a name="apidoc.element.soap.WSDL.prototype.processAttributes"></a>[function <span class="apidocSignatureSpan">soap.WSDL.prototype.</span>processAttributes (child, nsContext)](#apidoc.element.soap.WSDL.prototype.processAttributes)
- description and source-code
```javascript
processAttributes = function (child, nsContext) {
  var attr = '';

  if(child === null) {
    child = [];
  }

  var attrObj = child[this.options.attributesKey];
  if (attrObj && attrObj.xsi_type) {
    var xsiType = attrObj.xsi_type;

    var prefix = xsiType.prefix || xsiType.namespace;
    // Generate a new namespace for complex extension if one not provided
    if (!prefix) {
      prefix = nsContext.registerNamespace(xsiType.xmlns);
    } else {
      nsContext.declareNamespace(prefix, xsiType.xmlns);
    }
    xsiType.prefix = prefix;
  }


  if (attrObj) {
    for (var attrKey in attrObj) {
      //handle complex extension separately
      if (attrKey === 'xsi_type') {
        var attrValue = attrObj[attrKey];
        attr += ' xsi:type="' + attrValue.prefix + ':' + attrValue.type + '"';
        attr += ' xmlns:' + attrValue.prefix + '="' + attrValue.xmlns + '"';

        continue;
      } else {
        attr += ' ' + attrKey + '="' + xmlEscape(attrObj[attrKey]) + '"';
      }
    }
  }

  return attr;
}
```
- example usage
```shell
...
}

var i, n;
// start building out XML string.
if (Array.isArray(obj)) {
  for (i = 0, n = obj.length; i < n; i++) {
    var item = obj[i];
    var arrayAttr = self.processAttributes(item, nsContext),
        correctOuterNsPrefix = parentNsPrefix || ns; //using the parent namespace prefix if given

    parts.push(['<', appendColon(correctOuterNsPrefix), name, arrayAttr, xmlnsAttrib, '>'].join(''));
    parts.push(self.objectToXML(item, name, nsPrefix, nsURI, false, null, schemaObject, nsContext));
    parts.push(['</', appendColon(correctOuterNsPrefix), name, '>'].join(''));
  }
} else if (typeof obj === 'object') {
...
```

#### <a name="apidoc.element.soap.WSDL.prototype.processIncludes"></a>[function <span class="apidocSignatureSpan">soap.WSDL.prototype.</span>processIncludes (callback)](#apidoc.element.soap.WSDL.prototype.processIncludes)
- description and source-code
```javascript
processIncludes = function (callback) {
  var schemas = this.definitions.schemas,
    includes = [];

  for (var ns in schemas) {
    var schema = schemas[ns];
    includes = includes.concat(schema.includes || []);
  }

  this._processNextInclude(includes, callback);
}
```
- example usage
```shell
...
  process.nextTick(function() {
    try {
fromFunc.call(self, definition);
    } catch (e) {
return self.callback(e.message);
    }

    self.processIncludes(function(err) {
var name;
if (err) {
  return self.callback(err);
}

self.definitions.deleteFixedAttrs();
var services = self.services = self.definitions.services;
...
```

#### <a name="apidoc.element.soap.WSDL.prototype.toXML"></a>[function <span class="apidocSignatureSpan">soap.WSDL.prototype.</span>toXML ()](#apidoc.element.soap.WSDL.prototype.toXML)
- description and source-code
```javascript
toXML = function () {
  return this.xml || '';
}
```
- example usage
```shell
...
"xmlns:xsi=\"http://www.w3.org/2001/XMLSchema-instance\" " +
encoding +
this.wsdl.xmlnsInEnvelope + '>' +
((self.soapHeaders || self.security) ?
  (
    "<" + envelopeKey + ":Header>" +
    (self.soapHeaders ? self.soapHeaders.join("\n") : "") +
    (self.security && !self.security.postProcess ? self.security.toXML() : "") +
    "</" + envelopeKey + ":Header>"
  )
  :
    ''
  ) +
"<" + envelopeKey + ":Body" +
(self.bodyAttributes ? self.bodyAttributes.join(' ') : '') +
...
```

#### <a name="apidoc.element.soap.WSDL.prototype.xmlToObject"></a>[function <span class="apidocSignatureSpan">soap.WSDL.prototype.</span>xmlToObject (xml, callback)](#apidoc.element.soap.WSDL.prototype.xmlToObject)
- description and source-code
```javascript
xmlToObject = function (xml, callback) {
  var self = this;
  var p = typeof callback === 'function' ? {} : sax.parser(true);
  var objectName = null;
  var root = {};
  var schema = {
    Envelope: {
      Header: {
        Security: {
          UsernameToken: {
            Username: 'string',
            Password: 'string'
          }
        }
      },
      Body: {
        Fault: {
          faultcode: 'string',
          faultstring: 'string',
          detail: 'string'
        }
      }
    }
  };
  var stack = [{name: null, object: root, schema: schema}];
  var xmlns = {};

  var refs = {}, id; // {id:{hrefs:[],obj:}, ...}

  p.onopentag = function(node) {
    var nsName = node.name;
    var attrs  = node.attributes;

    var name = splitQName(nsName).name,
      attributeName,
      top = stack[stack.length - 1],
      topSchema = top.schema,
      elementAttributes = {},
      hasNonXmlnsAttribute = false,
      hasNilAttribute = false,
      obj = {};
    var originalName = name;

    if (!objectName && top.name === 'Body' && name !== 'Fault') {
      var message = self.definitions.messages[name];
      // Support RPC/literal messages where response body contains one element named
      // after the operation + 'Response'. See http://www.w3.org/TR/wsdl#_names
      if (!message) {
        // Determine if this is request or response
        var isInput = false;
        var isOutput = false;
        if ((/Response$/).test(name)) {
          isOutput = true;
          name = name.replace(/Response$/, '');
        } else if ((/Request$/).test(name)) {
          isInput = true;
          name = name.replace(/Request$/, '');
        } else if ((/Solicit$/).test(name)) {
          isInput = true;
          name = name.replace(/Solicit$/, '');
        }
        // Look up the appropriate message as given in the portType's operations
        var portTypes = self.definitions.portTypes;
        var portTypeNames = Object.keys(portTypes);
        // Currently this supports only one portType definition.
        var portType = portTypes[portTypeNames[0]];
        if (isInput) {
          name = portType.methods[name].input.$name;
        } else {
          name = portType.methods[name].output.$name;
        }
        message = self.definitions.messages[name];
        // 'cache' this alias to speed future lookups
        self.definitions.messages[originalName] = self.definitions.messages[name];
      }

      topSchema = message.description(self.definitions);
      objectName = originalName;
    }

    if (attrs.href) {
      id = attrs.href.substr(1);
      if (!refs[id]) {
        refs[id] = {hrefs: [], obj: null};
      }
      refs[id].hrefs.push({par: top.object, key: name, obj: obj});
    }
    if (id = attrs.id) {
      if (!refs[id]) {
        refs[id] = {hrefs: [], obj: null};
      }
    }

    //Handle element attributes
    for (attributeName in attrs) {
      if (/^xmlns:|^xmlns$/.test(attributeName)) {
        xmlns[splitQName(attributeName).name] = attrs[attributeName];
        continue;
      }
      hasNonXmlnsAttribute = true;
      elementAttributes[attributeName] = attrs[attributeName];
    }

    for(attributeName in elementAttributes){
      var res = splitQName(attributeName);
      if (res.name === 'nil' && xmlns[res.prefix] === 'http://www.w3.org/2001/XMLSchema-instance') {
        hasNilAttribute = true;
        break;
      }
    }

    if (hasNonXmlnsAttribute) {
      obj[self.options.attributesKey] = elementAttributes;
    }

    // Pick up the schema for the type specified in element's xsi:type attribute.
    var xsiTypeSchema;
    var xsiType = elementAttributes['xsi:type'];
    if (xsiType) {
      var type = splitQName(xsiType);
      var typeURI;
      if (type.prefix === TNS_PREFIX) {
        // In case of xsi:type = "MyType"
        typeURI = xmlns[type.prefix] || xmlns.xmlns;
      } else {
        typeURI = xmlns[type.prefix];
      }
      var typeDef = self.findSchemaObject( ...
```
- example usage
```shell
...

  return parseSync(body, response);

}));
return;
      }

      self.wsdl.xmlToObject(response, function (error, obj) {
self.lastResponse = response;
self.lastResponseHeaders = response && response.headers;
self.lastElapsedTime = Date.now() - startTime;
self.emit('response', '<stream>', response, eid);

if (error) {
  error.response = response;
...
```



# <a name="apidoc.module.soap.WSSecurity"></a>[module soap.WSSecurity](#apidoc.module.soap.WSSecurity)

#### <a name="apidoc.element.soap.WSSecurity.WSSecurity"></a>[function <span class="apidocSignatureSpan">soap.</span>WSSecurity (username, password, options)](#apidoc.element.soap.WSSecurity.WSSecurity)
- description and source-code
```javascript
function WSSecurity(username, password, options) {
  options = options || {};
  this._username = username;
  this._password = password;
  //must account for backward compatibility for passwordType String param as well as object options defaults: passwordType = 'PasswordText
', hasTimeStamp = true
  if (typeof options === 'string') {
    this._passwordType = options ? options : 'PasswordText';
    options = {};
  } else {
    this._passwordType = options.passwordType ? options.passwordType : 'PasswordText';
  }

  if (validPasswordTypes.indexOf(this._passwordType) === -1) {
    this._passwordType = 'PasswordText';
  }

  this._hasTimeStamp = options.hasTimeStamp || typeof options.hasTimeStamp === 'boolean' ? !!options.hasTimeStamp : true;
  /*jshint eqnull:true */
  if (options.hasNonce != null) {
    this._hasNonce = !!options.hasNonce;
  }
  this._hasTokenCreated = options.hasTokenCreated || typeof options.hasTokenCreated === 'boolean' ? !!options.hasTokenCreated :
true;
  if (options.actor != null) {
    this._actor = options.actor;
  }
  if (options.mustUnderstand != null) {
    this._mustUnderstand = !!options.mustUnderstand;
  }
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.soap.WSSecurity.prototype"></a>[module soap.WSSecurity.prototype](#apidoc.module.soap.WSSecurity.prototype)

#### <a name="apidoc.element.soap.WSSecurity.prototype.toXML"></a>[function <span class="apidocSignatureSpan">soap.WSSecurity.prototype.</span>toXML ()](#apidoc.element.soap.WSSecurity.prototype.toXML)
- description and source-code
```javascript
toXML = function () {
  // avoid dependency on date formatting libraries
  function getDate(d) {
    function pad(n) {
      return n < 10 ? '0' + n : n;
    }
    return d.getUTCFullYear() + '-'
      + pad(d.getUTCMonth() + 1) + '-'
      + pad(d.getUTCDate()) + 'T'
      + pad(d.getUTCHours()) + ':'
      + pad(d.getUTCMinutes()) + ':'
      + pad(d.getUTCSeconds()) + 'Z';
  }
  var now = new Date();
  var created = getDate(now);
  var timeStampXml = '';
  if (this._hasTimeStamp) {
    var expires = getDate( new Date(now.getTime() + (1000 * 600)) );
    timeStampXml = "<wsu:Timestamp wsu:Id=\"Timestamp-"+created+"\">" +
      "<wsu:Created>"+created+"</wsu:Created>" +
      "<wsu:Expires>"+expires+"</wsu:Expires>" +
      "</wsu:Timestamp>";
  }

  var password, nonce;
  if (this._hasNonce || this._passwordType !== 'PasswordText') {
    // nonce = base64 ( sha1 ( created + random ) )
    var nHash = crypto.createHash('sha1');
    nHash.update(created + Math.random());
    nonce = nHash.digest('base64');
  }
  if (this._passwordType === 'PasswordText') {
    password = "<wsse:Password Type=\"http://docs.oasis-open.org/wss/2004/01/oasis-200401-wss-username-token-profile-1.0#PasswordText\">" + this._password + "</wsse:Password>";
    if (nonce) {
      password += "<wsse:Nonce EncodingType=\"http://docs.oasis-open.org/wss/2004/01/oasis-200401-wss-soap-message-security-1.0#
Base64Binary\">" + nonce + "</wsse:Nonce>";
    }
  } else {
    password = "<wsse:Password Type=\"http://docs.oasis-open.org/wss/2004/01/oasis-200401-wss-username-token-profile-1.0#PasswordDigest\">" + passwordDigest(nonce, created, this._password) + "</wsse:Password>" +
      "<wsse:Nonce EncodingType=\"http://docs.oasis-open.org/wss/2004/01/oasis-200401-wss-soap-message-security-1.0#Base64Binary\">" + nonce + "</wsse:Nonce>";
  }

  return "<wsse:Security " + (this._actor ? "soap:actor=\"" + this._actor + "\" " : "") +
    (this._mustUnderstand ? "soap:mustUnderstand=\"1\" " : "") +
    "xmlns:wsse=\"http://docs.oasis-open.org/wss/2004/01/oasis-200401-wss-wssecurity-secext-1.0.xsd\" xmlns:wsu=\"http://docs.oasis
-open.org/wss/2004/01/oasis-200401-wss-wssecurity-utility-1.0.xsd\">" +
    timeStampXml +
    "<wsse:UsernameToken xmlns:wsu=\"http://docs.oasis-open.org/wss/2004/01/oasis-200401-wss-wssecurity-utility-1.0.xsd\" wsu:Id
=\"SecurityToken-" + created + "\">" +
    "<wsse:Username>" + this._username + "</wsse:Username>" +
    password +
    (this._hasTokenCreated ? "<wsu:Created>" + created + "</wsu:Created>" : "") +
    "</wsse:UsernameToken>" +
    "</wsse:Security>";
}
```
- example usage
```shell
...
"xmlns:xsi=\"http://www.w3.org/2001/XMLSchema-instance\" " +
encoding +
this.wsdl.xmlnsInEnvelope + '>' +
((self.soapHeaders || self.security) ?
  (
    "<" + envelopeKey + ":Header>" +
    (self.soapHeaders ? self.soapHeaders.join("\n") : "") +
    (self.security && !self.security.postProcess ? self.security.toXML() : "") +
    "</" + envelopeKey + ":Header>"
  )
  :
    ''
  ) +
"<" + envelopeKey + ":Body" +
(self.bodyAttributes ? self.bodyAttributes.join(' ') : '') +
...
```



# <a name="apidoc.module.soap.WSSecurityCert"></a>[module soap.WSSecurityCert](#apidoc.module.soap.WSSecurityCert)

#### <a name="apidoc.element.soap.WSSecurityCert.WSSecurityCert"></a>[function <span class="apidocSignatureSpan">soap.</span>WSSecurityCert (privatePEM, publicP12PEM, password, encoding)](#apidoc.element.soap.WSSecurityCert.WSSecurityCert)
- description and source-code
```javascript
function WSSecurityCert(privatePEM, publicP12PEM, password, encoding) {
  if (!ursa) {
    throw new Error('Module ursa must be installed to use WSSecurityCert');
  }
  this.privateKey = ursa.createPrivateKey(privatePEM, password, encoding);
  this.publicP12PEM = publicP12PEM.toString().replace('-----BEGIN CERTIFICATE-----', '').replace('-----END CERTIFICATE-----', '').
replace(/(\r\n|\n|\r)/gm, '');

  this.signer = new SignedXml();
  this.signer.signingKey = this.privateKey.toPrivatePem();
  this.x509Id = "x509-" + generateId();

  var _this = this;
  this.signer.keyInfoProvider = {};
  this.signer.keyInfoProvider.getKeyInfo = function (key) {
    return wsseSecurityTokenTemplate({ x509Id: _this.x509Id });
  };
}
```
- example usage
```shell
...

WS-Security X509 Certificate support.

''' javascript
  var privateKey = fs.readFileSync(privateKeyPath);
  var publicKey = fs.readFileSync(publicKeyPath);
  var password = ''; // optional password
  var wsSecurity = new soap.WSSecurityCert(privateKey, publicKey, password, 'utf8');
  client.setSecurity(wsSecurity);
'''

_Note_: Optional dependency 'ursa' is required to be installed successfully when WSSecurityCert is used.

## Handling XML Attributes, Value and XML (wsdlOptions).
Sometimes it is necessary to override the default behaviour of 'node-soap' in order to deal with the special requirements
...
```



# <a name="apidoc.module.soap.WSSecurityCert.prototype"></a>[module soap.WSSecurityCert.prototype](#apidoc.module.soap.WSSecurityCert.prototype)

#### <a name="apidoc.element.soap.WSSecurityCert.prototype.postProcess"></a>[function <span class="apidocSignatureSpan">soap.WSSecurityCert.prototype.</span>postProcess (xml, envelopeKey)](#apidoc.element.soap.WSSecurityCert.prototype.postProcess)
- description and source-code
```javascript
postProcess = function (xml, envelopeKey) {
  this.created = generateCreated();
  this.expires = generateExpires();

  var secHeader = wsseSecurityHeaderTemplate({
    binaryToken: this.publicP12PEM,
    created: this.created,
    expires: this.expires,
    id: this.x509Id
  });

  var xmlWithSec = insertStr(secHeader, xml, xml.indexOf('</soap:Header>'));

  var references = ["http://www.w3.org/2000/09/xmldsig#enveloped-signature",
    "http://www.w3.org/2001/10/xml-exc-c14n#"];

  this.signer.addReference("//*[name(.)='" + envelopeKey + ":Body']", references);
  this.signer.addReference("//*[name(.)='wsse:Security']/*[local-name(.)='Timestamp']", references);

  this.signer.computeSignature(xmlWithSec);

  return insertStr(this.signer.getSignatureXml(), xmlWithSec, xmlWithSec.indexOf('</wsse:Security>'));
}
```
- example usage
```shell
...
  (self.security && self.security.postProcess ? ' Id="_0"' : '') +
  ">" +
  message +
  "</" + envelopeKey + ":Body>" +
  "</" + envelopeKey + ":Envelope>";

if(self.security && self.security.postProcess){
  xml = self.security.postProcess(xml, envelopeKey);
}

self.lastMessage = message;
self.lastRequest = xml;
self.lastEndpoint = location;

var eid = options.exchangeId || uuid.v4();
...
```



# <a name="apidoc.module.soap.client"></a>[module soap.client](#apidoc.module.soap.client)

#### <a name="apidoc.element.soap.client.Client"></a>[function <span class="apidocSignatureSpan">soap.client.</span>Client (wsdl, endpoint, options)](#apidoc.element.soap.client.Client)
- description and source-code
```javascript
Client = function (wsdl, endpoint, options) {
  events.EventEmitter.call(this);
  options = options || {};
  this.wsdl = wsdl;
  this._initializeOptions(options);
  this._initializeServices(endpoint);
  this.httpClient = options.httpClient || new HttpClient(options);
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.soap.nscontext"></a>[module soap.nscontext](#apidoc.module.soap.nscontext)

#### <a name="apidoc.element.soap.nscontext.nscontext"></a>[function <span class="apidocSignatureSpan">soap.</span>nscontext ()](#apidoc.element.soap.nscontext.nscontext)
- description and source-code
```javascript
function NamespaceContext() {
  if (!(this instanceof NamespaceContext)) {
    return new NamespaceContext();
  }
  this.scopes = [];
  this.pushContext();
  this.prefixCount = 0;
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.soap.nscontext.prototype"></a>[module soap.nscontext.prototype](#apidoc.module.soap.nscontext.prototype)

#### <a name="apidoc.element.soap.nscontext.prototype.addNamespace"></a>[function <span class="apidocSignatureSpan">soap.nscontext.prototype.</span>addNamespace (prefix, nsUri, localOnly)](#apidoc.element.soap.nscontext.prototype.addNamespace)
- description and source-code
```javascript
addNamespace = function (prefix, nsUri, localOnly) {
  if (this.getNamespaceURI(prefix, localOnly) === nsUri) {
    return false;
  }
  if (this.currentScope) {
    this.currentScope.namespaces[prefix] = {
      uri: nsUri,
      prefix: prefix,
      declared: false
    };
    return true;
  }
  return false;
}
```
- example usage
```shell
...
     prefix = 'ns' + (++this.prefixCount);
     if (!this.getNamespaceURI(prefix)) {
       // The prefix is not used
       break;
     }
   }
 }
 this.addNamespace(prefix, nsUri, true);
 return prefix;
};

/**
* Declare a namespace prefix/uri mapping
* @param {String} prefix Namespace prefix
* @param {String} nsUri Namespace URI
...
```

#### <a name="apidoc.element.soap.nscontext.prototype.declareNamespace"></a>[function <span class="apidocSignatureSpan">soap.nscontext.prototype.</span>declareNamespace (prefix, nsUri)](#apidoc.element.soap.nscontext.prototype.declareNamespace)
- description and source-code
```javascript
declareNamespace = function (prefix, nsUri) {
  if (this.currentScope) {
    var mapping = this.currentScope.getNamespaceMapping(prefix);
    if (mapping && mapping.uri === nsUri && mapping.declared) {
      return false;
    }
    this.currentScope.namespaces[prefix] = {
      uri: nsUri,
      prefix: prefix,
      declared: true
    };
    return true;
  }
  return false;
}
```
- example usage
```shell
...
    // only add default namespace if the schema elementFormDefault is qualified
    if (qualified || soapHeader) xmlnsAttrib += ' xmlns="' + nsURI + '"';
  }
}

if (!nsContext) {
  nsContext = new NamespaceContext();
  nsContext.declareNamespace(nsPrefix, nsURI);
} else {
  nsContext.pushContext();
}

// explicitly use xmlns attribute if available
if (xmlnsAttr && !(self.options.overrideRootElement && self.options.overrideRootElement.xmlnsAttributes)) {
  xmlnsAttrib = xmlnsAttr;
...
```

#### <a name="apidoc.element.soap.nscontext.prototype.getNamespaceURI"></a>[function <span class="apidocSignatureSpan">soap.nscontext.prototype.</span>getNamespaceURI (prefix, localOnly)](#apidoc.element.soap.nscontext.prototype.getNamespaceURI)
- description and source-code
```javascript
getNamespaceURI = function (prefix, localOnly) {
  return this.currentScope && this.currentScope.getNamespaceURI(prefix, localOnly);
}
```
- example usage
```shell
...
      return 'http://www.w3.org/2000/xmlns/';
    default:
      var nsUri = this.namespaces[prefix];
      /*jshint -W116 */
      if (nsUri != null) {
        return nsUri.uri;
      } else if (!localOnly && this.parent) {
        return this.parent.getNamespaceURI(prefix);
      } else {
        return null;
      }
  }
};

NamespaceScope.prototype.getNamespaceMapping = function(prefix) {
...
```

#### <a name="apidoc.element.soap.nscontext.prototype.getPrefix"></a>[function <span class="apidocSignatureSpan">soap.nscontext.prototype.</span>getPrefix (nsUri, localOnly)](#apidoc.element.soap.nscontext.prototype.getPrefix)
- description and source-code
```javascript
getPrefix = function (nsUri, localOnly) {
  return this.currentScope && this.currentScope.getPrefix(nsUri, localOnly);
}
```
- example usage
```shell
...
    default:
      for (var p in this.namespaces) {
        if (this.namespaces[p].uri === nsUri) {
          return p;
        }
      }
      if (!localOnly && this.parent) {
        return this.parent.getPrefix(nsUri);
      } else {
        return null;
      }
  }
};

/**
...
```

#### <a name="apidoc.element.soap.nscontext.prototype.popContext"></a>[function <span class="apidocSignatureSpan">soap.nscontext.prototype.</span>popContext ()](#apidoc.element.soap.nscontext.prototype.popContext)
- description and source-code
```javascript
popContext = function () {
  var scope = this.scopes.pop();
  if (scope) {
    this.currentScope = scope.parent;
  } else {
    this.currentScope = null;
  }
  return scope;
}
```
- example usage
```shell
...
if (!obj.hasOwnProperty(name)) continue;
//don't process attributes as element
if (name === self.options.attributesKey) {
  continue;
}
//Its the value of a xml object. Return it directly.
if (name === self.options.xmlKey){
  nsContext.popContext();
  return obj[name];
}
//Its the value of an item. Return it directly.
if (name === self.options.valueKey) {
  nsContext.popContext();
  return xmlEscape(obj[name]);
}
...
```

#### <a name="apidoc.element.soap.nscontext.prototype.pushContext"></a>[function <span class="apidocSignatureSpan">soap.nscontext.prototype.</span>pushContext ()](#apidoc.element.soap.nscontext.prototype.pushContext)
- description and source-code
```javascript
pushContext = function () {
  var scope = new NamespaceScope(this.currentScope);
  this.scopes.push(scope);
  this.currentScope = scope;
  return scope;
}
```
- example usage
```shell
...
* @constructor
*/
function NamespaceContext() {
 if (!(this instanceof NamespaceContext)) {
   return new NamespaceContext();
 }
 this.scopes = [];
 this.pushContext();
 this.prefixCount = 0;
}

/**
* Look up the namespace URI by prefix
* @param {String} prefix Namespace prefix
* @param {Boolean} [localOnly] Search current scope only
...
```

#### <a name="apidoc.element.soap.nscontext.prototype.registerNamespace"></a>[function <span class="apidocSignatureSpan">soap.nscontext.prototype.</span>registerNamespace (nsUri)](#apidoc.element.soap.nscontext.prototype.registerNamespace)
- description and source-code
```javascript
registerNamespace = function (nsUri) {
  var prefix = this.getPrefix(nsUri);
  if (prefix) {
    // If the namespace has already mapped to a prefix
    return prefix;
  } else {
    // Try to generate a unique namespace
    while (true) {
      prefix = 'ns' + (++this.prefixCount);
      if (!this.getNamespaceURI(prefix)) {
        // The prefix is not used
        break;
      }
    }
  }
  this.addNamespace(prefix, nsUri, true);
  return prefix;
}
```
- example usage
```shell
...
var elementQName = childSchemaObject.$ref || childSchemaObject.$name;
if (elementQName) {
  elementQName = splitQName(elementQName);
  childName = elementQName.name;
  if (elementQName.prefix === TNS_PREFIX) {
    // Local element
    childNsURI = childSchemaObject.$targetNamespace;
    childNsPrefix = nsContext.registerNamespace(childNsURI);
    if (this.isIgnoredNameSpace(childNsPrefix)) {
      childNsPrefix = nsPrefix;
    }
  } else {
    childNsPrefix = elementQName.prefix;
    if (this.isIgnoredNameSpace(childNsPrefix)) {
      childNsPrefix = nsPrefix;
...
```



# <a name="apidoc.module.soap.security"></a>[module soap.security](#apidoc.module.soap.security)

#### <a name="apidoc.element.soap.security.BasicAuthSecurity"></a>[function <span class="apidocSignatureSpan">soap.security.</span>BasicAuthSecurity (username, password, defaults)](#apidoc.element.soap.security.BasicAuthSecurity)
- description and source-code
```javascript
function BasicAuthSecurity(username, password, defaults) {
  this._username = username;
  this._password = password;
  this.defaults = {};
  _.merge(this.defaults, defaults);
}
```
- example usage
```shell
...
as well.  The interface is quite simple. Each protocol defines 2 methods:
* 'addOptions' - a method that accepts an options arg that is eventually passed directly to 'request'
* 'toXML' - a method that returns a string of XML.

### BasicAuthSecurity

''' javascript
  client.setSecurity(new soap.BasicAuthSecurity('username', 'password'));
'''

### BearerSecurity

''' javascript
  client.setSecurity(new soap.BearerSecurity('token'));
'''
...
```

#### <a name="apidoc.element.soap.security.BearerSecurity"></a>[function <span class="apidocSignatureSpan">soap.security.</span>BearerSecurity (token, defaults)](#apidoc.element.soap.security.BearerSecurity)
- description and source-code
```javascript
function BearerSecurity(token, defaults) {
	this._token = token;
	this.defaults = {};
	_.merge(this.defaults, defaults);
}
```
- example usage
```shell
...
''' javascript
  client.setSecurity(new soap.BasicAuthSecurity('username', 'password'));
'''

### BearerSecurity

''' javascript
  client.setSecurity(new soap.BearerSecurity('token'));
'''

### ClientSSLSecurity

_Note_: If you run into issues using this protocol, consider passing these options
as default request options to the constructor:
* 'rejectUnauthorized: false'
...
```

#### <a name="apidoc.element.soap.security.ClientSSLSecurity"></a>[function <span class="apidocSignatureSpan">soap.security.</span>ClientSSLSecurity (key, cert, ca, defaults)](#apidoc.element.soap.security.ClientSSLSecurity)
- description and source-code
```javascript
function ClientSSLSecurity(key, cert, ca, defaults) {
  if (key) {
    if(Buffer.isBuffer(key)) {
      this.key = key;
    } else if (typeof key === 'string') {
      this.key = fs.readFileSync(key);
    } else {
      throw new Error('key should be a buffer or a string!');
    }
  }

  if (cert) {
    if(Buffer.isBuffer(cert)) {
      this.cert = cert;
    } else if (typeof cert === 'string') {
      this.cert = fs.readFileSync(cert);
    } else {
      throw new Error('cert should be a buffer or a string!');
    }
  }

  if (ca) {
    if(Buffer.isBuffer(ca) || Array.isArray(ca)) {
      this.ca = ca;
    } else if (typeof ca === 'string') {
      this.ca = fs.readFileSync(ca);
    } else {
      defaults = ca;
      this.ca = null;
    }
  }

  this.defaults = {};
  _.merge(this.defaults, defaults);
}
```
- example usage
```shell
...
_Note_: If you run into issues using this protocol, consider passing these options
as default request options to the constructor:
* 'rejectUnauthorized: false'
* 'strictSSL: false'
* 'secureOptions: constants.SSL_OP_NO_TLSv1_2' (this is likely needed for node >= 10.0)

''' javascript
  client.setSecurity(new soap.ClientSSLSecurity(
    '/path/to/key'
    , '/path/to/cert'
    , {/*default request options*/}
  ));
'''

### WSSecurity
...
```

#### <a name="apidoc.element.soap.security.ClientSSLSecurityPFX"></a>[function <span class="apidocSignatureSpan">soap.security.</span>ClientSSLSecurityPFX (pfx, passphrase, defaults)](#apidoc.element.soap.security.ClientSSLSecurityPFX)
- description and source-code
```javascript
function ClientSSLSecurityPFX(pfx, passphrase, defaults) {
  if (typeof passphrase === 'object') {
    defaults = passphrase;
  }
  if (pfx) {
    if (Buffer.isBuffer(pfx)) {
      this.pfx = pfx;
    } else if (typeof pfx === 'string') {
      this.pfx = fs.readFileSync(pfx);
    } else {
      throw new Error('supplied pfx file should be a buffer or a file location');
    }
  }

  if (passphrase) {
    if (typeof passphrase === 'string') {
      this.passphrase = passphrase;
    }
  }
  this.defaults = {};
  _.merge(this.defaults, defaults);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.soap.security.WSSecurity"></a>[function <span class="apidocSignatureSpan">soap.security.</span>WSSecurity (username, password, options)](#apidoc.element.soap.security.WSSecurity)
- description and source-code
```javascript
function WSSecurity(username, password, options) {
  options = options || {};
  this._username = username;
  this._password = password;
  //must account for backward compatibility for passwordType String param as well as object options defaults: passwordType = 'PasswordText
', hasTimeStamp = true
  if (typeof options === 'string') {
    this._passwordType = options ? options : 'PasswordText';
    options = {};
  } else {
    this._passwordType = options.passwordType ? options.passwordType : 'PasswordText';
  }

  if (validPasswordTypes.indexOf(this._passwordType) === -1) {
    this._passwordType = 'PasswordText';
  }

  this._hasTimeStamp = options.hasTimeStamp || typeof options.hasTimeStamp === 'boolean' ? !!options.hasTimeStamp : true;
  /*jshint eqnull:true */
  if (options.hasNonce != null) {
    this._hasNonce = !!options.hasNonce;
  }
  this._hasTokenCreated = options.hasTokenCreated || typeof options.hasTokenCreated === 'boolean' ? !!options.hasTokenCreated :
true;
  if (options.actor != null) {
    this._actor = options.actor;
  }
  if (options.mustUnderstand != null) {
    this._mustUnderstand = !!options.mustUnderstand;
  }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.soap.security.WSSecurityCert"></a>[function <span class="apidocSignatureSpan">soap.security.</span>WSSecurityCert (privatePEM, publicP12PEM, password, encoding)](#apidoc.element.soap.security.WSSecurityCert)
- description and source-code
```javascript
function WSSecurityCert(privatePEM, publicP12PEM, password, encoding) {
  if (!ursa) {
    throw new Error('Module ursa must be installed to use WSSecurityCert');
  }
  this.privateKey = ursa.createPrivateKey(privatePEM, password, encoding);
  this.publicP12PEM = publicP12PEM.toString().replace('-----BEGIN CERTIFICATE-----', '').replace('-----END CERTIFICATE-----', '').
replace(/(\r\n|\n|\r)/gm, '');

  this.signer = new SignedXml();
  this.signer.signingKey = this.privateKey.toPrivatePem();
  this.x509Id = "x509-" + generateId();

  var _this = this;
  this.signer.keyInfoProvider = {};
  this.signer.keyInfoProvider.getKeyInfo = function (key) {
    return wsseSecurityTokenTemplate({ x509Id: _this.x509Id });
  };
}
```
- example usage
```shell
...

WS-Security X509 Certificate support.

''' javascript
  var privateKey = fs.readFileSync(privateKeyPath);
  var publicKey = fs.readFileSync(publicKeyPath);
  var password = ''; // optional password
  var wsSecurity = new soap.WSSecurityCert(privateKey, publicKey, password, 'utf8');
  client.setSecurity(wsSecurity);
'''

_Note_: Optional dependency 'ursa' is required to be installed successfully when WSSecurityCert is used.

## Handling XML Attributes, Value and XML (wsdlOptions).
Sometimes it is necessary to override the default behaviour of 'node-soap' in order to deal with the special requirements
...
```



# <a name="apidoc.module.soap.server"></a>[module soap.server](#apidoc.module.soap.server)

#### <a name="apidoc.element.soap.server.Server"></a>[function <span class="apidocSignatureSpan">soap.server.</span>Server (server, path, services, wsdl, options)](#apidoc.element.soap.server.Server)
- description and source-code
```javascript
Server = function (server, path, services, wsdl, options) {
  var self = this;

  events.EventEmitter.call(this);

  options = options || {};
  this.path = path;
  this.services = services;
  this.wsdl = wsdl;
  this.suppressStack = options && options.suppressStack;

  if (path[path.length - 1] !== '/')
    path += '/';
  wsdl.onReady(function (err) {
    if (typeof server.route === 'function' && typeof server.use === 'function') {
      //handle only the required URL path for express server
      server.route(path).all(function (req, res, next) {
        if (typeof self.authorizeConnection === 'function') {
          if (!self.authorizeConnection(req)) {
            res.end();
            return;
          }
        }
        self._requestListener(req, res);
      });
    } else {
      var listeners = server.listeners('request').slice();
      server.removeAllListeners('request');
      server.addListener('request', function (req, res) {
        if (typeof self.authorizeConnection === 'function') {
          if (!self.authorizeConnection(req)) {
            res.end();
            return;
          }
        }
        var reqPath = url.parse(req.url).pathname;
        if (reqPath[reqPath.length - 1] !== '/') {
          reqPath += '/';
        }
        if (path === reqPath) {
          self._requestListener(req, res);
        } else {
          for (var i = 0, len = listeners.length; i < len; i++) {
            listeners[i].call(this, req, res);
          }
        }
      });
    }
  });

  this._initializeOptions(options);
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.soap.soap_stub"></a>[module soap.soap_stub](#apidoc.module.soap.soap_stub)

#### <a name="apidoc.element.soap.soap_stub.createClient"></a>[function <span class="apidocSignatureSpan">soap.soap_stub.</span>createClient (wsdlUrl, options, cb)](#apidoc.element.soap.soap_stub.createClient)
- description and source-code
```javascript
function createClient(wsdlUrl, options, cb) {
  if (!cb) {
    cb = options;
    options = {};
  }

  if (this.errOnCreateClient) {
    return setTimeout(cb.bind(null, new Error('forced error on createClient')));
  }

  var client = getStub(wsdlUrl);

  if (client) {
    resetStubbedMethods(client);
    setTimeout(cb.bind(null, null, client));
  } else {
    setTimeout(cb.bind(null, new Error('no client stubbed for ' + wsdlUrl)));
  }
}
```
- example usage
```shell
...
<!-- DON'T EDIT THIS SECTION, INSTEAD RE-RUN doctoc TO UPDATE -->


- [Features:](#features)
- [Install](#install)
- [Where can I file an issue?](#where-can-i-file-an-issue)
- [Module](#module)
- [soap.createClient(url[, options], callback) - create a new SOAP client from a WSDL url. Also supports a local filesystem path
.](#soapcreateclienturl-options-callback---create-a-new-soap-client-from-a-wsdl-url-also-supports-a-local-filesystem-path)
- [soap.listen(*server*, *path*, *services*, *wsdl*) - create a new SOAP server that listens on *path* and provides *services*.](#
soaplistenserver-path-services-wsdl---create-a-new-soap-server-that-listens-on-path-and-provides-services)
- [Options](#options)
- [Server Logging](#server-logging)
- [Server Events](#server-events)
- [SOAP Fault](#soap-fault)
- [Server security example using PasswordDigest](#server-security-example-using-passworddigest)
- [Server connection authorization](#server-connection-authorization)
...
```

#### <a name="apidoc.element.soap.soap_stub.createErroringStub"></a>[function <span class="apidocSignatureSpan">soap.soap_stub.</span>createErroringStub (err)](#apidoc.element.soap.soap_stub.createErroringStub)
- description and source-code
```javascript
function createErroringStub(err) {
  return function() {
    this.args.forEach(function(argSet) {
      setTimeout(argSet[1].bind(null, err));
    });
    this.yields(err);
  };
}
```
- example usage
```shell
...
var soapStub = require('soap/soap-stub');

var urlMyApplicationWillUseWithCreateClient = 'http://path-to-my-wsdl';
var clientStub = {
  SomeOperation: sinon.stub()
};

clientStub.SomeOperation.respondWithError = soapStub.createErroringStub({..error json...});
clientStub.SomeOperation.respondWithSuccess = soapStub.createRespondingStub({..success json...});

soapStub.registerClient('my client alias', urlMyApplicationWillUseWithCreateClient, clientStub);

// test.js
var soapStub = require('soap/soap-stub');
...
```

#### <a name="apidoc.element.soap.soap_stub.createRespondingStub"></a>[function <span class="apidocSignatureSpan">soap.soap_stub.</span>createRespondingStub (object, body)](#apidoc.element.soap.soap_stub.createRespondingStub)
- description and source-code
```javascript
function createRespondingStub(object, body) {
  return function() {
    this.args.forEach(function(argSet) {
      setTimeout(argSet[1].bind(null, null, object));
    });
    this.yields(null, object, body);
  };
}
```
- example usage
```shell
...

var urlMyApplicationWillUseWithCreateClient = 'http://path-to-my-wsdl';
var clientStub = {
  SomeOperation: sinon.stub()
};

clientStub.SomeOperation.respondWithError = soapStub.createErroringStub({..error json...});
clientStub.SomeOperation.respondWithSuccess = soapStub.createRespondingStub({..success json...});

soapStub.registerClient('my client alias', urlMyApplicationWillUseWithCreateClient, clientStub);

// test.js
var soapStub = require('soap/soap-stub');

describe('myService', function() {
...
```

#### <a name="apidoc.element.soap.soap_stub.getStub"></a>[function <span class="apidocSignatureSpan">soap.soap_stub.</span>getStub (aliasOrWsdlUrl)](#apidoc.element.soap.soap_stub.getStub)
- description and source-code
```javascript
function getStub(aliasOrWsdlUrl) {
  return aliasedClientStubs[aliasOrWsdlUrl] || clientStubs[aliasOrWsdlUrl];
}
```
- example usage
```shell
...
var soapStub = require('soap/soap-stub');

describe('myService', function() {
var clientStub;
var myService;

beforeEach(function() {
  clientStub = soapStub.getStub('my client alias');
  soapStub.reset();
  myService.init(clientStub);
});

describe('failures', function() {
  beforeEach(function() {
    clientStub.SomeOperation.respondWithError();
...
```

#### <a name="apidoc.element.soap.soap_stub.registerClient"></a>[function <span class="apidocSignatureSpan">soap.soap_stub.</span>registerClient (alias, urlToWsdl, clientStub)](#apidoc.element.soap.soap_stub.registerClient)
- description and source-code
```javascript
function registerClient(alias, urlToWsdl, clientStub) {
  aliasedClientStubs[alias] = clientStub;
  clientStubs[urlToWsdl] = clientStub;
}
```
- example usage
```shell
...
var clientStub = {
SomeOperation: sinon.stub()
};

clientStub.SomeOperation.respondWithError = soapStub.createErroringStub({..error json...});
clientStub.SomeOperation.respondWithSuccess = soapStub.createRespondingStub({..success json...});

soapStub.registerClient('my client alias', urlMyApplicationWillUseWithCreateClient, clientStub);

// test.js
var soapStub = require('soap/soap-stub');

describe('myService', function() {
var clientStub;
var myService;
...
```

#### <a name="apidoc.element.soap.soap_stub.reset"></a>[function <span class="apidocSignatureSpan">soap.soap_stub.</span>reset ()](#apidoc.element.soap.soap_stub.reset)
- description and source-code
```javascript
function reset() {
  _.forEach(clientStubs, resetStubbedMethods);
  this.errOnCreateClient = false;
}
```
- example usage
```shell
...

describe('myService', function() {
var clientStub;
var myService;

beforeEach(function() {
  clientStub = soapStub.getStub('my client alias');
  soapStub.reset();
  myService.init(clientStub);
});

describe('failures', function() {
  beforeEach(function() {
    clientStub.SomeOperation.respondWithError();
  });
...
```



# <a name="apidoc.module.soap.utils"></a>[module soap.utils](#apidoc.module.soap.utils)

#### <a name="apidoc.element.soap.utils.findPrefix"></a>[function <span class="apidocSignatureSpan">soap.utils.</span>findPrefix (xmlnsMapping, nsURI)](#apidoc.element.soap.utils.findPrefix)
- description and source-code
```javascript
findPrefix = function (xmlnsMapping, nsURI) {
  for (var n in xmlnsMapping) {
    if (n === TNS_PREFIX) continue;
    if (xmlnsMapping[n] === nsURI) {
      return n;
    }
  }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.soap.utils.passwordDigest"></a>[function <span class="apidocSignatureSpan">soap.utils.</span>passwordDigest (nonce, created, password)](#apidoc.element.soap.utils.passwordDigest)
- description and source-code
```javascript
function passwordDigest(nonce, created, password) {
  // digest = base64 ( sha1 ( nonce + created + password ) )
  var pwHash = crypto.createHash('sha1');
  var rawNonce = new Buffer(nonce || '', 'base64').toString('binary');
  pwHash.update(rawNonce + created + password);
  return pwHash.digest('base64');
}
```
- example usage
```shell
...

''' javascript
  server = soap.listen(...)
  server.authenticate = function(security) {
    var created, nonce, password, user, token;
    token = security.UsernameToken, user = token.Username,
            password = token.Password, nonce = token.Nonce, created = token.Created;
    return user === 'user' && password === soap.passwordDigest(nonce, created, 'password');
  };
'''

### Server connection authorization

The 'server.authorizeConnection' method is called prior to the soap service method.
If the method is defined and returns 'false' then the incoming connection is
...
```



# <a name="apidoc.module.soap.wsdl"></a>[module soap.wsdl](#apidoc.module.soap.wsdl)

#### <a name="apidoc.element.soap.wsdl.WSDL"></a>[function <span class="apidocSignatureSpan">soap.wsdl.</span>WSDL (definition, uri, options)](#apidoc.element.soap.wsdl.WSDL)
- description and source-code
```javascript
WSDL = function (definition, uri, options) {
  var self = this,
      fromFunc;

  this.uri = uri;
  this.callback = function() {
  };
  this._includesWsdl = [];

  // initialize WSDL cache
  this.WSDL_CACHE = (options || {}).WSDL_CACHE || {};

  this._initializeOptions(options);

  if (typeof definition === 'string') {
    definition = stripBom(definition);
    fromFunc = this._fromXML;
  }
  else if (typeof definition === 'object') {
    fromFunc = this._fromServices;
  }
  else {
    throw new Error('WSDL constructor takes either an XML string or service definition');
  }

  process.nextTick(function() {
    try {
      fromFunc.call(self, definition);
    } catch (e) {
      return self.callback(e.message);
    }

    self.processIncludes(function(err) {
      var name;
      if (err) {
        return self.callback(err);
      }

      self.definitions.deleteFixedAttrs();
      var services = self.services = self.definitions.services;
      if (services) {
        for (name in services) {
          services[name].postProcess(self.definitions);
        }
      }
      var complexTypes = self.definitions.complexTypes;
      if (complexTypes) {
        for (name in complexTypes) {
          complexTypes[name].deleteFixedAttrs();
        }
      }

      // for document style, for every binding, prepare input message element name to (methodName, output message element name)
mapping
      var bindings = self.definitions.bindings;
      for (var bindingName in bindings) {
        var binding = bindings[bindingName];
        if (typeof binding.style === 'undefined') {
          binding.style = 'document';
        }
        if (binding.style !== 'document')
          continue;
        var methods = binding.methods;
        var topEls = binding.topElements = {};
        for (var methodName in methods) {
          if (methods[methodName].input) {
            var inputName = methods[methodName].input.$name;
            var outputName="";
            if(methods[methodName].output )
              outputName = methods[methodName].output.$name;
            topEls[inputName] = {"methodName": methodName, "outputName": outputName};
          }
        }
      }

      // prepare soap envelope xmlns definition string
      self.xmlnsInEnvelope = self._xmlnsMap();

      self.callback(err, self);
    });

  });
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.soap.wsdl.open_wsdl"></a>[function <span class="apidocSignatureSpan">soap.wsdl.</span>open_wsdl (uri, options, callback)](#apidoc.element.soap.wsdl.open_wsdl)
- description and source-code
```javascript
function open_wsdl(uri, options, callback) {
  if (typeof options === 'function') {
    callback = options;
    options = {};
  }

  // initialize cache when calling open_wsdl directly
  var WSDL_CACHE = options.WSDL_CACHE || {};
  var request_headers = options.wsdl_headers;
  var request_options = options.wsdl_options;

  var wsdl;
  if (!/^https?:/.test(uri)) {
    debug('Reading file: %s', uri);
    fs.readFile(uri, 'utf8', function(err, definition) {
      if (err) {
        callback(err);
      }
      else {
        wsdl = new WSDL(definition, uri, options);
        WSDL_CACHE[ uri ] = wsdl;
        wsdl.WSDL_CACHE = WSDL_CACHE;
        wsdl.onReady(callback);
      }
    });
  }
  else {
    debug('Reading url: %s', uri);
    var httpClient = options.httpClient || new HttpClient(options);
    httpClient.request(uri, null /* options */, function(err, response, definition) {
      if (err) {
        callback(err);
      } else if (response && response.statusCode === 200) {
        wsdl = new WSDL(definition, uri, options);
        WSDL_CACHE[ uri ] = wsdl;
        wsdl.WSDL_CACHE = WSDL_CACHE;
        wsdl.onReady(callback);
      } else {
        callback(new Error('Invalid WSDL URL: ' + uri + "\n\n\r Code: " + response.statusCode + "\n\n\r Response Body: " + response
.body));
      }
    }, request_headers, request_options);
  }

  return wsdl;
}
```
- example usage
```shell
n/a
```



# misc
- this document was created with [utility2](https://github.com/kaizhu256/node-utility2)
