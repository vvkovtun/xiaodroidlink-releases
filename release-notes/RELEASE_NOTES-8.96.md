# XiaoDroidLink 8.96 (versionCode 242) — internal

## What changed

- **Readable car in anonymous statistics.** The `car` field in Google Analytics was only the CarLink codes (`002f/0011`). It is now `Xiaomi YU7 (002f/0011)` from a table of 20 confirmed models and 13 brands (`CarModels`). A model missing from the table gets the name the car itself sends after connecting (vendor_name + product_name, often Chinese, e.g. `Toyota 丰田 凯美瑞 (0041/0099)`); an unknown brand that never connected — codes only. The daily event also carries `car_name`.

## Verified

- Core tests 65/65, build OK.
- Not checked in Google Analytics yet.
