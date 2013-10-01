jQuery-Table-of-Contents
========================

On several occasions I've been asked to generate a table of contents using jQuery. This is my attempt at one size fits all plugin.

Examples
--------
```
$('#TOC').TOC(); // default
$('#TOC').TOC('#content'); // scoped to the content container
$('#TOC').TOC('#content', {nested: false }); // not nested
$('#TOC').TOC('#content', {ignoreContainers: '.navigation, .footer' }); // ignore containers
$('#TOC').TOC('#content', {startLevel: 2, depth: 2}); // h2 and h3 only - method:1
$('#TOC').TOC('#content', {headings: ['h2','h3']}); // h2 and h3 - method:2 -- should trigger nested: 'false'
$('#TOC').TOC('#content', {containerType: 'ol'}); // Use an ordered list
$('#TOC').TOC('#content', {containerType: 'div', itemType: 'span', linkText:'-> %'}); // Use divs, spans and '->'
```
Target any container the table of contents will be appended to any existing content.
```
<div id="TOC"></div>
```
Override JavaScript options with data attributes. 
```
<div id="TOC" data-container-type="" data-depth="2"></div>
```
In this example the depth will be set to 2 and the containerType will use the plugins default value even if a value was set when initialising the plugin.

###Gotchas

If you change the 'headings' option you can target elements other than h1-h6, however this will disable nesting options. See the examples for how to change the selected heading levels and retain the nesting options.
