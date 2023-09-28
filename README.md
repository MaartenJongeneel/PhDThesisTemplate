# PhD Thesis Template
Original template created by Bart Besselink, Benjamin Biemond, and Mark Rijnen and further cleaned up and made available by Brandon Caasenbrood and Maarten Jongeneel. 

# Template
The figure below shows a screenshot of some of the pages to give an impression of what the thesis looks like.

<img src="img/sample.png" width="100%" >
<br><br>

Alternatively, you can take a look at the [PhD_Thesis_Template.pdf](PhD_Thesis_Template.pdf) file to examine the full template.

# Editing of the document / compilation into PDF

Editing the document can be done in various manners, depending on your own preference. 

In all cases, first do the following:

Clone the repository to your local drive:

```bash
https://github.com/MaartenJongeneel/PhDThesisTemplate
```

Then choose one (or even both) of the following options for editing:

## 1. Use your own local LaTeX Editor / compiler:

After cloning this repo onto your local machine, as described above, use your own LaTeX environment, such as TeXStudio, MikTeX, VSCode (with LaTeX Workshop extension), etc.


## 2. Use Overleaf as LaTeX editor / compiler:

You can also use a web-based LaTeX editor such as Overleaf.

You will have to create your own account on Overleaf, if you haven't done so.

See for instructions on how to add Overleaf as a remote branch this instruction: [Creating an Overleaf project from an existing Git repository](https://www.overleaf.com/learn/how-to/Using_Git_and_GitHub).

1. To start with, we assume that you git on your computer.

2. Create a new project on Overleaf. You can do this from your My Projects dashboard. You might as well use the 'Blank' template, since we're going to overwrite it.

3. Find the git link for the project. You can find it using the Overleaf Project menu's 'Git' option on the left side.

4. Add the git link for the project as a remote in your local project. 

```bash
cd PhDThesisTemplate
git remote add overleaf <GIT-URL>
git checkout master
git pull overleaf master --allow-unrelated-histories
```

5. Revert the merge to get rid of the files in the existing Overleaf project. 

```bash
git revert --mainline 1 HEAD
```

6. Push your project to Overleaf. 

```bash
git push overleaf master
```

7. Visit the project on Overleaf. Your changes will be there. (You may have to open the Project panel to find the new main file.)

NOTE 1: If you made your local Git copy of this repo and you want to push back the changes in overleaf to git, you will have to do this manually, since changes in overleaf are not automatically pushed back. You can do this by following these steps.

1. After you made your changes in overleaf, pull the changes from overleaf to your local git repository via

```bash
git pull overleaf master --allow-unrelated-histories
```

2. and then push the changes to gitlab via

```bash
git push
```