## Get up and running with Git

Please clone a copy of this folder with the following command:

```
git clone https://github.com/mrhenderson/ecs.git GitHub
```

The next step is to create a folder for yourself to share code, documents, etc. Create a user folder for yourself (replace MHenderson with your First Initial and last name):

```
cd GitHub/UserFolder
mv Username <yourname>
cd ..
```

Identify yourself

```
git config --global user.name "Your Name"
git config --global user.email you@example.com
```

Use the git commands to add and commit this folder

```
git add -A
git commit -m "Adding a user folder for <yourname>"
git status
git push
```

Next, create a branch for yourself with the following commands:

```
git branch <yourname>
git checkout <yourname>
```

Modify the GitHub/UserFolder/<yourname>/readme.txt in some way.

Again, do a commit pass:

```
git add -A
git commit -m "Adding a user branch for <yourname>"
git status
```

A normal git push won't work here, because the master repository doesn't know anything about the new branch. You will need to use this command to add the new branch:

```
git push --set-upstream origin <yourname>
```
