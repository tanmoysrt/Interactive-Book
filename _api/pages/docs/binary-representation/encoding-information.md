{
  "name": "encoding-information.md",
  "path": "docs/binary-representation/encoding-information.md",
  "relative_path": "docs/binary-representation/encoding-information.md",
  "layout": "circuitverse",
  "title": "Encoding information",
  "nav_order": "l0s003",
  "cvib_level": "basic",
  "parent": "Binary representation",
  "has_children": false,
  "content": "<h1 class=\"no_toc\" id=\"encoding-information\">Encoding information</h1>\n\n<h2 class=\"no_toc text-delta\" id=\"table-of-contents\">Table of contents</h2>\n\n<ol id=\"markdown-toc\">\n  <li><a href=\"#binary-flags\" id=\"markdown-toc-binary-flags\">Binary flags</a></li>\n  <li><a href=\"#representing-a-character\" id=\"markdown-toc-representing-a-character\">Representing a character</a></li>\n</ol>\n\n<h2 id=\"binary-flags\">Binary flags</h2>\n<p>The new Interactive Book  for digital logic design requires you to study <a href=\"https://learn.circuitverse.org/docs/binary.html\">binary </a> and its uses.\nIn computing, a <em>flag</em> is a type of signal usually used to indicate whether something is true or false. To save time and make your program less complicated, you might want to combine these flags and send several pieces of information in one go.</p>\n\n<p>Imagine you wanted to send a message to your friend to indicate which subjects had set homework on a particular day. If it was only one subject, you can just send the name of the subect - e.g. English - but if there is more than one, it gets more complicated. One way to do it is to give each subject a number:</p>\n\n<table>\n  <thead>\n    <tr>\n      <th style=\"text-align: center\">Serial no.</th>\n      <th style=\"text-align: center\">Subject</th>\n    </tr>\n  </thead>\n  <tbody>\n    <tr>\n      <td style=\"text-align: center\">1</td>\n      <td style=\"text-align: center\">English</td>\n    </tr>\n    <tr>\n      <td style=\"text-align: center\">2</td>\n      <td style=\"text-align: center\">Maths</td>\n    </tr>\n    <tr>\n      <td style=\"text-align: center\">4</td>\n      <td style=\"text-align: center\">Science</td>\n    </tr>\n    <tr>\n      <td style=\"text-align: center\">8</td>\n      <td style=\"text-align: center\">Computing</td>\n    </tr>\n    <tr>\n      <td style=\"text-align: center\">16</td>\n      <td style=\"text-align: center\">History</td>\n    </tr>\n    <tr>\n      <td style=\"text-align: center\">32</td>\n      <td style=\"text-align: center\">Geography</td>\n    </tr>\n    <tr>\n      <td style=\"text-align: center\">64</td>\n      <td style=\"text-align: center\">French</td>\n    </tr>\n    <tr>\n      <td style=\"text-align: center\">128</td>\n      <td style=\"text-align: center\">German</td>\n    </tr>\n  </tbody>\n</table>\n\n<p>You can send combinations of subjects by adding together the numbers and sending the total. Try it below:</p>\n\n<div style=\"width: 100%\" align=\"center\">\n    <div style=\"margin: auto; width: 100%\"><div style=\"float: left; width: 200px; margin-right: 20px\"><p>Enter the homework code and click the button.</p>\n        <p>Code:\n            <input style=\"color: #026e57;\" type=\"text\" id=\"homework\" value=\"0\" size=\"3\" maxlength=\"3\" />\n            <input style=\"color: #026e57;\" type=\"button\" value=\"Send!\" onclick=\"decode();\" />\n        </p>\n    </div>\n        <div id=\"subjects\" style=\"width: 160px; height: 210px; border: 1px solid black; padding: 0 0 0 10px; float:left; margin-bottom: 10px;text-align: left;\"></div></div>\n\n    <p style=\"clear: left\"></p>\n</div>\n\n<p>This only works because of the numbers I’ve chosen - it’s a <a href=\"https://learn.circuitverse.org/docs/binary.html\">binary </a> sequence, with each number being one of the <a href=\"https://learn.circuitverse.org/docs/binary.html\">binary </a>column headings. \nThis means that each total can only be made up from one combination of subjects.</p>\n\n<p>If they’d been numbered as 1 = <strong>English</strong>, 2 = <strong>Maths</strong>, 3 = <strong>Science</strong>, 4 = <strong>Computing</strong>, etc., then it wouldn’t work, because a code of 3 could represent English and Maths, or it could be Science on its own. \nTo use this technique in your programming, you need to be familiar with <a href=\"https://learn.circuitverse.org/docs/binary2.html\">bitwise logic </a></p>\n\n<h2 id=\"representing-a-character\">Representing a character</h2>\n\n<p>The computer that you had when you were in the 80s - in common with a lot of personal computers at the time - allowed you to design your own text character.  You could use this in a game - e.g. to make a “space invader” - or you could use the same technique to make your own font.<br />\nI made my own font that looked like my handwriting!</p>\n\n<p>Characters were designed on an 8 x 8 grid, and created using eight numbers from 0-255.  Each number was converted to binary and the resulting pattern of 0s and 1s was used to make a pattern of black and white dots on a single row.</p>\n\n<p><strong>You can design a character in the same way by entering numbers from 0-255 in the boxes to the left of the grid.</strong>  Each number is converted to binary and used to create the pattern of dots.</p>\n\n<style>\n    #values\t\t\t{width: 40px; display: inline-block; vertical-align: top; float: left; margin: 15px 0px 10px 10px}\n    #values input\t{width: 40px; font-size: 16px; margin: 0px 0px 1px 0px; height: 27px; text-align: right}\n    #display\t\t{display: inline-block; width: 240px; vertical-align: top; margin: 0px 20px 10px 0px; float: left}\n    #character\t\t{display: inline-block; width: 310px; float: left}\n    .little\t\t\t{width: 30px; height: 15px; margin: 0px; display: run-in; float:left; font-size: 10px; text-align: center}\n    .pixel\t\t\t{width: 28px; height: 28px; margin: 0px; display: run-in; float:left; border: 1px solid lightgray; background-color: #F0F0F0}\n</style>\n\n<div id=\"character\">\n    <div id=\"values\">\n        <input type=\"text_2\" onkeyup=\"update_display();\" maxlength=\"3\" value=\"0\" />\n        <input type=\"text_2\" onkeyup=\"update_display();\" maxlength=\"3\" value=\"0\" />\n        <input type=\"text_2\" onkeyup=\"update_display();\" maxlength=\"3\" value=\"0\" />\n        <input type=\"text_2\" onkeyup=\"update_display();\" maxlength=\"3\" value=\"0\" />\n        <input type=\"text_2\" onkeyup=\"update_display();\" maxlength=\"3\" value=\"0\" />\n        <input type=\"text_2\" onkeyup=\"update_display();\" maxlength=\"3\" value=\"0\" />\n        <input type=\"text_2\" onkeyup=\"update_display();\" maxlength=\"3\" value=\"0\" />\n        <input type=\"text_2\" onkeyup=\"update_display();\" maxlength=\"3\" value=\"0\" />\n    </div>\n    <div id=\"display\">\n        <div class=\"little\">128</div>\n        <div class=\"little\">64</div>\n        <div class=\"little\">32</div>\n        <div class=\"little\">16</div>\n        <div class=\"little\">8</div>\n        <div class=\"little\">4</div>\n        <div class=\"little\">2</div>\n        <div class=\"little\">1</div>\n\n        <div class=\"pixel\"></div><div class=\"pixel\"></div><div class=\"pixel\"></div><div class=\"pixel\"></div><div class=\"pixel\"></div><div class=\"pixel\"></div><div class=\"pixel\"></div><div class=\"pixel\"></div>\n        <div class=\"pixel\"></div><div class=\"pixel\"></div><div class=\"pixel\"></div><div class=\"pixel\"></div><div class=\"pixel\"></div><div class=\"pixel\"></div><div class=\"pixel\"></div><div class=\"pixel\"></div>\n        <div class=\"pixel\"></div><div class=\"pixel\"></div><div class=\"pixel\"></div><div class=\"pixel\"></div><div class=\"pixel\"></div><div class=\"pixel\"></div><div class=\"pixel\"></div><div class=\"pixel\"></div>\n        <div class=\"pixel\"></div><div class=\"pixel\"></div><div class=\"pixel\"></div><div class=\"pixel\"></div><div class=\"pixel\"></div><div class=\"pixel\"></div><div class=\"pixel\"></div><div class=\"pixel\"></div>\n        <div class=\"pixel\"></div><div class=\"pixel\"></div><div class=\"pixel\"></div><div class=\"pixel\"></div><div class=\"pixel\"></div><div class=\"pixel\"></div><div class=\"pixel\"></div><div class=\"pixel\"></div>\n        <div class=\"pixel\"></div><div class=\"pixel\"></div><div class=\"pixel\"></div><div class=\"pixel\"></div><div class=\"pixel\"></div><div class=\"pixel\"></div><div class=\"pixel\"></div><div class=\"pixel\"></div>\n        <div class=\"pixel\"></div><div class=\"pixel\"></div><div class=\"pixel\"></div><div class=\"pixel\"></div><div class=\"pixel\"></div><div class=\"pixel\"></div><div class=\"pixel\"></div><div class=\"pixel\"></div>\n        <div class=\"pixel\"></div><div class=\"pixel\"></div><div class=\"pixel\"></div><div class=\"pixel\"></div><div class=\"pixel\"></div><div class=\"pixel\"></div><div class=\"pixel\"></div><div class=\"pixel\"></div>\n    </div>\n</div>\n\n<p>You can design a character in the same way by entering numbers from <strong>0-255</strong> in the boxes to the left of the grid.  Each number is converted to binary and used to create the pattern of dots.</p>\n\n<p>Fonts on a modern computer would be made up of a lot more than <strong>64 pixels</strong>, but the principle is the same.</p>\n\n<p>If you can’t see how the numbers are converted into the patterns of black and white blocks, try looking at the page on binary.  If you can see the link between the number and the pattern, then think about how the web page works</p>\n",
  "dir": "/docs/binary-representation/",
  "url": "/docs/binary-representation/encoding-information.html",
  "raw_content": "# Encoding information\n{: .no_toc}\n\n\n## Table of contents\n{: .no_toc .text-delta}\n\n1. TOC\n{:toc}\n\n## Binary flags\nThe new Interactive Book  for digital logic design requires you to study [binary ](https://learn.circuitverse.org/docs/binary.html) and its uses.\nIn computing, a <em>flag</em> is a type of signal usually used to indicate whether something is true or false. To save time and make your program less complicated, you might want to combine these flags and send several pieces of information in one go.\n\nImagine you wanted to send a message to your friend to indicate which subjects had set homework on a particular day. If it was only one subject, you can just send the name of the subect - e.g. English - but if there is more than one, it gets more complicated. One way to do it is to give each subject a number:\n\n| Serial no.      | Subject     |\n|:------------:|:------------:|\n| 1            |     English        | \n| 2            |       Maths      | \n| 4            |      Science       | \n| 8            |         Computing    | \n| 16            |       History     | \n| 32           |      Geography       | \n| 64           |        French     | \n| 128          |       German      | \n\n\nYou can send combinations of subjects by adding together the numbers and sending the total. Try it below:\n\n\n{% include application1.html %}\n\n\nThis only works because of the numbers I've chosen - it's a [binary ](https://learn.circuitverse.org/docs/binary.html) sequence, with each number being one of the [binary ](https://learn.circuitverse.org/docs/binary.html)column headings. \nThis means that each total can only be made up from one combination of subjects.\n\nIf they'd been numbered as 1 = **English**, 2 = **Maths**, 3 = **Science**, 4 = **Computing**, etc., then it wouldn't work, because a code of 3 could represent English and Maths, or it could be Science on its own. \nTo use this technique in your programming, you need to be familiar with [bitwise logic ](https://learn.circuitverse.org/docs/binary2.html)\n\n\n## Representing a character\n\nThe computer that you had when you were in the 80s - in common with a lot of personal computers at the time - allowed you to design your own text character.  You could use this in a game - e.g. to make a \"space invader\" - or you could use the same technique to make your own font.  \nI made my own font that looked like my handwriting!\n\nCharacters were designed on an 8 x 8 grid, and created using eight numbers from 0-255.  Each number was converted to binary and the resulting pattern of 0s and 1s was used to make a pattern of black and white dots on a single row.\n\n**You can design a character in the same way by entering numbers from 0-255 in the boxes to the left of the grid.**  Each number is converted to binary and used to create the pattern of dots.\n\n{% include application2.html %}\n\n\nYou can design a character in the same way by entering numbers from **0-255** in the boxes to the left of the grid.  Each number is converted to binary and used to create the pattern of dots.\n\nFonts on a modern computer would be made up of a lot more than **64 pixels**, but the principle is the same.\n\nIf you can't see how the numbers are converted into the patterns of black and white blocks, try looking at the page on binary.  If you can see the link between the number and the pattern, then think about how the web page works\n",
  "front_matter": {
    "layout": "circuitverse",
    "title": "Encoding information",
    "nav_order": "l0s003",
    "cvib_level": "basic",
    "parent": "Binary representation",
    "has_children": false
  },
  "front_matter_defaults": {
  },
  "http_url": "https://learn.circuitverse.org/docs/binary-representation/encoding-information.html",
  "api_url": "https://learn.circuitverse.org/_api/pages/docs/binary-representation/encoding-information.md"
}