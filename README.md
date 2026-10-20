# ensemble-kit — encrypted

This public repository contains **no readable source**. It holds one
GPG-encrypted archive of the full `ensemble-kit` repository, history included.
**Without the passphrase the contents cannot be recovered.**

| | |
|---|---|
| archive | `ensemble-kit-20261020.tar.zst.gpg` |
| sha256(ciphertext) | `a182a046936eb4bc6ada04fb1b9271ef22ace91a786ca8a5cefb1138dd0c877d` |
| size | 67 MB |
| key fingerprint | `sha256:f1f0bd1d0e82e8c808da9308` |

### Omitted from the archive

Nothing **git-tracked** is omitted, so the unarchived repo's `git status` is clean.
The following git-IGNORED, regenerable corpora are left out (the host rejects any
single file over 100 MB):

| path | why |
|---|---|
| `bench/corpus/b1_admitted.jsonl` | regenerable, git-ignored |

Each is rebuilt byte-for-byte from the pins recorded in the tracked
`bench/corpus/*.meta.json` / `*.summary.json` beside it — e.g.
`gen_tests.py gen --pool bench/corpus/b1_tasks.jsonl --refs bench/corpus/refs_post.jsonl --out bench/corpus/b1_admitted.jsonl`.

See [DECRYPT.md](DECRYPT.md). Built 2026-10-20T09:04:12Z.
