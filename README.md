# NuITP

NuITP is an inductive theorem prover for Maude equational specifications. It
combines narrowing, equality predicates, constructor variant unification,
order-sorted congruence closure, ordered rewriting, and strategy-based
rewriting to reason about Maude equational programs.

This repository is a small convenience fork used by the IMR/AXIOM workspace.
It keeps the upstream Alpha 39 release beside the project that consumes it; it
does not claim to be the upstream development repository.

## Included release

`NuITP_alpha39.maude` is NuITP Alpha 39, released 31 July 2026. It requires
Maude Alpha 165 or later. The accompanying AXIOM container pins Maude Alpha
165, the first compatible public release, so proofs use the same `rpo`
support expected by NuITP.

## Running it

Start Maude in the directory containing the specification and this release:

```console
$ Maude -allow-files
Maude> load my-specification.maude
Maude> load NuITP_alpha39.maude
Maude> erew in NuITP : init .
NuITP>
```

`-allow-files` is necessary only when loading or saving proof scripts. NuITP
works on Maude functional modules and relies on appropriately declared
constructors (`ctor`) and variant equations (`variant`); see the manual for
the full admissibility conditions and proof-command reference.

## Upstream documentation

- Website and releases: <https://nuitp.webs.upv.es/>
- User manual: <https://nuitp.webs.upv.es/download/NuITP.pdf>
- Maude releases: <https://github.com/maude-lang/Maude/releases>

The NuITP website recommends using the latest release. Alpha 39 is deliberately
kept here because the AXIOM proof scripts and container are pinned to its
Maude Alpha 165 compatibility boundary.

## License

NuITP is free software under GPL-3.0-or-later. See [LICENSE](LICENSE) and the
upstream site for the complete notice.
