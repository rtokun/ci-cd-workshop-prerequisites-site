id: ci-cd-workshop-prerequisites

summary: This are prerequisites for the CI/CD workshop.

authors: Artyom Okun, Nitzan Werber

# Android Academy CI/CD Workshop Prerequisites
<!-- ------------------------ -->
## Repository Setup

##### In order to save time during the workshop itself, we decided to create these prerequisites that include some environment preparations, which are kind of "standart" and necessary for saving time and focusing during this workshop on what really important. So please follow the instructions carefully and if you have any questions feel free to ask them via [Telegram Channel](https://t.me/joinchat/LTwIFUUp6E4Z5DP7WJYVsA) or [Facebook Group](https://www.facebook.com/groups/android.academy.ils). 

Duration: 0:05:00

1. Create a new "Hello world" application in Android Studio.
2. Build and compile a project.
3. Create a Github repository for this project. You can follow the instructions [here](https://docs.github.com/en/free-pro-team@latest/github/getting-started-with-github/create-a-repo).
4. Create first commit (we just want to verify our local copy is synced with remote). From the app root folder, open terminal and run:

*Note: pay attention to change a path to Github repository in the next script*

``` bash
git init
git add .
git commit -m "Initial commit"
git remote add origin <path to your repository i.e. git@github.com:rtokun/test-111.git>
git push origin main
```


## Create Firebase Project

#### We want to create Firebase project and connect it to our application.

#### 1. Create Firebase project for our app

1. Go to [Firebase console](https://console.firebase.google.com/), login and click `Add project`.
2. Follow the wizard instructions and complete project creation, including entering package details from our app (exact package name can be found in `Manifest.xml` file).
3. In the project overview click `Add app`:
![image_caption](resources/create-app-firebase.png)
4. Select `Android` and follow the wizard. Complete the wizard including downloading `google-services.json` file and putting it inside `app` folder, and modifying the gradle files.
5. Make sure to compile and run the application on the emulator/device after a successful integration.
6. Commit and push all changes you done to the Github repo.

#### 2. Create Firebase Login token

This token allows to 3rd party applications get an access to the Firebase project and make operations. We will use this token in the workshop.
In order to get one we need to install the Firebase console client on our local computer and login via client to our Firebase account.

&nbsp;&nbsp;1.</span> Open terminal and enter<br/>

``` bash
curl -sL https://firebase.tools | bash
```

&nbsp;&nbsp;<span>2.</span> After successful installation enter in terminal:<br/>

``` bash
firebase login:ci
```

It will open browser with Authentication page. Enter your credentials and after succesful authentication go back to your terminal window, you should see there your token:

``` bash
✔  Success! Use this token to login on a CI server:

1//03UkAUZpVhigPCgYIARAAGsotbjnrtl;ghkjnrts;lhkjntw;lhknrt;lhbknwrtl;khn;wlr0VcRQiYGtZSpo7DP1aS7X5OdCVJys
```

&nbsp;&nbsp;<span>3.</span> Copy this token to safe place, we will use it during workshop.<br/>

## Summary

#### At the end of these prerequisites we have to get 3 things:

1. Android "Hello World" starter project.
2. Created Github repository and connected to our local app.
3. Firebase project created and integrated to our app as well.
4. Firebase access token.


#### See you at the workshop! ❤️

