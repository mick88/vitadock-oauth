Vitadock OAuth dance Python Client Implementation
=============


```python
import vitadock

c = vitadock.VitadockOauthClient("APP_KEY_GOES_HERE","APP_SECRET_GOES_HERE")

c.getRequestTokens()

print "request token:", c.request_token
print "request token secret:", c.request_token_secret

print "GOTO: " + c.authorization_url + "?oauth_token=" + c.request_token

verifier = raw_input("What is the verifier? (see callback url)")

c.getAccessTokens(verifier)

print "access token:", c.access_token
print "access token secret:", c.access_token_secret
```


Requirements
============

* Python 2.6+
