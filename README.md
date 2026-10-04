# Track Body support website

Static English support and privacy pages. No build step, scripts, analytics, external fonts or dependencies.

Public contact: support@rblch.com

## Preview

Run `python3 -m http.server 8765` from this folder, then visit http://localhost:8765/.

## Deployment

Use GitHub Pages: Settings → Pages → Deploy from a branch → main → /(root).

Once the custom domain is verified in the GitHub account, set the Pages custom domain to `trackbody.rblch.com` and add the Squarespace DNS record:

| Type | Host | Target |
| --- | --- | --- |
| CNAME | trackbody | rblch.github.io |

Enable HTTPS after GitHub provisions its certificate. Test `/support/` and `/privacy/` anonymously before putting URLs in App Store Connect.

## Before release

- Verify the support address receives mail and can send replies as intended.
- Finalize the developer’s public postal contact details and any required legal notice. App Store Connect acceptance of a PO box does not establish compliance with German website legal-notice requirements.
- Confirm the provider used for support email and decide on a retention period for support messages.
- Review the privacy policy against the actual submitted build, including whether the Watch companion is shipped.
- Replace the privacy draft notice with an effective date and remove the `noindex` metadata once the policy is final.
- Add an easily accessible privacy-policy link inside the app. This website alone does not complete that Apple requirement.
- Complete App Store Connect’s App Privacy questionnaire separately.

Code audit: 4 October 2026. Source inspected: ModelContainerManager, HealthKitManager, TrendsView, SettingsView, CheckInDeletion, HistoryView, ReminderManager, PhoneWatchSync, WatchCheckInStore and WatchTransport.

No app source code, personal measurements or private account identifiers belong in this repository.
