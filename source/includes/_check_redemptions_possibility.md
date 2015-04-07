# Check Redemptions possible or not

```shell
Example Request
$ curl https://punchh.com/api/v5/redemptions/possible?phone='8013005479' -H 'Authorization: Token token="xxxxxx"'

```
```shell
Example Response

{
  "status": "Allowed discount of 500.0 is more than the effective possible discount of 0.0 on the receipt. Customer may wish to apply this redemption on a future invoice?",
  "redemption_amount": 0,
  "category": "redeemable"
}
```
```shell
Error Response

401 Unauthorized HTTP Token: Access denied.

404 Not found
User account not found
Reward is not available: None Alive
```

<p>Use <code>https://punchh.com/api/v5/redemptions</code> to create a redemption</p>
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