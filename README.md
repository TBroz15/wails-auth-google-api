# wails-auth-google-api
tuxebro's weirdest way of authenticating for wails apps to use google's api

### "Why?"

Google's OAuth needs a Redirect URI with HTTPS and a Top-Level Domain like `.io` and `.com`. But Wails applications runs locally, using `wails.localhost` in HTTP. So this hacky project was made to circumvent that problem. 

<img width="600" alt="image" src="https://github.com/user-attachments/assets/228a9c1a-7e61-43ac-becf-ec8dfb8dbd1b" />

###### todo: explain it better

### "Is `wails-auth-google-api` safe?"

`wails-auth-google-api` itself is safe. Since it is a 100% static HTML page hosted on Github that simply pass the auth code and the `state` parameter to any Wails application. The `state` parameter is required for the application to verify if it's the same person who authenticates from start to finish. (in nerd terms, it prevents CSRF i think.)

### Applications that use this website

none. (yet)
