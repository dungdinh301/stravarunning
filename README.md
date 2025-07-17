# Strava OAuth Helper

This is a small helper page to get a Strava authorization code for use in your Python script.

## 🚀 How to use

✅ Visit: [https://dungdinh301.github.io/stravarunning/](https://dungdinh301.github.io/stravarunning/)

✅ Click **Authorize Strava 🚴**

✅ Log in & approve

✅ After redirect, copy the **code** displayed on the page.

✅ Use that code in your Python script to exchange for an access token.

## 🐍 Python snippet

```python
import requests

client_id = '168168'
client_secret = 'YOUR_CLIENT_SECRET'
code = 'PASTE_YOUR_CODE_HERE'

resp = requests.post(
    'https://www.strava.com/oauth/token',
    data={
        'client_id': client_id,
        'client_secret': client_secret,
        'code': code,
        'grant_type': 'authorization_code'
    }
)

print(resp.json())
