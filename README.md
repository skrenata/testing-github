# testing

learning how github works...

...and trying to figure out how to keep track of stuff using git in Ubuntu.

### To see one's name / email locally on git:
- git config --global user.email
- git config --global user.name 

### To change one's name / email locally on git:
- git config --global user.email youremail@example.com
- git config --global user.name "Your Name"

### Note about emails and privacy
GitHub has an option that prevents your email address from becoming public when you push commits. Annoyingly, this means you're also blocked from pushing edits from your local computer to your own repositories (as other people who clone the repository would be able to see your address when doing so).

In order to prevent this from happening,
git config --global user.email

    Find your GitHub noreply address in your GitHub's Personal Settings → Emails. It's mentioned in the description of the Keep my email address private checkbox. Usually, it starts with a unique identifier, plus your username:

    {ID}+{username}@users.noreply.github.com

    Keep my email address private

    Change the global user e-mail address setting to be your GitHub noreply address:

    git config --global user.email {ID}+{username}@users.noreply.github.com

    Reset the author information on your last commit:

    git commit --amend --reset-author

    If you have multiple commits with your private e-mail address, see this answer.

    Now you can push the commit with the noreply e-mail address, and future commits will have the noreply e-mail address as well.

    git push

Source:  
https://stackoverflow.com/questions/43378060/meaning-of-the-github-message-push-declined-due-to-email-privacy-restrictions

### To generate an access token in order to be able to push stuff locally to GitHub:
If you use two-factor authentication, you won't be able to push stuff to GitHub from the command line using your normal password. You need to generate a specific token for that:
- Log in to GitHub
- Settings (drop-down menu on right-hand side)
- Developer Settings (bottom of left-hand column)
- Personal Access Tokens
- Generate New Token
- Choose the permissions you need
- Use that token as your password when requested by git
Source:  
https://help.github.com/articles/creating-a-personal-access-token-for-the-command-line/
