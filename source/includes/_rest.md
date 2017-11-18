# RESTFul APIs

## Create New Data



```shell
curl --request POST \
  --url BASE_URL/:project_key/:collection_name \
  --header 'cache-control: no-cache' \
  --header 'content-type: application/json' \
  --header 'postman-token: d2fba63a-53b5-1f85-82fd-4d2fd17d2125' \
  --data '{\r\n	"name":"arizal",\r\n	"hobby":["makan","minum","tidur"],\r\n	"sekolah":{\r\n		"sd":{\r\n			"name":"sd n1 pentur",\r\n			"rangking":1\r\n		},\r\n		"sma":{\r\n			"name":"sma n 1 simo",\r\n			"rangking":1\r\n		},\r\n		"smp":{\r\n			"name":"smp n1 pentur",\r\n			"rangking":1\r\n		}\r\n	},\r\n	"nikah":false\r\n}'
```


> The above command returns JSON structured like your json body data:

```json
{
    "name": "arizal",
    "hobby": [
        "makan",
        "minum",
        "tidur"
    ],
    "sekolah": {
        "sd": {
            "name": "sd n1 pentur",
            "rangking": 1
        },
        "sma": {
            "name": "sma n 1 simo",
            "rangking": 1
        },
        "smp": {
            "name": "smp n1 pentur",
            "rangking": 1
        }
    },
    "nikah": false,
    "id": "5a104231f08d282b70822e22",
    "createdAt": "2017-11-18T14:22:41.462Z",
    "updatedAt": "2017-11-18T14:22:41.462Z"
}
```

endpoint for creating new data.

### HTTP Request

`POST BASE_URL/:project_key/:collection_name`

<aside class="notice">
replace <code>:project_key</code> with your <code>project_key</code> and replace <code>:collection_name</code> wwith name what you want. <code>collection_name</code> just like table
</aside>


<aside class="notice">
don't forget using json request, and json body request is flexible, customable, create anything what you want.
</aside>


<aside class="success">
Remember — if you enable auth, don't forget add <code>API-Token</code> header
</aside>

## Update Data


```shell
curl --request PUT \
  --url BASE_URL/:project_key/:collection_name/:id \
  --header 'cache-control: no-cache' \
  --header 'content-type: application/json' \
  --header 'postman-token: c82946d2-900a-4ad6-1a34-3a5f78668331' \
  --data '{\r\n	"name":"arizal saputro",\r\n	"hobby":["makan","minum","tidur","ngoding"],\r\n	"sekolah":{\r\n		"sd":{\r\n			"name":"sd n1 pentur",\r\n			"rangking":3\r\n		},\r\n		"sma":{\r\n			"name":"sma n 1 simo",\r\n			"rangking":4\r\n		},\r\n		"smp":{\r\n			"name":"smp n1 pentur",\r\n			"rangking":6\r\n		}\r\n	},\r\n	"nikah":true\r\n}'
```


> The above command returns JSON structured like your json body data:

```json
{
    "nikah": true,
    "sekolah": {
        "smp": {
            "rangking": 6,
            "name": "smp n1 pentur"
        },
        "sma": {
            "rangking": 4,
            "name": "sma n 1 simo"
        },
        "sd": {
            "rangking": 3,
            "name": "sd n1 pentur"
        }
    },
    "hobby": [
        "makan",
        "minum",
        "tidur",
        "ngoding"
    ],
    "name": "arizal saputro",
    "id": "5a104231f08d282b70822e22",
    "createdAt": "2017-11-18T14:22:41.462Z",
    "updatedAt": "2017-11-18T14:36:03.897Z"
}
```

endpoint for updating new data.

### HTTP Request

`PUT BASE_URL/:project_key/:collection_name/:id`

<aside class="notice">
replace <code>:project_key</code> with your <code>project_key</code>
replace <code>:collection_name</code> wwith name what you want. <code>collection_name</code> just like table
replace <code>:id</code> with <code>id</code> of data
</aside>


<aside class="notice">
don't forget using json request, and json body request is flexible, customable, create anything what you want.
</aside>


<aside class="success">
Remember — if you enable auth, don't forget add <code>API-Token</code> header
</aside>


## Delete Single Data


```shell
curl --request DELETE \
  --url BASE_URL/:project_key/:collection_name/:id \
  --header 'cache-control: no-cache' \
  --header 'content-type: application/json' \
  --header 'postman-token: 24472e0b-c54d-d930-29da-08a8eefdc096'
```


> The above command returns JSON structured like your json body data:

```json
{
    "nikah": true,
    "sekolah": {
        "smp": {
            "rangking": 6,
            "name": "smp n1 pentur"
        },
        "sma": {
            "rangking": 4,
            "name": "sma n 1 simo"
        },
        "sd": {
            "rangking": 3,
            "name": "sd n1 pentur"
        }
    },
    "hobby": [
        "makan",
        "minum",
        "tidur",
        "ngoding"
    ],
    "name": "arizal saputro",
    "id": "5a104231f08d282b70822e22",
    "createdAt": "2017-11-18T14:22:41.462Z",
    "updatedAt": "2017-11-18T14:36:03.897Z"
}
```

endpoint for deleting single data.

### HTTP Request

`DELETE BASE_URL/:project_key/:collection_name/:id`

<aside class="notice">
replace <code>:project_key</code> with your <code>project_key</code>
replace <code>:collection_name</code> wwith name what you want. <code>collection_name</code> just like table
replace <code>:id</code> with <code>id</code> of data
</aside>

<aside class="success">
Remember — if you enable auth, don't forget add <code>API-Token</code> header
</aside>

## Delete Collection (all data inside collection)


```shell
curl --request DELETE \
  --url BASE_URL/:project_key/:collection_name/:id \
  --header 'cache-control: no-cache' \
  --header 'content-type: application/json' \
  --header 'postman-token: 24472e0b-c54d-d930-29da-08a8eefdc096'
```


> The above command returns JSON structured like your json body data:

```json
{
    "n": 0,
    "ok": 1
}
```

endpoint for deleting single data.

### HTTP Request

`DELETE BASE_URL/:project_key/:collection_name/:id`

<aside class="notice">
replace <code>:project_key</code> with your <code>project_key</code>
replace <code>:collection_name</code> wwith name what you want. <code>collection_name</code> just like table
replace <code>:id</code> with <code>id</code> of data
</aside>

<aside class="success">
Remember — if you enable auth, don't forget add <code>API-Token</code> header
</aside>



## Get List of Collection

```shell
curl --request GET \
  --url BASE_URL/:project_key/:collection_name/:id  \
  --header 'cache-control: no-cache' \
  --header 'content-type: application/json' \
  --header 'postman-token: b1e8c69f-a527-bad1-b409-019bb2725484'
```


> The above command returns JSON structured like this:

```json
{
    "meta": {
        "current_page": 1,
        "total_data": 4,
        "limit": 100,
        "sort": "-createdAt"
    },
    "data": [
        {
            "nikah": true,
            "sekolah": {
                "smp": {
                    "rangking": 1,
                    "name": "smp n1 pentur"
                },
                "sma": {
                    "rangking": 1,
                    "name": "sma n 1 simo"
                },
                "sd": {
                    "rangking": 1,
                    "name": "sd n1 pentur"
                }
            },
            "hobby": [
                "makan",
                "minum",
                "tidur"
            ],
            "name": "agi maulana ",
            "id": "5a104800f08d282b70822e24",
            "createdAt": "2017-11-18T14:47:28.684Z",
            "updatedAt": "2017-11-18T14:47:28.684Z"
        },
        {
            "nikah": false,
            "sekolah": {
                "smp": {
                    "rangking": 1,
                    "name": "smp n1 pentur"
                },
                "sma": {
                    "rangking": 1,
                    "name": "sma n 1 simo"
                },
                "sd": {
                    "rangking": 1,
                    "name": "sd n1 pentur"
                }
            },
            "hobby": [
                "makan",
                "minum",
                "tidur"
            ],
            "name": "arizal",
            "id": "5a1047e0f08d282b70822e23",
            "createdAt": "2017-11-18T14:46:56.579Z",
            "updatedAt": "2017-11-18T14:46:56.579Z"
        }
    ]
}
```

get list of collection.


### HTTP Request

`GET BASE_URL/:project_key/:collection_name`

### URL Parameters

Parameter | Description
--------- | -----------
project_key | key of project
collection_name | name of collection

### Query Parameters (Optional)

Parameter | Description | Example
--------- | ----------- | -------
field | name of field to get | "status"
value | value of field to find | true
sort |sorting data | "createdAt" , "-createdAt"
offset | offset data ,start at | 0
limit | limit data to show | 10
page | data page | 1 / 2 / 3

## Get a Data

```shell
curl --request GET \
  --url BASE_URL/:project_key/:collection_name/:id
  --header 'cache-control: no-cache' \
  --header 'content-type: application/json' \
  --header 'postman-token: 0924681e-0a48-2678-082f-6a2fb6727472'
```


> The above command returns JSON structured like this:

```json
{
    "nikah": true,
    "sekolah": {
        "smp": {
            "rangking": 1,
            "name": "smp n1 pentur"
        },
        "sma": {
            "rangking": 1,
            "name": "sma n 1 simo"
        },
        "sd": {
            "rangking": 1,
            "name": "sd n1 pentur"
        }
    },
    "hobby": [
        "makan",
        "minum",
        "tidur"
    ],
    "name": "agi maulana ",
    "id": "5a104800f08d282b70822e24",
    "createdAt": "2017-11-18T14:47:28.684Z",
    "updatedAt": "2017-11-18T14:47:28.684Z"
}
```

get a data of collection.


### HTTP Request

`GET BASE_URL/:project_key/:collection_name/:id`

### URL Parameters

Parameter | Description
--------- | -----------
project_key | key of project
collection_name | name of collection
id | id of collection


## Search Data

```shell
curl --request GET \
  --url 'BASE_URL/:project_key/:collection_name/search?field=name&value=ari' \
  --header 'cache-control: no-cache' \
  --header 'content-type: application/json' \
  --header 'postman-token: 1a66f8ab-af91-befb-2ac8-12f29e275ec0' \
```


> The above command returns JSON structured like this:

```json
{
    "meta": {
        "current_page": 1,
        "total_data": 1,
        "limit": 100,
        "sort": "-createdAt"
    },
    "data": [
        {
            "nikah": false,
            "sekolah": {
                "smp": {
                    "rangking": 1,
                    "name": "smp n1 pentur"
                },
                "sma": {
                    "rangking": 1,
                    "name": "sma n 1 simo"
                },
                "sd": {
                    "rangking": 1,
                    "name": "sd n1 pentur"
                }
            },
            "hobby": [
                "makan",
                "minum",
                "tidur"
            ],
            "name": "arizal",
            "id": "5a1047e0f08d282b70822e23",
            "createdAt": "2017-11-18T14:46:56.579Z",
            "updatedAt": "2017-11-18T14:46:56.579Z"
        }
    ]
}
```

search data inside collection


### HTTP Request

`GET BASE_URL/:project_key/:collection_name`

### URL Parameters

Parameter | Description
--------- | -----------
project_key | key of project
collection_name | name of collection

### Query Parameters (Optional)

Parameter | Description | Example
--------- | ----------- | -------
field | name of field to get | "status"
value | value of field to find | true
sort |sorting data | "createdAt" , "-createdAt"
offset | offset data ,start at | 0
limit | limit data to show | 10
page | data page | 1 / 2 / 3

## Is Data Exist

```shell
curl --request GET \
  --url 'BASE_URL/:project_key/:collection_name//is_exist?field=nikah&value=true' \
  --header 'cache-control: no-cache' \
  --header 'content-type: application/json' \
  --header 'postman-token: 65082054-4d1f-b96e-5cb2-029bc30cc6d6'
```


> The above command returns JSON structured like this:

```json
{
    "status": true
}
```

check if data with specific value


### HTTP Request

`GET BASE_URL/:project_key/:collection_name/is_exist`

### URL Parameters

Parameter | Description
--------- | -----------
project_key | key of project
collection_name | name of collection

### Query Parameters (Optional)

Parameter | Description | Example
--------- | ----------- | -------
field | name of field to get | "status"
value | value of field to find | true
sort |sorting data | "createdAt" , "-createdAt"
offset | offset data ,start at | 0
limit | limit data to show | 10
page | data page | 1 / 2 / 3

