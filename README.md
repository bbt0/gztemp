# Gozio temp backend

### API Responses
- GET `/gozio_wayfinding/assets` -> https://github.com/bbt0/gztemp/raw/master/api%20responses/gozio_asset_response.json
- GET `/layout_settings/gozio_wayfinding/filter` -> https://github.com/bbt0/gztemp/raw/master/api%20responses/gozio_filter_response.json
- GET `/gozio_wayfinding/screen_setup` -> https://github.com/bbt0/gztemp/raw/master/api%20responses/gozio_style.json
- GET `/gozio_wayfinding/indoor_nav_style` -> https://github.com/bbt0/gztemp/raw/master/api%20responses/gozio_indoor_nav_style.json

There are some duplicate api responses that aren't in the `api response` folder -- those are left in here so existing apps don't break. I plan to remove them soon. Please do not use them.

### Explanation of Gozio assets
For the proposed API call GET `/gozio_wayfinding/assets`
- JSON field `assets` -> gozio_assets.zip (this was/is "assets.zip" as well, but "gozio_assets" makes more sense. To not have apps break, I kept "assets.zip" here but I plan to remove it EOW)
- JSON field `gozio_data` -> gozio_data.zip
- JSON field `navigation` -> navigation_v2.json, navigation_voice_v2.json
- JSON field `place_tags` -> search_tags.json



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
