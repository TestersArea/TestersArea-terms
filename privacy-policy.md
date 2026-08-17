# Privacy Policy for Testers Area

**Last Updated:** August 17, 2025  
**App Name:** Testers Area  
**Developer:** Testers Area Team  
**Contact Email:** testersareaofficial@gmail.com

---

Welcome to **Testers Area** ("we", "our", "us"). This Privacy Policy explains how we collect, use, disclose, and safeguard your information when you use our mobile application ("App"). Please read this privacy policy carefully. By using the App, you agree to the collection and use of information in accordance with this policy.

If you do not agree with the terms of this privacy policy, please do not access or use the application.

---

## 1. Information We Collect

### 1.1 Account Information
- **Email Address:** Collected during registration (via Google Sign-In) to create and manage your account.
- **Display Name:** Your name as set in your Google account or chosen during signup, used for display within the App.
- **Profile Photo URL:** Your Google profile picture URL, used for display within the App.

### 1.2 Device Information
- **Android Device ID (Android ID):** We collect your unique Android Device ID to enforce our one-account-per-device policy and to prevent fraudulent multi-account abuse. This ID is stored securely and is **never shared** with other users or third parties.
- **Device Model, Manufacturer & Android Version:** Collected to display device information on your profile and to help with troubleshooting compatibility issues.

### 1.3 App Usage Data
- **Usage Statistics (PACKAGE_USAGE_STATS Permission):** To verify that you have actively tested a partner's app for the required minimum duration each day, our system reads your device's app usage statistics for the specific partner app only. This permission is requested explicitly with a prominent disclosure dialog explaining the purpose. This data is:
  - Used **only** for fairness verification of your testing activity.
  - Shared **only** with your assigned testing partner (as daily usage time in seconds).
  - **Not** used for advertising, profiling, or any other purpose.

### 1.4 Installed Apps Information
- **App Installation Check:** We check whether the partner's app is currently installed on your device to detect uninstallation fraud during the active 14-day testing period. We do **not** scan, list, or collect your full list of installed apps. We only query the installation status of the specific app you are assigned to test.

### 1.5 Media & Screenshots
- **Screenshots (READ_MEDIA_IMAGES / READ_EXTERNAL_STORAGE Permission):** You are required to select and upload screenshots from your device as proof of daily testing. These images are:
  - Compressed to WebP format on your device before upload to minimize data usage and storage.
  - Stored securely on our servers (Supabase Storage with Row Level Security).
  - Shared **only** with the app owner you are testing for, strictly for verification purposes.
  - **Automatically deleted** from our servers after the testing period is completed and verified.
- **Screenshot Metadata (EXIF):** We read the capture timestamp from your screenshot files (using EXIF data and filename patterns) to verify that the screenshot was genuinely taken during the testing period. We do **not** read or store GPS location data, camera model, or any other EXIF metadata beyond the capture timestamp.

### 1.6 Push Notification Data
- **Firebase Cloud Messaging (FCM) Token:** We collect your FCM device token to send you push notifications about testing requests, approvals, rejections, daily reminders, and other app-related updates. This token is stored in our database and is deleted when you delete your account.
- **Local Notifications (SCHEDULE_EXACT_ALARM / POST_NOTIFICATIONS Permission):** We schedule local alarm-based reminders for your daily testing tasks. These reminders are set and managed entirely on your device.

### 1.7 Chat Messages
- **In-App Chat:** Messages you send to your testing partner through our in-app chat feature are stored on our servers. Chat messages are visible only to you and your testing partner and are deleted when the testing request is completed or when either party deletes their account.

### 1.8 Locally Stored Data (On-Device Only)
The following data is stored **only on your device** using SharedPreferences and is **never sent to our servers:**
- Your selected app theme (Light/Dark mode preference).
- Your selected language preference.
- Your active app selection.
- Cached reputation score and golden points (for faster loading).
- Daily testing reminder times.
- Fraud detection flags (local backup).

### 1.9 Network Time Verification
- **NTP (Network Time Protocol):** We connect to public NTP servers to verify the current time independently of your device clock. This is used to prevent timestamp manipulation fraud. No personal data is sent during this process.

---

## 2. How We Use Your Information

| Purpose | Data Used |
|---|---|
| Account creation and authentication | Email, Name, Profile Photo |
| Testing matchmaking (pairing developers) | Email, App details |
| Fairness verification of daily testing | Usage Statistics, Screenshots, Screenshot Timestamps |
| Fraud prevention and detection | Device ID, Installed App Status, NTP Time, Screenshot EXIF |
| Push notifications and reminders | FCM Token, Notification Permission |
| Communication between testing partners | Chat Messages |
| Reputation and rewards system | Testing completion data, Violation records |
| Bug reports and feedback (voluntary) | User-submitted text and optional screenshot |
| App improvement and troubleshooting | Device Model, Android Version |

---

## 3. Information Sharing & Disclosure

We respect your privacy and **do not sell, rent, or trade** your personal data to any third parties.

### 3.1 Shared with Testing Partners
The following data is visible **only** to your assigned testing partner, **only** during the active testing period:
- Your display name and profile photo.
- Your uploaded testing screenshots (as proof).
- Your daily app usage time (in seconds) for their specific app.

### 3.2 Third-Party Service Providers
We use the following third-party services to operate the App. Each service processes data in accordance with their own privacy policies:

| Service | Data Processed | Purpose | Privacy Policy |
|---|---|---|---|
| Supabase | Email, Device ID, Screenshots, Chat | Authentication, Database, Storage | [supabase.com/privacy](https://supabase.com/privacy) |
| Google Firebase (FCM) | FCM Token | Push Notifications | [firebase.google.com/support/privacy](https://firebase.google.com/support/privacy) |
| Google Sign-In | Email, Name, Profile Photo | Authentication | [policies.google.com/privacy](https://policies.google.com/privacy) |
| Google Fonts | IP Address (automatic by browser) | Typography | [developers.google.com/fonts/faq/privacy](https://developers.google.com/fonts/faq/privacy) |

### 3.3 Legal Requirements
We may disclose your information if required by law, regulation, legal process, or in response to valid requests by public authorities (e.g., a court or government agency).

### 3.4 No Advertising or Analytics SDKs
We do **not** use any advertising SDKs, analytics SDKs (such as Google Analytics, Firebase Analytics, Facebook SDK), or any tracking/profiling services. We do not serve ads and do not track you across apps or websites.

---

## 4. Data Security

We implement industry-standard security measures to protect your personal information:

- **Row Level Security (RLS):** All database tables are protected with Row Level Security policies, ensuring users can only access their own data.
- **Encrypted Transit:** All data transmitted between your device and our servers uses HTTPS/TLS encryption.
- **Encrypted Storage:** Data at rest is encrypted on Supabase's infrastructure.
- **Secure Authentication:** We use Google Sign-In (OAuth 2.0) for authentication. No passwords are stored in our system. Supabase Auth handles all authentication securely.
- **Permission-Based Access Control:** All database functions verify the caller's identity (auth.uid()) before performing any action.
- **No Public API Exposure:** Anonymous (unauthenticated) users cannot access any data or execute any database functions.

---

## 5. Data Retention & Deletion

### 5.1 Automatic Deletion
- **Testing Screenshots:** Automatically deleted from our servers after the testing period is completed and verified.
- **Old Notifications:** Automatically cleaned up after a configurable retention period (default: 20 days).

### 5.2 Account Deletion
You can permanently delete your account at any time from **Settings > Delete Account**. Upon deletion, the following data is permanently removed:
- Your user profile and authentication record.
- All your submitted apps.
- All testing requests (sent and received).
- All uploaded testing proofs (screenshots).
- All chat messages.
- All notifications.
- Your FCM token.
- Your device linkage record.

This action is **irreversible** and takes effect immediately.

### 5.3 Local Data
Data stored locally on your device (SharedPreferences) is not automatically cleared when you delete your account. You can clear this by uninstalling the App or clearing the App's data from your device settings.

---

## 6. Android Permissions

| Permission | Why We Need It |
|---|---|
| `PACKAGE_USAGE_STATS` | To verify daily testing time for the partner's app (fairness check) |
| `READ_MEDIA_IMAGES` / `READ_EXTERNAL_STORAGE` | To let you pick screenshots from your gallery as testing proof |
| `READ_MEDIA_VISUAL_USER_SELECTED` | To support Android 14+ partial media access for photo selection |
| `POST_NOTIFICATIONS` | To send you push notifications about testing updates |
| `SCHEDULE_EXACT_ALARM` / `USE_EXACT_ALARM` | To schedule daily testing reminder alarms |
| `VIBRATE` | To vibrate your device when a notification arrives |
| `INTERNET` | To communicate with our servers (implicit permission) |

---

## 7. Children's Privacy

Testers Area is not intended for use by children under the age of 13. We do not knowingly collect personal information from children under 13. If we discover that a child under 13 has provided us with personal information, we will delete their account and data immediately. If you are a parent or guardian and believe your child has provided us with personal information, please contact us at the email below.

---

## 8. International Data Transfers

Your data is stored on Supabase cloud infrastructure, which may process and store data in data centers located outside your country of residence. By using the App, you consent to the transfer of your data to these locations. Supabase complies with applicable data protection standards.

---

## 9. Your Rights

Depending on your jurisdiction, you may have the following rights regarding your personal data:
- **Access:** Request a copy of the personal data we hold about you.
- **Deletion:** Delete your account and all associated data at any time from within the App.
- **Correction:** Update your profile information at any time.
- **Objection:** Contact us if you object to any specific data processing.

To exercise any of these rights, please contact us at the email address below.

---

## 10. Changes to This Privacy Policy

We may update this Privacy Policy from time to time. We will notify you of any material changes by updating the "Last Updated" date at the top of this page. You are advised to review this Privacy Policy periodically for any changes. Continued use of the App after changes constitutes acceptance of the updated policy.

---

## 11. Contact Us

If you have any questions, concerns, or requests regarding this Privacy Policy or your personal data, please contact us at:

**Email:** testersareaofficial@gmail.com

---

*This privacy policy was last reviewed and is effective as of the date stated above.*
