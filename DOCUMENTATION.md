# Maskbook VI Assets Management Standard

## Introduction

This document is part of specification "Maskbook-VI".

This document elaborates how should image assets be managed.

## Filename Normalization

### Conventions

- Every file must start with namespace "MB--".
- Filenames should case-sensitive, even if transportation methods and file systems are case-insensitive.
- The conjunction mark connecting components should generally be double-hyphen.
- Within each component, PascalCase writing should be used. Underscore and single-hyphen may be used marginally.
- In filename structure declaration, braces indicate filling with variable value, and brackets indicate that the content is optional.
- Valid extension names are "svg", "png", "jpg" (discouraged), "ico", and "webp".

### Types

In this repository, we have several major types:

- Logo
- Banner
- Tile
- Misc

### Type: Logo

Filename structure:

```plain
MB--{Type}--{Class}[-{Variation}]--{Usage}[--{Color}].{ext}
```

Logo files have several properties:

- Class
- Variation (Optional)
- Usage
- Color (Optional)

#### Property: Class

The Class property has several possible values:

| Data  | Description                               |
| ----- | ----------------------------------------- |
| Geo   | Geometric logo.                           |
| Text  | Text logo.                                |
| CombV | Combination of both in a vertically line. |
| CombH | Combination of both in a horizontal line. |

Additional values may be used separately as independent cases.

#### Property: Variation

The Variation property has several possible values:

| Data     | Description                                                  |
| -------- | ------------------------------------------------------------ |
| Squircle | The geometric logo component inside is the squircle edition. |
| Circle   | The geometric logo component inside is the circle edition.   |

This property be used only when the value of Class is "CombH" or "CombV".

#### Property: Usage

The Usage property has several possible values:

| Data          | Description                                                                      |
| ------------- | -------------------------------------------------------------------------------- |
| Core          | The core shape without any padding.                                              |
| FreeCanvas    | There is no particular restriction around the logo. For example, a large poster. |
| SquareCanvas  | The canvas is a square or a squircle.                                            |
| CircleCanvas  | The canvas is a circle. Corners will be trimmed.                                 |
| ForceCircle   | Transparent corners to make the image a circle, regardless of canvas.            |
| ForceSquircle | Transparent corners to make the image a squircle, regardless of canvas.          |

#### Property: Color

| Data        | Description                        |
| ----------- | ---------------------------------- |
| Blue        | #1C68F3.                           |
| Black       | #000000.                           |
| WhiteInBlue | #FFFFFF shape over #1C68F3 canvas. |

For "FreeCanvas" images, if no "In[Color]" is suffixed, the image should have transparent background. Other images must have their respective implied backgrounds.

### Type: Banner

Filename structure:

```
MB--{Type}--{Class}[-{Variation}]--E{Edition}.{ext}
```

Banner files have several properties:

- Class
- Variation (Optional)
- Edition (Optional)

### Type: Tile

Filename structure:

```plain
MB--{Type}--{Class}[-{Variation}]--E{Edition}.{ext}
```

Tile files have several properties:

- Class
- Variation (Optional)
- Edition (Optional)

### Type: Misc

Filename structure:

```plain
MB--{Type}--{Class}[-{Variation}]--E{Edition}.{ext}
```

Misc files have several properties:

- Class
- Variation (Optional)
- Edition (Optional)
