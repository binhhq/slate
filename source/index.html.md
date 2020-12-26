---
title: grpc-swagger v
language_tabs:
  - shell: Shell
  - http: HTTP
  - javascript: JavaScript
  - ruby: Ruby
  - python: Python
  - php: PHP
  - java: Java
  - go: Go
toc_footers: []
includes: []
search: true
highlight_theme: darkula
headingLevel: 2

---

<!-- Generator: Widdershins v4.0.1 -->

<h1 id="">grpc-swagger v</h1>

> Scroll down for code samples, example requests and responses. Select a language for code samples from the tabs above or the mobile navigation menu.

Base URLs:

* <a href="http://127.0.0.1:8080/">http://127.0.0.1:8080/</a>

<h1 id="-default">Default</h1>

## post__core.taxItem.TaxItemService.recover

> Code samples

```shell
# You can also use wget
curl -X POST http://127.0.0.1:8080/core.taxItem.TaxItemService.recover \
  -H 'Content-Type: application/json' \
  -H 'Accept: application/json'

```

```http
POST http://127.0.0.1:8080/core.taxItem.TaxItemService.recover HTTP/1.1
Host: 127.0.0.1:8080
Content-Type: application/json
Accept: application/json

```

```javascript
const inputBody = '{
  "taxItemId": "string"
}';
const headers = {
  'Content-Type':'application/json',
  'Accept':'application/json'
};

fetch('http://127.0.0.1:8080/core.taxItem.TaxItemService.recover',
{
  method: 'POST',
  body: inputBody,
  headers: headers
})
.then(function(res) {
    return res.json();
}).then(function(body) {
    console.log(body);
});

```

```ruby
require 'rest-client'
require 'json'

headers = {
  'Content-Type' => 'application/json',
  'Accept' => 'application/json'
}

result = RestClient.post 'http://127.0.0.1:8080/core.taxItem.TaxItemService.recover',
  params: {
  }, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Content-Type': 'application/json',
  'Accept': 'application/json'
}

r = requests.post('http://127.0.0.1:8080/core.taxItem.TaxItemService.recover', headers = headers)

print(r.json())

```

```php
<?php

require 'vendor/autoload.php';

$headers = array(
    'Content-Type' => 'application/json',
    'Accept' => 'application/json',
);

$client = new \GuzzleHttp\Client();

// Define array of request body.
$request_body = array();

try {
    $response = $client->request('POST','http://127.0.0.1:8080/core.taxItem.TaxItemService.recover', array(
        'headers' => $headers,
        'json' => $request_body,
       )
    );
    print_r($response->getBody()->getContents());
 }
 catch (\GuzzleHttp\Exception\BadResponseException $e) {
    // handle exception or api errors.
    print_r($e->getMessage());
 }

 // ...

```

```java
URL obj = new URL("http://127.0.0.1:8080/core.taxItem.TaxItemService.recover");
HttpURLConnection con = (HttpURLConnection) obj.openConnection();
con.setRequestMethod("POST");
int responseCode = con.getResponseCode();
BufferedReader in = new BufferedReader(
    new InputStreamReader(con.getInputStream()));
String inputLine;
StringBuffer response = new StringBuffer();
while ((inputLine = in.readLine()) != null) {
    response.append(inputLine);
}
in.close();
System.out.println(response.toString());

```

```go
package main

import (
       "bytes"
       "net/http"
)

func main() {

    headers := map[string][]string{
        "Content-Type": []string{"application/json"},
        "Accept": []string{"application/json"},
    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("POST", "http://127.0.0.1:8080/core.taxItem.TaxItemService.recover", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`POST /core.taxItem.TaxItemService.recover`

recover

> Body parameter

```json
{
  "taxItemId": "string"
}
```

<h3 id="post__core.taxitem.taxitemservice.recover-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|headers|query|object|false|Headers passed to gRPC server|
|body|body|[core.taxItem.RecoverTaxItemReq](#schemacore.taxitem.recovertaxitemreq)|true|none|

> Example responses

> 200 Response

```json
{
  "taxItemDto": {
    "owner": "string",
    "itemId": "string",
    "createdAt": "string",
    "updatedBy": "string",
    "createdBy": "string",
    "dataVersion": "string",
    "taxId": "string",
    "isArchived": true,
    "id": "string",
    "version": 0,
    "updatedAt": "string"
  }
}
```

<h3 id="post__core.taxitem.taxitemservice.recover-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|none|[core.taxItem.RecoverTaxItemRes](#schemacore.taxitem.recovertaxitemres)|

<aside class="success">
This operation does not require authentication
</aside>

## post__core.taxItem.TaxItemService.getTaxByItemId

> Code samples

```shell
# You can also use wget
curl -X POST http://127.0.0.1:8080/core.taxItem.TaxItemService.getTaxByItemId \
  -H 'Content-Type: application/json' \
  -H 'Accept: application/json'

```

```http
POST http://127.0.0.1:8080/core.taxItem.TaxItemService.getTaxByItemId HTTP/1.1
Host: 127.0.0.1:8080
Content-Type: application/json
Accept: application/json

```

```javascript
const inputBody = '{
  "itemId": "string"
}';
const headers = {
  'Content-Type':'application/json',
  'Accept':'application/json'
};

fetch('http://127.0.0.1:8080/core.taxItem.TaxItemService.getTaxByItemId',
{
  method: 'POST',
  body: inputBody,
  headers: headers
})
.then(function(res) {
    return res.json();
}).then(function(body) {
    console.log(body);
});

```

```ruby
require 'rest-client'
require 'json'

headers = {
  'Content-Type' => 'application/json',
  'Accept' => 'application/json'
}

result = RestClient.post 'http://127.0.0.1:8080/core.taxItem.TaxItemService.getTaxByItemId',
  params: {
  }, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Content-Type': 'application/json',
  'Accept': 'application/json'
}

r = requests.post('http://127.0.0.1:8080/core.taxItem.TaxItemService.getTaxByItemId', headers = headers)

print(r.json())

```

```php
<?php

require 'vendor/autoload.php';

$headers = array(
    'Content-Type' => 'application/json',
    'Accept' => 'application/json',
);

$client = new \GuzzleHttp\Client();

// Define array of request body.
$request_body = array();

try {
    $response = $client->request('POST','http://127.0.0.1:8080/core.taxItem.TaxItemService.getTaxByItemId', array(
        'headers' => $headers,
        'json' => $request_body,
       )
    );
    print_r($response->getBody()->getContents());
 }
 catch (\GuzzleHttp\Exception\BadResponseException $e) {
    // handle exception or api errors.
    print_r($e->getMessage());
 }

 // ...

```

```java
URL obj = new URL("http://127.0.0.1:8080/core.taxItem.TaxItemService.getTaxByItemId");
HttpURLConnection con = (HttpURLConnection) obj.openConnection();
con.setRequestMethod("POST");
int responseCode = con.getResponseCode();
BufferedReader in = new BufferedReader(
    new InputStreamReader(con.getInputStream()));
String inputLine;
StringBuffer response = new StringBuffer();
while ((inputLine = in.readLine()) != null) {
    response.append(inputLine);
}
in.close();
System.out.println(response.toString());

```

```go
package main

import (
       "bytes"
       "net/http"
)

func main() {

    headers := map[string][]string{
        "Content-Type": []string{"application/json"},
        "Accept": []string{"application/json"},
    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("POST", "http://127.0.0.1:8080/core.taxItem.TaxItemService.getTaxByItemId", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`POST /core.taxItem.TaxItemService.getTaxByItemId`

getTaxByItemId

> Body parameter

```json
{
  "itemId": "string"
}
```

<h3 id="post__core.taxitem.taxitemservice.gettaxbyitemid-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|headers|query|object|false|Headers passed to gRPC server|
|body|body|[core.taxItem.GetTaxByItemIdReq](#schemacore.taxitem.gettaxbyitemidreq)|true|none|

> Example responses

> 200 Response

```json
{
  "taxList": [
    {
      "owner": "string",
      "appToCreate": "string",
      "updatedBy": "string",
      "code": "string",
      "dataVersion": "string",
      "isArchived": true,
      "onlyVisibleToCreatorApp": true,
      "locationToCreate": "string",
      "objectClass": "string",
      "appSubClass": "string",
      "appSubKey": "string",
      "version": 0,
      "percent": 0,
      "createdAt": "string",
      "createdBy": "string",
      "name": "string",
      "objectName": "string",
      "appKey": "string",
      "id": "string",
      "updatedAt": "string"
    }
  ]
}
```

<h3 id="post__core.taxitem.taxitemservice.gettaxbyitemid-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|none|[core.taxItem.GetTaxByItemIdRes](#schemacore.taxitem.gettaxbyitemidres)|

<aside class="success">
This operation does not require authentication
</aside>

## post__core.taxItem.TaxItemService.archive

> Code samples

```shell
# You can also use wget
curl -X POST http://127.0.0.1:8080/core.taxItem.TaxItemService.archive \
  -H 'Content-Type: application/json' \
  -H 'Accept: application/json'

```

```http
POST http://127.0.0.1:8080/core.taxItem.TaxItemService.archive HTTP/1.1
Host: 127.0.0.1:8080
Content-Type: application/json
Accept: application/json

```

```javascript
const inputBody = '{
  "optimisticVersion": 0,
  "taxItemId": "string"
}';
const headers = {
  'Content-Type':'application/json',
  'Accept':'application/json'
};

fetch('http://127.0.0.1:8080/core.taxItem.TaxItemService.archive',
{
  method: 'POST',
  body: inputBody,
  headers: headers
})
.then(function(res) {
    return res.json();
}).then(function(body) {
    console.log(body);
});

```

```ruby
require 'rest-client'
require 'json'

headers = {
  'Content-Type' => 'application/json',
  'Accept' => 'application/json'
}

result = RestClient.post 'http://127.0.0.1:8080/core.taxItem.TaxItemService.archive',
  params: {
  }, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Content-Type': 'application/json',
  'Accept': 'application/json'
}

r = requests.post('http://127.0.0.1:8080/core.taxItem.TaxItemService.archive', headers = headers)

print(r.json())

```

```php
<?php

require 'vendor/autoload.php';

$headers = array(
    'Content-Type' => 'application/json',
    'Accept' => 'application/json',
);

$client = new \GuzzleHttp\Client();

// Define array of request body.
$request_body = array();

try {
    $response = $client->request('POST','http://127.0.0.1:8080/core.taxItem.TaxItemService.archive', array(
        'headers' => $headers,
        'json' => $request_body,
       )
    );
    print_r($response->getBody()->getContents());
 }
 catch (\GuzzleHttp\Exception\BadResponseException $e) {
    // handle exception or api errors.
    print_r($e->getMessage());
 }

 // ...

```

```java
URL obj = new URL("http://127.0.0.1:8080/core.taxItem.TaxItemService.archive");
HttpURLConnection con = (HttpURLConnection) obj.openConnection();
con.setRequestMethod("POST");
int responseCode = con.getResponseCode();
BufferedReader in = new BufferedReader(
    new InputStreamReader(con.getInputStream()));
String inputLine;
StringBuffer response = new StringBuffer();
while ((inputLine = in.readLine()) != null) {
    response.append(inputLine);
}
in.close();
System.out.println(response.toString());

```

```go
package main

import (
       "bytes"
       "net/http"
)

func main() {

    headers := map[string][]string{
        "Content-Type": []string{"application/json"},
        "Accept": []string{"application/json"},
    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("POST", "http://127.0.0.1:8080/core.taxItem.TaxItemService.archive", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`POST /core.taxItem.TaxItemService.archive`

archive

> Body parameter

```json
{
  "optimisticVersion": 0,
  "taxItemId": "string"
}
```

<h3 id="post__core.taxitem.taxitemservice.archive-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|headers|query|object|false|Headers passed to gRPC server|
|body|body|[core.taxItem.ArchiveTaxItemReq](#schemacore.taxitem.archivetaxitemreq)|true|none|

> Example responses

> 200 Response

```json
{
  "taxItemDto": {
    "owner": "string",
    "itemId": "string",
    "createdAt": "string",
    "updatedBy": "string",
    "createdBy": "string",
    "dataVersion": "string",
    "taxId": "string",
    "isArchived": true,
    "id": "string",
    "version": 0,
    "updatedAt": "string"
  }
}
```

<h3 id="post__core.taxitem.taxitemservice.archive-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|none|[core.taxItem.ArchiveTaxItemRes](#schemacore.taxitem.archivetaxitemres)|

<aside class="success">
This operation does not require authentication
</aside>

## post__core.taxItem.TaxItemService.showArchivedTaxItem

> Code samples

```shell
# You can also use wget
curl -X POST http://127.0.0.1:8080/core.taxItem.TaxItemService.showArchivedTaxItem \
  -H 'Content-Type: application/json' \
  -H 'Accept: application/json'

```

```http
POST http://127.0.0.1:8080/core.taxItem.TaxItemService.showArchivedTaxItem HTTP/1.1
Host: 127.0.0.1:8080
Content-Type: application/json
Accept: application/json

```

```javascript
const inputBody = '{
  "pagingAndSorting": {
    "sortOrder": "ASC",
    "limit": 0,
    "lastIndex": "string"
  }
}';
const headers = {
  'Content-Type':'application/json',
  'Accept':'application/json'
};

fetch('http://127.0.0.1:8080/core.taxItem.TaxItemService.showArchivedTaxItem',
{
  method: 'POST',
  body: inputBody,
  headers: headers
})
.then(function(res) {
    return res.json();
}).then(function(body) {
    console.log(body);
});

```

```ruby
require 'rest-client'
require 'json'

headers = {
  'Content-Type' => 'application/json',
  'Accept' => 'application/json'
}

result = RestClient.post 'http://127.0.0.1:8080/core.taxItem.TaxItemService.showArchivedTaxItem',
  params: {
  }, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Content-Type': 'application/json',
  'Accept': 'application/json'
}

r = requests.post('http://127.0.0.1:8080/core.taxItem.TaxItemService.showArchivedTaxItem', headers = headers)

print(r.json())

```

```php
<?php

require 'vendor/autoload.php';

$headers = array(
    'Content-Type' => 'application/json',
    'Accept' => 'application/json',
);

$client = new \GuzzleHttp\Client();

// Define array of request body.
$request_body = array();

try {
    $response = $client->request('POST','http://127.0.0.1:8080/core.taxItem.TaxItemService.showArchivedTaxItem', array(
        'headers' => $headers,
        'json' => $request_body,
       )
    );
    print_r($response->getBody()->getContents());
 }
 catch (\GuzzleHttp\Exception\BadResponseException $e) {
    // handle exception or api errors.
    print_r($e->getMessage());
 }

 // ...

```

```java
URL obj = new URL("http://127.0.0.1:8080/core.taxItem.TaxItemService.showArchivedTaxItem");
HttpURLConnection con = (HttpURLConnection) obj.openConnection();
con.setRequestMethod("POST");
int responseCode = con.getResponseCode();
BufferedReader in = new BufferedReader(
    new InputStreamReader(con.getInputStream()));
String inputLine;
StringBuffer response = new StringBuffer();
while ((inputLine = in.readLine()) != null) {
    response.append(inputLine);
}
in.close();
System.out.println(response.toString());

```

```go
package main

import (
       "bytes"
       "net/http"
)

func main() {

    headers := map[string][]string{
        "Content-Type": []string{"application/json"},
        "Accept": []string{"application/json"},
    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("POST", "http://127.0.0.1:8080/core.taxItem.TaxItemService.showArchivedTaxItem", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`POST /core.taxItem.TaxItemService.showArchivedTaxItem`

showArchivedTaxItem

> Body parameter

```json
{
  "pagingAndSorting": {
    "sortOrder": "ASC",
    "limit": 0,
    "lastIndex": "string"
  }
}
```

<h3 id="post__core.taxitem.taxitemservice.showarchivedtaxitem-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|headers|query|object|false|Headers passed to gRPC server|
|body|body|[core.taxItem.ShowArchivedTaxItemReq](#schemacore.taxitem.showarchivedtaxitemreq)|true|none|

> Example responses

> 200 Response

```json
{
  "listTaxItemDtoArchived": [
    {
      "owner": "string",
      "itemId": "string",
      "createdAt": "string",
      "updatedBy": "string",
      "createdBy": "string",
      "dataVersion": "string",
      "taxId": "string",
      "isArchived": true,
      "id": "string",
      "version": 0,
      "updatedAt": "string"
    }
  ]
}
```

<h3 id="post__core.taxitem.taxitemservice.showarchivedtaxitem-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|none|[core.taxItem.ShowArchivedTaxItemRes](#schemacore.taxitem.showarchivedtaxitemres)|

<aside class="success">
This operation does not require authentication
</aside>

## post__core.taxItem.TaxItemService.getById

> Code samples

```shell
# You can also use wget
curl -X POST http://127.0.0.1:8080/core.taxItem.TaxItemService.getById \
  -H 'Content-Type: application/json' \
  -H 'Accept: application/json'

```

```http
POST http://127.0.0.1:8080/core.taxItem.TaxItemService.getById HTTP/1.1
Host: 127.0.0.1:8080
Content-Type: application/json
Accept: application/json

```

```javascript
const inputBody = '{
  "id": "string"
}';
const headers = {
  'Content-Type':'application/json',
  'Accept':'application/json'
};

fetch('http://127.0.0.1:8080/core.taxItem.TaxItemService.getById',
{
  method: 'POST',
  body: inputBody,
  headers: headers
})
.then(function(res) {
    return res.json();
}).then(function(body) {
    console.log(body);
});

```

```ruby
require 'rest-client'
require 'json'

headers = {
  'Content-Type' => 'application/json',
  'Accept' => 'application/json'
}

result = RestClient.post 'http://127.0.0.1:8080/core.taxItem.TaxItemService.getById',
  params: {
  }, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Content-Type': 'application/json',
  'Accept': 'application/json'
}

r = requests.post('http://127.0.0.1:8080/core.taxItem.TaxItemService.getById', headers = headers)

print(r.json())

```

```php
<?php

require 'vendor/autoload.php';

$headers = array(
    'Content-Type' => 'application/json',
    'Accept' => 'application/json',
);

$client = new \GuzzleHttp\Client();

// Define array of request body.
$request_body = array();

try {
    $response = $client->request('POST','http://127.0.0.1:8080/core.taxItem.TaxItemService.getById', array(
        'headers' => $headers,
        'json' => $request_body,
       )
    );
    print_r($response->getBody()->getContents());
 }
 catch (\GuzzleHttp\Exception\BadResponseException $e) {
    // handle exception or api errors.
    print_r($e->getMessage());
 }

 // ...

```

```java
URL obj = new URL("http://127.0.0.1:8080/core.taxItem.TaxItemService.getById");
HttpURLConnection con = (HttpURLConnection) obj.openConnection();
con.setRequestMethod("POST");
int responseCode = con.getResponseCode();
BufferedReader in = new BufferedReader(
    new InputStreamReader(con.getInputStream()));
String inputLine;
StringBuffer response = new StringBuffer();
while ((inputLine = in.readLine()) != null) {
    response.append(inputLine);
}
in.close();
System.out.println(response.toString());

```

```go
package main

import (
       "bytes"
       "net/http"
)

func main() {

    headers := map[string][]string{
        "Content-Type": []string{"application/json"},
        "Accept": []string{"application/json"},
    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("POST", "http://127.0.0.1:8080/core.taxItem.TaxItemService.getById", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`POST /core.taxItem.TaxItemService.getById`

getById

> Body parameter

```json
{
  "id": "string"
}
```

<h3 id="post__core.taxitem.taxitemservice.getbyid-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|headers|query|object|false|Headers passed to gRPC server|
|body|body|[core.taxItem.GetTaxItemByIdReq](#schemacore.taxitem.gettaxitembyidreq)|true|none|

> Example responses

> 200 Response

```json
{
  "taxItemDto": {
    "owner": "string",
    "itemId": "string",
    "createdAt": "string",
    "updatedBy": "string",
    "createdBy": "string",
    "dataVersion": "string",
    "taxId": "string",
    "isArchived": true,
    "id": "string",
    "version": 0,
    "updatedAt": "string"
  }
}
```

<h3 id="post__core.taxitem.taxitemservice.getbyid-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|none|[core.taxItem.GetTaxItemByIdRes](#schemacore.taxitem.gettaxitembyidres)|

<aside class="success">
This operation does not require authentication
</aside>

## post__core.taxItem.TaxItemService.update

> Code samples

```shell
# You can also use wget
curl -X POST http://127.0.0.1:8080/core.taxItem.TaxItemService.update \
  -H 'Content-Type: application/json' \
  -H 'Accept: application/json'

```

```http
POST http://127.0.0.1:8080/core.taxItem.TaxItemService.update HTTP/1.1
Host: 127.0.0.1:8080
Content-Type: application/json
Accept: application/json

```

```javascript
const inputBody = '{
  "itemId": "string",
  "optimisticVersion": 0,
  "taxId": "string",
  "taxItemId": "string"
}';
const headers = {
  'Content-Type':'application/json',
  'Accept':'application/json'
};

fetch('http://127.0.0.1:8080/core.taxItem.TaxItemService.update',
{
  method: 'POST',
  body: inputBody,
  headers: headers
})
.then(function(res) {
    return res.json();
}).then(function(body) {
    console.log(body);
});

```

```ruby
require 'rest-client'
require 'json'

headers = {
  'Content-Type' => 'application/json',
  'Accept' => 'application/json'
}

result = RestClient.post 'http://127.0.0.1:8080/core.taxItem.TaxItemService.update',
  params: {
  }, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Content-Type': 'application/json',
  'Accept': 'application/json'
}

r = requests.post('http://127.0.0.1:8080/core.taxItem.TaxItemService.update', headers = headers)

print(r.json())

```

```php
<?php

require 'vendor/autoload.php';

$headers = array(
    'Content-Type' => 'application/json',
    'Accept' => 'application/json',
);

$client = new \GuzzleHttp\Client();

// Define array of request body.
$request_body = array();

try {
    $response = $client->request('POST','http://127.0.0.1:8080/core.taxItem.TaxItemService.update', array(
        'headers' => $headers,
        'json' => $request_body,
       )
    );
    print_r($response->getBody()->getContents());
 }
 catch (\GuzzleHttp\Exception\BadResponseException $e) {
    // handle exception or api errors.
    print_r($e->getMessage());
 }

 // ...

```

```java
URL obj = new URL("http://127.0.0.1:8080/core.taxItem.TaxItemService.update");
HttpURLConnection con = (HttpURLConnection) obj.openConnection();
con.setRequestMethod("POST");
int responseCode = con.getResponseCode();
BufferedReader in = new BufferedReader(
    new InputStreamReader(con.getInputStream()));
String inputLine;
StringBuffer response = new StringBuffer();
while ((inputLine = in.readLine()) != null) {
    response.append(inputLine);
}
in.close();
System.out.println(response.toString());

```

```go
package main

import (
       "bytes"
       "net/http"
)

func main() {

    headers := map[string][]string{
        "Content-Type": []string{"application/json"},
        "Accept": []string{"application/json"},
    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("POST", "http://127.0.0.1:8080/core.taxItem.TaxItemService.update", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`POST /core.taxItem.TaxItemService.update`

update

> Body parameter

```json
{
  "itemId": "string",
  "optimisticVersion": 0,
  "taxId": "string",
  "taxItemId": "string"
}
```

<h3 id="post__core.taxitem.taxitemservice.update-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|headers|query|object|false|Headers passed to gRPC server|
|body|body|[core.taxItem.UpdateTaxItemReq](#schemacore.taxitem.updatetaxitemreq)|true|none|

> Example responses

> 200 Response

```json
{
  "taxItemDto": {
    "owner": "string",
    "itemId": "string",
    "createdAt": "string",
    "updatedBy": "string",
    "createdBy": "string",
    "dataVersion": "string",
    "taxId": "string",
    "isArchived": true,
    "id": "string",
    "version": 0,
    "updatedAt": "string"
  }
}
```

<h3 id="post__core.taxitem.taxitemservice.update-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|none|[core.taxItem.UpdateTaxItemRes](#schemacore.taxitem.updatetaxitemres)|

<aside class="success">
This operation does not require authentication
</aside>

## post__core.taxItem.TaxItemService.countArchiveTaxItem

> Code samples

```shell
# You can also use wget
curl -X POST http://127.0.0.1:8080/core.taxItem.TaxItemService.countArchiveTaxItem \
  -H 'Content-Type: application/json' \
  -H 'Accept: application/json'

```

```http
POST http://127.0.0.1:8080/core.taxItem.TaxItemService.countArchiveTaxItem HTTP/1.1
Host: 127.0.0.1:8080
Content-Type: application/json
Accept: application/json

```

```javascript
const inputBody = '{}';
const headers = {
  'Content-Type':'application/json',
  'Accept':'application/json'
};

fetch('http://127.0.0.1:8080/core.taxItem.TaxItemService.countArchiveTaxItem',
{
  method: 'POST',
  body: inputBody,
  headers: headers
})
.then(function(res) {
    return res.json();
}).then(function(body) {
    console.log(body);
});

```

```ruby
require 'rest-client'
require 'json'

headers = {
  'Content-Type' => 'application/json',
  'Accept' => 'application/json'
}

result = RestClient.post 'http://127.0.0.1:8080/core.taxItem.TaxItemService.countArchiveTaxItem',
  params: {
  }, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Content-Type': 'application/json',
  'Accept': 'application/json'
}

r = requests.post('http://127.0.0.1:8080/core.taxItem.TaxItemService.countArchiveTaxItem', headers = headers)

print(r.json())

```

```php
<?php

require 'vendor/autoload.php';

$headers = array(
    'Content-Type' => 'application/json',
    'Accept' => 'application/json',
);

$client = new \GuzzleHttp\Client();

// Define array of request body.
$request_body = array();

try {
    $response = $client->request('POST','http://127.0.0.1:8080/core.taxItem.TaxItemService.countArchiveTaxItem', array(
        'headers' => $headers,
        'json' => $request_body,
       )
    );
    print_r($response->getBody()->getContents());
 }
 catch (\GuzzleHttp\Exception\BadResponseException $e) {
    // handle exception or api errors.
    print_r($e->getMessage());
 }

 // ...

```

```java
URL obj = new URL("http://127.0.0.1:8080/core.taxItem.TaxItemService.countArchiveTaxItem");
HttpURLConnection con = (HttpURLConnection) obj.openConnection();
con.setRequestMethod("POST");
int responseCode = con.getResponseCode();
BufferedReader in = new BufferedReader(
    new InputStreamReader(con.getInputStream()));
String inputLine;
StringBuffer response = new StringBuffer();
while ((inputLine = in.readLine()) != null) {
    response.append(inputLine);
}
in.close();
System.out.println(response.toString());

```

```go
package main

import (
       "bytes"
       "net/http"
)

func main() {

    headers := map[string][]string{
        "Content-Type": []string{"application/json"},
        "Accept": []string{"application/json"},
    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("POST", "http://127.0.0.1:8080/core.taxItem.TaxItemService.countArchiveTaxItem", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`POST /core.taxItem.TaxItemService.countArchiveTaxItem`

countArchiveTaxItem

> Body parameter

```json
{}
```

<h3 id="post__core.taxitem.taxitemservice.countarchivetaxitem-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|headers|query|object|false|Headers passed to gRPC server|
|body|body|[core.taxItem.CountArchiveTaxItemReq](#schemacore.taxitem.countarchivetaxitemreq)|true|none|

> Example responses

> 200 Response

```json
{
  "count": 0
}
```

<h3 id="post__core.taxitem.taxitemservice.countarchivetaxitem-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|none|[core.taxItem.CountRes](#schemacore.taxitem.countres)|

<aside class="success">
This operation does not require authentication
</aside>

## post__core.taxItem.TaxItemService.searchTaxItem

> Code samples

```shell
# You can also use wget
curl -X POST http://127.0.0.1:8080/core.taxItem.TaxItemService.searchTaxItem \
  -H 'Content-Type: application/json' \
  -H 'Accept: application/json'

```

```http
POST http://127.0.0.1:8080/core.taxItem.TaxItemService.searchTaxItem HTTP/1.1
Host: 127.0.0.1:8080
Content-Type: application/json
Accept: application/json

```

```javascript
const inputBody = '{
  "queryString": "string",
  "pagingAndSorting": {
    "sortOrder": "ASC",
    "limit": 0,
    "lastIndex": "string"
  }
}';
const headers = {
  'Content-Type':'application/json',
  'Accept':'application/json'
};

fetch('http://127.0.0.1:8080/core.taxItem.TaxItemService.searchTaxItem',
{
  method: 'POST',
  body: inputBody,
  headers: headers
})
.then(function(res) {
    return res.json();
}).then(function(body) {
    console.log(body);
});

```

```ruby
require 'rest-client'
require 'json'

headers = {
  'Content-Type' => 'application/json',
  'Accept' => 'application/json'
}

result = RestClient.post 'http://127.0.0.1:8080/core.taxItem.TaxItemService.searchTaxItem',
  params: {
  }, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Content-Type': 'application/json',
  'Accept': 'application/json'
}

r = requests.post('http://127.0.0.1:8080/core.taxItem.TaxItemService.searchTaxItem', headers = headers)

print(r.json())

```

```php
<?php

require 'vendor/autoload.php';

$headers = array(
    'Content-Type' => 'application/json',
    'Accept' => 'application/json',
);

$client = new \GuzzleHttp\Client();

// Define array of request body.
$request_body = array();

try {
    $response = $client->request('POST','http://127.0.0.1:8080/core.taxItem.TaxItemService.searchTaxItem', array(
        'headers' => $headers,
        'json' => $request_body,
       )
    );
    print_r($response->getBody()->getContents());
 }
 catch (\GuzzleHttp\Exception\BadResponseException $e) {
    // handle exception or api errors.
    print_r($e->getMessage());
 }

 // ...

```

```java
URL obj = new URL("http://127.0.0.1:8080/core.taxItem.TaxItemService.searchTaxItem");
HttpURLConnection con = (HttpURLConnection) obj.openConnection();
con.setRequestMethod("POST");
int responseCode = con.getResponseCode();
BufferedReader in = new BufferedReader(
    new InputStreamReader(con.getInputStream()));
String inputLine;
StringBuffer response = new StringBuffer();
while ((inputLine = in.readLine()) != null) {
    response.append(inputLine);
}
in.close();
System.out.println(response.toString());

```

```go
package main

import (
       "bytes"
       "net/http"
)

func main() {

    headers := map[string][]string{
        "Content-Type": []string{"application/json"},
        "Accept": []string{"application/json"},
    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("POST", "http://127.0.0.1:8080/core.taxItem.TaxItemService.searchTaxItem", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`POST /core.taxItem.TaxItemService.searchTaxItem`

searchTaxItem

> Body parameter

```json
{
  "queryString": "string",
  "pagingAndSorting": {
    "sortOrder": "ASC",
    "limit": 0,
    "lastIndex": "string"
  }
}
```

<h3 id="post__core.taxitem.taxitemservice.searchtaxitem-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|headers|query|object|false|Headers passed to gRPC server|
|body|body|[core.taxItem.SearchTaxItemReq](#schemacore.taxitem.searchtaxitemreq)|true|none|

> Example responses

> 200 Response

```json
{
  "data": [
    {
      "owner": "string",
      "itemId": "string",
      "createdAt": "string",
      "updatedBy": "string",
      "createdBy": "string",
      "dataVersion": "string",
      "taxId": "string",
      "isArchived": true,
      "id": "string",
      "version": 0,
      "updatedAt": "string"
    }
  ]
}
```

<h3 id="post__core.taxitem.taxitemservice.searchtaxitem-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|none|[core.taxItem.SearchTaxItemRes](#schemacore.taxitem.searchtaxitemres)|

<aside class="success">
This operation does not require authentication
</aside>

## post__core.taxItem.TaxItemService.countSearchTaxItem

> Code samples

```shell
# You can also use wget
curl -X POST http://127.0.0.1:8080/core.taxItem.TaxItemService.countSearchTaxItem \
  -H 'Content-Type: application/json' \
  -H 'Accept: application/json'

```

```http
POST http://127.0.0.1:8080/core.taxItem.TaxItemService.countSearchTaxItem HTTP/1.1
Host: 127.0.0.1:8080
Content-Type: application/json
Accept: application/json

```

```javascript
const inputBody = '{
  "queryString": "string"
}';
const headers = {
  'Content-Type':'application/json',
  'Accept':'application/json'
};

fetch('http://127.0.0.1:8080/core.taxItem.TaxItemService.countSearchTaxItem',
{
  method: 'POST',
  body: inputBody,
  headers: headers
})
.then(function(res) {
    return res.json();
}).then(function(body) {
    console.log(body);
});

```

```ruby
require 'rest-client'
require 'json'

headers = {
  'Content-Type' => 'application/json',
  'Accept' => 'application/json'
}

result = RestClient.post 'http://127.0.0.1:8080/core.taxItem.TaxItemService.countSearchTaxItem',
  params: {
  }, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Content-Type': 'application/json',
  'Accept': 'application/json'
}

r = requests.post('http://127.0.0.1:8080/core.taxItem.TaxItemService.countSearchTaxItem', headers = headers)

print(r.json())

```

```php
<?php

require 'vendor/autoload.php';

$headers = array(
    'Content-Type' => 'application/json',
    'Accept' => 'application/json',
);

$client = new \GuzzleHttp\Client();

// Define array of request body.
$request_body = array();

try {
    $response = $client->request('POST','http://127.0.0.1:8080/core.taxItem.TaxItemService.countSearchTaxItem', array(
        'headers' => $headers,
        'json' => $request_body,
       )
    );
    print_r($response->getBody()->getContents());
 }
 catch (\GuzzleHttp\Exception\BadResponseException $e) {
    // handle exception or api errors.
    print_r($e->getMessage());
 }

 // ...

```

```java
URL obj = new URL("http://127.0.0.1:8080/core.taxItem.TaxItemService.countSearchTaxItem");
HttpURLConnection con = (HttpURLConnection) obj.openConnection();
con.setRequestMethod("POST");
int responseCode = con.getResponseCode();
BufferedReader in = new BufferedReader(
    new InputStreamReader(con.getInputStream()));
String inputLine;
StringBuffer response = new StringBuffer();
while ((inputLine = in.readLine()) != null) {
    response.append(inputLine);
}
in.close();
System.out.println(response.toString());

```

```go
package main

import (
       "bytes"
       "net/http"
)

func main() {

    headers := map[string][]string{
        "Content-Type": []string{"application/json"},
        "Accept": []string{"application/json"},
    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("POST", "http://127.0.0.1:8080/core.taxItem.TaxItemService.countSearchTaxItem", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`POST /core.taxItem.TaxItemService.countSearchTaxItem`

countSearchTaxItem

> Body parameter

```json
{
  "queryString": "string"
}
```

<h3 id="post__core.taxitem.taxitemservice.countsearchtaxitem-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|headers|query|object|false|Headers passed to gRPC server|
|body|body|[core.taxItem.CountSearchTaxItemReq](#schemacore.taxitem.countsearchtaxitemreq)|true|none|

> Example responses

> 200 Response

```json
{
  "count": 0
}
```

<h3 id="post__core.taxitem.taxitemservice.countsearchtaxitem-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|none|[core.taxItem.CountRes](#schemacore.taxitem.countres)|

<aside class="success">
This operation does not require authentication
</aside>

## post__core.taxItem.TaxItemService.create

> Code samples

```shell
# You can also use wget
curl -X POST http://127.0.0.1:8080/core.taxItem.TaxItemService.create \
  -H 'Content-Type: application/json' \
  -H 'Accept: application/json'

```

```http
POST http://127.0.0.1:8080/core.taxItem.TaxItemService.create HTTP/1.1
Host: 127.0.0.1:8080
Content-Type: application/json
Accept: application/json

```

```javascript
const inputBody = '{
  "itemId": "string",
  "taxId": "string"
}';
const headers = {
  'Content-Type':'application/json',
  'Accept':'application/json'
};

fetch('http://127.0.0.1:8080/core.taxItem.TaxItemService.create',
{
  method: 'POST',
  body: inputBody,
  headers: headers
})
.then(function(res) {
    return res.json();
}).then(function(body) {
    console.log(body);
});

```

```ruby
require 'rest-client'
require 'json'

headers = {
  'Content-Type' => 'application/json',
  'Accept' => 'application/json'
}

result = RestClient.post 'http://127.0.0.1:8080/core.taxItem.TaxItemService.create',
  params: {
  }, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Content-Type': 'application/json',
  'Accept': 'application/json'
}

r = requests.post('http://127.0.0.1:8080/core.taxItem.TaxItemService.create', headers = headers)

print(r.json())

```

```php
<?php

require 'vendor/autoload.php';

$headers = array(
    'Content-Type' => 'application/json',
    'Accept' => 'application/json',
);

$client = new \GuzzleHttp\Client();

// Define array of request body.
$request_body = array();

try {
    $response = $client->request('POST','http://127.0.0.1:8080/core.taxItem.TaxItemService.create', array(
        'headers' => $headers,
        'json' => $request_body,
       )
    );
    print_r($response->getBody()->getContents());
 }
 catch (\GuzzleHttp\Exception\BadResponseException $e) {
    // handle exception or api errors.
    print_r($e->getMessage());
 }

 // ...

```

```java
URL obj = new URL("http://127.0.0.1:8080/core.taxItem.TaxItemService.create");
HttpURLConnection con = (HttpURLConnection) obj.openConnection();
con.setRequestMethod("POST");
int responseCode = con.getResponseCode();
BufferedReader in = new BufferedReader(
    new InputStreamReader(con.getInputStream()));
String inputLine;
StringBuffer response = new StringBuffer();
while ((inputLine = in.readLine()) != null) {
    response.append(inputLine);
}
in.close();
System.out.println(response.toString());

```

```go
package main

import (
       "bytes"
       "net/http"
)

func main() {

    headers := map[string][]string{
        "Content-Type": []string{"application/json"},
        "Accept": []string{"application/json"},
    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("POST", "http://127.0.0.1:8080/core.taxItem.TaxItemService.create", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`POST /core.taxItem.TaxItemService.create`

create

> Body parameter

```json
{
  "itemId": "string",
  "taxId": "string"
}
```

<h3 id="post__core.taxitem.taxitemservice.create-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|headers|query|object|false|Headers passed to gRPC server|
|body|body|[core.taxItem.CreateTaxItemReq](#schemacore.taxitem.createtaxitemreq)|true|none|

> Example responses

> 200 Response

```json
{
  "taxItemDto": {
    "owner": "string",
    "itemId": "string",
    "createdAt": "string",
    "updatedBy": "string",
    "createdBy": "string",
    "dataVersion": "string",
    "taxId": "string",
    "isArchived": true,
    "id": "string",
    "version": 0,
    "updatedAt": "string"
  }
}
```

<h3 id="post__core.taxitem.taxitemservice.create-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|none|[core.taxItem.CreateTaxItemRes](#schemacore.taxitem.createtaxitemres)|

<aside class="success">
This operation does not require authentication
</aside>

## post__core.taxItem.TaxItemService.purgeTaxItem

> Code samples

```shell
# You can also use wget
curl -X POST http://127.0.0.1:8080/core.taxItem.TaxItemService.purgeTaxItem \
  -H 'Content-Type: application/json' \
  -H 'Accept: application/json'

```

```http
POST http://127.0.0.1:8080/core.taxItem.TaxItemService.purgeTaxItem HTTP/1.1
Host: 127.0.0.1:8080
Content-Type: application/json
Accept: application/json

```

```javascript
const inputBody = '{
  "ageing": 0
}';
const headers = {
  'Content-Type':'application/json',
  'Accept':'application/json'
};

fetch('http://127.0.0.1:8080/core.taxItem.TaxItemService.purgeTaxItem',
{
  method: 'POST',
  body: inputBody,
  headers: headers
})
.then(function(res) {
    return res.json();
}).then(function(body) {
    console.log(body);
});

```

```ruby
require 'rest-client'
require 'json'

headers = {
  'Content-Type' => 'application/json',
  'Accept' => 'application/json'
}

result = RestClient.post 'http://127.0.0.1:8080/core.taxItem.TaxItemService.purgeTaxItem',
  params: {
  }, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Content-Type': 'application/json',
  'Accept': 'application/json'
}

r = requests.post('http://127.0.0.1:8080/core.taxItem.TaxItemService.purgeTaxItem', headers = headers)

print(r.json())

```

```php
<?php

require 'vendor/autoload.php';

$headers = array(
    'Content-Type' => 'application/json',
    'Accept' => 'application/json',
);

$client = new \GuzzleHttp\Client();

// Define array of request body.
$request_body = array();

try {
    $response = $client->request('POST','http://127.0.0.1:8080/core.taxItem.TaxItemService.purgeTaxItem', array(
        'headers' => $headers,
        'json' => $request_body,
       )
    );
    print_r($response->getBody()->getContents());
 }
 catch (\GuzzleHttp\Exception\BadResponseException $e) {
    // handle exception or api errors.
    print_r($e->getMessage());
 }

 // ...

```

```java
URL obj = new URL("http://127.0.0.1:8080/core.taxItem.TaxItemService.purgeTaxItem");
HttpURLConnection con = (HttpURLConnection) obj.openConnection();
con.setRequestMethod("POST");
int responseCode = con.getResponseCode();
BufferedReader in = new BufferedReader(
    new InputStreamReader(con.getInputStream()));
String inputLine;
StringBuffer response = new StringBuffer();
while ((inputLine = in.readLine()) != null) {
    response.append(inputLine);
}
in.close();
System.out.println(response.toString());

```

```go
package main

import (
       "bytes"
       "net/http"
)

func main() {

    headers := map[string][]string{
        "Content-Type": []string{"application/json"},
        "Accept": []string{"application/json"},
    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("POST", "http://127.0.0.1:8080/core.taxItem.TaxItemService.purgeTaxItem", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`POST /core.taxItem.TaxItemService.purgeTaxItem`

purgeTaxItem

> Body parameter

```json
{
  "ageing": 0
}
```

<h3 id="post__core.taxitem.taxitemservice.purgetaxitem-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|headers|query|object|false|Headers passed to gRPC server|
|body|body|[core.taxItem.PurgeTaxItemReq](#schemacore.taxitem.purgetaxitemreq)|true|none|

> Example responses

> 200 Response

```json
{
  "listTaxItemId": [
    "string"
  ]
}
```

<h3 id="post__core.taxitem.taxitemservice.purgetaxitem-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|none|[core.taxItem.PurgeTaxItemRes](#schemacore.taxitem.purgetaxitemres)|

<aside class="success">
This operation does not require authentication
</aside>

# Schemas

<h2 id="tocS_core.taxItem.UpdateTaxItemReq">core.taxItem.UpdateTaxItemReq</h2>
<!-- backwards compatibility -->
<a id="schemacore.taxitem.updatetaxitemreq"></a>
<a id="schema_core.taxItem.UpdateTaxItemReq"></a>
<a id="tocScore.taxitem.updatetaxitemreq"></a>
<a id="tocscore.taxitem.updatetaxitemreq"></a>

```json
{
  "itemId": "string",
  "optimisticVersion": 0,
  "taxId": "string",
  "taxItemId": "string"
}

```

UpdateTaxItemReq

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|itemId|string|false|none|none|
|optimisticVersion|integer(int64)|false|none|none|
|taxId|string|false|none|none|
|taxItemId|string|false|none|none|

<h2 id="tocS_core.taxItem.UpdateTaxItemRes">core.taxItem.UpdateTaxItemRes</h2>
<!-- backwards compatibility -->
<a id="schemacore.taxitem.updatetaxitemres"></a>
<a id="schema_core.taxItem.UpdateTaxItemRes"></a>
<a id="tocScore.taxitem.updatetaxitemres"></a>
<a id="tocscore.taxitem.updatetaxitemres"></a>

```json
{
  "taxItemDto": {
    "owner": "string",
    "itemId": "string",
    "createdAt": "string",
    "updatedBy": "string",
    "createdBy": "string",
    "dataVersion": "string",
    "taxId": "string",
    "isArchived": true,
    "id": "string",
    "version": 0,
    "updatedAt": "string"
  }
}

```

UpdateTaxItemRes

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|taxItemDto|[core.taxItem.TaxItemDto](#schemacore.taxitem.taxitemdto)|false|none|none|

<h2 id="tocS_core.taxItem.TaxItemDto">core.taxItem.TaxItemDto</h2>
<!-- backwards compatibility -->
<a id="schemacore.taxitem.taxitemdto"></a>
<a id="schema_core.taxItem.TaxItemDto"></a>
<a id="tocScore.taxitem.taxitemdto"></a>
<a id="tocscore.taxitem.taxitemdto"></a>

```json
{
  "owner": "string",
  "itemId": "string",
  "createdAt": "string",
  "updatedBy": "string",
  "createdBy": "string",
  "dataVersion": "string",
  "taxId": "string",
  "isArchived": true,
  "id": "string",
  "version": 0,
  "updatedAt": "string"
}

```

TaxItemDto

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|owner|string|false|none|none|
|itemId|string|false|none|none|
|createdAt|string|false|none|none|
|updatedBy|string|false|none|none|
|createdBy|string|false|none|none|
|dataVersion|string|false|none|none|
|taxId|string|false|none|none|
|isArchived|boolean|false|none|none|
|id|string|false|none|none|
|version|integer(int64)|false|none|none|
|updatedAt|string|false|none|none|

<h2 id="tocS_core.taxItem.TaxDto">core.taxItem.TaxDto</h2>
<!-- backwards compatibility -->
<a id="schemacore.taxitem.taxdto"></a>
<a id="schema_core.taxItem.TaxDto"></a>
<a id="tocScore.taxitem.taxdto"></a>
<a id="tocscore.taxitem.taxdto"></a>

```json
{
  "owner": "string",
  "appToCreate": "string",
  "updatedBy": "string",
  "code": "string",
  "dataVersion": "string",
  "isArchived": true,
  "onlyVisibleToCreatorApp": true,
  "locationToCreate": "string",
  "objectClass": "string",
  "appSubClass": "string",
  "appSubKey": "string",
  "version": 0,
  "percent": 0,
  "createdAt": "string",
  "createdBy": "string",
  "name": "string",
  "objectName": "string",
  "appKey": "string",
  "id": "string",
  "updatedAt": "string"
}

```

TaxDto

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|owner|string|false|none|none|
|appToCreate|string|false|none|none|
|updatedBy|string|false|none|none|
|code|string|false|none|none|
|dataVersion|string|false|none|none|
|isArchived|boolean|false|none|none|
|onlyVisibleToCreatorApp|boolean|false|none|none|
|locationToCreate|string|false|none|none|
|objectClass|string|false|none|none|
|appSubClass|string|false|none|none|
|appSubKey|string|false|none|none|
|version|integer(int64)|false|none|none|
|percent|number(double)|false|none|none|
|createdAt|string|false|none|none|
|createdBy|string|false|none|none|
|name|string|false|none|none|
|objectName|string|false|none|none|
|appKey|string|false|none|none|
|id|string|false|none|none|
|updatedAt|string|false|none|none|

<h2 id="tocS_core.taxItem.ShowArchivedTaxItemReq">core.taxItem.ShowArchivedTaxItemReq</h2>
<!-- backwards compatibility -->
<a id="schemacore.taxitem.showarchivedtaxitemreq"></a>
<a id="schema_core.taxItem.ShowArchivedTaxItemReq"></a>
<a id="tocScore.taxitem.showarchivedtaxitemreq"></a>
<a id="tocscore.taxitem.showarchivedtaxitemreq"></a>

```json
{
  "pagingAndSorting": {
    "sortOrder": "ASC",
    "limit": 0,
    "lastIndex": "string"
  }
}

```

ShowArchivedTaxItemReq

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|pagingAndSorting|[core.taxItem.PagingAndSorting](#schemacore.taxitem.pagingandsorting)|false|none|none|

<h2 id="tocS_core.taxItem.SearchTaxItemFilter">core.taxItem.SearchTaxItemFilter</h2>
<!-- backwards compatibility -->
<a id="schemacore.taxitem.searchtaxitemfilter"></a>
<a id="schema_core.taxItem.SearchTaxItemFilter"></a>
<a id="tocScore.taxitem.searchtaxitemfilter"></a>
<a id="tocscore.taxitem.searchtaxitemfilter"></a>

```json
{
  "itemId": [
    "string"
  ],
  "taxId": [
    "string"
  ],
  "taxItemId": [
    "string"
  ]
}

```

SearchTaxItemFilter

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|itemId|[string]|false|none|none|
|taxId|[string]|false|none|none|
|taxItemId|[string]|false|none|none|

<h2 id="tocS_core.taxItem.SearchTaxItemReq">core.taxItem.SearchTaxItemReq</h2>
<!-- backwards compatibility -->
<a id="schemacore.taxitem.searchtaxitemreq"></a>
<a id="schema_core.taxItem.SearchTaxItemReq"></a>
<a id="tocScore.taxitem.searchtaxitemreq"></a>
<a id="tocscore.taxitem.searchtaxitemreq"></a>

```json
{
  "queryString": "string",
  "pagingAndSorting": {
    "sortOrder": "ASC",
    "limit": 0,
    "lastIndex": "string"
  }
}

```

SearchTaxItemReq

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|queryString|string|false|none|none|
|pagingAndSorting|[core.taxItem.PagingAndSorting](#schemacore.taxitem.pagingandsorting)|false|none|none|

<h2 id="tocS_core.taxItem.GetTaxItemByIdReq">core.taxItem.GetTaxItemByIdReq</h2>
<!-- backwards compatibility -->
<a id="schemacore.taxitem.gettaxitembyidreq"></a>
<a id="schema_core.taxItem.GetTaxItemByIdReq"></a>
<a id="tocScore.taxitem.gettaxitembyidreq"></a>
<a id="tocscore.taxitem.gettaxitembyidreq"></a>

```json
{
  "id": "string"
}

```

GetTaxItemByIdReq

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|id|string|false|none|none|

<h2 id="tocS_core.taxItem.GetTaxItemByIdRes">core.taxItem.GetTaxItemByIdRes</h2>
<!-- backwards compatibility -->
<a id="schemacore.taxitem.gettaxitembyidres"></a>
<a id="schema_core.taxItem.GetTaxItemByIdRes"></a>
<a id="tocScore.taxitem.gettaxitembyidres"></a>
<a id="tocscore.taxitem.gettaxitembyidres"></a>

```json
{
  "taxItemDto": {
    "owner": "string",
    "itemId": "string",
    "createdAt": "string",
    "updatedBy": "string",
    "createdBy": "string",
    "dataVersion": "string",
    "taxId": "string",
    "isArchived": true,
    "id": "string",
    "version": 0,
    "updatedAt": "string"
  }
}

```

GetTaxItemByIdRes

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|taxItemDto|[core.taxItem.TaxItemDto](#schemacore.taxitem.taxitemdto)|false|none|none|

<h2 id="tocS_core.taxItem.SearchTaxItemRes">core.taxItem.SearchTaxItemRes</h2>
<!-- backwards compatibility -->
<a id="schemacore.taxitem.searchtaxitemres"></a>
<a id="schema_core.taxItem.SearchTaxItemRes"></a>
<a id="tocScore.taxitem.searchtaxitemres"></a>
<a id="tocscore.taxitem.searchtaxitemres"></a>

```json
{
  "data": [
    {
      "owner": "string",
      "itemId": "string",
      "createdAt": "string",
      "updatedBy": "string",
      "createdBy": "string",
      "dataVersion": "string",
      "taxId": "string",
      "isArchived": true,
      "id": "string",
      "version": 0,
      "updatedAt": "string"
    }
  ]
}

```

SearchTaxItemRes

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|data|[[core.taxItem.TaxItemDto](#schemacore.taxitem.taxitemdto)]|false|none|none|

<h2 id="tocS_core.taxItem.TimeRangeFilter">core.taxItem.TimeRangeFilter</h2>
<!-- backwards compatibility -->
<a id="schemacore.taxitem.timerangefilter"></a>
<a id="schema_core.taxItem.TimeRangeFilter"></a>
<a id="tocScore.taxitem.timerangefilter"></a>
<a id="tocscore.taxitem.timerangefilter"></a>

```json
{
  "createdFrom": "string",
  "updatedFrom": "string",
  "updatedTo": "string",
  "createdTo": "string"
}

```

TimeRangeFilter

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|createdFrom|string|false|none|none|
|updatedFrom|string|false|none|none|
|updatedTo|string|false|none|none|
|createdTo|string|false|none|none|

<h2 id="tocS_core.taxItem.PagingAndSorting">core.taxItem.PagingAndSorting</h2>
<!-- backwards compatibility -->
<a id="schemacore.taxitem.pagingandsorting"></a>
<a id="schema_core.taxItem.PagingAndSorting"></a>
<a id="tocScore.taxitem.pagingandsorting"></a>
<a id="tocscore.taxitem.pagingandsorting"></a>

```json
{
  "sortOrder": "ASC",
  "limit": 0,
  "lastIndex": "string"
}

```

PagingAndSorting

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|sortOrder|enum|false|none|none|
|limit|integer(int32)|false|none|none|
|lastIndex|string|false|none|none|

#### Enumerated Values

|Property|Value|
|---|---|
|sortOrder|ASC|
|sortOrder|DESC|

<h2 id="tocS_core.taxItem.ArchiveTaxItemReq">core.taxItem.ArchiveTaxItemReq</h2>
<!-- backwards compatibility -->
<a id="schemacore.taxitem.archivetaxitemreq"></a>
<a id="schema_core.taxItem.ArchiveTaxItemReq"></a>
<a id="tocScore.taxitem.archivetaxitemreq"></a>
<a id="tocscore.taxitem.archivetaxitemreq"></a>

```json
{
  "optimisticVersion": 0,
  "taxItemId": "string"
}

```

ArchiveTaxItemReq

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|optimisticVersion|integer(int64)|false|none|none|
|taxItemId|string|false|none|none|

<h2 id="tocS_core.taxItem.PurgeTaxItemRes">core.taxItem.PurgeTaxItemRes</h2>
<!-- backwards compatibility -->
<a id="schemacore.taxitem.purgetaxitemres"></a>
<a id="schema_core.taxItem.PurgeTaxItemRes"></a>
<a id="tocScore.taxitem.purgetaxitemres"></a>
<a id="tocscore.taxitem.purgetaxitemres"></a>

```json
{
  "listTaxItemId": [
    "string"
  ]
}

```

PurgeTaxItemRes

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|listTaxItemId|[string]|false|none|none|

<h2 id="tocS_core.taxItem.CreateTaxItemRes">core.taxItem.CreateTaxItemRes</h2>
<!-- backwards compatibility -->
<a id="schemacore.taxitem.createtaxitemres"></a>
<a id="schema_core.taxItem.CreateTaxItemRes"></a>
<a id="tocScore.taxitem.createtaxitemres"></a>
<a id="tocscore.taxitem.createtaxitemres"></a>

```json
{
  "taxItemDto": {
    "owner": "string",
    "itemId": "string",
    "createdAt": "string",
    "updatedBy": "string",
    "createdBy": "string",
    "dataVersion": "string",
    "taxId": "string",
    "isArchived": true,
    "id": "string",
    "version": 0,
    "updatedAt": "string"
  }
}

```

CreateTaxItemRes

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|taxItemDto|[core.taxItem.TaxItemDto](#schemacore.taxitem.taxitemdto)|false|none|none|

<h2 id="tocS_core.taxItem.PurgeTaxItemReq">core.taxItem.PurgeTaxItemReq</h2>
<!-- backwards compatibility -->
<a id="schemacore.taxitem.purgetaxitemreq"></a>
<a id="schema_core.taxItem.PurgeTaxItemReq"></a>
<a id="tocScore.taxitem.purgetaxitemreq"></a>
<a id="tocscore.taxitem.purgetaxitemreq"></a>

```json
{
  "ageing": 0
}

```

PurgeTaxItemReq

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|ageing|integer(int64)|false|none|none|

<h2 id="tocS_core.taxItem.ArchiveTaxItemRes">core.taxItem.ArchiveTaxItemRes</h2>
<!-- backwards compatibility -->
<a id="schemacore.taxitem.archivetaxitemres"></a>
<a id="schema_core.taxItem.ArchiveTaxItemRes"></a>
<a id="tocScore.taxitem.archivetaxitemres"></a>
<a id="tocscore.taxitem.archivetaxitemres"></a>

```json
{
  "taxItemDto": {
    "owner": "string",
    "itemId": "string",
    "createdAt": "string",
    "updatedBy": "string",
    "createdBy": "string",
    "dataVersion": "string",
    "taxId": "string",
    "isArchived": true,
    "id": "string",
    "version": 0,
    "updatedAt": "string"
  }
}

```

ArchiveTaxItemRes

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|taxItemDto|[core.taxItem.TaxItemDto](#schemacore.taxitem.taxitemdto)|false|none|none|

<h2 id="tocS_core.taxItem.CreateTaxItemReq">core.taxItem.CreateTaxItemReq</h2>
<!-- backwards compatibility -->
<a id="schemacore.taxitem.createtaxitemreq"></a>
<a id="schema_core.taxItem.CreateTaxItemReq"></a>
<a id="tocScore.taxitem.createtaxitemreq"></a>
<a id="tocscore.taxitem.createtaxitemreq"></a>

```json
{
  "itemId": "string",
  "taxId": "string"
}

```

CreateTaxItemReq

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|itemId|string|false|none|none|
|taxId|string|false|none|none|

<h2 id="tocS_core.taxItem.RecoverTaxItemRes">core.taxItem.RecoverTaxItemRes</h2>
<!-- backwards compatibility -->
<a id="schemacore.taxitem.recovertaxitemres"></a>
<a id="schema_core.taxItem.RecoverTaxItemRes"></a>
<a id="tocScore.taxitem.recovertaxitemres"></a>
<a id="tocscore.taxitem.recovertaxitemres"></a>

```json
{
  "taxItemDto": {
    "owner": "string",
    "itemId": "string",
    "createdAt": "string",
    "updatedBy": "string",
    "createdBy": "string",
    "dataVersion": "string",
    "taxId": "string",
    "isArchived": true,
    "id": "string",
    "version": 0,
    "updatedAt": "string"
  }
}

```

RecoverTaxItemRes

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|taxItemDto|[core.taxItem.TaxItemDto](#schemacore.taxitem.taxitemdto)|false|none|none|

<h2 id="tocS_core.taxItem.RecoverTaxItemReq">core.taxItem.RecoverTaxItemReq</h2>
<!-- backwards compatibility -->
<a id="schemacore.taxitem.recovertaxitemreq"></a>
<a id="schema_core.taxItem.RecoverTaxItemReq"></a>
<a id="tocScore.taxitem.recovertaxitemreq"></a>
<a id="tocscore.taxitem.recovertaxitemreq"></a>

```json
{
  "taxItemId": "string"
}

```

RecoverTaxItemReq

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|taxItemId|string|false|none|none|

<h2 id="tocS_core.taxItem.CountSearchTaxItemReq">core.taxItem.CountSearchTaxItemReq</h2>
<!-- backwards compatibility -->
<a id="schemacore.taxitem.countsearchtaxitemreq"></a>
<a id="schema_core.taxItem.CountSearchTaxItemReq"></a>
<a id="tocScore.taxitem.countsearchtaxitemreq"></a>
<a id="tocscore.taxitem.countsearchtaxitemreq"></a>

```json
{
  "queryString": "string"
}

```

CountSearchTaxItemReq

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|queryString|string|false|none|none|

<h2 id="tocS_core.taxItem.GetTaxByItemIdRes">core.taxItem.GetTaxByItemIdRes</h2>
<!-- backwards compatibility -->
<a id="schemacore.taxitem.gettaxbyitemidres"></a>
<a id="schema_core.taxItem.GetTaxByItemIdRes"></a>
<a id="tocScore.taxitem.gettaxbyitemidres"></a>
<a id="tocscore.taxitem.gettaxbyitemidres"></a>

```json
{
  "taxList": [
    {
      "owner": "string",
      "appToCreate": "string",
      "updatedBy": "string",
      "code": "string",
      "dataVersion": "string",
      "isArchived": true,
      "onlyVisibleToCreatorApp": true,
      "locationToCreate": "string",
      "objectClass": "string",
      "appSubClass": "string",
      "appSubKey": "string",
      "version": 0,
      "percent": 0,
      "createdAt": "string",
      "createdBy": "string",
      "name": "string",
      "objectName": "string",
      "appKey": "string",
      "id": "string",
      "updatedAt": "string"
    }
  ]
}

```

GetTaxByItemIdRes

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|taxList|[[core.taxItem.TaxDto](#schemacore.taxitem.taxdto)]|false|none|none|

<h2 id="tocS_core.taxItem.ShowArchivedTaxItemRes">core.taxItem.ShowArchivedTaxItemRes</h2>
<!-- backwards compatibility -->
<a id="schemacore.taxitem.showarchivedtaxitemres"></a>
<a id="schema_core.taxItem.ShowArchivedTaxItemRes"></a>
<a id="tocScore.taxitem.showarchivedtaxitemres"></a>
<a id="tocscore.taxitem.showarchivedtaxitemres"></a>

```json
{
  "listTaxItemDtoArchived": [
    {
      "owner": "string",
      "itemId": "string",
      "createdAt": "string",
      "updatedBy": "string",
      "createdBy": "string",
      "dataVersion": "string",
      "taxId": "string",
      "isArchived": true,
      "id": "string",
      "version": 0,
      "updatedAt": "string"
    }
  ]
}

```

ShowArchivedTaxItemRes

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|listTaxItemDtoArchived|[[core.taxItem.TaxItemDto](#schemacore.taxitem.taxitemdto)]|false|none|none|

<h2 id="tocS_core.taxItem.GetTaxByItemIdReq">core.taxItem.GetTaxByItemIdReq</h2>
<!-- backwards compatibility -->
<a id="schemacore.taxitem.gettaxbyitemidreq"></a>
<a id="schema_core.taxItem.GetTaxByItemIdReq"></a>
<a id="tocScore.taxitem.gettaxbyitemidreq"></a>
<a id="tocscore.taxitem.gettaxbyitemidreq"></a>

```json
{
  "itemId": "string"
}

```

GetTaxByItemIdReq

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|itemId|string|false|none|none|

<h2 id="tocS_core.taxItem.CountRes">core.taxItem.CountRes</h2>
<!-- backwards compatibility -->
<a id="schemacore.taxitem.countres"></a>
<a id="schema_core.taxItem.CountRes"></a>
<a id="tocScore.taxitem.countres"></a>
<a id="tocscore.taxitem.countres"></a>

```json
{
  "count": 0
}

```

CountRes

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|count|integer(int64)|false|none|none|

<h2 id="tocS_core.taxItem.CountArchiveTaxItemReq">core.taxItem.CountArchiveTaxItemReq</h2>
<!-- backwards compatibility -->
<a id="schemacore.taxitem.countarchivetaxitemreq"></a>
<a id="schema_core.taxItem.CountArchiveTaxItemReq"></a>
<a id="tocScore.taxitem.countarchivetaxitemreq"></a>
<a id="tocscore.taxitem.countarchivetaxitemreq"></a>

```json
{}

```

CountArchiveTaxItemReq

### Properties

*None*

