# Client certificate dialog validation

These screenshots were captured from real, isolated, headless Zen 1.23.3b windows on macOS. They use a self-signed test certificate for `test@example.com` and the synthetic hostname `certificate-authentication.long-hostname.example.com`.

The before images use the installed dialog script. The after images use the exact patched Firefox 158.0 dialog script loaded through a temporary chrome-resource override. The installed application and the user's browser profile were not modified. Images were captured directly from the dialog element with Marionette.

`validation.json` records the 224 passing assertions from the regression task executed through Marionette with minimal test-harness adapters: tab-modal and window-modal dialogs, light and dark themes, 13/16/20px dialog fonts, and window sizes of 1366x850, 1600x1000, and 1024x600. The task checks button bounds within the dialog and the browser window, enabled state, certificate selection, and remember-setting return values.

A full source build and the mach mochitest runner were not run. The screenshots and results are runtime validation of the patched dialog in the installed browser.
