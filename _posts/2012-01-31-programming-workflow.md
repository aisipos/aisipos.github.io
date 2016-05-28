---
id: 37
title: Programming Workflow
date: 2012-01-31T23:01:44+00:00
author: admin
layout: post
guid: http://www.softwarefuturism.org/?p=37
permalink: /2012/programming-workflow
categories:
  - Essays
---
Programmers are much enamored with their programming languages. Some so much so that it often defines what programmers are; you may hear &#8220;I am a Java programmer&#8221;, for instance. This runs deeper than we think. Often without realizing it, we are tied not only to the language but also its implementation. The implementation, rather than the language itself, imposes a workflow on how we write programs in the language, one that we usually do not see beyond.

For some time now, the most popular workflow of mainstream languages has been the familiar &#8220;edit, compile, run&#8221; (ECR) cycle. It has become so ingrained in many of us that we have forgotten other workflows, or worse never learned that any others exist. It was not always so. Popular languages of the past and present have included a different workflow, the &#8220;read, eval, print loop&#8221; (REPL). For myself, my first programming language was BASIC. My first programming prompt was a REPL.

Often when judging the merits of a language, we focus on the features of the language itself, rather than its implementation and workflows. This is dangerous, since the features of the language are only a part of what makes a programmer productive. The workflow of how you interact with a language is as much important as the language itself. Since many of us are used to only one workflow, more often than not that venerable &#8220;edit, compile, run&#8221; cycle, we have stopped looking for innovation in how we interact with programming languages.

With ECR, everything is a **program**. In order to get the computer to do something, you must edit a whole program (whether new or a modified old one), compile it, run it, rinse, lather, and repeat. This is a lot of effort for tasks that are very small. This is also a lot of effort when you need to experiment or tweak with small bits of code. Sometimes you only want to know the output of one function for one input. Sometimes you just need to get the base64 encoding of a string.

A REPL allows you to interact with the language one **statement** at a time. You can interact out of nothing, if you are just getting started on an idea, or you can interact with an existing program, one statement at a time. Feedback is usually instant. Writing a program with a REPL still means writing a program. But if you need something done that only requires one statement, then one statement is all you need. You cannot use just one statement with ECR. Small tasks become difficult with ECR, causing them more often than not to be skipped.

REPLs by their nature are interpreters. Because of this, they are typically only provided with interpreted languages. But interpretation versus compilation is merely an implementation detail. All languages can in theory be interpreted. Thus all languages could in principle offer a REPL. REPLs having a long tradition, heralding back to LISP and BASIC, both old languages. But with the rise of compiled languages, primarily C, C++, and Java, the REPL was largely forgotten by a generation of programmers. The &#8220;dynamic languages&#8221; such as Perl, Python, Ruby, and Javascript have brought a resurgence of the REPL, but not all programmers have explored the dynamic language world.

There&#8217;s no reason to not ship a REPL with modern compiled languages such as C# or Java. Mono in fact ships [C# REPL](http://www.mono-project.com/CsharpRepl), and [BeanShell](http://www.beanshell.org/) exists for Java. But merely providing a REPL is no guarantee that the masses will use it. Long exposure to the ECR for a generation of programmers has lulled us to sleep. Programmers used to the ECR in compiled languages are often amazed at REPL demos in their favorite language [<sup>1</sup>](#note-37-1 "http://blog.jonudell.net/2007/09/27/first-look-at-resolver-an-ironpython-based-spreadsheet/"), but immediately go back to ingrained habits. We are too enamored with our tools, and the mindsets they put us into.

The natural question that a Software Futurist might ask is, is there anything available more advanced than the REPL? The answer is yes. There is a slight variant of the REPL, the &#8220;notebook&#8221; interface. A notebook interface allows you to go back in your command history to change a statement and see the changed output. The REPL was designed in the days of teletypes- think of the REPL as like a long fixed interaction with the computer printed on paper. The Notebook interface allows you to go back to any point and make changes. While this seems like a minor advance, it really does make iterative development easier. Notebooks have long been a staple of mathematical systems, like Mathematica, but has been working its way into other languages like Python. 

While the notebook has advantes over a REPL, it is not a fundamental shift. For that, as we often do we have to look to the past rather than the future &#8211; Smalltalk.

Smalltalk implementations offer what is called &#8220;the **Image**&#8220;. It is a fundamentally different paradigm than ECR or the REPL. With the Image, you start a running instance of a complete environment. The Image contains the live objects of your program, as well as the development environment. You make changes to these live objects, or make new live objects, interactively with the development environment. This can be done textually, or graphically depending on what tools you choose to use and what is available at the time. Think of it as &#8220;sculpting&#8221; a collection of live objects. Once the live objects have reached a point you consider ready, you can freeze the Image, copy it and deploy it wherever you like. In Smalltalk, you work primarily with objects, rather than primarily with text.

So far as I know, this interaction paradigm is unique to smalltalk. Dan Ingalls, one of the creators of Smalltalk, has attempted to bring it to the Javascript language in a project called the <a href="http://www.lively-kernel.org/" title="Lively Kernel" target="_blank">Lively Kernel</a>. It is a laudable effort, but sadly few seem to be paying attention. Just as we have been lulled to sleep by ECR, the current generation seems to have been lulled to sleep by the REPL.

It remains to be seen if Image based programming is an advance on the REPL. Certainly it is essentially unknown outside the Smalltalk world, itself a fringe language by today&#8217;s standards. It is likely hampered by its all or nothing nature; the entire development environment must be implemented in Smalltalk, inside the Image. Entire ecosystems of supposedly language agnostic tools are thus unable to interact with it &#8211; source control tools, documentation generators, indexers. But as least the Image is a creative idea, one designed after the lessons of both ECR and the REPL. I haven&#8217;t seen such originality in other interaction paradigms. It&#8217;s originality that&#8217;s desperately needed if we are to design tools that will make any real leaps in productivity in the future.

Addendum:
  
<a href="http://worrydream.com" title="Brett Victor" target="_blank">Brett Victor</a> gave a great <a href="http://vimeo.com/36579366" title="talk" target="_blank">talk</a> talk that touched on this at CUSEC 2012. His guiding principle is the requirement of immediate feedback. He rightly points out that the REPL is a recreation of the teletype, a now obsolete relic from the 1970&#8217;s. He gives demonstrations of several javascript programming environments of his own creation, all of which allow you to vary parameters as you edit code and see the results immediately. 

<a href="http://subtextual.org/" title="Subtext" target="_blank">Subtext</a> is another post-REPL environment, where code and data are edited in an environment with immediate feedback. He states in his <a href="http://alarmingdevelopment.org/?p=5" title="manifesto" target="_blank">manifesto</a> &#8220;The language _is_ the IDE&#8221; (emphasis mine)

<div class="simple-footnotes">
  <p class="notes">
    Notes:
  </p>
  
  <ol>
    <li id="note-37-1">
      <a href="http://blog.jonudell.net/2007/09/27/first-look-at-resolver-an-ironpython-based-spreadsheet/" title="http://blog.jonudell.net/2007/09/27/first-look-at-resolver-an-ironpython-based-spreadsheet/">http://blog.jonudell.net/2007/09/27/first-look-at-resolver-an-ironpython-based-spreadsheet/</a> <a href="#return-note-37-1">&#8617;</a>
    </li>
  </ol>
</div>
