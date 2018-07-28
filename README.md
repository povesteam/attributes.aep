# attributes.aep

Usage instructions for https://videohive.net/item/attributes-logo-reveal/1390173?ref=povesteam

## Change font to use accents, diacritics, and other special characters

To support non-english alphabet, follow these steps:

<ol>
<li>Open the "Wall Builder" composition</li>
<li>Select all layers (CTRL+A or CMD+A)</li>
<li>Open the Character panel (CTRL+6 or CMD+6)
<p><img src="https://github.com/povesteam/attributes.aep/blob/master/composition-and-font.png?raw=true" /></p>
</li>
<li>Change the font to a font that has non-english letters. You can find a lot of fonts supporting non-english characters here: https://www.fontsquirrel.com/fonts/list/language</li>
<li>To change the word splitting to include the non-english characters, open the "Project Settings" composition, select the first layer "Line Above 7" and press E E to reveal all expressions.</li>
<li>Replace this line
<p><code>w = thisComp.layer("Type Words Here").text.sourceText.split(/[^a-z0-9]+/i)</code></p>
with this
<p><code>w = thisComp.layer("Type Words Here").text.sourceText.split(/\s+/i)</code></p>
<p><img src="https://github.com/povesteam/attributes.aep/blob/master/word-split-expression.png?raw=true" /></p>
</li>
<li>Click on "Source Text" under Layer Above 7 and go to Edit -> Copy Expression Only
<p><img src="https://github.com/povesteam/attributes.aep/blob/master/source-text-param.png?raw=true" /></p>
<p><img src="https://github.com/povesteam/attributes.aep/blob/master/copy-expression-only.png?raw=true" /></p>
</li>
<li>Select all layers containing "Line" and choose Edit -> Paste
<p><img src="https://github.com/povesteam/attributes.aep/blob/master/line-layers.png?raw=true" /></p>
</li>
<li>You may need to purge the cache to force re-render all layers
<p><img src="https://github.com/povesteam/attributes.aep/blob/master/purge-all.png?raw=true" /></p>
</li>
<li>Go back to the "Render Me" composition and enjoy
<p><img src="https://github.com/povesteam/attributes.aep/blob/master/render-diacritics.png?raw=true" /></p></li>
</ol>
