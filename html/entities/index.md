---
title: 'entities'
compatibility:
  feature: entities
  topic: html
notes:
  - 'Require manual conversion! See https://github.com/webplatform/mediawiki-conversion/issues/24'
readiness: 'Ready to Use'
summary: 'This article looks at the different codes that can be used to represent text characters when there is a need to escape them. Included is a list containing several characters and their codes.'
tags:
  - Markup_Structures
  - HTML
uri: html/entities

---
<p><br/></p>
<h2>Summary</h2>
<p>
This article looks at the different codes that can be used to represent text characters when there is a need to escape them. Included is a list containing several characters and their codes.</p><p><br/></p>
<h2>Common HTML entities used for typography</h2>
<h3>Introduction</h3>
<p>This article looks at the different codes that can be used to represent text characters when there is a need to escape them. There are a number of HTML entities that come in handy when there’s a need for first-rate typesetting. Many of those listed in the table below are useful only when used in foreign language copy (and copy written in specific dialects of English), so context should be taken into account before the choice is made to use them.
</p><p>For the sake of portability, Unicode entity references should be reserved for use in documents certain to be written in the UTF-8 or UTF-16 character sets. In all other cases, the alphanumeric references should be used.
</p>
<h3>HTML Entities Table</h3>
<table class="wikitable"><tr><th>Character(s)
</th>
<th>Literal(s)
</th>
<th>Alphanumeric value(s)
</th>
<th>Unicode value(s)
</th>
<th>Prefer to
</th></tr><tr><th>Cent (currency)
</th>
<td>¢
</td>
<td><code>&amp;cent;</code>
</td>
<td><code>&amp;#162;</code>
</td>
<td><code> </code>
</td></tr><tr><th>Pound (currency)
</th>
<td>£
</td>
<td><code>&amp;pound;</code>
</td>
<td><code>&amp;#163;</code>
</td>
<td><code> </code>
</td></tr><tr><th>Section <sup><a href="#note-sect">1</a></sup></th>
<td>§
</td>
<td><code>&amp;sect;</code>
</td>
<td><code>&amp;#167;</code>
</td>
<td><code> </code>
</td></tr><tr><th>Copyright
</th>
<td>©
</td>
<td><code>&amp;copy;</code>
</td>
<td><code>&amp;#169;</code>
</td>
<td><code>(c)</code>
</td></tr><tr><th>Guillemets <sup><a href="#note-laquo">2</a></sup></th>
<td>« »
</td>
<td><code>&amp;laquo; &amp;raquo;</code>
</td>
<td><code>&amp;#171; &amp;#187;</code>
</td>
<td><code>&amp;quot;</code>
</td></tr><tr><th>Registered trademark
</th>
<td>®
</td>
<td><code>&amp;reg;</code>
</td>
<td><code>&amp;#174;</code>
</td>
<td><code>(R)</code>
</td></tr><tr><th>Degree(s)
</th>
<td>°
</td>
<td><code>&amp;deg;</code>
</td>
<td><code>&amp;#176;</code>
</td>
<td><code> </code>
</td></tr><tr><th>Plus/minus
</th>
<td>±
</td>
<td><code>&amp;plusmn;</code>
</td>
<td><code>&amp;#177;</code>
</td>
<td><code>+/-</code>
</td></tr><tr><th>Pilcrow (paragraph) <sup><a href="#note-para">3</a></sup></th>
<td>¶
</td>
<td><code>&amp;para;</code>
</td>
<td><code>&amp;#182;</code>
</td>
<td><code> </code>
</td></tr><tr><th>Middle dot <sup><a href="#note-middot">4</a></sup></th>
<td>·
</td>
<td><code>&amp;middot;</code>
</td>
<td><code>&amp;#183;</code>
</td>
<td><code> </code>
</td></tr><tr><th>Fractional half <sup><a href="#note-frac12">5</a></sup></th>
<td>½
</td>
<td><code>&amp;frac12;</code>
</td>
<td><code>&amp;#188;</code>
</td>
<td><code>1/2</code>
</td></tr><tr><th>En dash <sup><a href="#note-ndash">6</a>, <a href="#note-linebreak">7</a></sup></th>
<td>–
</td>
<td><code>&amp;ndash;</code>
</td>
<td><code>&amp;#8211;</code>
</td>
<td><code>-</code> for ranges
</td></tr><tr><th>Em (long) dash <sup><a href="#note-linebreak">7</a>, <a href="#note-mdash">8</a></sup></th>
<td>—
</td>
<td><code>&amp;mdash;</code>
</td>
<td><code>&amp;#8212;</code>
</td>
<td><code>-</code> enclosed by spaces, or <code>--</code>
</td></tr><tr><th>Single quotes <sup><a href="#note-smart_quotes">9</a>, <a href="#note-rsquo">10</a></sup></th>
<td>‘ ’
</td>
<td><code>&amp;lsquo; &amp;rsquo;</code>
</td>
<td><code>&amp;#8216; &amp;#8217;</code>
</td>
<td><code>'</code> or <code>&amp;apos;</code>
</td></tr><tr><th>Single low quote <sup><a href="#note-low_quotes">11</a></sup></th>
<td>‚
</td>
<td><code>&amp;sbquo;</code>
</td>
<td><code>&amp;#8218;</code>
</td>
<td><code>'</code> or comma
</td></tr><tr><th>Double quotes <sup><a href="#note-smart_quotes">9</a></sup></th>
<td>“ ”
</td>
<td><code>&amp;ldquo; &amp;rdquo;</code>
</td>
<td><code>&amp;#8220; &amp;#8221;</code>
</td>
<td><code>", &amp;quot;</code>, <code><i/></code>, or <code>``</code>
</td></tr><tr><th>Double low quote <sup><a href="#note-low_quotes">11</a></sup></th>
<td>„
</td>
<td><code>&amp;bdquo;</code>
</td>
<td><code>&amp;#8222;</code>
</td>
<td><code>&amp;quot;</code> or <code>,,</code>
</td></tr><tr><th>Single &amp; double daggers
</th>
<td>† ‡
</td>
<td><code>&amp;dagger; &amp;Dagger;</code>
</td>
<td><code>&amp;#8224; &amp;#8225;</code>
</td>
<td><code>*</code> and <code>**</code>
</td></tr><tr><th>Bullet
</th>
<td>•
</td>
<td><code>&amp;bull;</code>
</td>
<td><code>&amp;#8226;</code>
</td>
<td><code>*</code>
</td></tr><tr><th>Ellipsis <sup><a href="#note-hellip">12</a></sup></th>
<td>…
</td>
<td><code>&amp;hellip;</code>
</td>
<td><code>&amp;#8230;</code>
</td>
<td><code>...</code>
</td></tr><tr><th>Prime &amp; double prime <sup><a href="#note-prime">13</a></sup></th>
<td>′ ″
</td>
<td><code>&amp;prime; &amp;Prime;</code>
</td>
<td><code>&amp;#8242; &amp;#8243;</code>
</td>
<td><code>'</code>, <code><i/></code>, <code>&amp;apos;</code>, <code>&amp;quot;</code>, <code>minutes:seconds</code> elapsed
</td></tr><tr><th>Euro sign
</th>
<td>€
</td>
<td><code>&amp;euro;</code>
</td>
<td><code>&amp;#8364;</code>
</td>
<td><code> </code>
</td></tr><tr><th>Trademark
</th>
<td>™
</td>
<td><code>&amp;trade;</code>
</td>
<td><code>&amp;#8482;</code>
</td>
<td><code>(tm)</code>
</td></tr><tr><th>Almost equal to
</th>
<td>≈
</td>
<td><code>&amp;asymp;</code>
</td>
<td><code>&amp;#8776;</code>
</td>
<td><code>~</code>
</td></tr><tr><th>Not equal to
</th>
<td>≠
</td>
<td><code>&amp;ne;</code>
</td>
<td><code>&amp;#8800;</code>
</td>
<td><code>!=</code>
</td></tr><tr><th>Less/greater than or equal to  
</th>
<td>≤ ≥
</td>
<td><code>&amp;le; &amp;ge;</code>
</td>
<td><code>&amp;#8804; &amp;#8805;</code>
</td>
<td><code>&lt;= or &gt;=</code>
</td></tr><tr><th>Less/greater than
</th>
<td>&lt; &gt;
</td>
<td><code>&amp;lt; &amp;gt;</code>
</td>
<td><code>&amp;#060; &amp;#062;</code>
</td>
<td>
</td></tr></table><p><b>Table 1:</b> HTML entities useful for proper typesetting, listed in order by decimal Unicode position.
</p>
<h3>HTML entity usage notes</h3>
<ol><li> <span id="note-sect">Citations of statute law, e.g., “29 USC § 794 (d),” are the matter most likely to reference this character.</span></li>
<li> <span id="note-laquo">Guillemets often enclose the names of stories, songs, films, public accommodations (e.g., «Rick’s Café Americain»), and popular toponyms in European languages, particularly those of the Romance sub-family. They are also used for quotes in certain European languages (such as French and Norsk); in these situations, you should always use <code>q</code> elements instead.</span></li>
<li> <span id="note-para">The pilcrow, used to mark the beginning of paragraphs that might otherwise be ambiguous, is useful when setting teaser copy. The print distribution of Rolling Stone magazine has often used such an approach. In technical writing, it might also be useful for marking an orphaned first line of a paragraph. ¶ Paragraphs marked with this symbol will most often be assigned a <code>display</code> value of <code>inline</code>, which will be explained in the introduction to the CSS layout model.</span></li>
<li> <span id="note-middot">The middle dot is an anachronistic analogue to the decimal point, still used by some designers to enumerate amounts of decimalized currency.</span></li>
<li> <span id="note-frac12">HTML also provides references to the code positions for one-quarter and three-quarters fractions.</span></li>
<li> <span id="note-ndash">The en dash is used between two quantities or dates to suggest a range, and is indistinguishable from a proper minus sign (<code>&amp;minus;</code>/<code>&amp;#8722;</code>). However, it should always be distinguished from a hyphen (<code>&amp;#45;</code>), which is used to separate the parts of an ad hoc compound word.</span></li>
<li> <span id="note-linebreak">Browsers create soft line breaks after hyphens (see above), but not after en dashes or em dashes.</span></li>
<li> <span id="note-mdash">The exclusive use of the em dash in English is to mark one or both ends of a dependent clause in lieu of parentheses, and to indicate that if spoken aloud the clause should be preceded and followed by uninflected pauses. In several other languages—particularly those of the Slavic sub-family—em dashes indicate dialogue from the beginning of a paragraph. Tradition dictates that this character not be enclosed itself by spaces, but the thoughtful user of markup may wish to do just that in order to avoid an especially ragged line.</span></li>
<li> <span id="note-smart_quotes">These are the members of the automated “Smart Quotes” set of characters incorporated into most popular word processing platforms.  They are often encoded at vendor-specific code positions rather than Unicode or ISO Latin code positions, which can cause problems when they are copied into a Web document.</span></li>
<li> <span id="note-rsquo">The single close quote character is also used in English as the apostrophe.</span></li>
<li> <span id="note-low_quotes">Low quotes are used in several Central and Eastern European langauges in preference to the analogous English opening and closing quote characters.</span></li>
<li> <span id="note-hellip">Since the ellipsis is a single character, the tracking of its constituent glyphs will <i>not</i> be affected by any value set for the <code>letter-spacing</code> or <code>text-align</code> properties.</span></li>
<li> <span id="note-prime">Primes are used to denote minutes (of both time elapsed and arc) and feet as units of measurement; the double prime in its turn denotes seconds and inches. The use of these characters in relation to units of time elapsed has decreased in popularity in recent years, a decrease that correlates strongly with the increased availability of word processing systems (and their common use by non-specialist operators). Many fonts use prime and double prime characters indistinguishable from single and double close quotes, but for reasons of portability these entities should still be used when called for, notwithstanding the characteristics of the intended display face.</span></li></ol>
