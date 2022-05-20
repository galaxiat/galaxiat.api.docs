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

## Hosts & Envs

### Production

- `https://galaxiatapp.com` > Production Frontend
- `https://api.galaxiatapp.com` > Production API
- `https://cdn.galaxiatapp.com` > Production CDN

### Dev

- `https://dev.galaxiatapp.com` > Beta Frontend
- `https://api-dev.galaxiatapp.com` > Beta API
- `https://cdn-dev.galaxiatapp.com` > Beta CDN

### API Versioning

| Version | Status    | Default | Docs |
| ------- | --------- | ------- | ---- |
| 1       | Soon      | x       | no   |
| 0       | Available | x       | no   |

Soon : API is in active development and will soon be available

Available : API is active

Deprecated : API will be removed soon

Discontinued : API no longer available

## Response

### Version (0,1)

| Field   | Type            | Description                                      |
| ------- | --------------- | ------------------------------------------------ |
| type    | "error" or "ok" | If the request was successful or not             |
| message | string          | Message of the request                           |
| data    | ?               | The data of the request => depend of the request |

## Resources

- [api](/docs/resources/api.md)
- [contents](/docs/resources/contents.md)
- [feeds](/docs/resources/feeds.md)
- [hashtags](/docs/resources/hashtags.md)
- [users](/docs/resources/user.md)
  
## Security

| Field           | Ver | Type   | Example                    | Description |
| --------------- | --- | ------ | -------------------------- | ----------- |
| `authorization` | 1   | string | user xxxx.xxxxxxxxx.xxxxxx | user token  |

## Passing data to the API

All data that are passed to the API are json body

## API routes 

Route relation `/vX/path_to_resources` where X is the version number of the API

Example : `/v1/users`

For API manager target directly the root path (`/`)

## How to read

| Field         | Version   | Type   | Description                                                                                                      |
| ------------- | ----- | ------ | ---------------------------------------------------------------------------------------------------------------- |
| random_info?  | 0-7   | string | random_info is available from version 0 to version 7 and may not be included in all the returns                  |
| random_info!  | 3,7   | string | random_info is available in version 3 and in version 7 and is readonly and will be included in returns           |
| random_info?! | 0,3-4 | string | random_info is available in version 0 and from version 3 to version 4 and may not be included in all the returns |
