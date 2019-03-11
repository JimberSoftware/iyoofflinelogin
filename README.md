# iyoofflinelogin
Direct login (without oAuth) for Itsyou.online

Using these PHP scripts users can login without oAuth to itsyouonline. Beware that oAuth is always preferred, this can be used for non web applications.

# Usage

## Initiate
```
php get2fa.php {username} {pw} #returns 2fa methods + cookie

```

## SMS 
```
php login_sms_initiate.php {cookie} #code is sent to mobile
php login_sms_sendcode.php {code} #returns new cookie
php login_sms_polling.php {cookie} #polls until user is logged in (returncode 0) or fails (returncode 1)
```

## TOTP

```
php login_totp.php {cookie} {TOTP code}
```

