# Brackets
## Get all Brackets
This endpoint retrieves all Brackets associated with the provided API key.

```json
[
  {
    id: 00000000-0000-0000-0000-000000000000,
    hrid: "a-perfect-bracket",
    contents: [{
      // see Content...
    }],
    description: "A beautiful bracket description"
  },
  {
    // ...
  }
]
```

### HTTP Request
`GET https://api.bracket.to.photo/v1/brackets`

### Response
The response is a `Bracket`-array, see [Models > Bracket](#bracket) for model documentation.

## Get a specific Bracket
This endpoint retrieves a specific Bracket identified by its ID.

```json
  {
    id: 00000000-0000-0000-0000-000000000000,
    hrid: "a-perfect-bracket",
    contents: [{
      // see Content...
    }],
    description: "A beautiful bracket description"
  }
```

### HTTP Request
`GET https://api.bracket.to.photo/v1/brackets`

### Response
The response is a `Bracket`-array, see [Models > Bracket](#bracket) for model documentation.