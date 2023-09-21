
{% info title="Account vs Users API" %}
Appwrite provides two APIs to manager user accounts. 

The Account API is the API you should use in your **client applications** like web, Flutter, mobile, and native apps.
Account API creates sessions, which represent an authenticated user and is attached to a user's [account](/docs/products/auth/account).
Sessions respect [permissions](/docs/advanced/platform/permissions), which means users can only access resources if they have been granted the correct permissions. 

You'll notice that the Account API doesn't allow you to view or make changes to other users. 
This is by design and for **security reasons**.

[Account API references](/docs/references/cloud/client-web/account)

The Users API is a dedicated API for managing users from an admin's perspective. **Do not use the Users API on client applications**.
It should be used with backend or server-side applications with the [Server SDK](#).

Users API uses API keys instead of sessions. 
This means they're not resticted by permissions, but by the scopes granted to the API key used.

[Users API references](/docs/references/cloud/server-nodejs/users)
{% /info %}