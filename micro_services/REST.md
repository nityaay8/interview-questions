## What is REST
https://www.geeksforgeeks.org/rest-api-architectural-constraints/

https://www.codecademy.com/article/what-is-rest

## what is REST
Representational state transfer (REST) is a software architectural style that describes a uniform interface between physically separate components, often across the Internet in a Client-Server architecture. REST defines four interface constraints:

1. Identification of resources
2. Manipulation of resources
3. Self-descriptive messages and
4. hypermedia as the engine of application state[1]


## SOAP vs REST web services

| Parameter | SOAP | REST |
|-----------|------|------|
|Acronym    |SOAP stands for simple object access protocol|REST stands for REpresentational State Transfer|
|Protocol vs Architectural style|SOAP is a standard protocol to create web services|Rest is architectural style to create web services.|
|Contract|Client and Server are bind with WSDL contract|There is no contract between client and Server.|
|Format Support|SOAP supports only XML format|REST web services supports XML, json and plain text etc.|
|Maintainability|SOAP web services are hard to maintain as if we do any changes in WSDL , we need to create client stub again|REST web services are generally easy to maintain.|
|Service interfaces vs URI|SOAP uses Service interfaces to expose business logic|Rest uses URI to expose business logic|
|Security|SOAP has its own security : WS-security|Rest inherits its security from underlying transport layer.|
|Bandwidth|SOAP requires more bandwidth and resources as it uses XML messages to exchange information|REST requires less bandwith and resources. It can use JSON also.|
|Learning curve|SOAP web services are hard to learn as you need to understand WSDL , client stub|REST web services are easy to understand as you need to annotate plain java class with JAX-RS annotations to use various HTTP methods.|
