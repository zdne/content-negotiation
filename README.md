# Content Negotiation and API Design

[Apiary Documentation for this API](http://docs.contentdemo.apiary.io/#)

This is a very simple API description that demonstrates how content negotiation works. 

This also demonstrates a very good **API design pattern** in the case where you are exposing the same resource twice: Once for human readers (Web) and once for machines (API). 

In other words:

> _"If you have a web, you already have an API."_

## How it Works

At its most basic example a content type is negotiated using the [`Accept`](https://github.com/for-GET/know-your-http-well/blob/master/headers.md#content-negotiation) HTTP header while making a request from client.

If everything goes well, a server responds with the matching [`Content-Type`](https://github.com/for-GET/know-your-http-well/blob/master/headers.md#metadata) HTTP header.

### Example Requests

To retrieve the HTML _represetnation_ of the `user` resource:

```
GET http://private-25959-contentdemo.apiary-mock.com/user
Accept: text/html
```

To retrieve the JSON _represetnation_ of the `user` resource:

```
GET http://private-25959-contentdemo.apiary-mock.com/user
Accept: application/json
```

Note the endpoints – unique address of the resource and HTTP method – are the **same**.

Try it yourself at at <http://private-25959-contentdemo.apiary-mock.com/user> or using cURL / Postman / Paw.
