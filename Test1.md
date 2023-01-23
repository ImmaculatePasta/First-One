<!--- This is the resource description which explains to the reader the information, or objects, returned by API call -->
# /{PetId}

Returns information about all the dogs in our store, including the category of dog, breed, fur and personality type. It also provides a photo. 

`{PetId}` is the unique identifier (integer) and is available for each dog in our online catalogue.

<!--- This is the description on how to access the resource-->
## Endpoint definition

`/Pet/{PetId}`  

<!--- This explains to the reader the API method used to make the API call. This call only allows for the GET Method -->
## HTTP method

<span class="label label-primary">GET</span>

<!--- This describes the path parameters and how to call for a pet in the API call, along with its data type-->
## Parameters

| Parameter | Description | Data Type |
|-----------|------|----------|
| {id} | The ID is four digits starting at 1111 and moves incrementally, 1112, 1113, 1114... to a max of 9999| integer |

<!--- This explains to the reader how to call the API by URL for the JSON payload and filter through IDs-->
## Sample request
To fetch a dog's data and render the JSON payload in a web browser, make the following request and change the ID path parameter.
```
  'https://petstore.swagger.io/v2/pet/1111' \
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

The following table describes each item in the JSON response.

|Response item | Description |
|----------|------------|
| **category** | The broadest description of the dog e.g. big, small. |
| **name** | The particular breed of dog. |
| **tags** | The physical and personality traits unique to that breed of dog. |
| **photoUrls** | A generic photo from Wikipedia Commons.  | 
| **status** | Checks if the dog is available or unavailable at our store.  |


## Error and status codes

The following table lists the status and error codes related to this request.

| Status code | Meaning |
|--------|----------|
| 200 | Successful response |
| 400 | Bad request -- one or more of the parameters was rejected. |
| 4112 | The Pet ID was not found in the lookup. |