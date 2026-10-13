# Mattress site

The public pages for the Mattress app, served by GitHub Pages at https://getmattress.app/ (set in `CNAME`).
The old `pedrojfs17.github.io/money-manager-app/` URLs forward there. This repository is renamed to
`mattress-site` on move day.

- `index.html`: the landing page.
- `privacy.html`: the privacy policy, also linked from the Google OAuth consent screen.
- `bank-redirect/`: the Enable Banking redirect URL.
- `banks/`: bank logos shown on the landing page, from Wikimedia Commons and Simple Icons. Each
  logo belongs to its bank.

## Bank redirect

After a bank login, Enable Banking sends the browser to `bank-redirect/`. The page forwards only `code`, `state`,
`error` and `error_description` to the app (`mattress://bank/callback`) and sends nothing anywhere else. The code
is useless without the private key that stays on the person's phone.

Register this URL in your Enable Banking application:

https://getmattress.app/bank-redirect/
