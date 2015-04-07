# Fetch User Balance

```shell
Example Request

$ curl https://punchh.com/api/v5/checkins/balance?phone='8013005479' -H 'Authorization: Token token="xxxxxx"'

$ curl https://punchh.com/api/v5/checkins/balance?email='threenet@yahoo.com' -H 'Authorization: Token token="xxxxxx"'

```
```shell
Example Response

{
  "first_name": "Tonya",
  "last_name": "Merkley",
  "registered": true,
  "avatar_url": "https://secure.gravatar.com/avatar/5ffa39b70fa77cd7250f11705bb7052a.png?d=http%3A%2F%2Flocalhost%3A3000%2Fimages%2Fdefault%2Favatar.png&r=PG&s=40",
  "points_added": 0
}
```
```shell
Error Response

401 Unauthorized HTTP Token: Access denied.

404 Not found
User account not found
```

<p>Use <code>https://punchh.com/api/v5/checkins/balance</code> to user balance information</p>
<p><b>Authentication</b></p>
<p>This API is authenticated. Location key token must be provided as credentials.</p>

<p><b>HTTP Request Type</b></p>
<p>GET</p>

<p><b>Query Parameters</b></p>
Every Request must have phone or email as a parameter.
<table>
  <thead>
    <tr>
      <th align="left"><strong>field</strong></th>
      <th align="left"><strong>sample value</strong></th>
      <th align="left"><strong>explanation</strong></th>
      <th align="left"><strong>mandatory</strong></th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td align="left"><code>phone</code></td>
      <td align="left"><code>8013005479</code></td>
      <td align="left">Phone number of the user</td>
      <td align="left">yes</td>
    </tr>
    <tr>
      <td align="left"><code>email</code></td>
      <td align="left"><code>threenet@yahoo.com</code></td>
      <td align="left">Email of the user</td>
      <td align="left">yes</td>
    </tr>
  </tbody>
</table>