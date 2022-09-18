---
title: "Public or Private Digital Brain"
tags:
- not finished
---
# Public or Private Digital Brain
When it comes to choosing to have the Digital 🧠 public or not there is three options. 

1. Private - The Github repo[^1] and the digital brain website is only accessible for me.
2. Public - The Github repo and the digital brain website is public.
3. Partly private - The Github repo is private but the digital brain website is public or partly public with some private notes.

These three options will be described in the next chapters.

[^1]: Repo is short for repository. A repository is a place where code is stored. 

I have currently chosen option 3, partly private using the Quartz ignore approach.

## Private
This is achieved with a private repo, but I am not sure how the website can be privet while still be available for me. Before it is even relevant to look into wether this is possible I have to understand why a private website would be preferable and if I need a website at all if it is private.

I think the one of the reasons I want to have a private website is because it would make it accessible on any device at any time, everywhere. It will also have no privacy problems which i will discuss in the other chapters.

By making it private I loose the ability to simply update my website with the latest changes in the Quartz repo which my website is based on. This is due to the fact that I can not use a fork of Quartz. I will also not be able to simply share notes with other people. Additionally, they will not be able to add changes to the notes.

| Pros              | Cons                 |
| ----------------- | -------------------- |
| No privacy issues | Not simple to update |
| Accessibility     | Not shareable       | 
## Public
Todo
## Partly Private
The main reason for this alternative is to choose what should be private or not. The main concern is how the notes should be held private. The website itself must be public, but the repo can be public or private. There are some pros and cons for both. Read more about ignoring notes in [Quartz Ignoring Notes documentation](https://quartz.jzhao.xyz/notes/ignore-notes/).

In a public repo you might think that every note is available for everyone. This is not true when `gitignore` is used. There are several pros and cons with this approach. 

| Pros                                                                        | Cons                                                                                                            |
| --------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------- |
| Simple update due to the fact that a fork can be used                       | Might forget to add to gitignore, big hassle to fix if something is pushed                                      |
| Only need to change gitignore and do not need to use quartz private feature | Difficult and scary to take everything down if I change my mind. All the notes should be considered compromised |
| Other people can update notes                                               | Can not add access logic to be able to view private notes on the website                                        |
|                                                                             |                                                                                                                 |

It is possible to add other people to a private repo. That way other people can be able to see everything in the repo, meaning all the notes. They can also change the notes. I can choose whether or not to add a lot of people or only the ones I greatly trust. Since I do not use `gitignore` with this approach, I have to use `ignoreFiles` or `draft: true`.

| Pros                                                                  | Cons                 |
| --------------------------------------------------------------------- | -------------------- |
| Partly private by default                                             | Not simple to update, Seems like Quartz is continuously cool updates |
| Easier and more secure to change my mind to set every note as private |                      |

## Relevant
There is a way of updating my private repo with changes in the original Quartz repo. This is explained in this [private fork doc](https://gist.github.com/0xjac/85097472043b697ab57ba1b1c7530274)