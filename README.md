<p align="center">
  <img src="./logo.svg" alt="HAPI FHIR AU Starter Project" width="400"/>
</p>

<h1 align="center">HAPI FHIR JPA Server Starter Project</h1>

<p align="center">
  <b>A fork of the HAPI FHIR JPA Server Starter Project.</b> <br> <br>
  <b>The fork is configured to sync with the upstream repository.</b> <br>
</p>

![divider](./divider.png)


## ❯ Quick Start

* [Quick Start Guide](docs/quick-start-guide)

## ❯ Screen Shots

Home (Welcome) Page

<p align="center">
  <img src="https://github.com/Robinyo/hapi-fhir-jpaserver-starter/blob/master/docs/screen-shots/welcome.png">
</p>

## ❯ Web Testpage Overlay

You can customise the Web Testpage Overlay by modifying the templates in the `src/main/webapp/WEB-INF/templates` directory.

For example:

<p align="center">
  <img src="https://github.com/Robinyo/hapi-fhir-jpaserver-starter/blob/master/docs/screen-shots/web-testpage-overlay.png">
</p>

## ❯ FHIR Implementation Guides

A FHIR Implementation Guide can be used to seed a FHIR data store:

```
hapi:
  fhir:
    default_encoding: json
    implementationguides:
      au_core:
        name: hl7.fhir.au.core
        version: 1.0.0-preview
        reloadExisting: false
        installMode: STORE_AND_INSTALL
        packageUrl: https://hl7.org.au/fhir/core/package.tgz
        fetchDependencies: true
    logical_urls:
      - http://hl7.org.au/*
```

For example:

<p align="center">
  <img src="https://github.com/Robinyo/hapi-fhir-jpaserver-starter/blob/master/docs/screen-shots/resources-au-core-1.0.0-preview.png">
</p>

## ❯ MCP Server

You can enable MCP capabilities by setting the `spring.ai.mcp.server.enabled` to `true`. 

For example:

```
server:
  max-http-request-header-size: 64KB
spring:
  ai:
    mcp:
      server:
        enabled: true
  main:
    banner-mode: off
hapi:
  fhir:
    fhir_version: R4
    tester:
      home:
        name: Local Tester
        server_address: 'http://localhost:8080/fhir'
        refuse_to_fetch_third_party_urls: false
        fhir_version: R4
```

## ❯ MCP Client

Claude for Desktop is a popular MCP Client.

We can configure Claude for Desktop to use HAPI FHIR's MCP server by updating its configuration file.

For example:

```
"mcpServers": {
  "hapi": {
    "command": "npx",
      "args": [
        "mcp-remote@latest",
        "http://localhost:8080/mcp/messages"
    ]
  }
}
```

Restart Claude for Desktop and then click on the 'Search and tools' button.

You should see something like:

<p align="center">
  <img src="https://github.com/Robinyo/hapi-fhir-jpaserver-starter/blob/master/docs/screen-shots/search-and-tools.png">
</p>

![divider](./divider.png)

## ❯ Resources

* Rob Ferguson's blog: [Getting Started with HAPI FHIR](https://rob-ferguson.me/getting-started-with-hapi-fhir/)
* Rob Ferguson's blog: [HAPI FHIR and FHIR Implementation Guides](https://rob-ferguson.me/hapi-fhir-and-fhir-implementation-guides/)
* Rob Ferguson's blog: [HAPI FHIR and AU Core Test Data](https://rob-ferguson.me/hapi-fhir-and-au-core-test-data/)
