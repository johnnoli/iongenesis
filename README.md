# Ion Genesis

PH hospital database + coverage map, deployed as a website and an Android app.

## Structure
- `www/` — the actual site (edit these files). `index.html` is the hospital database, `gasion_hospital_map_coverage.html` is the coverage map.
- `android/` — Capacitor Android shell. It loads https://genesis.gasioncloud.com directly, so the installed app always shows the latest deployed site.

## Updating the data
1. Edit the files in `www/`
2. Commit and push — Cloudflare Pages auto-deploys the site
3. Done. The website and the mobile app both update immediately. No APK rebuild needed.

## Rebuilding the APK (only needed for icon/name/config changes)
```
npx cap sync android
npx cap open android   # then Run or Build > Build APK(s) in Android Studio
```
