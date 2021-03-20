# MinifyingJSCode
samples on how to minify js code by simple compression and adopted lempel-ziv-method 

[runnable demo of the minified half pong game](https://codepen.io/mahagugu/pen/YzpRNWL)

## description of files

* __hpong.html__ original half pong game (playable)
* __hpong.js__ manually minified by using unicode characters and a lexicon
* __compression.html__ contains js code which minifies the game using a modified lempel-ziv-method
* __upong.js__ minified game by using the modified lempel-ziv compressions

## modified lempel ziv 

just looks for already appearing three to five character sequence and codes the reference to it as a unicode character. the index to the sequence is multiplied by 4 (to store the sequence length) then the sequence length minus 3 is added and then the whole thing is converted to a unicode character with __String.fromCharCode__
