{
  "name": "number-bases.md",
  "path": "docs/binary-representation/number-bases.md",
  "relative_path": "docs/binary-representation/number-bases.md",
  "layout": "circuitverse",
  "title": "Number bases",
  "nav_order": "l0s002",
  "cvib_level": "basic",
  "parent": "Binary representation",
  "has_children": false,
  "content": "<h1 class=\"no_toc\" id=\"other-number-bases\">Other number bases</h1>\n\n<h2 class=\"no_toc text-delta\" id=\"table-of-contents\">Table of contents</h2>\n\n<ol id=\"markdown-toc\">\n  <li><a href=\"#introduction\" id=\"markdown-toc-introduction\">Introduction</a></li>\n  <li><a href=\"#octal-number-system\" id=\"markdown-toc-octal-number-system\">Octal Number System</a></li>\n  <li><a href=\"#hexadecimal-number-system\" id=\"markdown-toc-hexadecimal-number-system\">Hexadecimal Number System</a></li>\n  <li><a href=\"#converting-between-bases\" id=\"markdown-toc-converting-between-bases\">Converting between bases</a>    <ol>\n      <li><a href=\"#octal-to-decimal-conversion\" id=\"markdown-toc-octal-to-decimal-conversion\">Octal to Decimal conversion</a></li>\n      <li><a href=\"#decimal-to-octal-conversion\" id=\"markdown-toc-decimal-to-octal-conversion\">Decimal to Octal conversion</a></li>\n      <li><a href=\"#hexadecimal-to-decimal-conversion\" id=\"markdown-toc-hexadecimal-to-decimal-conversion\">Hexadecimal to Decimal conversion</a></li>\n      <li><a href=\"#decimal-to-hexadecimal-conversion\" id=\"markdown-toc-decimal-to-hexadecimal-conversion\">Decimal to Hexadecimal conversion</a></li>\n    </ol>\n  </li>\n</ol>\n\n<h2 id=\"introduction\">Introduction</h2>\n\n<ul>\n  <li>Before, learning about other number bases let first understand what is <strong>Number Systems</strong>. It is a writing system used for expressing numbers. We can express number in various ways, but most commonly used systems are Binary Number System, Decimal Number System, Octal Number System and Hexadecimal Number System.</li>\n  <li>Now let’s have brief information about <strong>Number Bases</strong>. A number Base represents how many number of different digits or combination of digits and alphabets are used to represent a number in a particular Number System.</li>\n  <li><strong>Positional number systems</strong> uses the position of a digit to know the contribution of that particular digit in the number. I guess it might look little difficult to understand, so let’s discuss it using an example of a most popular Positional Number System called as <strong>Decimal System</strong>.</li>\n</ul>\n\n<p>According to Decimal System <code class=\"language-plaintext highlighter-rouge\">123</code> can be represented as <code class=\"language-plaintext highlighter-rouge\">1*100 + 2*10 + 3*1</code>. It shows that as <code class=\"language-plaintext highlighter-rouge\">1</code> is on hundredth place so its contribution in the number will be <code class=\"language-plaintext highlighter-rouge\">1*100=100</code> and so on.</p>\n\n<h2 id=\"octal-number-system\">Octal Number System</h2>\n<p><strong>Octal Number System</strong> has 8 as the base of the number. It uses digits from 0-7</p>\n\n<h2 id=\"hexadecimal-number-system\">Hexadecimal Number System</h2>\n<p><strong>Hexadecimal Number System</strong> has 16 as the base of the number. It uses digits 0, 1, 2, 3, 4, 5, 6, 7, 8, 9, A, B, C, D, E and F</p>\n\n<h2 id=\"converting-between-bases\">Converting between bases</h2>\n\n<h3 id=\"octal-to-decimal-conversion\">Octal to Decimal conversion</h3>\n<ul>\n  <li><strong>STEP 1:</strong> Write the decimal value of each digit on top of them respectively. The value which you seek to write is 8<sup>(place value from right)</sup> beginning from 0 i.e., 8<sup>0</sup>, 8<sup>1</sup>, 8<sup>8</sup> …. continuing up to 8<sup>7</sup>.</li>\n  <li><strong>STEP 2:</strong> Now, multiply each digit of octal number with its value.</li>\n  <li><strong>STEP 3:</strong> Add ‘em all.</li>\n  <li><strong>STEP 4:</strong> Result is ready :)</li>\n</ul>\n\n<h3 id=\"decimal-to-octal-conversion\">Decimal to Octal conversion</h3>\n<ul>\n  <li><strong>STEP 1:</strong> Divide the decimal number by 8</li>\n  <li><strong>STEP 2:</strong> At each step store the value of remainder in reverse order.</li>\n  <li><strong>STEP 3:</strong> Result is ready :)</li>\n</ul>\n\n<h3 id=\"hexadecimal-to-decimal-conversion\">Hexadecimal to Decimal conversion</h3>\n<ul>\n  <li><strong>STEP 1:</strong> Write the decimal value of each digit on top of them respectively. The value which you seek to write is 16<sup>(place value from right)</sup> beginning from 0 i.e., 16<sup>0</sup>, 16<sup>1</sup>, 16<sup>8</sup> …. continuing up to 16<sup>7</sup>.</li>\n  <li><strong>STEP 2:</strong> Now, multiply each digit of octal number with its value.</li>\n  <li><strong>STEP 3:</strong> Add ‘em all.</li>\n  <li><strong>STEP 4:</strong> Result is ready :)</li>\n</ul>\n\n<h3 id=\"decimal-to-hexadecimal-conversion\">Decimal to Hexadecimal conversion</h3>\n<ul>\n  <li><strong>STEP 1:</strong> Divide the decimal number by 16</li>\n  <li><strong>STEP 2:</strong> At each step store the value of remainder in reverse order (If the remainder is greater than 9 represent it using alphabet from the hex table For e.g., Use A if the remainder is 10).</li>\n  <li><strong>STEP 3:</strong> Result is ready :)</li>\n</ul>\n\n<p><strong><em>Note: Once you get the number in decimal form, you can convert decimal format into binary as shown before.</em></strong></p>\n",
  "dir": "/docs/binary-representation/",
  "url": "/docs/binary-representation/number-bases.html",
  "raw_content": "# Other number bases\n{: .no_toc}\n\n## Table of contents\n{: .no_toc .text-delta}\n\n1. TOC\n{:toc}\n\n## Introduction\n\n- Before, learning about other number bases let first understand what is **Number Systems**. It is a writing system used for expressing numbers. We can express number in various ways, but most commonly used systems are Binary Number System, Decimal Number System, Octal Number System and Hexadecimal Number System. \n- Now let's have brief information about **Number Bases**. A number Base represents how many number of different digits or combination of digits and alphabets are used to represent a number in a particular Number System. \n-  **Positional number systems** uses the position of a digit to know the contribution of that particular digit in the number. I guess it might look little difficult to understand, so let's discuss it using an example of a most popular Positional Number System called as **Decimal System**.\n\nAccording to Decimal System `123` can be represented as `1*100 + 2*10 + 3*1`. It shows that as `1` is on hundredth place so its contribution in the number will be `1*100=100` and so on. \n\n## Octal Number System\n**Octal Number System** has 8 as the base of the number. It uses digits from 0-7  \n\n## Hexadecimal Number System\n**Hexadecimal Number System** has 16 as the base of the number. It uses digits 0, 1, 2, 3, 4, 5, 6, 7, 8, 9, A, B, C, D, E and F \n\n## Converting between bases\n\n### Octal to Decimal conversion\n-   **STEP 1:** Write the decimal value of each digit on top of them respectively. The value which you seek to write is 8<sup>(place value from right)</sup> beginning from 0 i.e., 8<sup>0</sup>, 8<sup>1</sup>, 8<sup>8</sup> &#x2026;. continuing up to 8<sup>7</sup>.\n-   **STEP 2:** Now, multiply each digit of octal number with its value.\n-   **STEP 3:** Add 'em all.\n-   **STEP 4:** Result is ready :)\n\n### Decimal to Octal conversion\n-   **STEP 1:** Divide the decimal number by 8\n-   **STEP 2:** At each step store the value of remainder in reverse order.\n-   **STEP 3:** Result is ready :)\n\n### Hexadecimal to Decimal conversion\n-   **STEP 1:** Write the decimal value of each digit on top of them respectively. The value which you seek to write is 16<sup>(place value from right)</sup> beginning from 0 i.e., 16<sup>0</sup>, 16<sup>1</sup>, 16<sup>8</sup> &#x2026;. continuing up to 16<sup>7</sup>.\n-   **STEP 2:** Now, multiply each digit of octal number with its value.\n-   **STEP 3:** Add 'em all.\n-   **STEP 4:** Result is ready :)\n\n### Decimal to Hexadecimal conversion\n-   **STEP 1:** Divide the decimal number by 16\n-   **STEP 2:** At each step store the value of remainder in reverse order (If the remainder is greater than 9 represent it using alphabet from the hex table For e.g., Use A if the remainder is 10).\n-   **STEP 3:** Result is ready :)\n\n***Note: Once you get the number in decimal form, you can convert decimal format into binary as shown before.***\n",
  "front_matter": {
    "layout": "circuitverse",
    "title": "Number bases",
    "nav_order": "l0s002",
    "cvib_level": "basic",
    "parent": "Binary representation",
    "has_children": false
  },
  "front_matter_defaults": {
  },
  "http_url": "https://learn.circuitverse.org/docs/binary-representation/number-bases.html",
  "api_url": "https://learn.circuitverse.org/_api/pages/docs/binary-representation/number-bases.md"
}