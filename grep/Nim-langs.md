# Ceil division in Nim compiler and Nim libraries

## Nim

https://github.com/nim-lang/Nim

In `computeSizeAlign` proc in `compiler/sizealignoffsetimpl.nim`:

```nim
elif align(length, 8) mod 8 == 0:
  typ.size = align(length, 8) div 8
  typ.align = int16(conf.floatInt64Align)
else:
  typ.size = align(length, 8) div 8 + 1
  typ.align = int16(conf.floatInt64Align)
```

## nimx

https://github.com/yglukhov/nimx

In `draw` method in `nimx/image_view.nim`:

```nim
of ImageFillRule.Tile:
    let cols = r.width.int div v.image.size.width.int + 1
    let rows = r.height.int div v.image.size.height.int + 1
```

## nim-libp2p

https://github.com/status-im/nim-libp2p

In `write` method in `libp2p/protocols/secure/noise.nim`:

```nim
let
    frames = (message.len + MaxPlainSize - 1) div MaxPlainSize
```

## nimcrypto

https://github.com/cheatfate/nimcrypto

In `initTwofishContext` proc in `nimcrypto/twofish.nim`:

```nim
let k = (N + 63) div 64
```

## Pixie

https://github.com/treeform/pixie

In `renderEmojiSet` proc in `tests/megatest_emoji.nim`:

```nim
let
  columns = 40
  rows = (images.len + columns - 1) div columns
```

In `renderIconSet` in `tests/megatest_icons.nim`:

```nim
let
  columns = 40
  rows = (images.len + columns - 1) div columns
```
