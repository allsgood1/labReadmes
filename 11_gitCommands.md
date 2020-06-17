IntroductoryGitGuideCommonCommandsNote​: 
These command examples use [brackets] to denote placeholders. 
You will fill in theplaceholders, and not use brackets in the final command.
DescriptionCommand
Clone a repository from a remote git clone [url]
Check the status of a git repositorygit status
Stage a particular file for commitgit add [filename]
Stage all changes in the current directoryfor commitgit add .
Commit the staged changes (makes atimestamped commit/checkpoint)git commit -m "Your message here"
Push local commits to a remote repositorygit push
Push local commits to a remoterepository, saving the specifics of wherethat code should end upgit push -u [remote name] [remotebranch (master)]
Retrieve the latest changes from a remote(teams, multiple computers)git pull
Create a new git repository in the currentworking directorygit init
Add a new remotegit remote add [name] [url]
Remove a remotegit remote rm [name]
View list of remotes and their urlsgit remote -v
Set the name to include in all futurecommits (initial setup)git config --global user.name"Your Name Here"
Set the email address to include in allfuture commits (initial setup)git config --global user.email"yourEmailHere@something.com
