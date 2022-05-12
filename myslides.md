---
author: Froilán Irizarry Rivera
title: Inner Source
subtitle: Bringing open source practices into an enterprise
date: 2022-05-12
output:
  revealjs::revealjs_presentation:
    keep_md: TRUE
---

# What is inner source 🤔

---

From [Wikipedia](https://en.wikipedia.org/wiki/Inner_source):

> InnerSource is the use of [open source](https://en.wikipedia.org/wiki/Open-source_software) [software development](https://en.wikipedia.org/wiki/Software_development) best practices and the establishment of an [open source-like culture](https://en.wikipedia.org/wiki/Open-source_model) within organizations for the development of its non-open-source and/or [proprietary software](https://en.wikipedia.org/wiki/Proprietary_software).

---

## History side note

Tim O'Reilly coined the term in __2000__ 👀

[![](https://upload.wikimedia.org/wikipedia/commons/thumb/a/a0/Tim_O%27Reilly_-_2017_%2838700700672%29_%28cropped%29.jpg/220px-Tim_O%27Reilly_-_2017_%2838700700672%29_%28cropped%29.jpg){width=250px}](https://en.wikipedia.org/wiki/Tim_O%27Reilly)

So it's taken a while to catch on

# Let's break it down

---

## Open Source software development practices

---

![](https://media.giphy.com/media/xT5LMAi67OqKlS99Zu/giphy.gif){width=100%}

::: notes

As with all in our field. development practices is very vague. For simplicity I'll stick with what I consider the big two.

:::

---

### Publicly accessible

- source control (GitHub, GitLab, Bitbucket)
- bug/task list
- community or communication channels

::: notes

The first group of practices revolves around public accessibility, or can people that are not a part of the project or effort get to it freely.

This access impact three main things:

- Is the source control system that the project uses accessible to the public. I feel it's important to specify a VCS and not default to a folder somewhere on the internet. The practice of the community is to have version control at the forefront of our projects.
- Is the bug or task list accessible. An important part for a open source project to have publicly available. This is the only clear way people outside of the project can know where a project needs help and where to report any issues.
- Last but not least, community. This is a bit more "whatever works" for the maintainers. Many open source project default to have a community around them and have communications or the core team public.

:::

---

### contributor and community guidance

- documentation
- how to contribute
- code of conduct
- WYSIWYG / as is

::: notes

It's very common for mature projects that have a community of contributors and users to dedicate time to this.

Most successful open source projects of any size have clear instructions as to how to interact with the community and the project.

The general practice on platforms like GitHub is to have a CONTRIBUTING.md file that states how exactly new and established contributor should submit any contribution back to the project. This helps keep expectations in place as well as give the project maintainer some predictability when going into reviewing a pull request.

That said, it's totally OK for a project to say that there is not community around this project and that it's not accepting any contributions. The importance is to say so and be clear with people that are interested.

:::

---

## Open Source-like culture

---

![](https://media.giphy.com/media/MZQkUm97KTI1gI8sUj/giphy.gif)

::: notes

This made we pause and think.

As a term, open source has been around since 1995. Since that time it has made it's way into
the vocabulary fields outside of software. Data, art, literature, government, medicine, manufacturing. All these communities have taken up open source as a concept in some way.

It's given rise to the modern maker and craft movement, creating commons, open data, open government and open culture movements.

After a while of me just sitting, trying to articulate what was in my brain, I looked for a word cloud generator and pasted text from some wikipedia articles about the subject. Just to see what would come up

:::

---

![](../images/word-cloud.svg){width=100%}

::: notes

I asked the tool for 50 words and this is what came up.

Taking a look at this, we see the all too common open, source, and open-source terms.

We also see some interesting ones, creative, movement, community, exchange, free, public, and innovation

:::

---

### The embrace of openness and free exchange of ideas to push a community's creativity and innovation to solve problems

::: notes

So with that I'll try to define open source culture as:

The embrace of openness and free exchange of ideas to push a community's creativity and innovation to solve problems.

:::

---

# What does that mean for us

---

## collaboration

::: notes

Let's start with how we can collaborate in a more open and community driven way.

We need to be able to accept contributions into our repos from other pods. Even from teammates that aren't engineers. Closing ourselves off only creates silos and makes it difficult for us feed off of each other's knowledge.

While a pod may be the code owner for a repo, we should invite outside contributions, be it code, documentation, bugs, and especially questions.

:::

---

![](../images/github-logo.png){width=500px}

::: notes

This is where GitHub shines.

A big part of a project is not just it's code but also decisions, conversations, brainstorms, failures, and fixes. Keeping these close to the code makes finding these simpler. The easier it is to find something to collaborate on, the higher the chances are to receive contributions.

:::

---

![](../images/github-collab-features.png){width=100$}

::: notes

README files, GitHub issues, GitHub discussions, GitHub projects, and pull requests are our primary tools to make collaboration as simpler as we can make it.

:::

---

## openness

::: notes

Promoting collaboration and enabling it needs to go hand in hand with openness. In fact they could have been in the same section.

I thought it important to keep separate for one specific reason

:::

---

### Repo visibility

![](../images/github-repo-visibility.png)

::: notes

To be able to collaborate on a repository we first need to be able to see it and submit contributions to it. Repository visibility is one of the low hanging fruits that any enterprise can change today.

An internal repository is a repo that can be accessed by anybody that is a member of the GitHub enterprise org. The default access is of read but could be changed to write. This will enable everybody to contribute to a repo in the form of a pull request.

It will also let private repositories fulfill their roles as a private space for any sensitive needs.

A private repository is a repo that will only be viewable to the creator, teams or individuals that are granted access to it, and the GitHub enterprise org admins.

Private repositories can be used just as internal repos and default access can be granted through the enterprise settings but this creates unneeded friction and overhead to repo owners in the management of repo access.

:::

---

![](https://media.giphy.com/media/LpkLWXTp0v0qy70xPp/giphy.gif){width=100%}

::: notes

You may be saying to yourself

"Froi, giving write access to everybody to my repo is dangerous."

I'm glad you thought that because that leads use to ....

:::

---

## governance

::: notes

A big part of the success of major open source project is their project governance. In other words how they manage their repo and what rules and expectations they set for their contributors.

An enterprise practicing inner source is not different.

Even with tight access management, a team should have proper governance in place for their repo. This helps to ensure that not only are contributions following an approved process, but contributor will also know how to submit contributions.

Contributions that follow a good repo governance have a higher change of being better quality submissions, which in turn increases their chance of being accepted, and in turn increases the amount of contributions received.

:::

---

### Implementing

- READMEs
- CONTRIBUTING.md files
- code of conduct (important for any public facing open source projects)
- CODEOWNERS files
- branch protections

::: notes

To help us with governance, each repo should have most, if not all of these support files and features implemented.

:::

---

## community

![](https://media.giphy.com/media/DPVjijLfZOGArKi8Kr/giphy.gif)

::: notes

At the end all this is about fostering a contributor community in our enterprise. The past 20 years have shown how strong developer communities, regardless if they work in the public view or behind a firewall, create better software, are more effective, and innovate at a faster pace.

I'm not going to lie and say that these changes are easy or that we can do them over night. But I do think that it's worth to put the effort and start implementing them in a strategic way that can enable us help our teammate push the best products they can
:::

# Thanks!
