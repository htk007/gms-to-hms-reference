# Location & Maps

---

### Google Maps → Map Kit

* **Gotcha / Key Difference:** Map Kit uses Huawei's own tile servers and coordinate system calibrated for Chinese regulations (GCJ-02 in mainland China, WGS-84 elsewhere), so hardcoded coordinate transformations or tile URL assumptions will produce incorrect map positioning depending on the device's locale.
* **Migration Effort:** Hard
* **Official Docs:** [https://developer.huawei.com/consumer/en/doc/](https://developer.huawei.com/consumer/en/doc/)

---

### Fused Location Provider → Location Kit

* **Gotcha / Key Difference:** Location Kit's `FusedLocationProviderClient` mirrors the GMS API surface closely, but on devices without GMS it falls back to Huawei's own sensor-fusion stack rather than Google's, which may produce different accuracy characteristics and does not support the `setMockLocation` method used in GMS-based test environments.
* **Migration Effort:** Easy
* **Official Docs:** [https://developer.huawei.com/consumer/en/doc/](https://developer.huawei.com/consumer/en/doc/)

---

### Places API → Site Kit

* **Gotcha / Key Difference:** Site Kit's POI database is sourced from Huawei's own map data rather than Google's, so place IDs are not portable between the two systems and any persisted `placeId` values stored in your backend must be treated as entirely separate namespaces with no cross-referencing possible.
* **Migration Effort:** Medium
* **Official Docs:** [https://developer.huawei.com/consumer/en/doc/](https://developer.huawei.com/consumer/en/doc/)

---

### Nearby Share → Nearby Service

* **Gotcha / Key Difference:** Nearby Service provides both a Message (BLE beacon broadcast) and Connection (P2P data transfer) API, but the Connection API requires both devices to have HMS Core installed and does not interoperate with Android's Nearby Connections API, making cross-ecosystem peer-to-peer scenarios impossible without a relay server.
* **Migration Effort:** Hard
* **Official Docs:** [https://developer.huawei.com/consumer/en/doc/](https://developer.huawei.com/consumer/en/doc/)
