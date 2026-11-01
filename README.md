# Still

## GitHub Pages

The app is ready to deploy at https://yarrabothusuresh.github.io/playvideo/ after publishing is enabled and the workflow succeeds. It is not deployed merely by adding this configuration.

1. Upload this project to the `main` branch of `yarrabothusuresh/playvideo`, including `.github/workflows/pages.yml`.
2. In repository Settings → Pages → Build and deployment, choose **GitHub Actions** as the source.
3. Run **Deploy Still to GitHub Pages** from the Actions tab, or push a change to `main`.

The workflow publishes only `index.html`, `style.css`, and `app.js`. No Node server runs on GitHub Pages. Relative asset paths support the `/playvideo/` project URL. HTTPS video URLs are recommended on the hosted site; browsers may block insecure HTTP media. Playlists remain browser-local and do not transfer from localhost to the hosted site.

## Run locally

Double-click `Start Still.cmd` to run the local server and open the app. Node.js must be installed. YouTube links require this server launch; direct videos and local files also work by opening `index.html`.

- Paste a direct HTTP(S) video URL, then Load video. It is added to the playlist automatically.
- Open local video files (multiple selection supported).
- Use the native player for play/pause, seeking, volume, and fullscreen.
- Set speed, fit, loop, and autoplay next. Delete playlist entries with ×.
- URL playlists and settings are saved in this browser. Local files are session-only and must be selected again after reopening.

The app adds no advertising or analytics. YouTube links load the official external YouTube player, which may show ads. Video hosts still receive requests to their URLs. It does not remove ads embedded in media, bypass DRM, or extract videos from website pages. YouTube watch, share, shorts, live, and embed URLs are supported through an iframe. Use the YouTube player controls for speed and quality; Still settings are disabled for YouTube. Formats depend on browser codecs; MP4 with H.264/AAC and WebM are typical choices. Buffering uses the browser's native preload behavior; complete offline caching is not promised. Private or expiring URLs may stop working.

Optional local server: run `node server.js`, then open http://127.0.0.1:4173. The server binds only to your computer.

"# playvideo" 
