# OTA

Changelogs in Here

## Update feeds

The Lunaris updater reads these JSON files from branch `16.2`:

- Google Apps builds: `builds/surya.json`
- Vanilla builds: `builds/vanilla/surya.json`

Each file must contain a `response` array. Use the build-generated `surya.json`
as the source for each release, and update its `maintainer` and `download`
fields before publishing. The `download` URL must point to the uploaded ZIP;
`sha256`, `size`, and `timestamp` must match that exact ZIP/build.

Example:

```json
{
	"response": [
		{
			"maintainer": "F O X E S K Y",
			"oem": "Xiaomi",
			"device": "surya",
			"filename": "rom.zip",
			"download": "https://sourceforge.net/projects/foxlabs-ota/files/AOSP/rom.zip/download",
			"timestamp": 1794161436,
			"sha256": "<sha256>",
			"size": 123456789,
			"version": "3.13",
			"os_patch_level": "2026-10-01",
			"os_sdk_level": 36,
			"buildtype": "VANILLA"
		}
	]
}
```
