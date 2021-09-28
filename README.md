# DS-Token
Design Token for TISCO Design system v2.0

## Install
### 1. Install dependencies
``` Bash
From within the terminal cd your project folder.
run npm i ds-token --save to install the dependencies.

```
### 2. Import TISCO DS Token in project
``` Bash
@import 'ds-token/tisco-scss/helper-functions';
@import 'ds-token/tisco-scss/core-functions';
@import 'ds-token/tisco-scss/token';

```
### 3. Structure Token
Token Type | Token Name | Token Properties | Token variable
------------ | ------------- | ------------- | -------------
colors | Base | White | $color_token

#### Example token
```
$color_token: deep-map-merge(
	(
		'colors': (
			'Base': (
				'White': #ffffff,
				'Black': #181818,
				'Text': #2d2d2d,
				'Primary-brand': #1369b0,
				'Secondary-brand': #68b1ee,
				'Muted-Background': #f4f4f4,
				'Mute-Color': #dcdcdc,
				'Grey-Color': #ababab,
				'Dark-Grey-Color': #575F6E,				
			)			
		)
	),
	$token,
	true
);
```

### 4. Add token value in scss variable
``` Bash
token('colors.Base.White', $color_token); - Color Token
token('shadows.Dropshadow.step1', $shadows_token); - Shadows Token
token('fontFamilies.font-tisco-ad', $font_token); - Tisco-AD Font Family Token
token('fontFamilies.font-tisco-text', $font_token); - Tisco-Text Font Family Token
token('fontSizes.helperFooterNote', $font_token); - Font size Token
token('lineHeight.calculator', $font_token); - Line height Token
token('radius.small',$radius_token); - Radius Token small and medium
token('space.S',$space-token); - Spacing Token S M L XL XXL 
```
#### Emaple token
``` Bash
$White : token('colors.Base.White', $color_token);
$Black : token('colors.Base.Black', $color_token);
$Text  : token('colors.Base.Text', $color_token);
