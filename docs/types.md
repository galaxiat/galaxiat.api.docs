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

## Types : 

### `EMAIL` :
Email should be formatted according to [RFC5322](https://datatracker.ietf.org/doc/html/rfc5322#section-3.4.1)

Ref = `[EMAIL](/docs/types.md#email)`

### `LONGTEXT` : 
Longtext is a set of chars that can contain specials chars such as emojis, breaks, and spaces.

Ref = `[LONGTEXT](/docs/types.md#longtext)`

### `TEXT` :
Text is a set of chars that can contain specials chars such as emojis and spaces but no breaks.

Ref = `[TEXT](/docs/types.md#text)`

### `TEXTNORMAL` :
Textnormal is a set of chars that math the following regex `/^[a-zA-Z0-9]+$/`

Ref = `[TEXTNORMAL](/docs/types.md#textnormal)`

### `TEXTNORMALS` :
Textnormals is a set of chars that math the following regex `/^[a-zA-Z0-9 *]+$/`

Ref = `[TEXTNORMALS](/docs/types.md#textnormals)`

### `RESPONSE` :
RESPONSE is a json object that define api response and data in the data key (defined per route)

```json
{
  "type" : "ok" | "error",
  "message" : string,
  "data" : dataobject
}
```
Ref = `[RESPONSE](/docs/types.md#response)`