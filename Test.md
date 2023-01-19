# /{PetId}

Returns information about the dog, including the category of dog, breed name, fur and personality type. Also provides a photo

`{PetId}` refers to the unique ID number (integer) for the dog you want to look up. 

## Endpoint definition

`surfreport/{beachId}`

## HTTP method

<span class="label label-primary">GET</span>

## Parameters

| Parameter | Description | Data Type |
|-----------|------|----------|
| category | *Optional*. The number of days to include in the response.  | string |
| tags | *Optional*. If you include a description, then only such a will be returned in the response.| string |

## Sample request

```
curl -X 'GET' \
  'https://petstore.swagger.io/v2/pet/4444' \
  -H 'accept: application/json'
```

## Sample response

```json
{
  "id": 1111,
  "category": {
    "id": 0,
    "name": "Big dogs"
  },
  "name": "Labradoodle",
  "photoUrls": [
    "https://upload.wikimedia.org/wikipedia/commons/8/85/Labradoodle-Brown-Male-SideFace.jpg"
  ],
  "tags": [
    {
      "id": 0,
      "name": "fluffy"
    }
  ],
  "status": "available"
}
```

The following table describes each item in the response.

|Response item | Description |
|----------|------------|
| **Category** | The broadest description of the dog e.g. big, small. |
| **name** | The particular breed of dog. |
| **tags** | The physical traits unique to that breed of dog. |

## Error and status codes

The following table lists the status and error codes related to this request.

| Status code | Meaning |
|--------|----------|
| 200 | Successful response |
| 400 | Bad request -- one or more of the parameters was rejected. |
| 4112 | The Pet ID was not found in the lookup. |