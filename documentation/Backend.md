# Website-Documentation

## What runs the website?

The website of the bicycle project is built using the following tools:

- **Hugo** - a so-called static site engine.
- **GitHub** - a version control system which serves as the central hub for all
- **Wercker** - a tool that listens to changes in the Github repository and automatically updates the website by running hugo.

### Hugo
[Hugo](http://gohugo.io) is a static site engine that allows us to maintain the website without having a proper database in the background (NoDB). The reason for choosing such a NoDB-strategy is that it makes the website easier to maintain, less prone to problems associated with attacks, and easier to troubleshoot.

Think of hugo like an automated chef, who cooks up our website from recipes and ingredients. Because Hugo is an automated chef, he only accepts recipes and ingredients when handed over to him in a predictable manner: a standardised kitchen. Our version of this kitchen is our GitHub repository:

```
.
├── 404.html
├── archetypes
│   ├── group.md
│   ├── member.md
│   ├── post.md
│   ├── publication.md
│   └── resource.md
├── config.toml
├── content
│   ├── code.md
│   ├── member
│   ├── news
│   ├── publication
│   ├── research.md
│   └── resource
├── data
│   └── projects
├── deploy.sh
├── documentation
│   └── Backend.md
├── index.html
├── layouts
├── public
├── static
│   ├── img
│   ├── pdf
│   └── static
├── themes
│   └── bicycle
└── wercker.yml

```
The most important places to watch out for in this kitchen are:
- The `themes` folder - the shelf where the recipe books are stored.
- The `content` folder - a shelf where the ingredients are stored. This shelf only contains a certain type of ingredient, namely [**markdown**](https://en.wikipedia.org/wiki/Markdown)-files. Markdown allows you to write html-compatible text in a simple and concise manner and keeps the clutter away.
- The `static` folder - another shelf where ingredients are stored. This time, it's anything but text files, e.g. images, pdfs, etc.
- The `config.toml` file - the master instructions.

When you run Hugo, it first takes a look at the master instructions in the `config.toml` file, finds which cookbook you want it to use...

```toml
1 # Site settings
2 baseurl = "https://novakgroupoxford.github.io/bicycle-hugo/"
3 languageCode = "en-us"
4 title = "BBSRC Bistability of Cell Cycle Transitions Project"
5 theme = "bicycle"
```

...and goes to the recipe shelf, and picks up the cookbook. This cookbook will be the theme for our website. As you can see in the `themes`-folder, there's only one theme installed, which is called `bicycle` and is specified in the `config.toml`-file.

Now, Hugo can only cook the dishes from our recipe book, for which he has the right ingredients. So next, he goes to the `content`-folder, and checks which ingredients are present, and which dishes he can cook with it.The markdown files in our content folder contain not only markdown, but so-called front-matter. For different types of content (i.e. members, resources, news, publication, resources) this front-matter is different. The fields in the front matter are specified by so called *archetypes* that sit in the `archetypes`-folder. You can think of the frontmatter as extra scraps of ingredient lists that are attached to a type of markdown ingredient, that tell Hugo which image to use for a particular person and so forth. Generally these linked ingredients live in the `static` folder.

Once Hugo has collected all the ingredients - markdown files that contain text and the frontmatter, and the corresponding files from the static shelf - he starts cooking up our website.
The result is typically put in the public folder and is composed of `html`-files that are neatly organised in folders to reflect the structure of our website, along with bits and bops that make the site look like it does, for instance css-files that style the elements of the site, and javascript-files that instil the site with dynamism.

> A: Does Hugo actually run on my computer?
>
> B: No, as you shall see further down, Hugo does not run on your computer, but we've outsourced Hugo to wercker. All you have to do is keep the kitchen in order, update the ingredient shelf, and then sync the repository with GitHub.

### Github
Github is a powerful platform for storing code, collaborating on code and tracking changes in code ([*version control*](https://en.wikipedia.org/wiki/Version_control)). For the website we use Github for three purposes:

1. To allow different people to update the website and keep everything in sync.
2. To make the codebase (the kitchen) availabe to our outsourced chef.
3. Host the website.

In general, your interaction with github will be minimal and entail syncing the repository on your computer with the one stored on Github, and commiting changes to Github (i.e. tagging updates in the repository, such as new content, and uploading it to GitHub.)

What happens in the background is more impressive: Github tracks all the changes and allows us to backtrack if we made a terrible mistake. By tracking all the changes we commit to GitHub it also enables us to resolve conflicts, if people change the same bit of code in different way. In short, it's very useful and really powerful.

One aspect of being so powerful is what's called **branches**. These are essentially copies of the repository. Normally they start out as identical copies of the code in a repository, which diverge, as people start to make changes, such as developing a new feature to an existing piece of software without affecting the copy everybody has. When the new feature has matured, the branch on which it was developed is merged with the so called **master-branch**, and everybody will be able to use the new feature.

Branches are also important as they provide channels that allow access only to some parts of the github repository. GitHub has generalised this feature and called it GitHub-pages, allowing everybody to host websites directly from a specialised branch of any of their github-repositories, This branch is called **gh-pages**. This is where we serve our website to the public.

> A: This sounds terribly confusing!! - Do I have to keep multiple branches in order?
>
> B: No, in fact we can instruct our personal chef to keep things in order.
>
> A: Wait, but you said that I never have to run Hugo myself as he is "outsourced". How can I have control over what he does?


### Wercker
Wercker is where our personal instance of Hugo - i.e. our personal chef - lives. It's essentially a small computer on the internet that's under our control and is configured to provide our chef a cosy home. We've given this computer access to our github-repository, and it will listen carefully for any changes that happen in it (commits).

When it is notified of a new commit - e.g. a new content file - that is synced with github, it will fetch an up-to-date copy of our repository and pass it to Hugo, who will do his magic and build our website.
In order to make the site accessible to the public, the built website is pushed to the correct branch of our repository - the **gh-pages**-branch.

We control what wercker does using a nice [user-interface, which you can access here.](https://app.wercker.com/el-uhu/bicycle-hugo/runs) It will give you reports on past builds of the website, and allow you to reconfigure what it does and in which order.

# How do I update the website?

Make sure that you have Github installed. On Windows and Mac Github offers a convenient graphical user interface to sync your local repository with the one on github.

Make sure you have a copy of the repository on you local machine.

1. Sync with github - To make sure you pick up any changes that have happened in the meantime and to avoid conflicts.
2. Open your texteditor of choice, such as [**Atom**](http://atom.io)

## Update an existing entry

3. Find the right file in the `content`-folder and edit it.
4. Save changes in your texteditor
5. Go to the Github programme, commit your changes and sync again
6. Wecker will update the website. It should take about 2 minutes to update online.

## Add a new entry

3. Generate a new file in the appropriate sub-folder of the `content`-folder.
4. **NAMING:** avoid spaces, use `.md` as a file extension
5. Copy the frontmatter of an appropriate preexisting item
6. Edit frontmatter to fit to your new piece of content, add main text below.
7. Save changes
8. Go to the Github programme, commit your changes and sync again
9. Wecker will update the website. It should take about 2 minutes to update online.

## Add new static files such as images
1. Sync with github - To make sure you pick up any changes that have happened in the meantime and to avoid conflicts.
2. Open Explorer (Windows) or Finder (Mac) and navigate to where the github repository lives on your computer.
3. Copy/paste the new image to a suitable subfolder of `static/img`
4. **NAMING:** avoid spaces, use `.md` as a file extension
5. Edit frontmatter of the corresponding piece of content, in order to include image.
6. Save changes
7. Go to the Github programme, commit your changes and sync again
8. Wecker will update the website. It should take about 2 minutes to update online.
