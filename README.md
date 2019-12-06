# monthly-planning-files

Text files with [markdown](https://www.markdownguide.org/getting-started/) formatting to help plan &amp; log whatever it is you do. A lo-fi **attention** management system to complement your **task** management system.  

![keanu reeves as ted telling bill 'So after the report we can't forget to do this otherwise it won't happen'](/images/can't-forget.gif)

## recommended tools  

I've been using variations of these monthly planning text files since 2013, always in a text editor that syncs  what's on my phone and my computer. This setup works quite well, since it supplies two important things a paper planner lacks: 1. text tools like "search in project" or batch "find & replace" and 2. the ability to not be left behind in a coffeeshop or bus.  

Put differently, these files blend the basic system of a [bullet journal](https://bulletjournal.com/pages/learn) with all the coolness of [plain text](http://bettermess.com/a-plain-text-primer/) files edited in $yourFavoriteTextEditor. (If you don't already favorite text editor, I'd recommend [Atom](http://atom.io). If you want something more streamlined, on Mac you could try [nvALT](https://brettterpstra.com/projects/nvalt/), the forthcoming [nvULTRA](https://brettterpstra.com/2019/04/10/codename-nvultra/), on PC you could try [ResophNotes](https://www.resoph.com/ResophNotes/Welcome.html), and on Linux you could do just about anything your heart desires, up to and including using [nvPy](https://github.com/cpbotha/nvpy).)  

If you *do* use Atom, I'd recommend installing and using these packages:  
- [Toggle Markdown Task](https://atom.io/packages/toggle-markdown-task), which lets you mark tasks done  
- [markdown-folding](https://atom.io/packages/markdown-folding), which folds lines of text at different heading levels, all of which are marked with one or more `#`. With it, you can fold lines at the week and day level in these files, among others.  
- [language-markdown](https://atom.io/packages/language-markdown), which is an alternative for the built-in `language-gfm` that adds extra things for lists, including a very satisfying greyed-out effect when you've marked a task done by making its `[ ]` box have an `[x]` instead.  
- [wikilink](https://atom.io/packages/wikilink), which lets you link between notes using the name of the `[[target note]]` surrounded by two brackets. That's right: with the package installed, that `[[target note]]` could let you quickly jump to a separate note named `target note`. These files already include this style link for moving between months or years.  
- [Tomatimer](https://atom.io/packages/tomatimer), which puts a lightly configurable [pomodoro timer](https://en.wikipedia.org/wiki/Pomodoro_Technique) into Atom's status bar and reminds you to take occasional breaks. The files have the beginnings of a markdown-formatted table for each day in case you're moved to try the [Pomodoro technique](http://baomee.info/pdf/technique/1.pdf) in detail that day.  

As for the phone side of things… [Editorial](https://omz-software.com/editorial/) is the only iOS editor I know of that will quickly let you move through markdown files by heading. I hope it gets an update soon and/or that this feature begins being common in phone editors, of which there are [more than a few](https://brettterpstra.com/ios-text-editors/).  

## recommended use  

Whatever works for you is what you should do! 

The one thing I'd strongly recommend is to use something that can give you actual reminders to go along with these files. Please consider putting tasks into your calendar as events, using something like [OmniFocus](https://www.omnigroup.com/omnifocus) or [Todoist](https://todoist.com/home), or something else that can reach across time and say ["don't forget to wind your watch"](https://youtu.be/aK1gnNTVxvc?t=168).  

With these files themselves, what works for me is leaving each month's file open in a window while I do related work on my computer. That way I'll occasionally glance over at the file and be reminded of what I've told myself to focus on, which makes it easier to reevaluate whether I should change what I'm doing. If I'm going to be walking around a lot away from my computer, I'll make a little [hipster PDA](http://www.43folders.com/2004/09/03/introducing-the-hipster-pda) out of some scrap paper folded up as a [one-shot zine](https://www.rookiemag.com/2012/05/how-to-make-a-zine/).  

## sounds intriguing, but can you walk me through each file a little more?  

You got it, friendly invented interlocutor!  

### task lists  

The most basic thing is that each file uses [Github-Flavored Markdown task lists](https://github.github.com/gfm/#task-list-items-extension-). For each day, you have an ordered list of tasks (which I use as times of where I need to be somewhere) and an unordered lists of tasks (which I use for things that don't have to be in a particular time).  

Let's say it's currently 1:00pm and you're looking at this section of the file:  
```  
#### 2019-12-03 Tuesday  

1. [x] 10:00am--11:00am | Meeting, Office 110  
2. [ ] 2:30pm--5:00pm | Reference Desk Shift, Main Library   

<!-- -->  

- [x] start writing documentation for `monthly-planning-files` project @done(added sections; still need to go into detail about tags, why there are HTML comments, etc)  
  - [x] start a changelog @done(15minutes)  
- [ ] add detail to `monthly-planning-files` documentation  
  - [ ] give tag examples  
  - [ ] explain html comments  
- [ ] proofread documentation  
```  

I can quickly see that I've already had a meeting this morning, and that I've got another hour and a half before I need to be at the Main Library's reference desk and ready for that shift. In practice, I'll probably look at my calendar to make sure nothing else has been added—that's part of why this is an **attention** management system, not a system that's sufficient for everything. Having done that, I can select whatever else I want from those untimed tasks. I can also see that I've started the changelog. Since I added the time it took within the tag, if I ever need to do that again in the future, I can quickly search for `changelog` in the whole project and see if Past Me has ever written down how long it took me on a particular day.  

### structure  

Each file uses [markdown](https://www.markdownguide.org/getting-started/) headings (designated by one or more `#`) to let you fold away what you don't want to see. You can fold by week, by day, as well by other headings.  

At the top of each file, we've got some [yaml](https://yaml.org)-formatted [metadata](http://www.language-archives.org/documents/gentle-intro.html) that lets you search by either month number or the name of the month. It also spells out some optional autocompletion "status" terms, all of which you can change. More on this below!  

Below the metadata section, each file has links to other files in the `[[wikilink]]` format. You can put this type of link anywhere you want in a file. I treat the top of the file as a sort of index / breadcrumbs area, and I'll add other wikilinks anywhere else they're relevant.  

To prompt regular reviews—a crucial part of planning that I often overlook—there are lines for daily logs of what you've accomplished, as well as sections for planning before a week starts and for things you need to follow up on at the end. In each day, the little html-style `<!-- -->` comment is there to distinguish between the list of what you did & the previous tasks both for you, the human using the file, and for overambitious markdown rendering engines.  

Finally, even though most people use `.md` for markdown-formatted files, I prefer to have them be `.txt` (unless there's a need for them to be otherwise, like in Jekyll or other environments). You can of course change that for your own purposes. If you leave them as `.txt` files, you may need to tell Atom or whatever editor you're using to treat them as (github flavored) markdown files.  

## inspiration  

These files blend together a lot of strategies & tactics I've picked up from other people. Here's a link to a few of them; I'll add more as I recognize where things came from.  

- [Back to Work](http://5by5.tv/b2w) Merlin Mann & Dan Benjamin's podcast. In particular, their [episodes on Getting Things Done](http://5by5.tv/b2w/95) helped me think about my processes.  
- [Gina Trapani](https://ginatrapani.org) has a page of [`todo.txt`](http://todotxt.org) apps, as well as a [`todo.txt` format primer](https://github.com/todotxt/todo.txt).  
- [Dave Seah](https://davidseah.com/productivity-tools/) has a ton of great productivity tools, as well as a blog about refining processes and treating things as an ongoing experiment.  
- [A Better Mess](http://bettermess.com/start-here/) shares Michael Schechter's attempts to do better work while also being an ADHD mess.  

## license  

Licensed [CC-BY 4.0 International](https://creativecommons.org/licenses/by/4.0/). You are free to share or adapt this work.
