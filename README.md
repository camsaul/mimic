# mimic
*[ab]using Unicode to create tragedy*

### Introduction

<img alt="monster" align="right"
     src="https://cloud.githubusercontent.com/assets/1236420/10557120/f1faedfe-746b-11e5-8a7b-671bd3e30691.jpg" />

mimic provokes:
- fun
- frustration
- curiosity
- murderous rage

It's inspired by this terrible idea floating around:

<blockquote class="twitter-tweet" lang="en"><p lang="en" dir="ltr">MT: Replace a semicolon (;) with a greek question mark (;) in your friend&#39;s C# code and watch them pull their hair out over the syntax error</p>&mdash; Peter Ritchie (@peterritchie) <a href="https://twitter.com/peterritchie/status/534011965132120064">November 16, 2014</a></blockquote>
<script async src="//platform.twitter.com/widgets.js" charset="utf-8"></script>

There are many more characters in the Unicode character set that look, to some extent or another, like others – homoglyphs. Mimic substitutes common ASCII characters for obscure homoglyphs.

Fun games to play with mimic:
- Pipe some source code through and see if you can find all of the problems
- Pipe someone else's source code through without telling them
- Be fired, and then killed
 
### Installation

Install from a local directory if you've cloned:

```
pip install -e .
```

Install straight from the repo:

```
pip install git+git://github.com/reinderien/mimic.git
```


### Example usage

Before installation, invoke via `python -m mimic`. After, simply use `mimic`.

```
mimic --list           # Show all of the homoglyphs
mimic --explain=o      # What crazy things can we do with this letter?
mimic --me-harder 100  # Type some lines in and mess with every single char
mimic --reverse        # Undo the mayhem. Boooring.
cat somefile | mimic   # Pipe some source through at 1%

# Turn up the knob and save the results
cat somefile | mimic --me-harder 25 > mimicked

# Or, if your code acts strange, but you have seen this prank before:
cat mimicked | mimic --reverse > fixedfile
diff fixedfile somefile
```

### Results

Observe the mayhem:

<img alt="some bad code"
     src="https://cloud.githubusercontent.com/assets/1236420/10564931/76507da4-7592-11e5-9971-f6a04ad06298.png" />
*"BUT WHY?"*

Or, if you've been mimicked a little harder,

<img alt="some worse code"
     src="https://cloud.githubusercontent.com/assets/1236420/10564914/f7963ae4-7591-11e5-9b45-f123e42b22f4.png" />

### Solutions

*  [vim-troll-stopper](https://github.com/vim-utils/vim-troll-stopper): vim plugin
that alerts you by highlighting "troll" Unicode characters in red.
*  [emacs-unicode-troll-stopper](https://github.com/camsaul/emacs-unicode-troll-stopper) Emacs port of `vim-troll-stopper`.

### Discussion

People have noticed how terrible this is.

[Reddit](https://reddit.com/r/programming/3pcs0c)

[ycombinator](https://news.ycombinator.com/item?id=10437619)

### See also

[Wikipedia: Unicode Equivalence] (https://en.wikipedia.org/wiki/Unicode_equivalence)

[Wikipedia: IDN homograph attack](https://en.wikipedia.org/wiki/IDN_homograph_attack)

[Online homoglyph generator](http://www.irongeek.com/homoglyph-attack-generator.php)
