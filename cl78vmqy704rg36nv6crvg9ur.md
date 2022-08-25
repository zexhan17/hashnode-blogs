## Deploy Web App to Heroku

Agenda  
What is Heroku?  
Deploy web App to Heroku
## Whats is Heroku
Heroku is a platform as a service (PaaS) that enables developers to build, run, and operate applications entirely in the cloud.  
## Deploy
Prerequisites:  

- Git
- Heroku Account
- Heroku CLI

### Install Git:  

Install for your OS  [🔗](https://git-scm.com/downloads)  
You can confirm installation by `git –version` 

### Install Heroku CLI

Install for your OS [🔗](https://devcenter.heroku.com/articles/heroku-cli#install-with-an-installer)  
I'm on Ubuntu. So, for me this command. 
 
```
sudo curl https://cli-assets.heroku.com/install.sh | sh
```  

confirm installation by pasting command `heroku -version`  
Now create your heroku [account](https://signup.heroku.com/) if you don't have one  

Open terminal in your project directory  
Login to Heroku through terminal  `heroku login`  
it may show something like this:  

```
› Warning: Our terms of service have changed:
› https://dashboard.heroku.com/terms-of-service
heroku: Press any key to open up the browser to login or q to exit:
```   

Press any button login will open in browser. In browser just click Login button close the tab and come back to terminal. Remember, you should have a heroku account first. A confirmation message will display in terminal.  

Now push our project using Git.  

Initialization `git init`  

Push All  `git add .`  

Add Commit `git commit -m 'initial commit`  

If you have not configured git you may see something like this  

```
Author identity unknown

*** Please tell me who you are.

Run

  git config --global user.email "you@example.com"
  git config --global user.name "Your Name"

to set your account's default identity.
Omit --global to set the identity only in this repository.

fatal: unable to auto-detect email address (got 'test@test-VirtualBox.(none)')
```  
Don’t worry Run these commands  
put your email and name between double quotes  

```
git config --global user.email "you@example.com"
git config --global user.name "Your Name"
```  
Try again above command `git commit -m 'intial commit' `  
Next step  

```
heroku create
```  
This will create App within heroku account  
Now go to heroku's dashboard web app. You will an application with some name  

So, next thing we wanna do is go to terminal and paste this command in command after `-a` paste your App name. It was auto generated when we create it  

```
heroku git:remote -a your-app-name
```   

Now push to heroku master  

```
git push heroku master
```  

This will take some time depending on your internet speed.
After completing it open your app.  

```
heroku open
```  
we're done. Your app is now deployed.


