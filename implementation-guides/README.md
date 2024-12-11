# Implementation Guides

Australian Base IG (FHIR IG)

https://hl7.org.au/fhir/history.html

--

https://groups.google.com/g/hapi-fhir/c/4Wff9CyZLi0/m/rOZFLzLYAgAJ

You don't need to load the IG in order to use the tags it describes - HAPI will accept and index any tags you send it, 
and you can search by those tags using the _tag parameter too. Loading the IG is only necessary if you want to validate 
your resources against that IG.

How you do that really depends on your architecture and how you want things to work, but one example is 
here: https://hapifhir.io/hapi-fhir/docs/validation/instance_validator.html#packages. 

If you're using the JPA server you'd want to specify your package in the YAML config to be loaded on startup.

Validating Using Packages

When using the HAPI FHIR JPA Server you can simply upload your packages into the JPA Server package registry and the contents will be made available to the validator.

https://hl7.org.au/fhir/core/1.0.0-ballot/index.html

https://hl7.org.au/fhir/core/1.0.0-ballot/downloads.html

https://hl7.org.au/fhir/core/1.0.0-ballot/examples.html

--

https://hl7.org.au/fhir/4.1.0/guidance.html

# HL7 AU FHIR Test Data

https://github.com/hl7au/au-fhir-test-data

Implementation Guide install examples
