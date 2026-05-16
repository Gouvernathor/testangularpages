# TestAngularPages

This project was generated using [Angular CLI](https://github.com/angular/angular-cli) version 19.0.1.

## Setting it up on Pages

### Gitlab Pages

Create a repo on Gitlab. It may be a private repo.  
In the case where the repo is private, if you want the website to be publicly accessible, you need to go to the repo's "Settings" > "General" > "Visibility", scroll down to "Pages", and select "Everyone".

Either push directly to that repo, or set up a mirror to that repo from your main forge.  
From Codeberg, you need to go in the project "Settings", section "Mirror settings", and add a push mirror.
The url needs to be the .git url of the GitLab repo, the username is yours and the password is a GitLab Token.  
To create a token for your whole GitLab account, go in your account "Preferences", then "Access" > "Personal Access Tokens".
It needs to have the 6 following scopes : Code: Push, Read ; Commit: Update, Create, Delete, Read.

Copy the `.gitlab-ci.yml` file to the root of your repo.  
Go in the GitLab project settings, in "Deploy" > "Pages". Activate the service (TBD).  
To set up a custom domain name, go to the "Domains & settings" tab of the "Pages" menu.
Click the "Add domain" button.
Fill in the domain name, and check-enable the "Automatic certificate management". Confirm.
You will then need to add two DNS entries : one CNAME (or other, depending on your provider) and one TXT, as described in the page.
How to do that will depend on your domain name provider. The page will link to GitLab help pages with more information about the DNS process.  
After setting up the DNS, click the refresh button near "Verification status" until it is verified, then click "Save changes".  
Then, it is advised to force HTTPS, to uncheck "Use unique domain", and to select your custom domain name as "Primary domain".
