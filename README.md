
# Accela-Velosimo Connect Platform 

A curated list of information related to [velosimo](https://velosimo.com)

![Image_Logo_Velosimo 2019-07-29 10-26-21](https://user-images.githubusercontent.com/7420659/62069001-d8f5ce80-b226-11e9-81b5-4ecae2a87e6a.png)


## Overview about this Docs

Velosimo App is using docsify to generate  its site documentation. The same is under a Bitbucket Cloud repository, so you'll need to know how to add new files and edit existing files. From there, you'll commit your changes to [this repository](https://bitbucket.org/velosimo/docs/src/master/), making it possible for you (or anyone else) to refer to that point in the repository.

You can make and commit your changes locally before pushing them to [this repository](https://bitbucket.org/velosimo/docs/src/master/) on Bitbucket, or you can edit from the online editor.

## Quick Start and Contribuition to this repo

1- It is recommended to install docsify-cli globally, which helps initializing and previewing the website locally.

```
 npm i docsify-cli -g
```

2- Preview your site
Run the local server with docsify serve. You can preview your site in your browser on http://localhost:3000.

```
  cd docs

  docsify serve docs
```

3- Writing content
After the step 2 is complete, you can see the file list in the ./docs subdirectory.

> index.html as the entry file

4- More pages
If you need more pages, you can simply create more markdown files in your docsify directory. 

```
.
└── docs
    ├── coverpage.md
    ├── introduction.md
    └── themes.md
```

Matching routes will be

```
docs/coverpage.md   => http://domain.com
docs/themes.md     => http://domain.com/#/themes
```

> Sidebar, is an special page. In order to have sidebar, then you can modify the sidebar.md (see this documentation's sidebar and witing more pages for an example)
[Docsify a easy documentation site generator.](https://docsify.js.org/#/more-pages)

### Contributing to Velosimo Features Documentation

- Create or choose a Folder in your local machine: `my-folder`
- From the terminal window on your machine, navigate to your Folder directory you want to work: `cd ~\my-folder`
- From Bitbucket, go to left sidebar Repositories and select Docs repository. Check for the Clone button top-rigth and Clone it! the repository to your Folder local machine, [clone repo](https://www.atlassian.com/git/tutorials/learn-git-with-bitbucket-cloud)
- Create your feature branch: `git checkout -b my-new-documentation`
- Commit your changes: `git commit -am 'Add some feature docs'`
- Push to the branch: `git push origin my-new-documentation`
- Submit a pull request, from [bitbucket/repositories/docs](https://bitbucket.org/velosimo/docs/pull-requests/new)

## Deploy

This site is deploy in [ZEIT](https://vercel.com). The steps here could be two ways:

- Can link a Github repo with you Zeit account. Import repo. Easy one and each time that repo update will be automatic deploy. More info here [ZEIT import repo](https://vercel.com/import)

- The other could be from the local folder:
  - Install Now CLI, 
  ```
   npm i -g now
  ```
 - Change directory to your docsify website, for example 
  ```
    cd docs
  ```
 - Deploy with a single command, 
 
 ```
  vercel --prod
 ```














