# Luma Beta build 3.0.1

Production TypeScript/Vite compilation, packaged startup/persistence/security smoke test and packaged interface verification cover this branding patch. Existing updater and desktop behavior are unchanged from 3.0.0. The public update feed must offer build 3.0.1 to 3.0.0 clients and report 3.0.1 current. Public metadata and installer hashes are checked after publication.

Luma Beta is the public product label. Package version 3.0.1, existing appId/productName and the existing GitHub update provider preserve install/update and user-data compatibility. Do not reduce the package version to 1.0.0 for a future public Luma 1.0 launch; keep marketing version separate from the monotonically increasing build number.

Only Windows Setup copies support automatic updates. Portable and Mac preview remain manual. Windows binaries are unsigned. Installer execution is not exercised against the personal installation; previous 3.0 updater tests intercept process spawning. Full replacement, physical mixed-DPI and Explorer/fullscreen compatibility limits remain.
