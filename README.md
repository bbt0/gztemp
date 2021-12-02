# Gozio temp backend

> TODO

### Pcap info
**CUH-Admissions.pcap**
- siteID = 1
- buildingID = 10
- floorID = 101
- poiKey = "pv_uh1_316"
- ID in gozio_places.json = 14476

---

**visitor-parking.pcap**
- siteID = 1
- buildingID = 12
- floorID = 101
- poiKey = "cu1_parking_level1"
- ID in gozio_places.json = 10007
This one actually doesn't have a floor id or poi, but it has a default floor ID that maps to another POI. That is `map_floor_id` 102, which is at Gozio place ID `12633`


---

**5fac4c991b67cd496bbb055b-CUH-level1.pcap**
- siteID = 1
- buildingID = 10
- floorID = 101
- poiKey = "pv_uh1_003"

This works when calling `gzmLocationService.addSiteRegion(siteId: 1, hasIps: true, hasOutdoorIps: true, latitude: 32.819, longitude: -96.849, radius: 800, rotation: 0.0)` per the email from Chelsea on 12/1 and 12/2 referencing their support ticket SUPPORT-1199

---

**CUH-level1-2.pcap**
??? Unsure
