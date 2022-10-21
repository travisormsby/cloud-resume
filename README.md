# cloud-resume

This repository holds code for my attempt at the Cloud Resume Challenge. Many of the steps of the challenge have costs like "essentially nothing" or "close to free". I wanted to attempt the challenge using only free-tier resources from cloud servie providers. The total cost of the project is $9.15 / year, the price of registering a .com domain with Cloudflare.

The resume itself is in the form of an HTML document. When changes to the resume are pushed to the main branch of this repo, it triggers a GitHub action to sync the files to an Oracle Cloud Infrastruction object storage bucket.

The resume is served from a vanity URL, [travisormsby.com](https://travisormsby.com), by a CloudFlare worker instance. The worker fetches the resume document from the object storage bucket and serves it to the client.
