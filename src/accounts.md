# Manage your account

### Obtaining the Auth Token
sTeX's auth mechanism relies on the so called `sauth` or `stellar_auth`, which simply is the result of an encryption between a private user key and a temporary signature. It is called stellar auth because once the app verifies the validity of a `sauth`, it returns the stellar secret key of the user's account (remember sTeX is a centralised and custodial service).

To obtain this token, you'll currently have to make a request as follows:

```
POST /signin

{
	"email": YOUR_EMAIL,
	"password": YOUR_PASSWORD
}
```

We understand this isn't a best practice for an API, thus are considering the idea of allowing to create API auth tokens.

