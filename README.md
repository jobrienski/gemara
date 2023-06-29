# Gemara Engine

Gemara is an open-source, contextual search engine, and meta-context for the Internet.

## Why the name?

Gemara is derived from Aramaic, and rooted in the semetic word "gamar" - "to finish" or "complete." There is definitely a thread in the Talmud that God made man to be co-creators with Him, to complete creation here on earth. Of course this work is never done.

The Gemara engine is an effort to complete the Internet as a repository of human knowledge and perspectives, and to make finding knowledge and knowledge about knowledge easier.

## Why a search engine for developers?

The initial effort for this project would be aimed at developers. They require highly contextual information that is only relevent to specific criteria. However, this project will expand to be useful to all people who use the internet.

## How Gemara Helps Developers

As a developer, how often do you search for solutions to problems, or how to do something you may have forgotten because you switch between a variety of programming languages and sdks?

Developers need to find information specific to the problem at hand, and the information needs to have deep informational content. Google and bing's search results are geared towards serving ads. Therefore there's a proliferation of single page sites with very limited content that just scratches the surface of your needs. These are what show up when your looking for information.

Less commercial search engines like duck-duck-go may not be as ad-driven in their search results, but they do not tailor results to your specific needs as a developer.

Search needs an update. The old paradigm is broken.

## How is Gemara different?

Gemara is a new paradigm in search. It leverages the power of similar contextual searches of other developers with matching context, while maintaining anonymity and protecting private and proprietary data. The solutions are scored in terms of context specificity.

Instead of searching the entire web, you are searching the searches of similar contexts (or contextual similarity).

The contextual similarity factors include the version of language, packages, and devops frameworks (docker, kubernetes, etc), and level of expertise. Some of these contexts are determined by meta-data around current projects, and/or profile and manual configuration. See "configuration"

When you or someone finds an answer, you can easily tag it. Once tagged, that context and search is now sharable as a hyperlink. It becomes a problem space with a solution.

So instead of searching the entire web, you are meta-searching on solutions and matching on contextual problems. Your chances of success are greater, and if you don't get an exact match you have much closer results to look through.

### Gemara search lives in the tools you use

The shell, vim, vscode, intellij, git, issue trackers. You don't have to leave these tools, jump to a browser to get search results. Gemara also lives in the browser, but it isn't restricted.

- Have a build error - automatically search on it.
- Want to find a github issue related to the project your working on? You don't have to leave the IDE or shell.

### Context is everything

Your search is probably related to the code and branch you are working on now. If not, you can easily switch contexts among the projects your are working on or researching.

Leveraging others searches also depends on the context of their searches.

### Meta-web overlay

Gemara allows tagging of searches for answers with the best solution. This creates a permanent contextual search hyperlink, which can be commented on, versioned, and shared. It also becomes searchable and prioritized in the Gemara meta-search. Information on the web is often inaccurate, but corrections can be made in the meta-web.

### Local search

Gemara is also a local search engine. It can index your projects, code repos, and search results - think "google desktop". But unlike google desktop, the information is stored locally, encrypted and protected. With local results, you can maintain a memory of past solutions without bookmarking.

### Machine learning to allow collaborative search

Federated local machine learning allows Gemara to anonymously search through the web search solutions of other solutions with the same context, prioritizing these results. This gives you a meta-search capability and leverages the searches of others, saving you time and finding relevant information much quicker. The information is relevant because the context is the same. I'll go into more detail about that later.

No more filtering through click-bait ad sites, or pages that contain your terms but not the context of the problem you are trying to solve.

### Ad-based content is de-prioritized

Ad-based content will appear lower in the results. Why? Because the more ads a page has, the less relevant information it has. The creators of the page are working with google to capture as much traffic as possible. It's a win-win for google and the content generators. But it's a loss for you - a loss of time and energy. It's also a loss for the internet.

We can reverse this process and restore the informational value of the internet by creating search engines that de-prioritize ad-based content. At the same time, we can find information faster, and maybe spend more time away from the computer or on hobbies. Think of the amount of time you can save as a developer with a decent search engine that prioritizes information content instead of ads, and takes into account the context of our search.

As developers, we owe it to ourselves to build this. You can do eet.

## Objections

### Open source? search is too hard

If search was so easy google wouldn't be a multi-billion dollar company - right?

Well... Think about when google arrived on the scene. AltaVista was the primary web-crawler and indexer. AltaVista returned millions of results but they were hardly relevant. Google was a huge improvement in terms of speed and relevance of results.

But the bar was really low. I was a developer then, so I remember. Google just happened to be at the right place, at the right time.

#### Is search really that hard?

Think about it. If you're an experienced web developer/engineer, could you write a basic search engine? I bet you could.

Essentially a search engine is a crawler and an indexer. There are plenty of open-source examples for site-searches and intranets, and the tools for processing large data sets and matching information content with queries have improved significantly.

#### Limiting scope - no porn

Limiting scope is also helpful. Gemara is a search engine for finding technical answers. Therefore, no porn. That eliminates 80-90% of the internet. (If you want porn, use a different search engine)

### Privacy

Wait? Gemara is indexing my code? How can we trust that?

No - Gemara is not indexing the actual source code. It's indexing metadata around the code, like the type of package manager used, the versions of languages and packages. These only include public packages.

Examples of what would be indexed:

- Python project
  - Dependencies portion of `Pipfile`, `requirements.txt`, or `setup.py`
  - Dev dependencies for same files
- Node project
  - Dependencies and dev dependencies sections of `package.json`
- Java project
  - Dependencies and dev dependency sections of `mvn` `pom.xml` or `gradle` `build.gradle`

One - you have full configuration and control over local indexing and indexing of search results. You don't have to enable these features. But when you understand the anonymity and data protection described below, I believe you will want to.

#### All data is local

Local indexing means local. Your data is not stored in the cloud without your control. Your data is encrypted with your keys and can only be decrypted by you.

#### Federated/anonymous machine learning

If you choose to enable this, you will have context oriented search and leverage the power of others' searches as well as your own. The machine learning outputs are run locally and then completely anonymized during the model creation process. Your code is only indexed for local search. Otherwise only meta-data around your code, such as things like "python version", "package manager and version", docker version etc are used to provide context around your search and the solutions you found. This context can be leveraged by others and yourself while maintaining privacy, anonymity, and protecting your data.

#### Look at the source

This is an open source project, not some hidden algorithm with huge privacy-violating data centers. Any privacy concerns or vulnerabilities will be brought up as issues by the community of developers creating and using this platform. Or you may find them yourself by looking at the source and reading the documentation.

## Components of Gemara

### Web-crawler

Documentation pending

### Indexers

Documentation pending

#### web indexer

Documentation pending

#### local indexer

Documentation pending

### search-interface

Documentation pending

### IDE plugins

Documentation pending

### federated machine learning

Documentation pending

## Architecture

### Languages and Frameworks

Haven't decided. I would like to use a distributed computing/volunteer computing model to avoid the cloud services and expenses. https://en.wikipedia.org/wiki/Volunteer_computing

Another option is dfinity - https://dfinity.org/ They're not quite there yet, but could be in the near future, and this would be a good showcase app for them. Since they're all about avoiding the cloud monopoly, they might be happy about avoiding the search monopoly.

Some kind of stream producer/consumer protocol will be used. That may need to be distributed as well so it is possible that a distributed hashtable may be the solution.

The choice of distributed/volunteer computing frameworks will determine the other frameworks and languages.

#### Crawler

TBD

#### Indexer

TBD

#### Search UI

Don't really have a choice in that matter - `javascript` or preferably `typescript`. A customization of the chrome browser is a possibility as well.

#### Local indexer

TBD

#### Distributed machine learning

TBD

#### Federated local machine learning

TBD
