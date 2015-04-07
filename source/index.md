---
title: API Reference

language_tabs:
  - shell

toc_footers:
  - <a href='https://punchh.com'>Documentation Powered by Punchh Inc.</a>

includes:
  - create_a_checkin
  - fetch_user_balance
  - birthday_reward_with_checkin
  - check_redemptions_possibility
  - create_a_redemption

search: true
---

# Overview

Punchh Server has implemented a new set of APIs which are more streamlined for client access.

Each API is designed to respond with JSON.

Base URI for production: [`https://punchh.com/api/v5`](https://punchh.com/api/v5)
and for integration: [`https://intg.punchh.com/api/v5`](https://intg.punchh.com/api/v5)


Location key token must be provided as credentials in each API call in header like 'Authorization: Token token="xxxxxx"'. If this header is not provided, then we can not determine location of particular request. So, it's mandatory to provide location key token in every API request.

phone or email must be provided as a parameter in each API call. If this parameter is not provided, then we can not determine user. So, for identification of user,  phone or email must be provided.

`curl https://punchh.com/api/v5/RESOURCE -X METHOD -d 'key=value&key1=value1'`

<ul>
  <li>
    <p>
      <strong>CheckinsController</strong> deals with listing checkin balance of a user, creating a checkin
    </p>
    <table>
      <thead>
        <tr>
          <th align="left"></th>
          <th align="left"><strong>Description</strong></th>
          <th align="left"><strong>VERB</strong></th>
          <th align="left"><strong>URL</strong></th>
        </tr>
      </thead>
      <tbody>
        <tr>
          <td align="left">1.</td>
          <td align="left"><a href="#create-a-checkin" class="internal present">Create a checkin from POS</a></td>
          <td align="left"><code>POST</code></td>
          <td align="left"><code>https://punchh.com/api/v5/checkins</code></td>
        </tr>
        <tr>
          <td align="left">2.</td>
          <td align="left"><a href="#fetch-user-balance" class="internal present">Fetch checkin balance information</a></td>
          <td align="left"><code>GET</code></td>
          <td align="left"><code>https://punchh.com/api/v5/checkins/balance</code></td>
        </tr>
      </tbody>
    </table>
  </li>
  <li>
    <p>
      <strong>RedemptionsController</strong> deals with creating a redemption for a user points
    </p>
    <table>
      <thead>
        <tr>
          <th align="left"></th>
          <th align="left"><strong>Description</strong></th>
          <th align="left"><strong>VERB</strong></th>
          <th align="left"><strong>URL</strong></th>
        </tr>
      </thead>
      <tbody>
        <tr>
          <td align="left">3.</td>
          <td align="left"><a href="#create-a-redemptions" class="internal present">Create a Redemptions</a></td>
          <td align="left"><code>POST</code></td>
          <td align="left"><code>https://punchh.com/api/v5/redemptions</code></td>
        </tr>
        <tr>
          <td align="left">4.</td>
          <td align="left"><a href="#check-redemptions-possible-or-not" class="internal present">Check Redemptions possible or not</a></td>
          <td align="left"><code>GET</code></td>
          <td align="left"><code>https://punchh.com/api/v5/redemptions/possible</code></td>
        </tr>
      </tbody>
    </table>
  </li>
  <li>
    <p>
      <strong>RedemptionCodesController</strong> deals with redeem rewards for a user
    </p>
    <table>
      <thead>
        <tr>
          <th align="left"></th>
          <th align="left"><strong>Description</strong></th>
          <th align="left"><strong>VERB</strong></th>
          <th align="left"><strong>URL</strong></th>
        </tr>
      </thead>
      <tbody>
        <tr>
          <td align="left">3.</td>
          <td align="left"><a href="#redeem-rewards-of-the-user" class="internal present"> Redeem rewards of a user</a></td>
          <td align="left"><code>PUT</code></td>
          <td align="left"><code>https://punchh.com/api/v5/redemption_codes/birthday</code></td>
        </tr>
      </tbody>
    </table>
  </li>
</ul>




