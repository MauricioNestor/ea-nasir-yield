# Ea-Nasir Yield

A pure JSON content mod for Vintage Story 1.22.

It adds a fifth ore grade below `poor`: `eanasir`.

## Initial copper ores

- Native copper
- Malachite

An Ea-Nasir ore chunk reports **5 metal units**, so hammering it produces exactly **one copper nugget**. Crystallized Ea-Nasir ore keeps the vanilla 2x crystallized bonus and reports 10 units.

The item models deliberately reuse the vanilla `poor` models. The block texture is already grade-independent, so an Ea-Nasir vein looks deceptively respectable until mined.

## Compatibility design

The yield rule is generic:

```json
"ore-eanasir-*": 5
```

Other mods can opt a copper ore into the grade by adding valid `ore-eanasir-<ore>-<rock>` variants and inserting `eanasir` into that ore's worldgen grade arrays. No C# is required.

## Development test

Use this together with `testing-world-gen-only-ores`, which forces the supported copper deposits to generate as Ea-Nasir grade at absurd frequency.

## Status

Experimental. Built against the 1.22 asset layout.
