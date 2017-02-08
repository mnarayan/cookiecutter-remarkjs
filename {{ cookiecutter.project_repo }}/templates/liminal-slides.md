class: center, middle

.title[Liminal]
.subtitle[A Theme for *Remark* by Ole Petter Bang]
&nbsp;
&nbsp;
&nbsp;
&nbsp;
&nbsp;
.author[Jonathan Lilly]
.institution[NorthWest Research Associates, Seattle]
&nbsp;
.coauthor[Sherlock S. Holmes<sup>1</sup>, John H. Watson<sup>2</sup>]
.institution[<sup>1</sup>Baker Street Research, <sup>2</sup>Edinburgh University]
&nbsp;
&nbsp;
.date[January 8, 2016]   
&nbsp;
&nbsp;
&nbsp;
.center[[{download}](http://www.jmlilly.net/liminal.zip)]

.footnote[Created with [{Remark.js}](http://remarkjs.com/) using [{Markdown}](https://daringfireball.net/projects/markdown/) +  [{MathJax}](https://www.mathjax.org/)]

---
class: center
#  How does this work?
--


Remark is a Javascript interpreter for the Markdown language, intended for presentations.  Go to its [{home page}](http://remarkjs.com/) for more details.
--


The [{Markdown}](https://daringfireball.net/projects/markdown/) language itself is a very simple markup language, much easier than writing in LaTeX or HTML.
--


Remark lets you write a presentation in Markdown, and have it rendered live by a browser, with no compilation needed.
--


Thus, you can give a presentation directly from your browser.
--


Liminal is a theme I wrote for Remark that is intended to be suitable for scientific presentations.
--


It is just a little bit of CSS and some Javascript I found elsewhere.
--


Feel free to use and/or modify it.
---
class: left
##  What is Cool About Remark?
1.  I've used Beamer for years.
--

2.  But I find it a bit cumbersome to make new slides, honestly.
--

3.  And one grows tired of having to compile.
--

4.  Plus, you don't get something you can show on the web.
--


###  Okay, tell me more.
1. It's very easy to make a list in Markdown.
1. You don't have to worry about the numbering.
5. (Look at the source to understand what I mean here.)
--


I like that you can just write in a simple way and get something you can show for a presentation and also put on the web.
--


Markdown does take some getting used to.   It assigns meaning to some invisible characters, like two spaces in a row.
--


So if you have spaces at the end of line when you shouldn't, or don't when you should, this can throw off the formatting.  Just a heads up.
--


Probably, if you prefer source (e.g. Beamer) to WYSIWYG (e.g. PowerPoint), you'll find it easy to work with Remark.

---
class: center
#  Show Me a Figure
--

<img style="width:50%"  src="../figures/qqb.png">

Here is a figure.

--


To delay the presentation of an item, like we're doing here, you put a line containing **only** two hypens '--' followed by an empty line.

---
class: center
## Can I Do Animations?

<video preload="auto" width="70%" height="auto"  data-setup="{}" autoplay loop controls><source src="../videos/vortexmovie.mp4" type="video/mp4" /></video>

Yes, those are extremely easy.

---
class: left
##  How About Some Gnarly Equations?

I'm glad you asked.  With a link to the MathJax Javascript library, you can write inline equations  `\(E=mc^2\)`, or full-line equations like:

`$$\Gamma(t)=  \pi \, \Im\left\{ \mathbf{x}_+^H(t) \, \frac{\mathrm{d}}{\mathrm{d} t}\mathbf{x}_+(t)\right\}$$`

You can just write in LaTeX, with minor modifications for specifying in-line or full-line equations.  Also, in Remark, the equations are surrounded by backquotes, as you see in the source.


[{MathJax}](https://www.mathjax.org/) lets you write your equations in other ways; see the documentation for details.


Note that writing equations in MathJax impacts the portability of your talk.  Currently, this template links to a local copy of Remark, but a remote (online) copy of MathJax.  If you want the equations to work when you are offline, you need to copy the entire MathJax project, about 150 Mb.  See the comments at the bottom of this file.


---
class: left
## What is Liminal?

Almost nothing, hence the name.  It is a minimal theme for Remark for scientific presentations.  It is just this file together with the accompanying directory structure.  I added the following:

*  Markup for a title slide
*  Choice of font and a black-and-gray color scheme
*  Markup for references
.cite[See Moriarty (1888) and Adler, Holmes, and Watson (1891)]
*  A fade in/out transition that I found on the web
*  Some comments of things I learned in making it work

In Liminal the text is monochromatic, apart from for the references, to show off your colorful figures.

Curly braces indicate links, like this one to my [{home page}](http://www.jmlilly.net).  I just think it looks cool.  Of course you can change the styling very easily.

I was just going to use this for own work, but several people have asked me about it, so I decided to make the template available.

---
class: middle, center
#  That's All!

To get started, [{download}](http://www.jmlilly.net/liminal.zip) this template.


For more information see the Remark [{web site}](http://remarkjs.com/) or [{wiki}]( https://github.com/gnab/remark/wiki).

Also, we are on the bleeding edge here, so beware of things like cross-browser compatibility.  Don't just assume it is going to look great when you give your talk on another computer&mdash;check first.

Have fun!
