# Play Console — copy & paste reference

Quick answers when filling Play Console forms for **Neon Keyboard Themes** (`dev.neonkeyboard.app`).

## Privacy policy URL

```
https://neonkeyboard.app/legal/privacy
```

Until custom domain is live, use your GitHub Pages URL and update `LegalUrls.kt` + this form.

## App category

- **Category:** Personalization (or Tools)
- **Tags:** keyboard, themes, customization

## Data safety — summary

| Question | Answer |
|----------|--------|
| Collect or share user data? | **No** (MVP — no analytics SDK) |
| Data encrypted in transit? | **Yes** (HTTPS for billing/legal only) |
| Users can request deletion? | N/A — no account, no server data |

**Not collected:** name, email, location, contacts, messages/SMS, **keyboard typed text**, photos uploaded to server, device IDs for tracking.

**On-device only:** theme preferences (DataStore), DIY photos (app private storage), clipboard paste locally in IME.

**Permissions:** `INTERNET` (app — billing, legal links), `RECORD_AUDIO` (optional voice dictation, on-device), `BIND_INPUT_METHOD`.

Full detail: [`DATA_SAFETY.md`](DATA_SAFETY.md) · **All forms (filled):** [`PLAY_FORMS_FILLED.md`](PLAY_FORMS_FILLED.md)

## IME / custom keyboard declaration

| Item | Answer |
|------|--------|
| Custom keyboard? | **Yes** |
| Collects typed text? | **No** |
| Sends keystrokes to server? | **No** |
| Clipboard | Local paste only — not uploaded |
| Network from IME | No upload of user input |

Full detail: [`IME_DECLARATION.md`](IME_DECLARATION.md)

## Subscriptions

| Paywall plan | Product ID |
|--------------|------------|
| Year | `neon_vip_yearly` |
| Month | `neon_vip_monthly` |
| Week | `neon_vip_weekly` |

Add license testers before test purchase. See [`PLAY_BILLING_SETUP.md`](../product/PLAY_BILLING_SETUP.md).

## Release notes (versionCode 2)

Copy from upload package:

- `WHATS_NEW_en-US.txt`
- `WHATS_NEW_ru-RU.txt`

Or from `fastlane/metadata/android/*/changelogs/2.txt`.

## Content rating

- User-generated content shared publicly: **No**
- Violence, sexual content, etc.: standard keyboard app — **None**

## Contact

```
support@neonkeyboard.app
```

(In-app Feedback uses same intent.)

## Internal testing release checklist

1. `./scripts/pre_upload_gate.sh`
2. Upload AAB from `dist/play-upload/neon-keyboard-themes-{version}-{code}/`
3. Paste WHATS_NEW files per locale
4. Complete Data safety + IME + subscriptions
5. Add testers → Start rollout

See [`PLAY_CONSOLE_FIRST_UPLOAD.md`](PLAY_CONSOLE_FIRST_UPLOAD.md)
