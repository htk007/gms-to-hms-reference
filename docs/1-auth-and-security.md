# Auth & Security

---

### Google Sign-In → Huawei ID

* **Gotcha / Key Difference:** Huawei ID uses OAuth 2.0 / OpenID Connect but issues its own `idToken` signed by Huawei's authorization server, so any backend token verification must call Huawei's token introspection endpoint rather than Google's `tokeninfo` API.
* **Migration Effort:** Easy
* **Official Docs:**[Huawei ID](https://id1.cloud.huawei.com/AMW/portal/home.html) [Google Sign-In](https://support.google.com/accounts/answer/27441?hl=en&co=GENIE.Platform%3DAndroid)

---

### SafetyNet → Safety Detect (SysIntegrity)

* **Gotcha / Key Difference:** Unlike SafetyNet Attestation — which returns a signed JWS blob verifiable with Google's public key — SysIntegrity returns a response verified against Huawei's TEE-backed key, requiring your backend to call Huawei's cloud verification API to validate the nonce and certificate chain.
* **Migration Effort:** Medium
* **Official Docs:** [SafetyNet](https://developers.google.com/android/reference/com/google/android/gms/safetynet/SafetyNet)  [Safety Detect (SysIntegrity)](https://developer.huawei.com/consumer/en/hms/huawei-safetydetectkit/)

---

### reCAPTCHA → Safety Detect (UserDetect)

* **Gotcha / Key Difference:** UserDetect is a risk-scoring API like reCAPTCHA v3, but it does not expose a JavaScript widget or score threshold — the result is a boolean `isRealPerson` flag returned server-side, so any UI logic gating on score bands must be redesigned to binary gating.
* **Migration Effort:** Easy
* **Official Docs:** [https://developer.huawei.com/consumer/en/doc/](https://developer.huawei.com/consumer/en/doc/)
