# DXSpider public download mirror

This repository provides a secondary distribution source for public DXSpider resources. The synchronisation process retrieves files from `http://dxspider.dxcluster.net/download/`, validates supported formats and preserves the original bytes. The mirror is not a copy of any node's private operational lists.

## Download resources

- [Current file catalogue](manifest.txt)
- [SHA-256 checksums](SHA256SUMS)

Raw download base URL:

```text
https://raw.githubusercontent.com/dxspider-official/download/main/
```

Example:

```sh
curl -fLO https://raw.githubusercontent.com/dxspider-official/download/main/badip.global
```

## Updates and integrity

The catalogue is generated from validated files. Availability may change. A missing or invalid upstream response is not installed over a previously validated copy. Updates are scheduled hourly; actual freshness depends on successful synchronisation and upstream availability.

To verify all files in a local checkout:

```sh
sha256sum -c SHA256SUMS
```

Checksums verify the bytes in this mirror, not the authenticity of the upstream HTTP source.

## Notes for SYSOPs

Downloads are not automatically merged with local lists or reloaded into DXSpider. Back up local lists before replacing them, especially native DXHash files. Consult the [upgrade guides](https://github.com/dxspider-official/documentation) for build-specific update examples.

DXSpider is developed by Dirk Koopman (G1TLH).
