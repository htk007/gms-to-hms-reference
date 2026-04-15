# Communication & Growth

---

### Firebase Cloud Messaging (FCM) → Push Kit

* **Gotcha / Key Difference:** Push Kit requires obtaining an `access_token` via Huawei's OAuth 2.0 client-credentials flow on every server-side send call (tokens expire in 60 minutes), whereas FCM uses a long-lived server key, so your push dispatch backend must implement token caching and refresh logic.
* **Migration Effort:** Medium
* **Official Docs:** [https://developer.huawei.com/consumer/en/doc/](https://developer.huawei.com/consumer/en/doc/)

---

### Firebase Dynamic Links → App Linking

* **Gotcha / Key Difference:** App Linking deep-link resolution requires that the app be published to AppGallery and the SHA-256 fingerprint registered in AppGallery Connect, meaning deferred deep links cannot function during development with debug builds unless the SHA-256 is explicitly whitelisted in the console.
* **Migration Effort:** Medium
* **Official Docs:** [https://developer.huawei.com/consumer/en/doc/](https://developer.huawei.com/consumer/en/doc/)

---

### Google Analytics → Analytics Kit

* **Gotcha / Key Difference:** Analytics Kit auto-collects a different set of predefined events than GA4 (e.g., no automatic `screen_view` from `Activity` lifecycle by default), so event parity requires explicit `onEvent` calls for events that Google's SDK would have collected passively.
* **Migration Effort:** Easy
* **Official Docs:** [https://developer.huawei.com/consumer/en/doc/](https://developer.huawei.com/consumer/en/doc/)

---

### App Indexing → App Search

* **Gotcha / Key Difference:** App Search indexes content for the Huawei Search app and HUAWEI Assistant rather than Google Search, so any SEO strategy or web-to-app indexing via `rel=alternate` links has no HMS equivalent and must be replaced with in-app discoverability patterns.
* **Migration Effort:** Medium
* **Official Docs:** [https://developer.huawei.com/consumer/en/doc/](https://developer.huawei.com/consumer/en/doc/)
