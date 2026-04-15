# Infrastructure & ML

---

### Firebase Crashlytics → Crash Service

* **Gotcha / Key Difference:** Crash Service symbolication requires uploading a mapping file via the AppGallery Connect console or the `agcp` Gradle plugin — unlike Crashlytics which handles this automatically during the release build — so any CI/CD pipeline performing minified releases must be updated to include the mapping upload step.
* **Migration Effort:** Easy
* **Official Docs:** [https://developer.huawei.com/consumer/en/doc/](https://developer.huawei.com/consumer/en/doc/)

---

### Google Drive API → Drive Kit

* **Gotcha / Key Difference:** Drive Kit scopes access to an app-specific folder by default (analogous to `drive.appdata`) with no equivalent to the full `drive` scope for user-owned file browsing, so applications that read or manipulate arbitrary user files outside the app's own folder cannot be migrated without a fundamental redesign of the file-access model.
* **Migration Effort:** Hard
* **Official Docs:** [https://developer.huawei.com/consumer/en/doc/](https://developer.huawei.com/consumer/en/doc/)

---

### Firebase Cloud Storage → Cloud Storage

* **Gotcha / Key Difference:** Huawei Cloud Storage is built on OBS (Object Storage Service) and uses Huawei's STS token model for security rules rather than Firebase's expression-based `rules` language, requiring a complete rewrite of storage access-control logic from declarative rules to IAM-policy-style token grants.
* **Migration Effort:** Medium
* **Official Docs:** [https://developer.huawei.com/consumer/en/doc/](https://developer.huawei.com/consumer/en/doc/)

---

### Firebase Remote Config → Remote Configuration

* **Gotcha / Key Difference:** Remote Configuration fetches and caches config values using an interval-based model identical to Firebase, but it does not support Firebase's condition targeting by app version, OS, or custom user properties — all targeting must be handled server-side via A/B Testing Kit or omitted entirely.
* **Migration Effort:** Easy
* **Official Docs:** [https://developer.huawei.com/consumer/en/doc/](https://developer.huawei.com/consumer/en/doc/)

---

### ML Kit (Google) → ML Kit (Huawei)

* **Gotcha / Key Difference:** Huawei ML Kit runs most models on-device using the NPU on Kirin chipsets for hardware acceleration, but falls back to CPU inference on non-Kirin devices, meaning latency and battery benchmarks established on Pixel/Snapdragon hardware are not valid for Huawei device targets.
* **Migration Effort:** Medium
* **Official Docs:** [https://developer.huawei.com/consumer/en/doc/](https://developer.huawei.com/consumer/en/doc/)

---

### Google Fit → Health Kit

* **Gotcha / Key Difference:** Health Kit requires users to explicitly grant each data-type permission through a Huawei Health authorization flow that launches a separate system UI (not an in-app dialog), and access to sensitive health data types additionally requires Huawei's manual review and approval of the application before runtime permissions can be granted.
* **Migration Effort:** Hard
* **Official Docs:** [https://developer.huawei.com/consumer/en/doc/](https://developer.huawei.com/consumer/en/doc/)
