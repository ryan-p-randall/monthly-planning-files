# monthly-planning-files

Text files with [markdown](https://www.markdownguide.org/getting-started/) formatting to help plan &amp; log whatever it is you do. A lo-fi **attention** management system to complement your **task** management system.  

These files blend the basic system of a [bullet journal](https://bulletjournal.com/pages/learn) with elements of [the pomodoro technique](https://francescocirillo.com/products/the-pomodoro-technique-sheets), then add all the coolness of [plain text](http://bettermess.com/a-plain-text-primer/) files edited in $yourFavoriteTextEditor.  

I've been refining these monthly planning text files since 2013, always in a text editor that syncs  what's on my phone and my computer. This setup works quite well, since it supplies two important things a paper planner lacks: 1. text tools like "search in project" or batch "find & replace" and 2. the ability to not be left behind in a coffeeshop or bus.  

![keanu reeves as ted telling bill 'So after the report we can't forget to do this otherwise it won't happen'](/images/can't-forget.gif)  

## table of contents  

- [recommended tools](#recommended-tools)  
  - [recommended packages for vscode](#recommended-packages-for-vscode)  
  - [recommended packages for atom](#recommended-packages-for-atom)  
  - [phone text editors](#phone-text-editors)  
- [recommended use](#recommended-use)  
- [sounds intriguing but can you walk me through each file a little more?](#sounds-intriguing-but-can-you-walk-me-through-each-file-a-little-more)  
  - [task lists](#task-lists)  
    - [tasks to do at certain times](#tasks-to-do-at-certain-times)  
    - [tasks that can be done at any time](#tasks-that-can-be-done-at-any-time)  
    - [task annotations](#task-annotations)  
  - [example of a day](#example-of-a-day)    
  - [structure](#structure)  
    - [front matter](#front-matter)  
    - [wikilinks](#wikilinks)  
    - [planning and review](#planning-and-review)  
    - [conventions and duplication](#conventions-and-duplication)  
    - [file extension](#file-extension)  
 - [inspiration](#inspiration)  
 - [license](#license)  

## recommended tools  

If you don't already have a favorite text editor, I'd recommend [VSCode](https://code.visualstudio.com) or [Atom](http://atom.io). Both work on Mac, PC, and Linux and is highly extendable and customizable. I've used Atom for years, but recently started primarily using VSCode because of the new [Dendron](https://dendron.so) package for taking interconnected notes.  

If you want an app that's more streamlined, on Mac you could try [nvALT](https://brettterpstra.com/projects/nvalt/) or the forthcoming [nvULTRA](https://brettterpstra.com/2019/04/10/codename-nvultra/). On PC you could try [ResophNotes](https://www.resoph.com/ResophNotes/Welcome.html). On Linux you could do just about anything your heart desires, up to and including using [nvPy](https://github.com/cpbotha/nvpy).  

### recommended packages for vscode  

If you use VSCode, consider installing and befriending these packages:  
  - [Dendron](https://dendron.so), which has many features for making interconnected notes more easily  
  - [Markdown Todo](https://github.com/fabiospampinato/vscode-markdown-todo), which lets you "check off" tasks with a keyboard shortcut  
  - [Todo Tree](https://github.com/Gruntfuggly/todo-tree), which lets you add customizable tags to tasks, plus see them all in a dedicated pane  
  - [VSCode TODO Highlight](https://github.com/jgclark/vscode-todo-highlight), which lets you highlight keywords or other patterns  

If you use the [VSCode TODO Highlight](https://github.com/jgclark/vscode-todo-highlight) package, you can extend its highlighting patterns. Below are a couple simple RegEx patterns I made for it to recognize lines with patterns like `[x]`, `[>]`, or `@urgent` and instead of highlighting with a background color, it applies different colors to the text of those lines. The `"pattern"` line in the first example will find lines with `[x]` and make each whole line look greyed out, and the `"pattern"` line in the second example will find `@urgent` and make each whole line a brighter color. You'd have to add the below lines to the `todohighlight.keywords` sections of your `settings.json` file for them to work—and you can, of course, customize the colors as well. I've gone with colors from Jan T. Sott's [Paraíso Dark](https://github.com/idleberg/atom-paraiso-dark/blob/master/styles/colors.less) theme, which I think work well with Sarah Drasner's [Night Owl](https://github.com/sdras/night-owl-vscode-theme) VSCode theme.  

```
  "todohighlight.keywords": [
    {
        "text": "[x]",
        "color": "#776e71;",
        "backgroundColor": "rgba(0,0,0,0);",
        "regex": {
            "pattern": "([^\\s])(.*?)\\[x\\].*([^\\s])",
        },
    },
    {
        "text": "@urgent",
        "color": "#f99b15;",
        "backgroundColor": "rgba(0,0,0,0);",
        "regex": {
            "pattern": "([^\\s])(.*?)@urgent",
        },
    },
  ]
```

### recommended packages for atom  

If you use Atom, consider installing and befriending these packages:  
  - [Toggle Markdown Task](https://atom.io/packages/toggle-markdown-task), which lets you mark tasks done  
  - [markdown-folding](https://atom.io/packages/markdown-folding), which folds lines of text at different heading levels, all of which are marked with one or more `#`. It lets you fold lines at the week and day level in these files, as well as any other headings.  
  - [language-markdown](https://atom.io/packages/language-markdown), which is an alternative for the built-in `language-gfm` that adds extra things for lists, including a very satisfying greyed-out effect when you've marked a task done by making its `[ ]` box have an `[x]` instead.  
  - [wikilink](https://atom.io/packages/wikilink), which lets you link between notes using the name of the `[[target note]]` surrounded by two brackets. That's right: with the package installed, that `[[target note]]` could let you quickly jump to a separate note named `target note`. These files already include this style link for moving between months or years.  
  - [Tomatimer](https://atom.io/packages/tomatimer), which puts a lightly configurable [pomodoro timer](https://en.wikipedia.org/wiki/Pomodoro_Technique) into Atom's status bar and reminds you to take occasional breaks. The files have the beginnings of a markdown-formatted table for each day in case you're moved to try the [Pomodoro technique](http://baomee.info/pdf/technique/1.pdf) in detail that day.  

### phone text editors  

As for the phone side of things, [Editorial](https://omz-software.com/editorial/) is unfortunately the only iOS editor I know of that will quickly let you move through markdown files. In addition to simple scrolling, the file's title doubles as a scrollable table of contents based on headings. This single feature makes it far faster to get to the last week of a month!  

Hopefully Editorial gets an update soon, and/or this feature begins being common in phone editors. Here are [more than a few iOS options](https://brettterpstra.com/ios-text-editors/).  

If you know of others phone editors that let users move through markdown files by heading, please let me know. Maybe submit a comment as an issue here on Github?  

## recommended use  

Whatever works for you is what you should do! 

The one thing I'd strongly recommend is using some tech tool that can give you proactive time-based reminders to go along with these files. Please consider putting tasks into your calendar as events, using something like [OmniFocus](https://www.omnigroup.com/omnifocus) or [Todoist](https://todoist.com/home), or something else that can reach across time and say ["don't forget to wind your watch"](https://youtu.be/aK1gnNTVxvc?t=168).  

With these files themselves, what works for me is leaving each month's file open in a window while I do related work on my computer. That way I'll occasionally glance over at the file and be reminded of what I've told myself to focus on, which makes it easier to reevaluate whether I should change what I'm doing. If I'm going to be walking around a lot away from my computer, I'll make a little [hipster PDA](http://www.43folders.com/2004/09/03/introducing-the-hipster-pda) out of some scrap paper folded up as a [one-shot zine](https://www.rookiemag.com/2012/05/how-to-make-a-zine/).  

## sounds intriguing, but can you walk me through each file a little more?  

You got it, friendly invented interlocutor!  

### task lists  

The most basic thing is that each file uses the [Github-Flavored Markdown task lists](https://github.github.com/gfm/#task-list-items-extension-) convention. For each day, you have an ordered list of tasks and an unordered lists of tasks. In between, the `<!-- -->` html comment serves both as a visual separator for you and as a programmatic separator for any markdown rendering tools you use. Without it, the unnumbered list of tasks will likely be rendered as a continuation of the previous numbered list of tasks with start & end times.  

#### tasks to do at certain times  

The ordered list (which starts with `1. [ ]`) shows you tasks or activities that should happen at a particular time & place. I use a `|` to separate the time and the place.  

Putting timed tasks both helps prompt me to remember when things need to happen, and to actually think through the process of my day. For instance, I'll often add an extra "buffer" task that tell me to leave my office 35 minutes before it's time to work with a class on our other campus.  

I also often use this section for "time blocking" or for logging what I was doing at particular times. As long as each line starts with a number, any Markdown tool should treat the line as part of that list, whether or not you put a `[ ]` check mark in there.  

#### tasks that can be done at any time  

The unordered list (which starts with `- [ ]`) shows you tasks that can be done whenever. I try to break each task into indented sub-tasks, each of which represents the minimum possible unit of success. That helps keep me motivated & on track to completing the larger task, while also helping me keep track of where I am when I inevitably get interrupted or distracted.  

#### task annotations  

I try to mark each task with one or more tags, each of which contains extra info in parenthesis. The front matter in each file is there to suggest a taxonomy of tags, to simply things for you and your text editor's autocomplete functions. If you want to change these tags, it's simple to use find & replace in project to swap the ones I wrote with whatever you prefer.  

A good example of how you might annotate these tags is the two tags reflecting the types of interruptions you'd track with the [Pomodoro Technique](https://wellness.ucsd.edu/CAPS/Documents/tx_forms/koch/pomodoro_handouts/pomodoro_cheat_sheet.pdf). For instance, if you're working on a task but continually find yourself distracted by your own thoughts, you might add `@internalInterruption()` as a tag, then use the annotation for details: `@internalInterruption(worriedAboutBills)` or `@internalInterruption(tooHungryToFocus)`. You can also annotate `@externalInterruption()` to track another type of interruptions: `@externalInterruption(referenceQuestionOutsideMyShift)` or `@externalInterruption(labPartnerCouldn'tRememberProcedures)`.  

### example of a day  

Let's say it's currently 1:00pm and you're looking at this section of the file:  
```  
#### 2019-12-03 Tuesday  

1. [x] 10:00am--11:00am | Meeting, Office 110  
2. [ ] 2:00pm--2:30pm | Get over to Main Library  
3. [ ] 2:30pm--5:00pm | Reference Desk Shift, Main Library  

<!-- -->  

- [x] start writing documentation for `monthly-planning-files` project @done(added sections; still need to go into detail about tags, why there are HTML comments, etc)  
  - [x] start a changelog @done(15minutes)  
- [ ] add detail to `monthly-planning-files` documentation  
  - [ ] give tag examples  
  - [ ] explain html comments  
- [ ] proofread documentation  
```  

The ordered list shows that you've already had a meeting this morning, and that you've got another hour and a half before you need to be at the Main Library's reference desk and ready for that shift. However, since it takes a half hour to get over there, you've been kind to Near Future, 2:30PM You and added in your travel time as a task.  

In practice, if it's 1:00pm and I'm looking at this file, I'll also look at the tool I used to collaborate with my colleagues to make sure nothing else has been added. This need for extra systems is part of why I stress that this is an **attention** management system, not a system that's sufficient for managing all your tasks & committments. 

Having checked whatever tools you use to coordinate with your team, you're free to select whatever seems like the right thing to do from those tasks that don't have specific start & end times and also aren't already marked completed with a `[x]`.  

You can also see from the unordered list of tasks that you've started writing documentation, specifically the changelog. Since you've added the time it took within the optional element after your `@done` tag, if you ever need to do that again in the future, you can quickly search for `changelog` in the whole project and see if Past You has ever written down how long it took you to do that on a particular day. I find that extra time information really helpful when trying to figure out what to do and how long it might take.  

### structure  

Each file uses [markdown](https://www.markdownguide.org/getting-started/) headings (designated by one or more `#`) to let you fold away what you don't want to see. You can fold by week, by day, as well by other headings.  

#### front matter  

At the top of each file, you've got some basic [YAML](https://yaml.org)-formatted front matter with [metadata](http://www.language-archives.org/documents/gentle-intro.html) that you can easily search by either month number or the name of the month. This front matter also spells out some optional autocompletion "status" terms, all of which you can change. 

Since these are ultimately just text files and not actually converted into web pages or anything, it's not important for them to be in YAML format. I've followed that convention to make searchable front matter mostly because I'm used to using [Jekyll](https://jekyllrb.com/), a program for making static websites used by GitHub, GitLab, and a bunch of other sites.  

As of the 2021 files, I'm letting the Dendron package for VSCode control most of the front matter for each file. If you're not using Dendron, you can easily copy & paste useful parts from the 2020 or 2019 files.  

#### wikilinks  

Below the front matter / metadata section, each file has links to other files in the `[[wikilink]]` format. You can put this type of link anywhere you want in a file.  

I treat the top of the file as a sort of index / breadcrumbs area, and I add other wikilinks anywhere else they're relevant. If you use the [wikilink package in Atom](https://atom.io/packages/wikilink), or if you use Dendron in VSCode, you can also follow these links with simple key commands. I don't often use the included [time log template](time%20log%20template.txt), but I do find it extremely useful on hectic days or ones where I'm more easily distracted than usual.  

__Potential Gotcha if you use Atom; no longer relevant if you use Dendron:__ If you're not used to thinking about file paths, please pay close attention to them when you use, change, or create wikilinks. I mention this because at the beginning of every year I rename my personal files to add another underscore at the front of the file name, which pushes it further down in the file directory. It takes me 5-10 minutes to use "find and replace in project" to update this change in all the files, which feels like a decent trade-off to make to have the current year's files at the top of the file directory the entire rest of the year. In this collection of starter files, the file paths don't match what I actually do in my own notes. If you find yourself wanting to rename the files to improve how they're sorted in your own system, please remember to also update the wikilink file paths. On the plus side, the only thing that happens when a path is wrong is that you either open the wrong file or start a new, empty file. So the errors aren't destructive, just surprising or jarring at worst.  

#### planning and review  

To prompt regular planning and review—crucial parts of planning that I increasingly overlook the busier I become—these files have multiple prompts for planning and review.  

There is a section for setting goals at the beginning of both each month and each week. At the end of each day, there's an unordered list where you can log what you actually did. Each week also has a "weekly holdovers" section where you can collect all the things you still think are worth doing and don't want to forget, or where you can collect and annotate why you've decided to cancel or postpone certain projects.  

I'll often note things that I did without planning in these various review sections. Things like I went for a walk, I read a specific article I saw shared on social media, or other actions that weren't exactly planned but still worth jotting down. The more you jot down, the more likely you make figuring out patterns in the future, or figuring out which readings you should cite since they helped you come up with an interesting interdisciplinary idea.  

#### conventions and duplication  

These files mostly use [ISO 8601](https://en.wikipedia.org/wiki/ISO_8601) conventions for time, both in writing dates as `YYYY-MM-DD` and in naming weeks. Because as [XKCD agrees](https://xkcd.com/1179/), it is the correct format. In particular, ISO 8601 format puts the numbers in largest to smallest unit. Therefore your computer's file manager will sort files named according to that format correctly.  

Having double entries for a particular date (i.e. days at the end of beginning or end of a month on two separate monthly files) sets you up for mistakes. Therefore, each date and week only shows up on a single file, determined by the beginning of the week that includes that date.  

#### file extension (no longer relevant now that I use Dendron)  

Even though most people use `.md` for markdown-formatted files, I prefer to have them be `.txt` (unless there's a need for them to be otherwise, like in Jekyll or other environments). You can of course change that for your own purposes. If you leave them as `.txt` files, you may need to tell Atom or whatever editor you're using to treat them as (github flavored) markdown files.  

## inspiration  

These files blend together a lot of strategies & tactics I've picked up from other people. Here's a link to a few of them; I'll add more as I recognize where things came from.  

- [Bullet Journal](http://web.archive.org/web/20150502033040/http://www.bulletjournal.com/) conventions & patterns are super useful. Ryder Carroll's book on his method is also very helpful.  
- [Back to Work](http://5by5.tv/b2w) is Merlin Mann & Dan Benjamin's podcast. In particular, their [episodes on Getting Things Done](http://5by5.tv/b2w/95) helped me think about my processes.  
- [Gina Trapani](https://ginatrapani.org) has a page of [`todo.txt`](http://todotxt.org) apps, as well as a [`todo.txt` format primer](https://github.com/todotxt/todo.txt).  
- [D.Sri Seah](https://davidseah.com/productivity-tools/) has a ton of great productivity tools, as well as a blog about refining processes and treating things as an ongoing experiment.  
- [A Better Mess](http://bettermess.com/start-here/) shares Michael Schechter's attempts to do better work while also being an ADHD mess.  
- Francesco Cirillo's [Pomodoro Technique](https://francescocirillo.com/pages/pomodoro-technique), particularly tracking interruptions  
  - Here's a [one-sheet primer](https://wellness.ucsd.edu/CAPS/Documents/tx_forms/koch/pomodoro_handouts/pomodoro_cheat_sheet.pdf)  
  - Here's the [detailed version](https://web.archive.org/web/20090306080717/http://www.pomodorotechnique.com/resources/cirillo/ThePomodoroTechnique_v1-3.pdf), which is absolutely worth making time to read if you've felt the need to read all this documentation  

## license  

Licensed [CC-BY 4.0 International](https://creativecommons.org/licenses/by/4.0/). You are free to share or adapt this work.
