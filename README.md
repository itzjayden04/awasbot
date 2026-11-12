# AWASBOT

**Scam stops here.** AWASBOT checks any suspicious message, link or screenshot, explains in plain English why it is (or isn't) a scam, scores whole conversations for romance and investment scam patterns, and prepares a redacted report you can send to the right place in one tap.

Built for HackAI 2026, Track 3: Scam Defence & Awareness.

> [!NOTE]
> This public repository holds the AWASBOT app downloads, release notes and user guides. The source code is private. See [LICENSE](LICENSE).

## Before you install

**Requirements**

| | |
| --- | --- |
| Phone | Android 7.0 or newer (Android 10+ recommended; call screening needs Android 10+) |
| Tested on | Honor (Android, MagicOS) |
| Internet | Optional. Built-in checks work offline; AI, web search and Trace lookups need data or Wi-Fi |
| Account or API key | None |

> [!IMPORTANT]
> **Disclaimer: Android only, installed outside the Play Store.**
> - AWASBOT is a hackathon prototype distributed as an APK file. It does not run on iPhone, iPad, Windows or Mac.
> - Install it with your phone brand's own installer or app store, for example **Xiaomi / Redmi / POCO, vivo / iQOO, Honor, OPPO / realme / OnePlus** (Honor users can also get it through the Honor App Market). These installers let you open the APK directly.
> - Phones that rely only on **Google's package installer with Google Play Protect** (such as Google Pixel, and some Samsung and Android One phones) may warn about or block an app that asks for Accessibility and notification access when it is not from the Play Store. On those phones installation may not be possible.
> - After installing, Android treats AWASBOT as a "restricted" app. You must **allow restricted settings** before you can turn on Accessibility and notification access (steps below).
> - AWASBOT reads your notifications and the screen you have open **only to detect scams**. Messages are checked on the phone. When AI or web search is used, names, phone numbers, IC numbers and account numbers are masked first. Nothing is uploaded without a cloud icon showing it in the activity log.
> - AWASBOT's verdicts are an aid, not a guarantee. It can miss a scam or flag a genuine message. If money is at stake, call the person or company on a number you already know, and call **NSRC 997** if you have already paid.

## Download

AWASBOT is a single file, `AWASBOT-android.apk`. AI is built in, so there is nothing else to install.

**Direct download link (open it on the phone):**
**https://github.com/itzjayden04/awasbot/releases/latest/download/AWASBOT-android.apk**

Or from the release page, step by step:

1. On the Android phone, open Chrome (or your phone's browser) and go to **https://github.com/itzjayden04/awasbot/releases/latest**.
2. Scroll down to **Assets** (tap **Assets** to expand it if the list is closed).
3. Tap **AWASBOT-android.apk**. Do not tap "Source code (zip)" or "Source code (tar.gz)"; those are not the app.
4. If the browser warns "This type of file can harm your device", tap **Download anyway**.
5. When the download finishes, tap **Open** in the notification, or open **Files / File Manager > Downloads > AWASBOT-android.apk**. Then follow the install steps below.

## Install on Android

No Android phone? See [Run AWASBOT on a Windows PC](docs/run-on-windows-emulator.md) (Android Emulator, or mirror a phone with scrcpy).


1. **Download** `AWASBOT-android.apk` on the phone and open it from the notification or the Files / File Manager app.
2. **Allow unknown apps.** If asked, allow your browser or file manager to "Install unknown apps", then tap **Install**. (If a security scan appears, tap **Install anyway** / **Continue installation**.)
3. **Allow restricted settings.** Android blocks Accessibility and notification access for apps installed this way until you allow it:
   - Open **Settings > Apps** (called **Manage apps** or **App management** on Xiaomi, OPPO, vivo and Honor) **> AWASBOT**.
   - Tap the **three dots (⋮)** at the top right and choose **Allow restricted settings**, then confirm with your PIN or fingerprint.
   - If you don't see the three dots yet, first try turning on AWASBOT under Accessibility once (it will say "Restricted setting"), then come back here.
   - AWASBOT's setup has an **Allow restricted settings** button that opens this page for you.
4. **Open AWASBOT and follow setup.** It walks you through each permission in order. Tap **Allow** on each card and follow Android's screens:
   - **Notifications**: so AWASBOT can warn you.
   - **Notification access**: reads new WhatsApp, Telegram, SMS and email messages.
   - **Display over other apps**: shows the pause card, call warning and blocked-site screen.
   - **Accessibility** (Installed / Downloaded apps > AWASBOT > On): reads the open chat or website so AWASBOT can warn you and close scam pages.
   - **Caller ID & spam app**: lets AWASBOT warn about risky callers.
   - **Photos**: checks QR codes in new screenshots.
   - **Battery**: choose **Don't optimise** / **Unrestricted**.
5. **Keep AWASBOT running (Xiaomi, OPPO, vivo, Honor, Huawei).** These phones close background apps aggressively. Also:
   - Turn on **Autostart** for AWASBOT (Settings > Apps > AWASBOT > Autostart, or in the Security / Phone Manager app).
   - Set battery to **No restrictions** / **Allow background activity**.
   - Lock AWASBOT in the recent-apps screen (swipe down on its card or tap the lock icon).
6. **Check it works.** The top bar shows a green **Protected** pill. Tap it to open the Protection centre and preview each warning.

If something stops working after an update or restart, open AWASBOT once: the pill turns amber and shows which permission needs turning back on.

## New in v1.4.0

- **Kantoi is now AWASBOT.** New name and tagline, "Scam stops here.", across the app, notifications, reports and emails. Your account, history and safe words carry over: v1.4.0 installs as an update over Kantoi.

## New in v1.3.0

- **Online accounts (Firebase).** Accounts made with Google or email now live in Firebase, so they work on any phone. Log in with your username or email; "Forgot password" emails a reset link. Builds without the Firebase settings keep accounts on the phone as before.
- **Shared scam database goes live.** Submitted reports and high-confidence scams are sent to Firestore as masked details only (scam type, signs, website names, one-way codes for numbers). The same scam checked twice is shared once, and "This was actually legit" takes back one that hasn't been sent yet.
- **Delete my data deletes the online account too,** along with the reports you shared.
- **New look.** Cleaner sections, blue headers on Trace and Emergency, a floating tab bar and tick shields.
- **Clearer Google sign-in errors** when Google sign-in isn't set up or Google rejects the app.

## New in v1.2.0

- **Account.** Every user signs up once, with Google or with an email code plus a username and password. Sign-up has an unticked Privacy Notice box (PDPA 2010). Email accounts are logged out after 7 days without use; Google accounts stay signed in.
- **Five tabs:** Check, Trace, **Report**, Learn, Emergency.
- **Report tab.** Pick one of 20 scam types in 5 groups, then four short steps: who contacted you, what happened, money lost (amount, currency, payment method, transaction ID) and evidence. AWASBOT fills in what it already knows from your last check. The finished report can go to the AWASBOT scam database (masked) and opens the police, bank and MCMC form packs and the police PDF. Emergency's "Prepare my report" lands here.
- **Scam Monitor** (in Check). Pick which of 42 messaging, social, email and shopping apps AWASBOT watches, see what each one caught over 7 days, hide scam notifications automatically, and open any alert in Trace or Report.
- **Safe word vault** (in Emergency and Settings). Save a family safe word for each person. Words are encrypted on the phone, unlocked by fingerprint or screen lock, never backed up and never sent anywhere. When a message or call claims to be someone you know, AWASBOT tells you to ask for the safe word.
- **Sharing to help others.** High-confidence scams and submitted reports are queued as masked details only (scam type, signs, website names, one-way codes for numbers). It is on by default and can be switched off in Settings. The online database comes in the next version.
- **History and your data** in Settings: every check, trace, quiz and report, searchable, plus "Download my data".
- **Sharper checks.** The AI names the scam type from the same 20 types; a website that is unranked, not official and young or of unknown age is marked "Unfamiliar website"; a second Gemini key takes over when the first hits its quota.

## What it does

AWASBOT follows the eight branches of the product blueprint.

1. **Bring anything in.** Paste a message, link or email (headers included), or add a screenshot, QR code, PDF, Word file, voice note, short video or Android app file. On Android, share straight from WhatsApp or scan a QR with the camera. While AWASBOT checks, a live view shows each stage (read, protect your details, scam signs, links, AI, verdict) and marks what stayed on the phone.
   - **Auto-protection** (one switch per guard in the Protection centre, running in the background):
     - **Messages:** new WhatsApp, Telegram, SMS and email notifications are checked as they arrive.
     - **Chats on screen:** a small risk badge floats over the open WhatsApp, Telegram or Messenger chat and scores the person you are talking to.
     - **WhatsApp Web on the phone:** WhatsApp Web opened in Chrome gets the same badge and pause card. AWASBOT checks the open chat as soon as the page opens and warns about a new scam message within about two seconds.
     - **Websites:** a scam page opened in Chrome, Samsung Internet, Firefox, Edge and other browsers is closed, with a "AWASBOT closed this page" screen.
     - **Calls:** risky callers get an "Answer carefully" warning and blocked numbers are rejected. AWASBOT never listens to calls.
     - **New apps and pictures:** newly installed apps and QR codes in new photos or screenshots are checked.
     - **Before you pay:** opening a banking or e-wallet app soon after a risky chat shows a pause card first.
     - Every warning is a notification; tapping it opens the Trace.
2. **Investigate it.**
   - **Words:** pressure words are highlighted, including Malay, Manglish, Chinese and Tamil. AWASBOT also catches disguised spelling and says which step of a known scam script the message has reached.
   - **Links:** every redirect is followed in a locked-down way, and each hop shows its domain age, certificate, hosting country, brand look-alike checks and the login form on the page. AWASBOT also checks whether the page shows phone visitors something different, and looks the link up in safety lists. With a VirusTotal key, the link and its website are checked against 70+ security companies, and a link VirusTotal has never seen gets a fresh scan. Links that point into your own home or phone network are never opened.
   - **Files and apps:** risky app permissions, macros and links inside documents, and forged letterheads are flagged.
   - **Genuine messages:** an official-sender list and known-good templates let a real message come out as "Looks legitimate".
3. **Relationship check.** It runs by itself when you open a chat (see the chat badge above). You can also score a WhatsApp or Telegram chat export, or answer 9 questions instead. The score looks at how you met, how fast money came up, texting rhythm, story contradictions and copy-paste replies. It also spots a hijacked friend's account, and shows a risk timeline with the key messages highlighted.
4. **Who's behind it.** The Trace tab starts a live investigation from any link, number, account, email or whole message. The map grows as each real lookup returns: redirects, domain registration, DNS, hosting company and country, certificates and certificate logs, look-alike brands and links to earlier cases. Every lookup appears in a timestamped log, and the findings export as a police PDF. AWASBOT also keeps a scam map on your device. It draws on certificate logs, public phishing feeds, domain records, news and approved reports. Shared nameservers, accounts, numbers and message scripts link items into campaigns, which you can explore as a network. Tracing a number or account also searches the web for public scam reports and links to Semak Mule. Campaigns are named; people never are.
5. **Explain it.** You get the answer, the reasons highlighted in the message and the full evidence, with an honest confidence level and what would change the verdict. Buttons say "This was actually legit" or "This was actually a scam", and an "Honest limits" page shows measured accuracy.
6. **Act on it.**
   - **Emergency tab:** a "Call 997" button, the call script, a "what to do right now" checklist that remembers what you have done, and verified bank fraud hotlines.
   - **Report packs:** a pack for each channel, with copy buttons in form order, covering NSRC, bank, PDRM, Semak Mule, MCMC, WhatsApp, Telegram, Facebook, Instagram and TikTok.
   - **Police PDF:** a PDF for the police station with your evidence screenshots.
   - **Your control:** personal details are masked, and nothing is sent until you approve.
7. **Learn from it.**
   - "How this scam works" cards.
   - Practice drills that bring back the signs you missed.
   - A family guardian alert that never includes the message.
   - Shareable warning pictures.
   - A safety check-up.
8. **Privacy you can see.**
   - **Activity log:** a lock icon marks steps that stayed on the device; a cloud icon marks steps that went online.
   - **Files:** only a file's fingerprint is ever checked online.
   - **Links:** an unknown link may be sent to VirusTotal for a fresh scan (VirusTotal shares scans with its paying users), so phone, IC, card and account numbers and emails in the link are removed first.
   - **Retention:** data is kept for 7 or 30 days, and one button deletes everything.
   - **AI safety:** prompt-injection attempts are flagged as a scam sign.

## Honest limits

AWASBOT's built-in checks were measured with the network and AI switched off, on synthetic Malaysian messages written for this project (no real personal data):

- **Held-out set (32 messages: 18 scam, 14 genuine, never used for tuning):** 100% precision (0 genuine messages flagged) and 66.7% recall (12 of 18 scams caught) at the "Suspicious" threshold.
- **Tuning set (90 messages):** 100% precision and 96% recall. This is optimistic, because the rules were tuned on it.

On WhatsApp Web, the page does not say who sent a message, so warnings name the chat "WhatsApp Web" rather than the contact.

AWASBOT's verdicts are an aid, not a guarantee.

## Licence

Copyright (c) 2026 Team Five Guys. All rights reserved. You may install the official APK on your own devices for personal, non-commercial use. Copying, modifying, redistributing or reverse engineering AWASBOT is not allowed without written permission. See [LICENSE](LICENSE) for the full terms.
