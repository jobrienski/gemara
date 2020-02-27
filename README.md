# noodle

noodle is an open-source, context-oriented search engine for developers - by developers.

## why do developers need another search engine?

As a developer, how often do you search for solutions to problems, or how to do something you may have forgotten because you switch between a variety of programming languages and sdks?

Developers need to find information specific to the problem at hand, and the information needs to have deep informational content. Google and bing's search results are geared towards serving ads. Therefore there's a proliferation of single page sites with very limited content that just scratches the surface of your needs. These are what show up when your looking for information.

Less commercial search engines like duck-duck-go may not be as ad-driven in their search results, but they do not tailor results to your specific needs as a developer.

## how is noodle different?

noodle is a new paradigm in search. It leverages the power of similar contextual searches of other developers with matching context, while maintaining anonymity and protecting private and proprietary data. The solutions are scored in terms of context specificity. The contextual similarity factors include the version of language, packages, and devops frameworks (docker, kubernetes, etc), and level of expertise. Some of these contexts are determined by meta-data around current projects, and/or profile and manual configuration. See "configuration"

### local search

noodle is also a local search engine. It can index your projects, code repos, and search results - think "google desktop". But unlike google desktop, the information is stored locally, encrypted and protected. With local results, you can maintain a memory of past solutions without bookmarking.

### collaborative context oriented search

Federated local machine learning allows noodle to anonymously search through the web search solutions of other solutions with the same context, prioritizing these results. This gives you a meta-search capability and leverages the searches of others, saving you time and finding relevant information much quicker. The information is relevant because the context is the same. I'll go into more detail about that later.

No more filtering through click-bait ad sites, or pages that contain your terms but not the context of the problem you are trying to solve.

### Ad-based content is de-prioritized

Ad-based content will appear lower in the results. Why? Because the more ads a page has, the less relevant information it has. The creators of the page are working with google to capture as much traffic as possible. It's a win-win for google and the content generators. But it's a loss for you - a loss of time and energy. It's also a loss for the internet.

We can reverse this process and restore the informational value of the internet by creating search engines that de-prioritize ad-based content. At the same time, we can find information faster, and maybe spend more time away from the computer or on hobbies. Think of the amount of time you can save as a developer with a decent search engine that prioritizes information content instead of ads, and takes into account the context of our search.

As developers, we owe it to ourselves to build this. You can do eet.

## open source? search is too hard

If search was so easy google wouldn't be a multi-billion dollar company - right?

Well... Think about when google arrived on the scene. AltaVista was the primary web-crawler and indexer. AltaVista returned millions of results but they were hardly relevant. Google was a huge improvement in terms of speed and relevance of results.

But the bar was really low. I was a developer then, so I remember. Google just happened to be at the right place, at the right time.

### is search really that hard?

Think about it. If you're an experienced web developer/engineer, could you write a basic search engine? I bet you could.

Essentially a search engine is a crawler and an indexer. There are plenty of open-source examples for site-searches and intranets, and the tools for processing large data sets and matching information content with queries have improved significantly.

### limiting scope - no porn

Limiting scope is also helpful. noodle is a search engine for finding technical answers. Therefore, no porn. That eliminates 80-90% of the internet. (If you want porn, use a different search engine)

## components of noodle

### web-crawler

Documentation pending

### indexers

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

## privacy and anonymity

Wait? noodle is indexing my code? How can we trust that?

No - noodle is not indexing the actual source code. It's indexing metadata around the code, like the type of package manager used, the versions of languages and packages. These only include public packages.

Examples of what would be indexed:

- Python project
  - Dependencies portion of `Pipfile`, `requirements.txt`, or `setup.py`
  - Dev dependencies for same files
- Node project
  - Dependencies and dev dependencies sections of `package.json`
- Java project
  - Dependencies and dev dependency sections of `mvn` `pom.xml` or `gradle` `build.gradle`

One - you have full configuration and control over local indexing and indexing of search results. You don't have to enable these features. But when you understand the anonymity and data protection described below, I believe you will want to.

### all data is local

Local indexing means local. Your data is not stored in the cloud without your control. Your data is encrypted with your keys and can only be decrypted by you.

### federated/anonymous machine learning

If you choose to enable this, you will have context oriented search and leverage the power of others' searches as well as your own. The machine learning outputs are run locally and then completely anonymized during the model creation process. Your code is only indexed for local search. Otherwise only meta-data around your code, such as things like "python version", "package manager and version", docker version etc are used to provide context around your search and the solutions you found. This context can be leveraged by others and yourself while maintaining privacy, anonymity, and protecting your data.

### look at the source

Since this is an open source project, any privacy concerns or vulnerabilities will be brought up as issues by the community of developers creating and using this platform. Or you may find them yourself by looking at the source and reading the documentation.

## Architecture

### Languages and Frameworks

#### Crawler

The crawler will be written in `golang`.

### Indexer

The
