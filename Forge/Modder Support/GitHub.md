# GitHub
When you have an issue with your mod the most helpful thing you can do when asking for help is to provide your code to those helping you. The most convenient way to do this is via GitHub or another source control hub.

When setting up a GitHub repo it might seem easy to just upload everything, however this method has the potential for mistakes that could lead to trouble later on, it is recommended to use a Git client or to get comfortable with the Git command line. The following instructions will use the Git Command Line and as such they assume you already have it installed and that you have created a repository.

1. Open a command prompt (CMD, Powershell, Terminal, etc).
2. Navigate to the folder you extracted Forge's MDK to (the one that had all the licenses in).
3. Run the following commands:
    - ``git init``
    - ``git remote add origin [Your Repository's URL]``
        - In the case of GitHub it should look like:  
          https://<span>GitHub</span>.com/[Your Username]/[Repo Name].git
    - ``git fetch``
    - ``git checkout --track origin/master``
    - ``git stage *``
    - ``git commit -m "[Your commit message]"``
    - ``git push``
4. Navigate to GitHub and you should now see most of the files, note that it is intentional that some are not synced with GitHub and this is done with the (hidden) .gitignore file that Forge's MDK has provided (hence the strictness on which folder ``git init`` is run from)
5. Now you can share your GitHub link with those who you are asking for help.