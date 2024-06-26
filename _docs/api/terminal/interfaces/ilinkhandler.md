---
category: API-interfaces
layout: docs
---


***

[@xterm/xterm]({% link _docs/api/terminal/readme.md %}) / ILinkHandler

# Interface: ILinkHandler

A link handler for OSC 8 hyperlinks.

## Properties

### allowNonHttpProtocols?

> **`optional`** **allowNonHttpProtocols**: `boolean`

Whether to receive non-HTTP URLs from LinkProvider. When false, any
usage of non-HTTP URLs will be ignored. Enabling this option without
proper protection in `activate` function may cause security issues such
as XSS.

#### Source

[xterm.d.ts:1345](https://github.com/xtermjs/xterm.js/blob/5.5.0/typings/xterm.d.ts#L1345)

## Methods

### activate()

> **activate**(`event`, `text`, `range`): `void`

Calls when the link is activated.

#### Parameters

• **event**: `MouseEvent`

The mouse event triggering the callback.

• **text**: `string`

The text of the link.

• **range**: [`IBufferRange`]({% link _docs/api/terminal/interfaces/ibufferrange.md %})

The buffer range of the link.

#### Returns

`void`

#### Source

[xterm.d.ts:1318](https://github.com/xtermjs/xterm.js/blob/5.5.0/typings/xterm.d.ts#L1318)

***

### hover()?

> **`optional`** **hover**(`event`, `text`, `range`): `void`

Called when the mouse hovers the link. To use this to create a DOM-based
hover tooltip, create the hover element within `Terminal.element` and
add the `xterm-hover` class to it, that will cause mouse events to not
fall through and activate other links.

#### Parameters

• **event**: `MouseEvent`

The mouse event triggering the callback.

• **text**: `string`

The text of the link.

• **range**: [`IBufferRange`]({% link _docs/api/terminal/interfaces/ibufferrange.md %})

The buffer range of the link.

#### Returns

`void`

#### Source

[xterm.d.ts:1329](https://github.com/xtermjs/xterm.js/blob/5.5.0/typings/xterm.d.ts#L1329)

***

### leave()?

> **`optional`** **leave**(`event`, `text`, `range`): `void`

Called when the mouse leaves the link.

#### Parameters

• **event**: `MouseEvent`

The mouse event triggering the callback.

• **text**: `string`

The text of the link.

• **range**: [`IBufferRange`]({% link _docs/api/terminal/interfaces/ibufferrange.md %})

The buffer range of the link.

#### Returns

`void`

#### Source

[xterm.d.ts:1337](https://github.com/xtermjs/xterm.js/blob/5.5.0/typings/xterm.d.ts#L1337)
