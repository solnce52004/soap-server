Create the domain (methods and parameters) for service first.<br> 
Then use an XML schema file (XSD) that Spring-WS will export automatically as a WSDL.<br>

mvn clean install<br>
mvn spring-boot:run<br>
http://localhost:8000/ws/countries.wsdl
<br>
http://localhost:8000/ws

```xml
<soapenv:Envelope xmlns:soapenv="http://schemas.xmlsoap.org/soap/envelope/" xmlns:gen="http://ru/soap/server/domain/gen">
    <soapenv:Header/>
    <soapenv:Body>
        <gen:getCountryRequest>
            <gen:name>Spain</gen:name>
        </gen:getCountryRequest>
    </soapenv:Body>
</soapenv:Envelope>
```

