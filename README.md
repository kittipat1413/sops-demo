[Encrypting your files using Mozilla SOPS](https://dev.to/kittipat1413/encrypting-your-files-using-mozilla-sops-33fd)

### Generate a key
```bash
gpg --batch --full-generate-key --rfc4880 --digest-algo sha512 --cert-digest-algo sha512 <<EOF
%no-protection
Key-Type: RSA
Key-Length: 4096
Subkey-Type: RSA
Subkey-Length: 4096
Expire-Date: 0
Name-Comment: ${GPG_COMMENT}
Name-Real: ${GPG_NAME}
EOF
```
