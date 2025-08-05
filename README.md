# youtube_playlist_manager

## i have a wildly first-world issue
youtube's native playlist editing, while serviceable, has no real batching capacibility and is overall clunky past adding and removing videos here and there. this is fine until you have a profile like mine that's been around for a few years, and presents the second major issue: youtube at some arbitrary amount of playlists stops displaying the full list, making them essentially inaccessible on mobile/desktop unless you begin deleting them. the obsessive organizers among us with years-old profiles and channels  (that hopefully isn't only me) will likely have ran into this issue already.

## there's an app for everything
and i don't plan to buck that trend today. plus this gives me an excuse to mess around with Rust+Tauri more and have my first big boy application under my belt. 

## planned tech stack
- Rust
- Tauri (backend / filesystem things)
- Astro (for the frontend)

## planned features
- batch listing, editing, and deletion ability of user channel playlists
  - choice of in-place playlist editing

## about the client-secrets file
given [google's documentation on desktop/mobile applications](https://developers.google.com/identity/protocols/oauth2#installed) and various other netsphere places i've scoured, their recommendation seems to be to treat these "secrets" as non-secret entirely, which would make some sense given the seeming difficulty of trying to keep a zero-sum of secrets out of desktop/mobile code (trying to figure out the "give a secret to keep your secrets secure" of other secrets management engines has been driving me insane the last few months). 

this in particular illustrates: 
> The process results in a client ID and, in some cases, a client secret, which you embed in the source code of your application. (In this context, the client secret is obviously not treated as a secret.)

it still feels **wrong** to be committing anything *.secret files to version control, but until I see anything different i'll roll with this for now.



