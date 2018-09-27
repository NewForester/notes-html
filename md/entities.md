<!DOCTYPE html>
<html>

<head>
    <meta charset="UTF-8" />
    <link rel="stylesheet" href="../styles/style-sheet.css" />
    <style>
        table, th, td {
            border: 1px solid black;
            border-collapse: collapse;
        }
        table {
            border-spacing: 5px;
        }
        th, td {
            padding: 5px;
        }
        th {
            text-align: left;
        }
        caption {
            padding: 20px;
        }
       .symbol {
            text-align: center;
        }
    </style>
</head>

<body>
# HTML5


## HTML Symbols

Mathematical, technical, currency and other symbols that are not present on a normal keyboard
can be added to a HTML document using a character entity name (if one exists) or a decimal or hexadecimal reference.

For a limited number of reserved characters, character entities or numeric references must be used.

There are three forms:

 1. &amp;name;      - easy to remember named character entity
 1. &amp;#nnnn;     - decimal reference
 1. &amp;#xhhhh;    - hexadecimal reference

Entity names are case sensitive.
In HTML5 numeric references are Unicode code points.

For example, to avoid  `<`  being mistaken for an open tag use either of:

```html
    &lt;
    &#60;
```


<hr /><!-- Non-breaking Space -->

The non-breaking space `&nbsp` is a commonly used character entity.

The browser reformats texts, removing redundant white space but it will not remove non-breaking spaces.

The browser will not insert a line break either side of a non-breaking space.
So use a non-breaking space between words that must appear together such as a value and its units
(e.g 100&nbsp;km/h).

Similar to the non-breaking space is the non-breaking hyphen (&amp;#8209;).


<hr /><!-- Useful Character Entities -->

<!--
Some useful character entities:

| Symbol    | Name          | Number      | Description          |
| :----:    | ----          | ------      | -----------          |
| &lt;      | &amp;lt;      | &amp;#60;   | less than            |
| &gt;      | &amp;gt;      | &amp;#62;   | greater than         |
| &amp;     | &amp;amp;     | &amp;#38;   | ampersand            |
| &quot;    | &amp;quot;    | &amp;#34;   | quotes               |
| &apos;    | &amp;apos;    | &amp;#39;   | apostrophe           |
|           | &amp;nbsp;    | &amp;#160;  | non-breaking space   |
| &#8209;   |               | &amp;#8209; | non-breaking hyphen  |
-->

<table width="50%">
<caption>Some Useful Character Entities</caption>
<tr><th class="symbol"> Symbol    </th><th> Name          </th><th> Number      </th><th> Description          </th></tr>
<tr><td class="symbol"> &lt;      </td><td> &amp;lt;      </td><td> &amp;#60;   </td><td> less than            </td></tr>
<tr><td class="symbol"> &gt;      </td><td> &amp;gt;      </td><td> &amp;#62;   </td><td> greater than         </td></tr>
<tr><td class="symbol"> &amp;     </td><td> &amp;amp;     </td><td> &amp;#38;   </td><td> ampersand            </td></tr>
<tr><td class="symbol"> &quot;    </td><td> &amp;quot;    </td><td> &amp;#34;   </td><td> quotes               </td></tr>
<tr><td class="symbol"> &apos;    </td><td> &amp;apos;    </td><td> &amp;#39;   </td><td> apostrophe           </td></tr>
<tr><td class="symbol">           </td><td> &amp;nbsp;    </td><td> &amp;#160;  </td><td> non-breaking space   </td></tr>
<tr><td class="symbol"> &#8209;   </td><td>               </td><td> &amp;#8209; </td><td> non-breaking hyphen  </td></tr>
</table>


<hr /><!-- Diacritical Marks -->

Diacritical marks, sometimes known as glyphs or accents can appear
above, below or inside a letter or even between two letters.

In HTML, diacritical marks can be used in combination with alphanumeric characters
to produce accented characters than might not be present in the character set encoding of the web page.

<!--
| Mark    | Name       |
| :---:   | ----       |
| &#768;  | grave      |
| &#769;  | acute      |
| &#770;  | circumflex |
| &#771;  | tilde      |
-->

<table width="20%">
<tr><th class="symbol"> Mark   </th><th> Name       </th></tr>
<tr><td class="symbol"> &#768; </td><td> grave      </td></tr>
<tr><td class="symbol"> &#769; </td><td> acute      </td></tr>
<tr><td class="symbol"> &#770; </td><td> circumflex </td></tr>
<tr><td class="symbol"> &#771; </td><td> tilde      </td></tr>
</table>

However, with HTML5, the default character set is UTF8 and practically any character may be represented using a Unicode numeric reference.


<hr /><!-- Mathematical Symbols -->

<!--
Some mathematical symbols:

| Symbol    | Name          | Number      | Description          |
| :----:    | ----          | ------      | -----------          |
| &forall;  | &amp;forall;  | &amp;#8704; | for all              |
| &exist;   | &amp;exist;   | &amp;#8707; | there exists         |
| &empty;   | &amp;empty;   | &amp;#8709; | empty set            |
| &isin;    | &amp;isin;    | &amp;#8712; | element of           |
| &prod;    | &amp;prod;    | &amp;#8719; | product              |
| &sum;     | &amp;sum;     | &amp;#8721; | sum                  |
-->

<table width="50%">
<caption>Some Mathematical Symbols</caption>
<tr><th class="symbol"> Symbol    </th><th> Name          </th><th> Number      </th><th> Description          </th></tr>
<tr><td class="symbol"> &forall;  </td><td> &amp;forall;  </td><td> &amp;#8704; </td><td> for all              </td></tr>
<tr><td class="symbol"> &exist;   </td><td> &amp;exist;   </td><td> &amp;#8707; </td><td> there exists         </td></tr>
<tr><td class="symbol"> &empty;   </td><td> &amp;empty;   </td><td> &amp;#8709; </td><td> empty set            </td></tr>
<tr><td class="symbol"> &isin;    </td><td> &amp;isin;    </td><td> &amp;#8712; </td><td> element of           </td></tr>
<tr><td class="symbol"> &prod;    </td><td> &amp;prod;    </td><td> &amp;#8719; </td><td> product              </td></tr>
<tr><td class="symbol"> &sum;     </td><td> &amp;sum;     </td><td> &amp;#8721; </td><td> sum                  </td></tr>
</table>

See the [Maths Reference](http://www.w3schools.com/charsets/ref_utf_math.asp) page.


<hr /><!-- Greek Letters Symbols -->

<!--
Some Greek letters:

| Symbol    | Name          | Number      | Description          |
| :----:    | ----          | ------      | -----------          |
| &alpha;   | &amp;alpha;   | &amp;#945;  | alpha                |
| &beta;    | &amp;beta;    | &amp;#946;  | beta                 |
| &gamma;   | &amp;gamma;   | &amp;#947;  | gamma                |
| &delta;   | &amp;delta;   | &amp;#948;  | delta                |
| &epsilon; | &amp;epsilon; | &amp;#949;  | epsilon              |
| &zeta;    | &amp;zeta;    | &amp;#950;  | zeta                 |
-->

<table width="50%">
<caption>Some Greek Letters</caption>
<tr><th class="symbol"> Symbol    </th><th> Name          </th><th> Number      </th><th> Description          </th></tr>
<tr><td class="symbol"> &alpha;   </td><td> &amp;alpha;   </td><td> &amp;#945;  </td><td> alpha                </td></tr>
<tr><td class="symbol"> &beta;    </td><td> &amp;beta;    </td><td> &amp;#946;  </td><td> beta                 </td></tr>
<tr><td class="symbol"> &gamma;   </td><td> &amp;gamma;   </td><td> &amp;#947;  </td><td> gamma                </td></tr>
<tr><td class="symbol"> &delta;   </td><td> &amp;delta;   </td><td> &amp;#948;  </td><td> delta                </td></tr>
<tr><td class="symbol"> &epsilon; </td><td> &amp;epsilon; </td><td> &amp;#949;  </td><td> epsilon              </td></tr>
<tr><td class="symbol"> &zeta;    </td><td> &amp;zeta;    </td><td> &amp;#950;  </td><td> zeta                 </td></tr>
</table>

<!--
Some Greek capital letters:

| Symbol    | Name          | Number      | Description          |
| :----:    | ----          | ------      | -----------          |
| &Alpha;   | &amp;Alpha;   | &amp;#913;  | capital alpha        |
| &Beta;    | &amp;Beta;    | &amp;#914;  | capital beta         |
| &Gamma;   | &amp;Gamma;   | &amp;#915;  | capital gamma        |
| &Delta;   | &amp;Delta;   | &amp;#916;  | capital delta        |
| &Epsilon; | &amp;Epsilon; | &amp;#917;  | capital epsilon      |
| &Zeta;    | &amp;Zeta;    | &amp;#918;  | capital zeta         |
-->

<table width="50%">
<caption>Some Greek Capital Letters</caption>
<tr><th class="symbol"> Symbol    </th><th> Name          </th><th> Number      </th><th> Description          </th></tr>
<tr><td class="symbol"> &Alpha;   </td><td> &amp;Alpha;   </td><td> &amp;#913;  </td><td> capital alpha        </td></tr>
<tr><td class="symbol"> &Beta;    </td><td> &amp;Beta;    </td><td> &amp;#914;  </td><td> capital beta         </td></tr>
<tr><td class="symbol"> &Gamma;   </td><td> &amp;Gamma;   </td><td> &amp;#915;  </td><td> capital gamma        </td></tr>
<tr><td class="symbol"> &Delta;   </td><td> &amp;Delta;   </td><td> &amp;#916;  </td><td> capital delta        </td></tr>
<tr><td class="symbol"> &Epsilon; </td><td> &amp;Epsilon; </td><td> &amp;#917;  </td><td> capital epsilon      </td></tr>
<tr><td class="symbol"> &Zeta;    </td><td> &amp;Zeta;    </td><td> &amp;#918;  </td><td> capital zeta         </td></tr>
</table>

See the [Greek Reference](http://www.w3schools.com/charsets/ref_utf_greek.asp) page.


<hr /><!-- Currency Symbols -->

<!--
Some currency symbols:

| Symbol    | Name          | Number      | Description          |
| :----:    | ----          | ------      | -----------          |
|     ¢     | &amp;cent;    | &amp;#162;  | cent                 |
|     £     | &amp;pound;   | &amp;#163;  | pound                |
|     ¥     | &amp;yen;     | &amp;#165;  | yen                  |
|     €     | &amp;euro;    | &amp;#8364; | euro                 |
-->

<table width="50%">
<caption>Some Currency Symbols</caption>
<tr><th class="symbol"> Symbol    </th><th> Name          </th><th> Number      </th><th> Description          </th></tr>
<tr><td class="symbol"> ¢         </td><td> &amp;cent;    </td><td> &amp;#162;  </td><td> cent                 </td></tr>
<tr><td class="symbol"> £         </td><td> &amp;pound;   </td><td> &amp;#163;  </td><td> pound                </td></tr>
<tr><td class="symbol"> ¥         </td><td> &amp;yen;     </td><td> &amp;#165;  </td><td> yen                  </td></tr>
<tr><td class="symbol"> €         </td><td> &amp;euro;    </td><td> &amp;#8364; </td><td> euro                 </td></tr>
</table>

See the [Currency Reference](http://www.w3schools.com/charsets/ref_utf_currency.asp) page.


<hr /><!-- Other Symbols -->

<!--
| Symbol    | Name          | Number      | Description          |
| :----:    | ----          | ------      | -----------          |
| &larr;    | &amp;larr;    | &amp;#8592; | left arrow           |
| &uarr;    | &amp;uarr;    | &amp;#8593; | up arrow             |
| &rarr;    | &amp;rarr;    | &amp;#8594; | right arrow          |
| &darr;    | &amp;darr;    | &amp;#8595; | down arrow           |
| &spades;  | &amp;spades;  | &amp;#9824; | spades               |
| &clubs;   | &amp;clubs;   | &amp;#9827; | clubs                |
| &hearts;  | &amp;hearts;  | &amp;#9829; | hearts               |
| &diams;   | &amp;diams;   | &amp;#9830; | diamond              |
|     ©     | &amp;copy;    | &amp;#169;  | copyright            |
|     ®     | &amp;reg;     | &amp;#174;  | registered trademark |
|     ™     | &amp;trade;   | &amp;#8482; | trademark            |
-->

<table width="50%">
<caption>Some Miscellaneous symbols</caption>
<tr><th class="symbol"> Symbol    </th><th> Name          </th><th> Number      </th><th> Description          </th></tr>
<tr><td class="symbol"> &larr;    </td><td> &amp;larr;    </td><td> &amp;#8592; </td><td> left arrow           </td></tr>
<tr><td class="symbol"> &uarr;    </td><td> &amp;uarr;    </td><td> &amp;#8593; </td><td> up arrow             </td></tr>
<tr><td class="symbol"> &rarr;    </td><td> &amp;rarr;    </td><td> &amp;#8594; </td><td> right arrow          </td></tr>
<tr><td class="symbol"> &darr;    </td><td> &amp;darr;    </td><td> &amp;#8595; </td><td> down arrow           </td></tr>
<tr><td class="symbol"> &spades;  </td><td> &amp;spades;  </td><td> &amp;#9824; </td><td> spades               </td></tr>
<tr><td class="symbol"> &clubs;   </td><td> &amp;clubs;   </td><td> &amp;#9827; </td><td> clubs                </td></tr>
<tr><td class="symbol"> &hearts;  </td><td> &amp;hearts;  </td><td> &amp;#9829; </td><td> hearts               </td></tr>
<tr><td class="symbol"> &diams;   </td><td> &amp;diams;   </td><td> &amp;#9830; </td><td> diamond              </td></tr>
<tr><td class="symbol"> ©         </td><td> &amp;copy;    </td><td> &amp;#169;  </td><td> copyright            </td></tr>
<tr><td class="symbol"> ®         </td><td> &amp;reg;     </td><td> &amp;#174;  </td><td> registered trademark </td></tr>
<tr><td class="symbol"> ™         </td><td> &amp;trade;   </td><td> &amp;#8482; </td><td> trademark            </td></tr>
</table>

See the [Arrows Reference](http://www.w3schools.com/charsets/ref_utf_arrows.asp) page.

See the [Symbols Reference](http://www.w3schools.com/charsets/ref_utf_symbols.asp) page.

<hr />

</body>
</html>
