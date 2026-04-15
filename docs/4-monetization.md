# Monetization

---

### Google Play Billing → In-App Purchases (IAP)

* **Gotcha / Key Difference:** HMS IAP requires all purchasable products to be pre-registered in AppGallery Connect before they can be queried at runtime — unlike Play Billing where product creation is decoupled from the client SDK — meaning any dynamic product catalog pattern must be rearchitected to a static, console-managed catalog.
* **Migration Effort:** Medium
* **Official Docs:** [https://developer.huawei.com/consumer/en/doc/](https://developer.huawei.com/consumer/en/doc/)

---

### Google AdMob → Ads Kit

* **Gotcha / Key Difference:** Ads Kit ad unit IDs are issued from Huawei's Publisher Service console and are not interchangeable with AdMob unit IDs, so dual-stack implementations serving both GMS and HMS devices must maintain two separate ad unit ID registries and a runtime branch to select the correct SDK.
* **Migration Effort:** Easy
* **Official Docs:** [https://developer.huawei.com/consumer/en/doc/](https://developer.huawei.com/consumer/en/doc/)

---

### Google Play Games → Game Service

* **Gotcha / Key Difference:** Game Service leaderboards and achievements require the player to be signed in with Huawei ID (not a guest account), and all leaderboard/achievement metadata must be configured in AppGallery Connect — there is no programmatic API to create or modify these resources at runtime as is possible with the Play Games REST management API.
* **Migration Effort:** Hard
* **Official Docs:** [https://developer.huawei.com/consumer/en/doc/](https://developer.huawei.com/consumer/en/doc/)
