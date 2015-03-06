
#Teach Yourself to Code!
##beccca aaronson
*[baaronson@texastribune.org](http://mailto:baaronson@texastribune.org)*
*[@becca_aa](https://twitter.com/becca_aa)*
*Github: [brickaa](https://github.com/brickaa)

###Goal: To give you enough tools in *one hour* to teach yourself how to code. 

It will actually take months, even years, to get good at these things. So start small, stay patient and keep pushing yourself to learn new things.

+ [Links to all the best tutorials](http://teachyourselftocode.com/)
+ [Top 10 Ways to Teach Yourself to Code](http://lifehacker.com/top-10-ways-to-teach-yourself-to-code-1684250889)
+ [Which programming language should I learn first?](http://lifehacker.com/which-programming-language-should-i-learn-first-1477153665)
+ Learn how to use Github in [15 minutes](https://try.github.io/levels/1/challenges/1)

###Things to Install

+ XCode (for Macs)
+ Homebrew (makes it easier to install things from the command line)
+ Sublime Text

###The Basics
+ **HTML:** The structure of your website
+ **CSS:** The visual styles (CSS ="Cascading style sheet")
+ **Javascript:** The interactive functionality

    <!DOCTYPE html>
        <html>
          <head>
            <title>Name of your website</title>
    
            <!-- Load stylesheet -->
            <link rel="stylesheet" type="text/css" href="/path-to-your-stylesheet/main.css">
          </head>
    
          <body>
            <h1>Hello world!</h1>
    
            <!-- Load script -->
            <script type="text/javascript" src="/path-to-your-script-code/main.js"></script>
    
          </body>
        </html>  

###Web Frameworks
For large websites, web frameworks do the heavy lifting &mdash; like send/receive user requests to a database.

+ Python / [Django](https://www.djangoproject.com/)
+ Ruby / [Ruby on Rails](http://rubyonrails.org/)

###Front-end Frameworks
Front-end frameworks are also a great place to find example code, because they're built to be reusable and adaptable. 

+ [Bootstrap](http://getbootstrap.com/)
+ [Foundation](http://foundation.zurb.com/)
+ [Bourbon](http://bourbon.io/)

**The DOM:** The HTML parsed by a browser and turned into a website. Here's a [longer explanation](https://css-tricks.com/dom/).

##Let's inspect the DOM

In a Chrome browser, open <a href="/examples/basic-web-structure-comments.html" target="_blank">basic-web-structure-comments.html</a>. Highlight "Hello World!", right-click and choose "Inspect element" to open your browser development tools.

You can also go to "View > Developer > Developer Tools" or use the keyboard shortcut "alt+command+i" (⌥⌘I)  

Click on the tab "Elements," if it isn't already selected. Look, it's your HTML! Except, it's a bit different, because this is the DOM. This is how the browser READ your HTML. 

##Interact with the DOM

You can interact with ANY website through the DOM. For example, let's change the color of "Hello World!" &mdash; Click on the h1 element. To the right, you'll see the styles the brower has already applied. Under element.style {} add the text "color: blue;" and check out your page, now "Hello World!" is blue. 

OK, now go to your favorite website, or [this](http://www.theatlantic.com/photo/2015/03/a-visit-to-aoshima-a-cat-island-in-japan/386647/) website, open the browser development tools and look around.

(Here's a [video tutorial](https://www.youtube.com/watch?v=FQKvro1Wz-E) if you're reading this online.)

###Try this:

+ Change the color of any element. 
+ Find a color block within the styles of an element. Click the square, and look, an eyedropper! Use that eyedropper to select a color on the page and get the hex code.
+ Find an element that changes on hover (like a button). Right-click that element in the dev inspector window, and click "Force Element State" > : hover. Look what happens to the styles.
+ Delete all the elements in the DOM. All of them. JK, delete one or two.
+ Now move things around. Whoa.

###Device testing

Chrome and Firefox both have tools to test what your website will look like on various devices. In Chrome, click the button in the top left of the "Development Tools" window that looks like a tablet. Select the type of device you want to test, and reload. This can't completely replace actual device testing, but it helps you see how your design looks on various screen sizes.

**The Console:** A place to test the interactive parts of your website by interacting directly with the DOM. [A longer explanation](https://developer.chrome.com/devtools/docs/console)

Click on the tab "Console" in your open Developer Tools window. ("View > Developer > JavaScript Console"). Type the following, then hit enter:

  console.log("Hello World");

See how the words are printed out? 

**console.log();** &mdash; A debugging tool that let's you see what your code is doing. Here's a [good explanation](http://stackoverflow.com/questions/4539253/what-is-console-log) of console.log(). It also explains how to access the console in a variety of browsers and web platforms, not just Chrome.

You should use console.log() **ALL THE TIME**. Especially when you first start coding, you should use console.log() on nearly every line to double-check that your code is functioning as you expect. 

An annoying lil secret: console.log() often breaks Internet Explorer. Remember to delete any console.log() left in your script before you deploy your website.

##Google Charts

Google charts has many wonderful [code examples](https://developers.google.com/chart/interactive/docs/gallery/barchart), and step-by-step instructions on how to change up the code to make it work for you.

##Let's code something together

Open [examples/index.html](examples/index.html). We're going to use Google Charts to build a pie chart. 

Go [here](https://developers.google.com/chart/interactive/docs/basic_load_libs) and copy/paste that first block of code into index.html

###Don't be afraid of the Terminal!

If you're scared of the big black box, make it pretty. Go to Terminal > Preferences > Profiles and change the color scheme. You can import new color schemes, like [this](http://ethanschoonover.com/solarized).  

###Proof the terminal isn't scary

Type the following into your terminal. (If you haven't downloaded XCode, it won't work.)
<pre><code>
python
</code></pre>

Congrats, you've connected the python library.

Now type (>>> is already there, you don't type that part):
<pre><code>
>>> print "Hello world!"
</code></pre>

Ok, so what if you pull down an example from GitHub, open the page in your browser and it doesn't work? The project probably needs a server to compile the styles, scripts, and other components. 

In your console, type:
<pre><code>python -m SimpleHTTPServer 8000</code></pre>

Now, open your browser to localhost:8000. You'll see your webpage, hosted from a server on your local computer. 