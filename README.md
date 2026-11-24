# Kilna packages

The official package repository of **Kilna**, an independent Linux distribution
(not based on any other distro) with its own init (spark), package manager
(anvil) and build system (molds).

The packages are in the [`repo` release](https://github.com/jalfarocode/kilna-packages/releases/tag/repo).
Kilna uses them with `anvil sync`, `anvil install <name>` and `anvil upgrade`.

## Security

GitHub is only the transport. The `index` lists the sha256 and size of every
package and is signed with Ed25519 (`index.sig`). anvil verifies the signature
with the key that ships in Kilna (`/etc/anvil/keys/kilna.pub`), then checks every
downloaded package against the index, and rejects old or expired indexes.
A modified file here would be rejected.

Public key:

    4b3da1a1a2b20bbf9dea1a5a8d2028baa056c3abbfb348df84df1477bcd87223
