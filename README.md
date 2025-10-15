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

![divider](./divider.png)

## ❯ Resources

* Rob Ferguson's blog: [Getting Started with HAPI FHIR](https://rob-ferguson.me/getting-started-with-hapi-fhir/)
* Rob Ferguson's blog: [HAPI FHIR and FHIR Implementation Guides](https://rob-ferguson.me/hapi-fhir-and-fhir-implementation-guides/)
* Rob Ferguson's blog: [HAPI FHIR and AU Core Test Data](https://rob-ferguson.me/hapi-fhir-and-au-core-test-data/)
