
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

###The Basics of a Website
+ **Servers:** Boxes in a faraway warehouse that host the data for your website and respond to requests from users. (i.e. Amazon S3)
+ **Web application frameworks:** Receive the request to access the website from the user and generate the HTML webpage. Basically, it does all the hard work.
    + Django (Python)
    + Ruby on Rails

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

**The DOM:** The HTML parsed by a browser and turned into a website. Here's a [longer explanation](https://css-tricks.com/dom/).

##Let's inspect the DOM

In a Chrome browser, highlight "Hello World!", right-click and choose "Inspect element" to open your browser development tools.
You can also go to "View > Developer > Developer Tools" or use the keyboard shortcut "alt+command+i" (⌥⌘I)

Click on the tab "Elements," if it isn't already selected. Look, it's your HTML! Except, it's a bit different, because this is the DOM. It's how the browser READ your HTML. 

You can interact with your website through the DOM. For example, let's change the color of "Hello World!" &mdash; Click on the h1 element. To the right, you'll see the styles the brower has already applied. Under element.style {} add the text "color: blue;" and check out your page, now "Hello World!" is blue.

**The Console:** A place to test the interactive parts of your website by interacting directly with the DOM. [A longer explanation](https://developer.chrome.com/devtools/docs/console)

Click on the tab "Console" in your open Developer Tools window. ("View > Developer > JavaScript Console"). Type the following, then hit enter:

  console.log("Hello World");

See how the words are printed out? 

**console.log();** &mdash; A debugging tool that let's you see what your code is doing. Here's a [good explanation](http://stackoverflow.com/questions/4539253/what-is-console-log) of console.log(). It also explains how to access the console in a variety of browsers and web platforms, not just Chrome.

You should use console.log() **ALL THE TIME**. Especially when you first start coding, you should use console.log() on nearly every line to double-check that your code is functioning as you expect. 

An annoying lil secret: console.log() often breaks Internet Explorer. Remember to delete any console.log() left in your script before you deploy your website.
