# Detect Man-In-The-Middle Attack in your HTTPS traffic

## Origin

This notebook is inspired from this [site](https://checkmyhttps.net/) and corresponding [Firefox extension](https://addons.mozilla.org/en-US/firefox/addon/checkmyhttps/)


## General Idea

The general idea is to get a certificate's digest from a safe computer and network, store it as reference, and update it from time to time.

In a suspicious environment, typically where the computer and/or network is potentially unsecure (e.g. corporate setting, internet café, etc), use the browser to check a website's fingerprint. **DO NOT** stop at the green <span style="color: green;">https:</span>//a-web-site.com symbol that suggests everything is fine. If the digest you read is different from the reference, it means the certificate was fabricated and appears valid only because a root certificate was planted in the computer you use by a malevolent administrator.

In this case your are very likely experiencing a [Man-In-The-Middle Attack](https://en.wikipedia.org/wiki/Man-in-the-middle_attack). Your passwords are probably read and stored by the attacker. DANGER ! 

These attacks are very frequent particularly from proxies..

## Run

Build the SHA1 certificate digests for a list of urls with [this notebook](http://nbviewer.jupyter.org/github/oscar6echo/detect-https-mitm-attack/blob/master/check_mitm_attack.ipynb).

