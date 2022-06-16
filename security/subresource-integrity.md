# Subresource Integrity

[Subresource Integrity](https://developer.mozilla.org/en-US/docs/Web/Security/Subresource_Integrity) (SRI) is a security feature to protect website delivery by validating assets served by a third party, such as a [CDN](https://developer.mozilla.org/en-US/docs/Glossary/CDN). This works by specifying a cryptographic hash that the fetched resource must match. If the file has been changed and the hash does not match, the script will not load.

An example:

```
<script src="https://code.jquery.com/jquery-3.6.0.slim.js"
        integrity="sha256-HwWONEZrpuoh951cQD1ov2HUK5zA5DwJ1DNUXaM6FsY="
        crossorigin="anonymous">
</script>
```

There is a handy [SRI Hash Generator](https://www.srihash.org/) that can be used to quickly generate an Integrity hash, or you can do it manually with the following shell command:

```
cat FILENAME.js | openssl dgst -sha384 -binary | openssl base64 -A
```

The `crossorigin` attribute is required for requests not on the same origin, and `crossorigin="anonymous"` doesn't send any credentials or identity info to the cross-origin site hosting the content.

TL:DR; if you are using a CDN, then including a SRI is a must.

Further reading:

- [Protecting your embedded content with subresource integrity (SRI)](https://www.troyhunt.com/protecting-your-embedded-content-with-subresource-integrity-sri/) by Troy Hunt
