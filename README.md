## The Security Checklist

##### Server Security + Improvements
- [ ] Use HTTPS everywhere.
- [ ] Patch LOGJAM Vulnerability.
- [ ] Destroy the session identifier after `logout`.  
- [ ] Destroy all active sessions on reset password (or offer to).  
- [ ] Must have the `state` parameter in OAuth2.
- [ ] No open redirects after successful login or in any other intermediate redirects.
- [ ] When parsing Signup/Login input, sanitize for javascript://, data://, CRLF characters.
- [ ] Set secure, httpOnly cookies.
- [ ] In Mobile `OTP` based mobile verification, do not send the OTP back in the response when `generate OTP` or `Resend OTP`  API is called.
- [ ] Limit attempts to `Login`, `Verify OTP`, `Resend OTP` and `generate OTP` APIs for a particular user. Have an exponential backoff set or/and something like a captcha based challenge.
- [ ] Check for randomness of reset password token in the emailed link or SMS.
- [ ] Set an expiration on the reset password token for a reasonable period.
- [ ] Expire the reset token after it has been successfully used.
