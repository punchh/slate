# Create a Checkin

```shell
Example Request

$ curl https://punchh.com/api/v5/checkins -X POST -d 'phone=8013005479&amp;pos_version=V03&amp;sequence_no=2124&amp;transaction_no=4488&amp;receipt_datetime=01/18/15 15:07:26&amp;menu_items[]=Adult|1|23.95|M|1001|1|1&amp;menu_items[]=Adult|1|23.95|M|1001|1|1&amp;=Iced Tea|1|2.75|M|110002|1|38&amp;Adult|1|23.95|M|1001|1|1&amp;=Santa Fe Nut|1|5.00|M|102004|4|79&amp;employee_id=135&amp;employee_name=Chelsea&amp;amount=30.95&amp;cc_last4=0000&amp;punchh_key=xxxx&amp;pos_type=micros&amp;process=true' -H 'Authorization: Token token="xxxxxx"'
```
```shell
Example Response

{
  "first_name": "Tonya",
  "last_name": "Merkley",
  "registered": true,
  "avatar_url": "https://secure.gravatar.com/avatar/5ffa39b70fa77cd7250f11705bb7052a.png?d=http%3A%2F%2Flocalhost%3A3000%2Fimages%2Fdefault%2Favatar.png&r=PG&s=40",
  "points_added": 48
}

```
```shell
Error Response

401 Unauthorized
HTTP Token: Access denied.

404 Not found
User account not found
```

<p>Use <code>https://punchh.com/api/v5/checkins</code> to create a Checkin for a user</p>
<p><b>Authentication</b></p>
<p>This API is authenticated. Location key token must be provided as credentials.</p>

<p><b>HTTP Request Type</b></p>
<p>POST</p>

<p><b>Query Parameters</b></p>
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
      <td align="left"><code>8013005479</code></td>
      <td align="left">Email of the user</td>
      <td align="left">yes</td>
    </tr>
    <tr>
      <td align="left"><code>amount</code></td>
      <td align="left"><code>30.95</code></td>
      <td align="left">Amount of receipt</td>
      <td align="left">yes</td>
    </tr>
    <tr>
      <td align="left"><code>pos_version</code></td>
      <td align="left"><code>V03</code></td>
      <td align="left">POS version</td>
      <td align="left">no</td>
    </tr>
    <tr>
      <td align="left"><code>sequence_no</code></td>
      <td align="left"><code>2124</code></td>
      <td align="left">Sequence number</td>
      <td align="left">no</td>
    </tr>
    <tr>
      <td align="left"><code>transaction_no</code></td>
      <td align="left"><code>4488</code></td>
      <td align="left">Trasaction Number</td>
      <td align="left">no</td>
    </tr>
    <tr>
      <td align="left"><code>receipt_datetime</code></td>
      <td align="left"><code>01/18/15 15:07:26</code></td>
      <td align="left">Receipt Datetime</td>
      <td align="left">no</td>
    </tr>
    <tr>
      <td align="left"><code>menu_items[]</code></td>
      <td align="left"><code>Adult|1|23.95|M|1001|1|1</code></td>
      <td align="left">Menu Items</td>
      <td align="left">no</td>
    </tr>
    <tr>
      <td align="left"><code>employee_id</code></td>
      <td align="left"><code>135</code></td>
      <td align="left">Employee id for the user</td>
      <td align="left">no</td>
    </tr>
    <tr>
      <td align="left"><code>employee_name</code></td>
      <td align="left"><code>Chelsea</code></td>
      <td align="left">Employee name of the user</td>
      <td align="left">no</td>
    </tr>
    <tr>
      <td align="left"><code>cc_last4</code></td>
      <td align="left"><code>0000</code></td>
      <td align="left">cc last 4 digits of card number</td>
      <td align="left">no</td>
    </tr>
    <tr>
      <td align="left"><code>punchh_key</code></td>
      <td align="left"><code>xxxx</code></td>
      <td align="left">Punchh Key</td>
      <td align="left">no</td>
    </tr>
    <tr>
      <td align="left"><code>pos_type</code></td>
      <td align="left"><code>micros</code></td>
      <td align="left">POS type</td>
      <td align="left">no</td>
    </tr>
    <tr>
      <td align="left"><code>process</code></td>
      <td align="left"><code>true</code></td>
      <td align="left">Process</td>
      <td align="left">no</td>
    </tr>
  </tbody>
</table>