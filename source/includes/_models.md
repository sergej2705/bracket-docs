# Models
## Bracket
A whole project is called `Bracket`. You can have multiple Brackets in an account.

> An exmple `Bracket` object:

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

field | type | description | mandatory | default value
------|------|-------------|-----------|--------------
id | uuid | unique id | true |
hrid | string | human readable id. MUST be systemwide unique. MUST be only alphanumeric and hyphens. MUST NOT match an uuid regex! | false | `null`
contents | Content[] | the complete user contents, see [Content](#content) | true |
description | string | user's description for this Bracket | false | null

## Content
A `Content` is a user generated content wrapper, it can contain different media file types.

> An exmple `Content` object:

```json
{
  id: 11111111-1111-1111-1111-111111111111,
  description: "A beautiful image",
  mime-type: "image/jpeg",
  previewuri: "https://s3.bracket.to.photo/0000000-0000-0000-0000-000000000000/11111111-1111-1111-1111-111111111111.jpeg"
}
```

field | type | description | mandatory | default value
------|------|-------------|-----------|--------------
id | uuid | unique id | true |
description | string | user's description for this Bracket | false | null
mime-type | string | mime type of the original image (caution: the mime-type of the loaded preview can differ, according to the `Accept`-header) | true