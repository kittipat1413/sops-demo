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