## The Backup Tool That Every Rookie Sysadmin Would Love To Have But Is Too Ashamed To Admit It 

## **The Problem:**

The Linux command line is extremely powerful and highly relevant with the vast majority of servers running some Linux distro.

But with great power comes great responsibility. It's prodigiously easy to f**k things up.

A well known classic:

`rm -rf / `

Congratulations. You just combined the deletion operator with the bit that makes it do folders too. And finally you specified that it should start from the root of the filesystem. 

![jcb](/images/jcb.png)

*(Illustration: a bulldozer. If rm -rf / were to be represented by a piece of heavy machinery, this would be it)*

If you suppress its output or go out to grab a quick coffee after initiating it, **the command will recurse into every nook and cranny of the filesystem until absolutely no bits and bytes are left standing to save the remaining shreds of your dignity.** I'm willing to bet that rm -rf / has been the death of many a code repository - and the end of many a job contract.

*(— One I learned today: you know when you run 'ufw enable' to set up a firewall and give yourself a pat on the back for thinking of security but you then realise don't add an enable rule for SSH access? Well yeah. You can lock yourself out of your own server. Very easily)*

## The Solution:

How useful would it be if you could ... you know ... just roll back Linux commands? It would be ... kind of a game-changer actually. You could feel confident administering Linux boxes without needing to set up sandbox environments. 

The problem?

You can't.

Unless ... somebody finds a way.

## Your Task:

You're going to have to develop some kind of middleware that sits between the developer and the Bash environment that they're administering. 

You're going to have to give this a frontend that makes it look like the actual environment so that their boss still thinks they're competent and doesn't realise that a combination of frantic Googling and your rescue tool is all that's standing between them and nothing working ever. 

So the product here is a terminal environment that parses commands and output back and forth between the user and the actual terminal environment it's protecting. 

Here are the features:

- **Every command issued generates a micro snapshot**: This would allow you to roll back the filesystem to precisely the point before somebody did something very stupid. This is way better than rolling back the filesystem to something like an hourly snapshot because in a busy developing environment that might also still risk a lot of data loss. 
- **There's a command based recovery UI**: If you do screw something up it would be nice to have a recovery UI that's in the terminal and one that pops open to a UI where you can look through a potentially very long list of commands issued (paradigm: how GitGraken displays commit histories). I mean you could even frontend the terminal input with Git ... okay I've drunk too much coffee but that's another direction to consider. 

## The Target Market:

Everyone who administers Linux servers. It would be handy even for desktop users who use CLIs a lot too.

## The Model:

SaaS / subscription based. It could be bought by developers or the companies they work for. 

## The Name And The Marketing:

Something that captures the utility of the tool without insulting the intelligence of the potential user base. You could go down the path of naming it something congenial sounding like Jeeves or Claude (JeeveBox!?). 

It would be nice to emphasise in the marketing that this is about building confidence. Kind of like training wheels for bicycles.