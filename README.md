## Get up and running with Git

#Do not enter greater-than and less-than symbols, these indicate information that needs to be changed.

### Create an account on http://github.com using your school email address.
Be sure to reply to any verification emails you get from GitHub.
### Reply to the discussion on our schoology page to supply your email and GitHub username. I will need these to add you as a collaborator. You will also need to reply to my email invitation to become a collaborator.

Please clone a copy of this folder with the following command:

```
git clone https://github.com/mrhenderson/ecs.git GitHub
```

The next step is to create a folder for yourself to share code, documents, etc. Create a user folder for yourself (replace <YourName> with your First Initial and last name):

```
cd GitHub/UserFolder
cp -r Username <YourName>
cd ..
```

Identify yourself

```
git config --global user.name "YourName"
git config --global user.email you@example.com
```

Use the git commands to add and commit this folder

```
git add -A
git commit -m "Adding a user folder for <YourName>"
```

Be sure you have completed the assignment to supply your GitHub email and username before you can complete the git push command.
You will need to have Accepted my invitation to be a collaborator. Note the use of the pull before pushing. This will ensure that you have any latest changes (folders added by other users). If you get a strange MERGE screen when pulling, you may have changed something you shouldn't have.

```
git status
git pull
git push
```
When you perform this push command, you will be required to supply your GitHub credentials. Although the password prompts looks like it's not doing anything, it is. Just enter your password normally at this prompt.

Next, create a branch for yourself with the following commands:

```
git branch <yourname>
git checkout <yourname>
```

Modify the GitHub/UserFolder/<yourname>/Projects/readme.txt in some way. Use the Atom editor we installed before, or brave the waters with the vi editor. Add your name, a comment, anything really.

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
