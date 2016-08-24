# Content Negotiation and API Design

This is a very simple API description that demonstrates how content negotiation works. 

This also demonstrates a good API design patter in the case where you are exposing the same resource twice: Once for human readers (Web) and once for machines (API).

To retrieve the HTML represetnation of the user resource:

```
GET http://private-25959-contentdemo.apiary-mock.com/user
Accept: text/html
```

To Retrieve the JSON represetnation of the user resource:

```
GET http://private-25959-contentdemo.apiary-mock.com/user
Accept: application/json
```

Note the endpoints – unique address of the resource and HTTP method – are the **same**.

Try it yourself at at <http://private-25959-contentdemo.apiary-mock.com/user> or using cURL / Postman / Paw.
