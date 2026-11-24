# Kyria firmware

Make all configuration updates on `two-remaps` and build firmware from that branch only. Both the firmware manifest (`config/west.yml`) and the reusable GitHub Actions workflow track upstream ZMK `main`, so rebuilding can pick up newer firmware without a config change.

Pushing to `two-remaps` starts a build. To rebuild against current upstream manually:

```sh
gh workflow run build.yml --ref two-remaps
```
