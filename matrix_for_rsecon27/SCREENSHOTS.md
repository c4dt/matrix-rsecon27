# Screenshots to take

Put each file into `screenshots/` with exactly the name below. Until a file exists,
the deck shows an orange placeholder box with the filename, so you can always see
what's still missing (`devbox run serve27` → http://localhost:8001).

**Before you start**

- Use a **throwaway matrix.org account** (and ideally a throwaway GitHub account).
  Some screenshots show a recovery key and the account name, so don't use your real ones.
- If you only have your real GitHub account, blur the username and avatar on 02-2.
- *wide* = browser/desktop, ~1600×900, cropped to the relevant window.
  *phone* = portrait phone screenshot (iOS or Android, but use the same one throughout).
- Check the button labels in the captions in `index.html` while you go. They were
  written from Element's current flows and may differ slightly.

The order below follows the deck. The fastest way through is:
**A** (browser, new account) → **B** (phone, sign in = second device) → **C** (both).
Note that **B** gives you the "verify new device" screens (07-x) as well, because the phone is
the *second* device in that run. Take the phone versions of 03a-5/03a-6 (setting up recovery)
with a *second* throwaway account that signs in on the phone first, or skip them
and reuse the web ones.

## A — Browser, fresh account (wide)

| File | What to capture |
|---|---|
| `02-1-register-choices.png` | account.matrix.org/register with "Continue with GitHub" visible |
| `02-2-github-authorize.png` | GitHub "Authorize …" screen |
| `02-3-choose-username.png` | matrix.org asks for the Matrix username after GitHub |
| `02-4-account-done.png` | Confirmation / account page after creation |
| `02-5-register-password.png` | The classic username + password + e-mail form (don't submit) |
| `03b-1-welcome.png` | app.element.io welcome page with "Sign in" |
| `03b-2-github-login.png` | matrix.org login page reached from Element, "Continue with GitHub" |
| `03b-3-notifications.png` | "Enable desktop notifications" banner/prompt |
| `03b-4-recovery-setup.png` | "Set up recovery" prompt |
| `03b-5-recovery-key.png` | Recovery key shown with Copy / Download |
| `03b-6-home.png` | Element Web home, empty, after login |
| `04-4-matrixto-desktop.png` | matrix.to/#/#rsecon27:epfl.ch in the browser, client chooser |
| `04-5-space-desktop.png` | RSECon27 space home in Element Web with room list + Join buttons |
| `05-2-profile-desktop.png` | Settings → Account: display name + avatar |
| `05-3-add-email.png` | Adding an e-mail address (Element settings or account.matrix.org) |

## B — Phone, Element X (phone)

| File | What to capture |
|---|---|
| `03a-1-welcome.png` | Element X start screen |
| `03a-2-server.png` | Server selection showing matrix.org + Continue |
| `03a-3-github-login.png` | matrix.org login page in Element X with "Continue with GitHub" |
| `03a-4-notifications.png` | Notification permission prompt |
| `03a-5-recovery-setup.png` | "Set up recovery" (first-device run only, see above) |
| `03a-6-recovery-key.png` | Recovery key shown (first-device run only) |
| `03a-7-home.png` | Empty chat list |
| `04-1-matrixto-mobile.png` | matrix.to link opened from the QR code, choosing Element X |
| `04-2-space-join-mobile.png` | Space preview with "Join" |
| `04-3-space-rooms-mobile.png` | Room list inside the RSECon27 space |
| `05-1-profile-mobile.png` | Element X profile editing (name, photo) |

## C — Verification and chatting (both devices)

| File | Device | What to capture |
|---|---|---|
| `07-1-confirm-identity.png` | wide | New session asks "Confirm your identity" (use another device / recovery key) |
| `07-2-qr-shown.png` | wide | Computer showing the verification QR code |
| `07-3-qr-scan.png` | phone | Phone scanning / confirming the verification |
| `07-4-recovery-key-entry.png` | wide | Entering the recovery key |
| `07-5-verified.png` | wide | "Device verified" confirmation |
| `06-1-message.png` | wide | Writing "Hello 👋" in a room of the space |
| `06-2-thread.png` | wide | Thread panel open with a reply |
| `06-3-thread-mobile.png` | phone | Long-press menu on a message (Reply / React) |
| `06-4-react-mention.png` | wide | Message with an emoji reaction + autocomplete for an @mention |
| `06-5-dm.png` | wide | User info panel with "Send message" |

**Total: 36 screenshots** (25 wide, 11 phone).

## QR codes (already done)

QR codes are drawn in the browser by `lib/qrcode-generator/qrcode.js` (v2.0.4, MIT).
Each one is a link in `index.html`, so the URL you see in the `href` is exactly the URL
encoded in the QR code. You can also click it to test it:

```html
<a class="qr" data-show-url href="https://matrix.to/#/#rsecon27:epfl.ch" ...></a>
```

`data-show-url` additionally prints the URL below the code. To change a target, edit the `href`.

## Still to fill in on the slides

- Section 8, "Etiquette": link to the code of conduct, and a contact person or help room (marked `TODO`).
