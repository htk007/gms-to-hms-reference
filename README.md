# GMS to HMS Migration Reference

> The definitive, community-maintained reference for Android developers migrating from Google Mobile Services (GMS) to Huawei Mobile Services (HMS). Built for engineers who need authoritative, architectural-level guidance — not marketing copy.

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](LICENSE)
[![PRs Welcome](https://img.shields.io/badge/PRs-welcome-brightgreen.svg)](CONTRIBUTING.md)
[![Services Mapped](https://img.shields.io/badge/Services%20Mapped-20-blue.svg)](#service-mapping)

---

## Why This Exists

Since Google Mobile Services became unavailable on Huawei devices (post-2019), Android developers targeting the Huawei ecosystem have faced an underdocumented, fragmented migration path. This repository consolidates that path into a single, opinionated, technically precise reference — covering API equivalence, architectural gotchas, and migration effort estimates.

---

## Service Mapping

| # | GMS Service | HMS Equivalent | Category | Effort |
|---|-------------|----------------|----------|--------|
| 1 | Google Sign-In | Huawei ID | Auth & Security | Easy |
| 2 | SafetyNet | Safety Detect (SysIntegrity) | Auth & Security | Medium |
| 3 | reCAPTCHA | Safety Detect (UserDetect) | Auth & Security | Easy |
| 4 | Firebase Cloud Messaging (FCM) | Push Kit | Communication & Growth | Medium |
| 5 | Firebase Dynamic Links | App Linking | Communication & Growth | Medium |
| 6 | Google Analytics | Analytics Kit | Communication & Growth | Easy |
| 7 | App Indexing | App Search | Communication & Growth | Medium |
| 8 | Google Maps | Map Kit | Location & Maps | Hard |
| 9 | Fused Location Provider | Location Kit | Location & Maps | Easy |
| 10 | Places API | Site Kit | Location & Maps | Medium |
| 11 | Nearby Share | Nearby Service | Location & Maps | Hard |
| 12 | Google Play Billing | In-App Purchases (IAP) | Monetization | Medium |
| 13 | Google AdMob | Ads Kit | Monetization | Easy |
| 14 | Google Play Games | Game Service | Monetization | Hard |
| 15 | Firebase Crashlytics | Crash Service | Infrastructure & ML | Easy |
| 16 | Google Drive API | Drive Kit | Infrastructure & ML | Hard |
| 17 | Firebase Cloud Storage | Cloud Storage | Infrastructure & ML | Medium |
| 18 | Firebase Remote Config | Remote Configuration | Infrastructure & ML | Easy |
| 19 | ML Kit (Google) | ML Kit (Huawei) | Infrastructure & ML | Medium |
| 20 | Google Fit | Health Kit | Infrastructure & ML | Hard |

---

## Documentation

Each category has a dedicated deep-dive document:

- [Auth & Security](docs/1-auth-and-security.md)
- [Communication & Growth](docs/2-communication-and-growth.md)
- [Location & Maps](docs/3-location-and-maps.md)
- [Monetization](docs/4-monetization.md)
- [Infrastructure & ML](docs/5-infrastructure-and-ml.md)

---

## Roadmap

### Phase 2 — Extended Coverage
- [ ] Wearables: Wear OS → HUAWEI Wear Engine
- [ ] Wallet: Google Pay → Huawei Pay
- [ ] Cast: Chromecast SDK → Cast+ Connect
- [ ] AR: ARCore → AR Engine
- [ ] Speech: Google Speech-to-Text → ML Kit ASR

### Phase 3 — Tooling
- [ ] Automated dependency scanner to flag GMS usages in a project
- [ ] Side-by-side API diff tables at the method level
- [ ] Sample migration app demonstrating dual-stack (GMS + HMS) patterns

### Phase 4 — Community
- [ ] Verified migration case studies from production apps
- [ ] Complexity scoring model based on surface-area analysis
- [ ] Integration with Huawei DevEco toolchain

---

## Contributing

See [CONTRIBUTING.md](CONTRIBUTING.md) for the PR process and editorial standards.

---

## License

MIT — see [LICENSE](LICENSE).
