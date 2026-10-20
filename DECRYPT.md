# How to decrypt

You need the passphrase (a file called `repo-key.txt`).

```sh
# decrypt (enter the passphrase when prompted, or use --passphrase-file FILE)
gpg -d ensemble-kit-20261020.tar.zst.gpg > ensemble-kit.tar.zst
# verify the archive is intact (compare to the hash in README.md)
sha256sum ensemble-kit-20261020.tar.zst.gpg
# unpack into a new directory -> a complete git repo, .git history included
mkdir ensemble-kit && tar -I zstd -xf ensemble-kit.tar.zst -C ensemble-kit
cd ensemble-kit && git log --oneline
```

If `gpg` is unavailable: `zstd` + any OpenPGP tool with the same passphrase.
