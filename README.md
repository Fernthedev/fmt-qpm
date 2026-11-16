# {fmt} for QPM v2

Header-only {fmt} 12.2.1, pinned by the `fmt` submodule.

```sh
git submodule update --init --recursive
qpm restore
qpm qpkg
```

Use a QPM v2 executable (`qpm2` when installed under that name). Packaging needs
no NDK or library build. Consumers receive `FMT_HEADER_ONLY` and the include root
for `#include <fmt/format.h>` automatically.

To test a local package in a consumer workspace:

```sh
qpm install --path /path/to/fmt.qpkg
```

Add `fmt` with version range `^12.2.1` and `qmod: "none"` to the consumer's
`dependencies`, then run `qpm restore`.
