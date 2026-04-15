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

> Phase 1 (20 services) is complete. Phases 2–5 below list all known remaining GMS→HMS mappings, organized by domain.

### Phase 2 — Payments, Wearables & Device Ecosystem

| GMS Service | HMS Equivalent |
|-------------|----------------|
| Google Pay | Huawei Pay |
| Google Wallet Passes | Wallet Kit |
| Wear OS | Wear Engine |
| Chromecast SDK | Cast+ Connect |
| Android Auto | HiCar |
| Android TV | HUAWEI Vision (Smart Screen) |
| Google Home / Smart Home | HiLink (Smart Home SDK) |
| Google Play Instant Apps | Quick App |

### Phase 3 — AR, Identity & Sensing

| GMS Service | HMS Equivalent |
|-------------|----------------|
| ARCore | AR Engine |
| Google Identity Services (One Tap Sign-In) | Huawei ID (QuickLogin) |
| Google Smart Lock for Passwords | no direct HMS equivalent |
| Activity Recognition API | Activity Identification (Location Kit) |
| Geofencing API | Geofence (Location Kit) |
| Awareness API | no direct HMS equivalent |
| Wifi Aware (NAN) | no direct HMS equivalent |
| Android Backup / Auto Backup | Device Backup (HMS Core) |

### Phase 4 — Firebase Backend Services

| GMS (Firebase) Service | HMS / AGC Equivalent |
|------------------------|----------------------|
| Firebase Authentication (email / phone / OAuth) | Auth Service (AppGallery Connect) |
| Firebase Firestore | Cloud DB (AppGallery Connect) |
| Firebase Realtime Database | Cloud DB (AppGallery Connect) |
| Firebase A/B Testing | A/B Testing Kit (AppGallery Connect) |
| Firebase In-App Messaging | In-App Messaging (AppGallery Connect) |
| Firebase Performance Monitoring | APM Kit (AppGallery Connect) |
| Firebase App Distribution | Distribution (AppGallery Connect) |
| Firebase Test Lab | Cloud Debugging (AppGallery Connect) |
| Firebase App Check | no direct HMS equivalent |
| Google Tag Manager | no direct HMS equivalent |

### Phase 5 — ML & Speech Expansion

| GMS Service | HMS Equivalent |
|-------------|----------------|
| Google Speech-to-Text | ML Kit ASR |
| Google Text-to-Speech | ML Kit TTS |
| Google Cloud Vision API | ML Kit Image Classification / Object Detection |
| Google Cloud Translation API | ML Kit Translation |
| Google Cloud Natural Language API | ML Kit Natural Language Understanding |
| Google Cloud Face Detection | ML Kit Face Detection |
| Google Lens (on-device) | ML Kit Scene Detection |
| Google Cloud Barcode Scanning | ML Kit Scan Kit |

### Phase 6 — Tooling & Community
- [ ] Automated dependency scanner to flag GMS usages in a project
- [ ] Side-by-side API diff tables at the method level
- [ ] Sample migration app demonstrating dual-stack (GMS + HMS) patterns
- [ ] Verified migration case studies from production apps
- [ ] Complexity scoring model based on surface-area analysis
- [ ] Integration with Huawei DevEco toolchain

---

## Contributing

See [CONTRIBUTING.md](CONTRIBUTING.md) for the PR process and editorial standards.

---

## License

MIT — see [LICENSE](LICENSE).
