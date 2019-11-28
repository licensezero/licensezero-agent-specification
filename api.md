# License Zero Agent API

## Endpoints

### Offer Data

`GET /api/1.0.0/offers/{offerID}`

- `offerID`: a version 4 UUID

Response: `application/json`

### Licensor Data

`GET /api/1.0.0/licensors/{licensorID}`

`licensorID`: a version 4 UUID

`application/json`

### Order

`POST /order`

Request: `multipart/form-data`

- `licensee`: licensee's full legal name
- `jurisdiction`: ISO 3166-2 code for the licensee's jurisdiction
- `email`: licensee's e-mail address
- `notEntity`: the string `The licensee is a natural person, not a legal entity.`
- `offerID[]`: the `offerID`s for which to buy licenses

Response: `303`

Header: `Location: {url}`
