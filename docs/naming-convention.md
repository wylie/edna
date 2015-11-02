## Positioning

`.pos(@pos: s)`

Available Values: 

- s = `position: static;`*
- a = `position: absolute;`
- r = `position: relative;`
- f = `position: fixed;`

## Z-Index

`.z(@z: a)`

Available Values: 

- a = `z-index: auto;`*
- 1-9 = `z-index: 1-9;`

The value of `@z` can be a letter (a) or number (1–9)

## Display

`.d(@d: i)`

Available Values: 

- n = `display: none;`
- b = `display: block;`
- i = `display: inline;`*
- ib = `display: inline-block;`
- tb = `display: table;`
- tbcl = `display: table-column;`
- tbr = `display: table-row;`
- tbc = `display: table-cell;`

## Box-Sizing

`.bxz(@bxz: cb)`

Available Values: 

- cb = `box-sizing: content-box;`*
- bb = `box-sizing: border-box;`

## Float

`.fl(@fl: n)`

Available Values: 

- n = `float: none;`*
- l = `float: left;`
- r = `float: right;`

## Width

```css
.w(@w: 100%) {
	& when ( isnumber(@w) ) {
		width: @w;
	}
}
```

## Height

```css
.h(@h: 100%) {
	& when ( isnumber(@h) ) {
		height: @h;
	}
}
```

## Padding

**padding**

You can pass 1–4 values into this mixin. Must be a number.

```css
.p(@p: 10px) {
	& when ( isnumber(@p) ) {
		padding: @p;
	}
}
```

**padding-top**

```css
.p-t(@p: 10px) {
	& when ( isnumber(@p) ) {
		padding-top: @p;
	}
}
```

**padding-right**

```css
.p-r(@p: 10px) {
	& when ( isnumber(@p) ) {
		padding-right: @p;
	}
}
```

**padding-bottom**

```css
.p-b(@p: 10px) {
	& when ( isnumber(@p) ) {
		padding-bottom: @p;
	}
}
```

**padding-left**

```css
.p-l(@p: 10px) {
	& when ( isnumber(@p) ) {
		padding-left: @p;
	}
}
```

## Margin

**margin**

You can pass 1–4 values into this mixin. Must be a number.

```css
.m(@p: 10px) {
	& when ( isnumber(@p) ) {
		margin: @p;
	}
}
```

**margin-top**

```css
.m-t(@m: 10px) {
	& when ( isnumber(@m) ) {
		margin-top: @m;
	}
}
```

**margin-right**

```css
.m-r(@m: 10px) {
	& when ( isnumber(@m) ) {
		margin-right: @m;
	}
}
```

**margin-bottom**

```css
.m-b(@m: 10px) {
	& when ( isnumber(@m) ) {
		margin-bottom: @m;
	}
}
```

**margin-left**

```css
.m-l(@m: 10px) {
	& when ( isnumber(@m) ) {
		margin-left: @m;
	}
}
```

## Overflow

`.ov(@ov: v)`

Available Values: 

- v = `overflow: visible;`*
- h = `overflow: hidden;`
- s = `overflow: scroll;`
- a = `overflow: auto;`

## Clear

`.cl(@cl: n)`

Available Values: 

- n = `clear: none;`*
- l = `clear: left;`
- r = `clear: right;`
- b = `clear: both;`

## Font

**font-size**

```css
.fz(@fz: 1.6) {
	& when ( isnumber(@fz) ) {
		@remFz: @fz;
		@pxFz: (@fz * 10);
		font-size: unit(@pxFz, px);
		font-size: unit(@remFz, rem);
	}
}
```

**font-family**

`.ff(@ff: sans)`

Available Values: 

- sans = `font-family: Helvetica, Arial, sans-serif;`
- serif = `font-family: Georgia, serif;`
- lucida = `font-family: Lucida Grande", sans-serif;`
- tahoma = `font-family: Tahoma, sans-serif;`
- mono = `font-family: monospace;`
- code = `font-family: Monaco, Menlo, Consolas, "Courier New", monospace;`

**font-weight**

`.fw(@fw: n)`

Available Values: 

- n= `font-weight: normal;`
- b= `font-weight: bold;`

## Line-Height

```css
.lh(@lh: 1) {
	& when ( isnumber(@lh ) {
		line-height: @lh;
	}
}
```

## Color

```css
.c(@c: @colorS1) {
	color: @c
}
```

## Vertical-Align

`.va(@va: bl)`

Available Values: 

- sup = `vertical-align: super;`
- t = `vertical-align: top;`
- tt = `vertical-align: text-top;`
- m = `vertical-align: middle;`
- bl = `vertical-align: baseline;`*
- b = `vertical-align: bottom;`
- tb = `vertical-align: text-bottom;`
- sub = `vertical-align: sub;`

## List

**list-style**

`.lis(@lis: n)`

Available Values: 

- n = `list-style: none;`*

**list-style-position**

`.lis(@lisp: o)`

Available Values: 

- i = `list-style-position: inside;`
- o = `list-style-position: outside;`*

**list-style-type**

`.list(@list: d)`

Available Values: 

- n = `list-style-type: none;`
- d = `list-style-type: disc;`*
- c = `list-style-type: circle;`
- s = `list-style-type: square;`
- dc = `list-style-type: decimal;`
- dclz = `list-style-type: decimal-leading-zero;`
- lr = `list-style-type: lower-roman;`
- ur = `list-style-type: upper-roman;`

## White-Space

**white-space**

`.whs(@whs: n)`

Available Values: 

- n = `white-space: normal;`*
- p = `white-space: pre;`
- nw = `white-space: nowrap;`
- pw = `white-space: pre-wrap;`
- pl = `white-space: pre-line;`

**white-space-collapse**

`.whsc(@whsc: n)`

Available Values: 

- n = `white-space-collapse: normal;`*
- p = `white-space-collapse: keep-all;`
- nw = `white-space-collapse: loose;`
- pw = `white-space-collapse: break-strict;`
- pl = `white-space-collapse: break-all;`

## Word-Wrap

`.wow(@wow: nm)`

Available Values: 

- nm = `word-wrap: normal;`*
- n = `word-wrap: none;`
- u = `word-wrap: unrestricted;`
- s = `word-wrap: suppress;`
- b = `word-wrap: break-word;`

## Word-Break

`.wob(@wob: n)`

Available Values: 

- n = `word-break: normal;`*
- all = `word-break: keep-all;`
- ba = `word-break: break-all;`

## Cursor

`.cur(@cur: a)`

Available Values: 

- a = `cursor: auto;`*
- d = `cursor: default;`
- c = `cursor: crosshair;`
- ha = `cursor: hand;`
- he = `cursor: help;`
- m = `cursor: move;`
- p = `cursor: pointer;`
- t = `cursor: text;`

## Background

**background-color**

```css
.bgc(@bgc: #000) {
	background-color: @bgc;
}
```

**background-image**

```css
.bgi(@bgi) {
	background-image: url(@bgi);
}
```

**background-repeat**

```css
.bgr {
	background-repeat: no-repeat;
}
```

**background-position**

```css
.bgp(@x, @y) {
	background-position: @x @y;
}
```

**background-position-x**

```css
.bgpx(@x) {
	background-position-x: @x;
}
```

**background-position-y**

```css
.bgpy(@y) {
	background-position-y: @y;
}
```

**background-size**

```css
.bgsz(@bgsz: 100%) {
	& when ( isnumber(@bgsz) ) {
		background-size: @bgsz;
	}
}
```

## Border

**border**

```css
.bd(@w: 1px ,@s: solid ,@c: #000) {
	border: unit(@w, px) @s @c;
}
```

**border-top**

```css
.bdt(@w: 1px ,@s: solid ,@c: #000) {
	border-top: unit(@w, px) @s @c;
}
```

**border-right**

```css
.bdr(@w: 1px ,@s: solid ,@c: #000) {
	border-right: unit(@w, px) @s @c;
}
```

**border-bottom**

```css
.bdb(@w: 1px ,@s: solid ,@c: #000) {
	border-bottom: unit(@w, px) @s @c;
}
```

**border-left**

```css
.bdl(@w: 1px ,@s: solid ,@c: #000) {
	border-left: unit(@w, px) @s @c;
}
```

**border-color**

```css
.bdc(@bdc: #000) {
	border-color: @bdc;
}
```

**border-style**

```css
.bds(@bds: solid) {
	border-style: @bds;
}
```

**border-width**

```css
.bdw(@bdw: 1px) {
	& when ( isnumber(@bdw) ) {
		border-width: unit(@bdw, px);
	}
}
```

**border-radius**

```css
.bdrs(@bdrs: 3px) {
	& when ( isnumber(@bdrs) ) {
		border-radius: unit(@bdrs, px);
	}
}
```

## Content

`.cnt(@cnt: n)`

Available Values: 

- n = `content: normal;`*
- oq = `content: open-quote;`
- noq = `content: no-open-quote;`
- cq = `content: close-quote`
- ncq = `content: no-close-quote;`
- a = `content: attr();`
- c = `content: counter();`
- cs = `content: counters();`

## Opacity

```css
.op(@op: 1) {
	& when ( isnumber(@op) ) {
		opacity: @op;
	}
}
```

## Visibility

`.v(@v: v)`

Available Values: 

- v = `visibility: visible;`*
- h = `visibility: hidden;`
- c = `visibility: collapse;`



** * = default value