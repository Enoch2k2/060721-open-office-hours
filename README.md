# 0621-open-office-hours

## How To Setup a JS project + Github Repository For Practice


### Creating the project

* Find a good location in your terminal to create a project.
* Type mkdir project-name (where project-name is the name of your project, never add spaces, sperate with either _ or -)
* Open project in your editor with `code project-name`.
* Create your filestructure:
```
  mkdir images
  mkdir css
  mkdir javascripts
  touch javascripts/index.js
  touch index.html
  touch README.md
```
* Add your html to your `index.html` by typing `html:5` and hitting tab inside the file.
* Inside the `<body></body>` tag type `script:src` and hit tab. It should create a script tag with a src= attribute. Within the `""` of the src= attribute, type javascripts/index.js. It should look like this:
```
<body>

  <script src="javascripts/index.js"></script>
</body>
```
* Test that it works by adding `alert('hello');` inside your `index.js` file and dragging the `index.html` to your browser tab.
* You should get a pop up that says hello! Just click the ok button and you are good to go!

### Creating A Local Repository
Local repositories are on your machine only. It's easy to confuse it with a github repository. A repository is basically a project you are working on that is managed by a project management tool, such as git. Before you can push up changes to github you will need a local repository that's connected to a remote repository (github). To do this you will need to do the following. In the terminal type:
```
  git init (This will initialize a new local repository. You only need to do this once per project. This will create a hidden .git folder inside of your project where all of your commits will be stored as well as other repository information).

  git add . (which will stage all the files for commit in that current directory. Staging files is basically saying, these files we want to put in a box and save it under a commit)
  
  git commit -m 'initial commit' (This will take all of the files you have staged and label it with a name as well as a SHA key that will be like an identifier for that commit.)
```

### Connecting to a Remote Repository (github)
Remote repositories such as github repositories are kind of a centralized place to go for your project management. Other developers are able to connect to that remote repository to fork / clone, or work directly with that repository in order to make changes. The way that we work with github repositories is we connect our local repository to the remote via a git remote. Let's connect our local repository to a remote repository (github)

* First thing you will want to do is go to https://github.com/new . As long as you are signed in, you can go directly to the new repository page from that link.
* Next you will want to add a new name to the repository and click the button to create.
* Next we will need to find the instructions from github, it will take you to a page that has different snippets of instructions. The one you want is existing repositories. To break down what it's going to ask you to do (These commands get typed in the terminal in your editor):
```
  git remote add origin git@github.com/username/repo-name (this is how we assign a url from a local repository to github to be able to push or pull changes)
  git branch -M Main (This is purely optional, but if you want to work out of a Main branch instead of master, then run this step.)
  git push -u origin Main (Push allows us to send all of our changes that we made from making commits to github, -u is setting the upstream, you only need to set an upstream once, afterwards you can just do git push)
```
* Once you are done with those steps, refresh your github tab and you should see all of your files and folders in the repository.
* After you do these initial steps, then from there, all you will need to do is when you want to update github: 
```
  git add <filename or ., just remember the . stands for current directory>
  git commit -m 'commit message' (commit messages are a very short summary of the work you just did. Make sure to commit often!)
  git push (will send any commits you have made to github, you don't actually have to git push every change you make, you can make many different commits and then do git push to send all the commits at once!)
```

So this is how you can make an easy js practice project and connect with github. Hope this helps!
