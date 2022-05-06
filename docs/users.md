<div align="center">
  <br />
  <p>
    <a href="https://galaxiatapp.com"><img src="https://galaxiatapp.com/logo_texte_appli_avec_arrondie_et_ombre.png" width="546" alt="galaxiat.serve.seo" /></a>
  </p>
  <br />
  <p>
    <a href="https://discord.galaxiat.fr"><img src="https://img.shields.io/discord/804787354703364116?color=5865F2&logo=discord&logoColor=white" alt="Discord server" /></a>
  </p>
</div>

## POST `/users`

### Path Params :

- NONE

### Query Params :

- username
  - min : 2 chars
  - max : 15 chars
  - type : [TEXTNORMAL](/docs/types.md#textnormal)
- username_at
  - min : 2 chars
  - max : 15 chars
  - type : [TEXTNORMAL](/docs/types.md#textnormal)
- email
  - type : [EMAIL](/docs/types.md#email)
- password
  - min : 6 chars
  - max : 200 chars
  - type : [TEXT](/docs/types.md#text)

### Headers Params :

- NONE

### Reponse :

- [RESPONSE](/docs/types.md#response)

```json
{
  "data": null
}
```

---

## GET `/users`

### Path Params :

- NONE

### Query Params :

- email
  - type : [EMAIL](/docs/types.md#email)
- password
  - min : 6 chars
  - max : 200 chars
  - type : [TEXT](/docs/types.md#text)

### Headers Params :

- NONE

### Reponse :

- [RESPONSE](/docs/types.md#response)
- data :
  - username : [TEXTNORMAL](/docs/types.md#textnormal)
  - username_at : [TEXTNORMAL](/docs/types.md#textnormal)
  - coins : [NUMBER](/docs/types.md#number)
  - xp : [NUMBER](/docs/types.md#number)
  - email_verified : [BOOLEAN](/docs/types.md#boolean)
  - email : [EMAIL](/docs/types.md#email),
  - admin : [BOOLEAN](/docs/types.md#boolean)

```json
{
  "data": {
    "username": "warstrolo",
    "username_at": "galaxiat",
    "coins": 1000,
    "xp": 1200,
    "email_verified": true,
    "email": "hello@galaxiatapp.com",
    "admin": true
  }
}
```

---
