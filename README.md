# webmon
Simple visitor monitor test: `index.html` sends a push notification to your
phone via [ntfy](https://ntfy.sh) whenever someone opens the page.

## Usage

1. Install the ntfy app (Android / iOS) and subscribe to a topic, e.g. `webmon-ictsmart-test`.
   Use a hard-to-guess name: anyone who knows a topic on ntfy.sh can read it.
2. Set `DEFAULT_TOPIC` in `index.html` to that topic (or open the page with `?topic=your-topic`).
3. Host the page (GitHub Pages, any web server) or open it locally, e.g. `python3 -m http.server`.
4. Open the page — your phone gets a "Webmon: new visitor" notification with page, referrer,
   IP, language, timezone, screen size and user agent. Use the button to send a manual test.

Auto-notify fires immediately on every visit (including refreshes). A self-hosted ntfy
server can be used with `?server=https://ntfy.example.com`.
