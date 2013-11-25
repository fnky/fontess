# Fontess - A Font Custom Boilerplate

Using Font Custom to generate font icons from SVGs is easy. Making them crisp and eliminate half pixels is hard, therefore a process for each icon will be different.

This is a base boilerplate with documentation from various sources on how to make icons with Font Custom. You might need to refine them after the process for extra eye-candy.

## Dependencies

- [Font Custom](https://github.com/FontCustom/fontcustom/) (Requires Ruby 1.9.2+, FontForge with Python scripting.)

## Getting Started

Using Fontess is very easy:

- Clone the repository `git remote add origin https://github.com/Humanoidism/fontess.git`
- Change your preferred configuration in the `fontcustom.yml` file.
- Create your awesome icons and export the SVGs (read documentation below)
- Use `fontcustom compile` to compile your icons to beautiful fonts.
- Done!

You can also use `fontcustom watch` to watch changes as you design your icons!

## Document & Icon Sizes

A base document size can vary but to keep it simple there are some base sizes that can be used.

**Document Size:** 512x512
**Icon Size:** 256x256

Best practice is to keep the height of the icon at the half of the document size. The width can vary from icon to icon.

## Importing vectors

When Font Custom compiles the font, SVG images gets parsed into a single layer and color. This is necessary for font glyphs. The following tips might be useful in case your SVG doesn't import properly:

- Strokes gets ignored by the compiler. You can convert them to fills.
- Unite/combine your fills.
- Avoid using white filles. All if your fills will have one color after compiling.
- Don't use the evenodd fill-rule

## SVG Gotchas Exporting from Illustrator

When saving SVG from Illustrator, makes sure to use the following properties:

- Set SVG Profile to **SVG Tiny 1.1+**
- Set Fonts > Type setting to **Convert to outline**
- Set Options > Image Location to **Link** and uncheck **Preserve Illustrator Editing Capabilities**


Also make sure that in Advanced Options *(More Options)* that Decimal Places is set to **3** and Encoding is **Unicode (UTF-8)**. Also untick all checkboxes.

**IMPORTANT:** All of your glyphs should be the same height. There's a long explanation for this, but they should vary in width, not height (unless you intend that, but I bet you don't).

## Round Circles in Illustrator

Illustrator handles circles different from other software. If the font icons are malformed you try this quick fix:

- Select the path of a circle.
- Go to **Effect** > **Path** > **Offset Path**
- Apply a **-0.205px** Offset Path Effect.

Make sure your view is in **Pixel Preview** mode (**View** > **Check Pixel Preview**) to get an accurate preview of the result when zooming.

## Credits

- [Icomoon](http://icomoon.io/) has a great documentation on how to optimize icon fonts. You can read the documentation [here](http://icomoon.io/docs.html).
- [James Bryant](http://jamesbryant.com.au/round-circles-in-illustrator/) help to keep perfect circles in Illustrator.
- [Ward Penny at Pivotallabs](http://pivotallabs.com/generate-icon-fonts-automatically-with-fontcustom/) get just the right file format and more SVG quirkness for Font Custom.
- [Font Custom](http://fontcustom.com/) which this boilerplate is made out of, simply a great and very easy tool.
