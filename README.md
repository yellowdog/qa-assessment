
## Run

```
docker-compose up -d
```

## API

All endpoints are exposed under `http://localhost:8080/api/contacts`

### Find all contacts

```http request
GET http://localhost:8080/api/contacts
```

### Create contact

```http request
POST http://localhost:8080/api/contacts
Content-Type: application/json

{
  "firstName": "John",
  "surname": "Smith",
  "addresses": [
    {
      "addressType": "HOME",
      "houseNumber": "214",
      "streetAddress": "Example Road",
      "city": "Example City",
      "postCode": "BS24 3SQ"
    }
  ]
}
```

### Get contact

```http request
GET http://localhost:8080/api/contacts/{{contacts_id}}
```

### Update contact

```http request
PUT http://localhost:8080/api/contacts/{{contacts_id}}
Content-Type: application/json

{
  "id": "{{contacts_id}}",
  "firstName": "John",
  "surname": "Doe",
  "addresses": [
    {
      "addressType": "HOME",
      "houseNumber": "214",
      "streetAddress": "Example Road",
      "city": "Example City",
      "postCode": "BS24 3SQ"
    }
  ]
}
```

### Delete Contact

```http request
DELETE http://localhost:8080/api/contacts/{{contacts_id}}
```

## Database

Mongo is exposed at `http://localhost:27017`