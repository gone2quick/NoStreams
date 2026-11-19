# PCStream Android app

A tiny Android app that opens your PCStream server (`https://server.tail1be5a7.ts.net`) full screen,
so you don't need a browser. It is just the system WebView pointed at the server: watching, chat,
login, fullscreen video and MP4 downloads all work. The server address is in
`app/src/main/res/values/strings.xml` (`server_url`).

## Build it with GitHub Actions

1. Create a new GitHub repo and push the contents of this folder to it (the `.github` folder must be at the repo root).
2. Open the repo's **Actions** tab. The **Build APK** workflow runs on every push to `main`/`master`,
   or press **Run workflow** to start it by hand.
3. When it's green, open the run and download the **PCStream-apk** artifact (a zip containing `app-debug.apk`).
4. Copy the APK to your phone and open it. Android will ask you to allow installs from this source.

Optional: push a tag (`git tag v1 && git push origin v1`) and the APK is also attached to a GitHub Release,
which gives you a direct download link you can open on the phone.

## Notes

- Needs Android 10 or newer.
- Each build is signed with a fresh debug key, so to install a newer APK over an older one you have to
  uninstall the old one first. You rarely need to: the app loads your site live, so site changes show up without a new APK.
