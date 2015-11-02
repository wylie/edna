## Positioning

**position**

`.pos(@pos: s)`

Available Values: 

- s = `position: static;`*
- a = `position: absolute;`
- r = `position: relative;`
- f = `position: fixed;`

**top**

`.t(@t: a)`

Available Values: 

- a = `top: auto;`
- &lt;number> = `top: <number>;`

**right**

`.r(@r: a)`

Available Values: 

- a = `right: auto;`
-  &lt;number> = `right: <number>;`

**bottom**

`.b(@b: a)`

Available Values: 

- a = `bottom: auto;`
-  &lt;number> = `bottom: <number>;`

**left**

`.l(@l: a)`

Available Values: 

- a = `left: auto;`
-  &lt;number> = `left: <number>;`

## Z-Index

`.z(@z: a)`

Available Values: 

- a = `z-index: auto;`*
- &lt;number> = `z-index: <number>;`

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

`@w` must be any number **with any unit type**. This will fail if it's not.

```css
.w(@w: 100%) {
	& when ( isnumber(@w) ) {
		width: @w;
	}
}
```

## Height

`@h` must be a number **with any unit type**. This will fail if it's not.

```css
.h(@h: 100%) {
	& when ( isnumber(@h) ) {
		height: @h;
	}
}
```

## Padding

`@p` must be a number **with any unit type**. This will fail if it's not.

**padding**

You can pass 1–4 values into this mixin.

```css
.p(@p: 10px) {
	& when ( isnumber(@p) ) {
		padding: @p;
	}
}
```

**padding-top**

```css
.pt(@p: 10px) {
	& when ( isnumber(@p) ) {
		padding-top: @p;
	}
}
```

**padding-right**

```css
.pr(@p: 10px) {
	& when ( isnumber(@p) ) {
		padding-right: @p;
	}
}
```

**padding-bottom**

```css
.pb(@p: 10px) {
	& when ( isnumber(@p) ) {
		padding-bottom: @p;
	}
}
```

**padding-left**

```css
.pl(@p: 10px) {
	& when ( isnumber(@p) ) {
		padding-left: @p;
	}
}
```

## Margin

`@m` must be a number **with any unit type**. This will fail if it's not.

**margin**

You can pass 1–4 values into this mixin.

```css
.m(@m: 10px) {
	& when ( isnumber(@m) ) {
		margin: @m;
	}
}
```

**margin-top**

```css
.mt(@m: 10px) {
	& when ( isnumber(@m) ) {
		margin-top: @m;
	}
}
```

**margin-right**

```css
.mr(@m: 10px) {
	& when ( isnumber(@m) ) {
		margin-right: @m;
	}
}
```

**margin-bottom**

```css
.mb(@m: 10px) {
	& when ( isnumber(@m) ) {
		margin-bottom: @m;
	}
}
```

**margin-left**

```css
.ml(@m: 10px) {
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

`@fz` must be a number **with no unit type**. This will fail if it's not.

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

`@lh` must be a number **with no unit type**. This will fail if it's not.

```css
.lh(@lh: 1) {
	& when ( isnumber(@lh ) {
		line-height: @lh;
	}
}
```

## Color

`@c` must be a color **of any type: hex, rgb, rgba, or hsla**. This will fail if it's not.

```css
.c(@c: @colorS1) {
	& when ( iscolor(@c) ) {
		color: @c
	}
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

`@bgc` must be a color **of any type: hex, rgb, rgba, or hsla**. This will fail if it's not.

```css
.bgc(@bgc: #000) {
	& when ( iscolor(@bgc) ) {
		background-color: @bgc;
	}
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
	background-size: @bgsz;
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

`@bdw` must be a number **with no type**. This will fail if it's not.

```css
.bdw(@bdw: 1px) {
	& when ( isnumber(@bdw) ) {
		border-width: unit(@bdw, px);
	}
}
```

**border-radius**

`@bdrs` must be a number **with no type**. This will fail if it's not.

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

`@op` must be a number **with no type**. This will fail if it's not.

```css
.op(@op: 1) {
	& when ( isnumber(@op) ) {
		opacity: unit(@op, );
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