How to Open Source at Zalando
==================

A guide to releasing an open-source project at [Zalando](https://www.zalando.com>), Europe's largest online fashion platform.

Table of Contents 
------------------------------------------------------------

  - [Why Open Source?](#why-open-source)
  - [Our Open Source First Principles](#our-open-source-first-principles)
  - [To Open Source, or Not to Open Source?](#to-open-source-or-not-to-open-source)
    - [Never Open-Source These](#never-open-source-these)
    - [Open Source Workflow](#open-source-workflow)
      - Aim for "Truly" Open Source
      - Our Main Org Page: for the "Truly Open-Source"
      - If Your Project Isn't "Truly Open Source"  
  - [How to Open-Source](#our-open-source-first-principles)
    - Create a Useful README
      - Do
      - Don't
      - Syntax and Formatting
      - Official Namespace
      - Applying Changes
      - Versioning
    - Maintain Your Project
      - Create a Maintainers File
      - Be Prompt and Responsive
      - Use Issues Creatively
    - Code Review
    - Deprecate Responsibly
      - How to Deprecate
      - Tips for Finding a New Owner
    - Licensing 
      - Quick FAQ
      - Create a License File
      - Add a README Note
      - Restrictions Imposed by the License
    - Official Repositories
    - Working With External Contributors
    - Promotion
      - Catwatch
      - Communication
- Other Open-Source Topics
  - Forks: Make Them Meaningful
  - Contributing to Non-Zalando Open-Source Projects
    - General
    - Google Projects
  
###Why Open Source? 

Because It Can:

- improve quality
- mitigate risks
- increase trust
- save us money
- expand our technology choices
- be fun 
- enable us to give back to the community
- strengthen our tech brand
- attract talent

##Our Open Source First Principles

- **Do “Open Source First”**: If your Zalando project can also be useful to non-Zalandos, release it as open source from the start.
- **Take Ownership**: Your team is responsible for ensuring that it’s possible to open-source your project. Your delivery lead is available for guidance.
- **Share Your Code**: All code shared between teams must be open source.
- **Be Safe**: To ensure the broadest possible use of your project, use the MIT License only.
- **Deliver Quality**: Provide a great out-of-the-box experience.
- **Provide Documentation**: Include a clear README and default working configuration.
- **Stay Secure**: Make sure your project doesn’t include Zalando specifics, such as credentials and private identifiers.
- **Ask for Help**: Find colleagues to brainstorm ideas for your project and to review your work.
- **Promote**: Tell the world about your project via blog posts, social media and conference talks.
- **Join the Open Source Guild**: Help us make open source stronger at Zalando!

[Go here](https://zalando-open-source-principles.readthedocs.org/en/latest/) to read the accompanying docs. [This blog post](https://tech.zalando.com/blog/zalando-techs-new-open-source-principles/) might also be of interest.

To Open Source, or Not to Open Source?
------------------------------------------------------------

###Never open-source these:

- PCI DSS-related projects: e.g. payment services
- Domain knowledge
- Anything that would risk our competitive advantage: confidential source code, recommendation algorithms, etc.
- Customer data
- Unique Selling Points (USPs)

If you're open-sourcing a project that has contained sensitive information in the past, the sensitive information can still be retrieved from the git commit history. Create an entirely new git repo for it before pushing it to GitHub.

**No issues? Great! On to the next section ...

##Open Source Workflow

##Aim for "Truly" Open Source
Creating a new open source project should almost always be a team decision. This is because maintaining a project requires commitment, time, and resources. Before starting a new project, ask these questions:
- Does the project already exist? (Do research so you can avoid reproducing an existing effort.)
- Who is the audience?
- Who will be a maintainer? 
     - We require at least one. 
- Will you try to build community around the project?
     - Internal community: This is very important. Promote your project to as many Zalando teams as possible so they can      consider using it. The internal success of a project can give you a good idea about its potential to be adopted/used externally. 
     - External community: If you’re not eager to promote your project to the public, keep it internal.
 
If you want to launch a new project separate from your team, talk to your delivery lead first. Let them know about your plan. Then ask yourself the questions immediately above.

###"Truly Open Source": How-To and Tips  
Our open source work should reflect and reinforce the principles of Radical Agility:
- Autonomy: We support teams and individuals who contribute to open source
- Mastery: Our projects reflect a high level of quality, thoughtfulness, and skill
- Purpose: Our projects are useful to our team, and to the community at large

####Getting—and Keeping—Your Project on Our Main Org Page (Github.com/zalando)
#####Criteria
Our main repository is reserved for projects that meet our “Truly Open Source” criteria. This means they embody the spirit of “Open Source First.” Your code doesn’t have to be perfect before you open-source it. We *want* you to code in public from Day One. 

That said, to appear on github.com/zalando (our main org page) your project should be “truly open-source,” or in active development toward that goal. This means:
- it’s useful and interesting to non-Zalandos. It might serve an entire language community, users of specific tools (Docker, Maven, etc.), or some other group. 
- it’s useable out of the box and independent of our systems
- it has a clear README that:
    - enables non-Zalando devs to download, install, run and use the project with minimal friction  
    - invites contributors via a TODO list 
- You respond promptly (within 72 hours) to PRs, issues, and queries
 
#####How to Make Your Project “Truly Open Source”

Some tips:
- Before writing a single line of code, try define as clearly as possible what the project will do and not do. What is its purpose? What is it trying to solve?
- Identify potential users/audience. Who will use it? How broadly can you promote it?  
     - Our tech team is a great focus group. Ask your colleagues for input and feedback. 
- Ask yourself: Will you want to be working on/maintaining it six months from now? A year from now? Who else can maintain the project with you? 
- Build community: If a project is in development, list unfinished features/components in the “TODO” of your README and in your conversations with potential contributors.
- Before releasing your project, ensure that the README is clear enough for potential contributors and users to understand what it does and the problem(s) it solves. See README guidance below.

The Open Source Guild, your team, your delivery lead, LinkedIn groups, community forums/boards, and Meetup audiences can all be great sources of help.  

####If Your Project Is Not Useful Beyond Zalando (Yet)
If a project is in very early-stage development, dependent on our systems, built primarily for Zalando use, “experimental,” ”maybe useful to others someday,” or created for Hack Week, it’s not suitable for the main org repo—yet. The Guild will place your project in our "Zincubator" organization, so that your code remains public. Or, you can:
 
- keep the project on your personal GitHub account. This makes sense if it isn’t tied to Zalando development. 
- maintain the project as a private repo on GitHub Enterprise. We don't recommend this option, as projects here will be much less likely to reflect “open source first” values, lose visibility, and possibly disappear into the ether.
     - Is it possible to transfer GitHub issues from one project to the other? No.
     - Is it possible to transfer the ownership of a Github repo to someone else? Yes.

Code/Project Review
------------------------------

Ask your team and other peers to review your code and install and test your project prior to public release. Peer review tends to be more effective than unit testing. Not sure what to ask for, or how to peer-review? This list of [11 best practices](https://smartbear.com/learn/code-review/best-practices-for-peer-code-review/) should help.

Creating a README
------------------------------

A project's success depends a great deal on README quality. Your README should:
- begin with a short description of what the project is, does, and does not do
- list features
- place your project in context: who is likely to use it, and why?
- cover all technical details and configuration options
- link to additional and more advanced documentation (optional)
- cover the basics: installing, running, configuring, etc.
- eliminate as much friction as possible separating the user from your software
- address any remaining friction points in separate sections
- include a TODO list to invite potential contributors, citing specific needs/bugs/etc.
- include badges
- if possible, include screenshots and demo videos

Your README should NOT:
- refer to Zalando specifics, such as internal teams and processes
- include large chunks of code without explaining what they represent
- lack details critical to a user’s ability to install/run/use your project
- include any code that presents security vulnerabilities

###Syntax and Formatting
Markdown is the simplest and most easily understood syntax; we recommend using it for all your documentation. However, we realize that there are exceptions: PyPi, for example, uses reStructuredText, and the Python community in general doesn’t use Markdown. If Markdown isn’t practical, then we recommend using only one markup format in your project. The format you choose should be [GitHub-supported](https://github.com/github/markup#markups).

For readability, break up text often.

Think about SEO.

Maintainers
------------------------------

Maintainers are the contact people for a project. They are also the only contributors who can package new versions and apply changes to the repository (i.e., merge pull requests). Every project must have at least one maintainer. [This helper script](https://github.com/zalando-stups/github-maintainer-cli) gives us an overview of repos that users are maintainers for. 

The Open Source Guild reserves the right to contact maintainers to ensure a project remains active/maintained. If the project is not being maintained, we will work with you to either find a new maintainer or remove the project from our organization page. Please be responsive to all internal queries about your project and its status. 

###Maintainers File

Every project needs a ‘[MAINTAINERS](https://git.kernel.org/cgit/linux/kernel/git/torvalds/linux.git/tree/MAINTAINERS)’ file (listing all maintainers) at its root. Your build/packaging configuration file (e.g., [pom.xml for Maven](https://maven.apache.org/pom.html#Developers)) can fulfill the purpose of a MAINTAINERS file. Format:

     [full name] <email address>
     [second full name] <email address>
     etc.

Our Catwatch application [will collect maintainers from the MAINTAINERS files](https://github.com/zalando/catwatch/issues/29).

###Maintainer Responsibilities

Respond promptly to pull requests and issues. “Within 72 hours” is a good window. Open issues do not make your project “look popular.” Instead, they make it look like you're neglecting your project. If project workload becomes unmanageable, ask the Guild or the community for help.

If you are away/on vacation and can’t respond to PRs/issues promptly, find someone who can. 

If you're not going to accept a PR, reject it ASAP and include a brief explanation why.  

####Issues: Be Clear, and Get Creative
Issues can be good for planning or for onboarding contributors. Issues should include a description of the point, question, discovery, or other detail prompting the issue. 

Issues that consist solely of a title appear unprofessional and do not do much to invite discussion from the community.

Label your issues with clear tags. This is a great way to organize and categorize issues.

Forks: Make Them Meaningful
------------------------------------------------------------
*“Forks are for making your own snapshot of a codebase so that you can make a new version of it with your own special sauce, or so that you can contribute a change in the form of a pull request. Simply, you must make a fork whenever you need to modify the codebase, but do not have direct access to do so. New users don’t understand this and end up equating the ‘fork’ button with ‘download’ or ‘bookmark’. Little do they know, you can download code directly from the original repository and you can bookmark things using Github’s stars.”* —[Eric Greer](http://ericgreer.info/github/funny/stupidity/2016/02/28/judging-the-stupidity-of-github-projects.html)

To fork, or not to fork? Some guidelines:
- Only keep the fork open as long as needed.
- “True/Long-Lived forks” are highly discouraged, even from Zalando projects. We avoid internal forks in order to avoid diverging widely from what we have published, and the inevitable hassle of getting the project to a state where we can support both code bases
- Avoid two forks of the same project.

If your goal is to make a small fix to a project, use your own/personal GitHub account.  

Manage Your Deprecated Projects Responsibly
------------------------------------------------------------

To deprecate a project:
- add “Deprecated” at the top of your README, as well as a notice stating your plans for the project: deletion, finding a new owner, etc.  
- After announcing your decision to deprecate your project:
     - notify your users and put a notice on your README. Wait 60 days. Or:
     - Find a new owner. Consider internal options first, then seek an external owner. Ask the Guild for help. Or:
     - Parking it on your personal page.

####Tips for Finding a New Owner
Internally, you can use internal mailing lists and HipChat to announce your need. Externally, try social media platforms and community boards. Add 1-2 sentences to your announcements suggesting how your project might have potential to evolve into something bigger and better.

Contributing to Non-Zalando Open-Source Projects
------------------------------------------------------------
We encourage you to contribute to other open-source projects in ways that benefit Zalando — for example, by making bug fixes in Apache, or submitting a patch to a language. Let the Guild know about your external contributions so we can help you get the recognition and support you deserve.

**Contributing to Google projects:** For typical CLAs, we are safe — but ask our legal team (guild can provide their contact info) to double-check whenever you’re in doubt. CLAs that are safe: Oracle, Apache.

Working with External Contributors
------------------------------------------------------------
The Guild supports you in recruiting non-Zalandos to contribute to your project. We simply require that you have external contributors sign a contributor licensing agreement (CLA). A few good models to follow and adapt:
 - [.Net Foundation](https://cla2.dotnetfoundation.org/) example (electronic submission via GitHub account)
 - [Google’s CLA](https://github.com/angular/angular.js/blob/master/CONTRIBUTING.md#-signing-the-cla) for contributing to AngularJS is a simple click-through form with a Googlebot that automatically checks for signatures
 - Selenium/Software Freedom Conservancy uses a [Google form](https://docs.google.com/a/zalando.de/forms/d/11Z8LoYpTGUIwCegifVH1YtL9smxVDNk-fOykUZTAWhE/viewform?hl=en_US&formkey=dFFjXzBzM1VwekFlOWFWMjFFRjJMRFE6MQ#gid=0)

Licensing
------------------------------------------------------------
To allow the most broad usage of our source code, and to keep open-sourcing easy and safe, we use [the MIT license](https://opensource.org/licenses/MIT). MIT is succinct, straightforward, and easy use in closed-source projects.  

To reiterate: You must apply the MIT license to all newly created open-source projects. If you fork other (external) projects or contribute to them, keep the original license.

**If Open-Sourcing a Library**: consider using a weak copyleft license that won’t restrict the software that uses it to the same license; will allow usage in closed source software; and will potentially increase the number of users and contributors.

Please do not use any other license without a very compelling reason. Licensing questions? Ask the Open Source Guild or see our TechWiki page (internal doc) for the link to more detailed information about licensing.

If your team uses an external project whose license is not Zalando-recommended, you can can use GPL code — but only internally. Be sure it's a version of the GPL that continues to allow for the ASP loophole. AGPL and versions of the GPL with additional restrictions won't work.

**Who is the license owner?**

Zalando SE.

**LICENSE document**

Every project needs a ‘LICENSE’ file at the root of the repository that contains the copy of the selected license (see above). [Here is an example](https://opensource.org/licenses/MIT) for MIT.

**README note**

Every README{.md,.rst} file must state the following at the end:

>The MIT License (MIT)
>Copyright © [yyyy] Zalando SE, https://tech.zalando.com

>Permission is hereby granted, free of charge, to any person obtaining a copy of this software and associated documentation files (the “Software”), to deal in the Software without restriction, including without limitation the rights to use, copy, modify, merge, publish, distribute, sublicense, and/or sell copies of the Software, and to permit persons to whom the Software is furnished to do so, subject to the following conditions:

>The above copyright notice and this permission notice shall be included in all copies or substantial portions of the Software.

>THE SOFTWARE IS PROVIDED “AS IS”, WITHOUT WARRANTY OF ANY KIND, EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.
>

Replace the [yyyy] field with the year that you created the project, and do not update it. Do not provide multiple years.

**Still unsure about what to do?**

If in doubt, ask your delivery lead.

**Equally simple guideline for delivery leads**:

If you’re in doubt, ask your department head. Management can work with Legal to determine Intellectual Property concerns.

**Repository of meta information**

Many package managers include a feature to make the applied license machine readable. Use these! An example for [Maven](https://maven.apache.org/pom.html#Licenses):

 ```<licenses>
 <license>
   <name>MIT</name>
   <url>https://opensource.org/licenses/MIT</url>
   <distribution>repo</distribution>
  </license>
 </licenses>
 ```
An example for [Node](https://docs.npmjs.com/files/package.json#license), according to [this](https://gist.github.com/robertkowalski/7620849):

```
“license”: “MIT”
 ```
An example for Scala (with sbt):
```
licenses += ("MIT", url("http://opensource.org/licenses/MIT"))
```
Restrictions Imposed by the License
------------------------------------------------------------
“Dependency” typically means “being linked with,” “included in your artifact,” or “depends on it during runtime.” Dependencies can limit you. To remain in compliance, check the licenses of your projects. Your build tool’s license does not affect your software’s license. A jar file or Python dependency will affect your software.

*There is no license*

A project always has a license. If there is no license statement, the author automatically receives a copyright. [This](http://choosealicense.com/no-license/) implies that no one has the right to modify or redistribute the software. If you really need the software, contact the author (who is likely unaware) and ask him/her to provide a proper license.

*Unusual additions*

As stated by Zalando Legal, it is OK to use React and other Facebook open-source software projects for Zalando projects.

Official Repositories
------------------------------------------------------------
Some guidelines:
- Host **all** source code in [the ‘zalando’ space](https://github.com/zalando) on GitHub.
- GitHub organization owners must enable [Two-Factor Authentication (2FA/MFA)](https://help.github.com/articles/about-two-factor-authentication/).
- Host JVM artifacts (*.jar) on Maven Central in [the ‘org.zalando’ group](https://repo1.maven.org/maven2/org/zalando/).  To do this, get a [Sonatype](http://central.sonatype.org/) account and ask the STUPS team to add it to Zalando.
- Host Python packages on [PyPI](https://pypi.python.org/pypi/) (PyPI has no namespaces) and make sure that multiple persons have “maintainer” rights.
- Publish SBT plugins [on Bintray](https://bintray.com/zalando). An example of the publishing process is [here](http://www.scala-sbt.org/0.13/docs/Bintray-For-Plugins.html); these SBT files ([#1](https://github.com/zalando/swagger-speccer/blob/master/build.sbt) and [#2](https://github.com/zalando/swagger-speccer/blob/master/project/bintray.sbt)) illustrate the publishing configuration.
- [Node](https://www.npmjs.com/) modules [now have namespaces](http://blog.npmjs.org/post/116936804365/solving-npms-hard-problem-naming-packages). We prefix them with our (hopefully short!) product name — e.g. [karma](https://karma-runner.github.io/0.12/index.html) plugins are prefixed “karma-”; the same goes for gulp, grunt, etc. Host your Node modules in the public NPM registry. Here is [how to publish to NPM](https://gist.github.com/coolaj86/1318304).
- For Docker images: You can currently browse it [here](https://registry.opensource.zalan.do/ui/), or with the Pier One command line utility. We have an [open source registry](https://registry.opensource.zalan.do/ui/) that everyone can read. It is deployed in the AWS open source account and Docker images can be pushed by any team member to their respective team repo:

```bash
$ # you need to login to registry-write.opensource.zalan.do (workaround for Docker V2 bug)
$ pierone login --url registry-write.opensource.zalan.do
$ docker push registry-write.opensource.zalan.do/myteam/myartifact:1.0
$ # on any other computer:
$ docker pull registry.opensource.zalan.do/myteam/myartifact:1.0 # no auth needed for download!
```


**Official Namespace**

The official namespace for our projects is ‘**org.zalando**’, where applicable.

**Applying Changes**

All repository changes, including those made by maintainers, should come from GitHub pull requests so that we can streamline review and change tracking (as per [GitHub Flow](https://guides.github.com/introduction/flow/)). Everyone should have their own fork, though you can still edit READMEs/documentation/related files with the GitHub “Edit” button. The ‘master’ branch should be the accepted development head; pull requests get merged there.

**Versioning**

All project artifacts should be [versioned semantically](http://semver.org/). Tag all versions in GitHub with the exact version name (like ‘0.1.0’, i.e. do not prefix tags with “v.” or similar). For a better user experience, use the GitHub “release notes” feature to add notes whenever you change something in the new version.

Project Promotion
------------------------------------------------------------

###Catwatch
All Zalando open-source projects are listed on [zalando.github.io](http://zalando.github.io/) (also called [CatWatch](https://github.com/zalando/catwatch)): our own metrics dashboard measuring our most popular public projects and our most active contributors in terms of commits, stars and forks. Please add a [.catwatch.yaml file](https://github.com/zalando/zmon/blob/master/.catwatch.yaml) to the root of your repository to set a human-readable project title and image URL.

###Communication
Share your project with:
- relevant LinkedIn Groups
- community forums/boards
- e-newsletters and websites/newsletters dedicated to the problem(s) your project is trying to solve, the relevant languages, etc.
- if you have contacts at a university, pitch your project to their students
- major players in the industry
