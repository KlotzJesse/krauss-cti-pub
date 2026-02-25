# KRAUSS CTI — Distribution

Auto-hosted distribution repo for the **KRAUSS CTI** Chrome / Edge extension.

## Install via policy (recommended)

Use this value in your **ExtensionInstallForcelist** policy:

```
klcgohoohnbilgkcjjjgpcfbnllcljea;https://github.com/KlotzJesse/krauss-cti-pub/raw/main/update.xml
```

### Microsoft Intune

1. Intune Admin Center → **Devices** → **Configuration profiles** → **Create profile**
2. Platform: **Windows 10 and later** / Profile type: **Settings catalog**
3. Search **"Microsoft Edge"** → **Extensions** → **Control which extensions are installed silently**
4. Add the value above and assign to your device group.

### Group Policy (on-prem)

Path: `Computer Configuration → Administrative Templates → Microsoft Edge → Extensions`  
Policy: **Control which extensions are installed silently**

### Registry (testing)

```
HKLM\SOFTWARE\Policies\Microsoft\Edge\ExtensionInstallForcelist
Name:  1
Value: klcgohoohnbilgkcjjjgpcfbnllcljea;https://github.com/KlotzJesse/krauss-cti-pub/raw/main/update.xml
```

## Manual install

1. Download `krauss-cti.crx`
2. Open `edge://extensions` or `chrome://extensions`
3. Enable **Developer Mode**
4. Drag & drop the CRX file

## Files

| File | Description |
|------|-------------|
| `krauss-cti.crx` | Signed extension package |
| `update.xml` | Auto-update manifest (appid + version + download URL) |

## Update URL

```
https://github.com/KlotzJesse/krauss-cti-pub/raw/main/update.xml
```

## Extension ID

```
klcgohoohnbilgkcjjjgpcfbnllcljea
```
