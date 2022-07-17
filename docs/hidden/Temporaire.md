---
share: true
category: hidden
---
```toml
	[buildPlans.fira-iosevka]
	family = "Fira Iosevka"
	spacing = "normal"
	serifs = "sans"
	no-cv-ss = true
	
	[buildPlans.fira-iosevka.variants]
	inherits = "ss05"
	
	[buildPlans.fira-iosevka.variants.design]
	l = "tailed-serifed"
	paren = "large-contour"
	brace = "straight"
	ampersand = "upper-open"
	ascii-single-quote = "raised-comma"
	ascii-grave = "raised-turn-comma"
	
	[buildPlans.iosevka-custom.ligations]
	inherits = "dlig"
```

```dataview
LIST FROM "20. Compendium"
```
