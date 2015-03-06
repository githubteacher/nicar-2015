# GitHub 201 Workshop // NICAR 2015
An exercise for Git and GitHub on the command line used in a workshop at NICAR.

[**Git Cheat Sheet**](https://training.github.com/kit)

## Fork Repository

If you haven't already, log into GitHub (remember not to save your password on a public computer). Click the Fork button to fork this repository to your GitHub account.

## Clone & Configure
Open Terminal app. Follow the instructions below and type the commands (except for the `$` which is just notation for a command) as instructed.

Clone your fork to your computer. Get the URL from the right side of your fork's page and in terminal:

```bash
$ git clone https://github.com/githubteacher/nicar-2015.git
```

Navigate (_change directory_) into your cloned repository and let Git know who is making these changes by setting a configuration:

```bash
$ cd nicar-2105
$ git config user.name "Your Name"
$ git config user.email "youremail@email.com"
```

## Pull from Upstream
By this time I've already updated the original repository you forked—you're out of date! To stay up to date create a remote connection the original, commonly named `upstream`, so that we can pull in updates when they've been made.

```
$ git remote add upstream https://github.com/githubteacher/nicar-2015.git
$ git pull upstream master
```

When you clone your fork a remote connection to your fork named `origin` is automatically set up. To view your remotes:

```
$ git remote -v
```

## Branch
Now create and move onto a new branch to put your changes on:

```bash
$ git checkout -b fixes
```

Open the `index.html` file to see what it looks like before you change it (it will open in the default browser):

```bash
$ open index.html
```

## Make Changes

Now open the `nicar-2015` directory in a text editor (depending on the editor installed you can type `atom .`, `subl .` or `mate .` from Terminal).

There are a few things that should be fixed in this repository:

- [ ] The [background color](https://github.com/githubteacher/nicar-2015/blob/master/index.html#L9) should be something appropriate, like `peachpuff` :peach:
- [ ] The population figure looks off, [check the data](https://github.com/githubteacher/nicar-2015/blob/master/population-data-2011.csv#L41) and correct it.

Save your changes. You can refresh the tab in your browser to see the updates.

## Commit your Changes
Add and commit your saved changes.

```bash
$ git add index.html
$ git commit -m "accurate data, better color"
```

## Push your changes
Push your changes to your fork:

```bash
$ git push origin fixes
```

## Make a Pull Request
Make a pull request to capture your changes. On your repositories home page click the green Compare & Pull Request button. 

Here you can see your changes and give your Pull Request a description and title. Pull Requesting yourself may seem odd but it's actually really useful, future users can see how decisons came to be when they come across this PR.

Click to create a Pull Request.

## Merge a Pull Request
Merge your pull request because it's great and perfect!

## Pull in changes from `master`
Now that you've merged a branch into your `master` branch on GitHub, you'll need to pull those updates onto the clone on your computer. First change back to your `master` branch and then pull in the changes:

```bash
$ git checkout master
$ git pull origin master
```

## Create & Push a `gh-pages` branch
GitHub will host web files from a branch named `gh-pages` in a repository. Create a `gh-pages` branch that is a duplicate of `master` as it is now and deploy it by pushing it to our fork.

While on the `master` branch, create and move onto a new branch named `gh-pages`
```bash
$ git checkout -b gh-pages
```
Next, push this branch to your fork:

```bash
$ git push origin gh-pages
```

Now that your GitHub repository contains a branch named `gh-pages`, in a few minutes you'll be able to see the site at `github.io/YOURUSERNAME/nicar-2015`.

## Delete folder
Before leaving the workshop, be sure to delete the `nicar-2015` folder from the computer you used (so to not leave your name and email behind).
