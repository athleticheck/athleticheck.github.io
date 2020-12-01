# AthletiCheck

AthletiCheck is an application that allows for:

  * Easy access to athlete profiles for both the athlete and the trainer
  * A single location for all of an athlete's annotated visits with trainers
  * Commenting on specific trainer visits

You can view the website, hosted by DigitalOcean, [here](https://athleticheck.xyz/#/).

You can view the Github Organization page with all of the repos [here](https://github.com/athleticheck/athleticheck).

You can view the Milestone 1 Project [here](https://github.com/athleticheck/athleticheck/projects/1).

You can view the Milestone 2 Project [here](https://github.com/athleticheck/athleticheck/projects/2).

## Project Idea:
Ever since the transition to electronic medical record systems for athletic staff at university sports programs, a tremendous amount of time has been spent on recording athletes’ data.  This is due to the fact that most record systems do not provide a user friendly interface and are not easily accessible by athletic trainers.  As a result, trainers often end up recording data during athlete visits and then copying the data into the EMS at the end of the day.  This process leads to wasted time and unnecessary repetition of information.  Previously conducted interviews and surveys with athletic trainers ranging from junior level programs to D1 sports across the country support this claim.  The collected data shows that trainers spend anywhere from 2-4 hours a day on documentation alone.  Unfortunately, the University of Hawaii's athletic program is not an exception.  Our group's solution to this problem is AthletiCheck, a website that creates an easy-to-use record system targeted at both the athletes and their trainers.  Each athlete will have a profile where their basic information will be stored.  On top of this, a comprehensive history of each visit with a trainer will be attached to their record.  The athletes will be able to view their own profile and comment on the recorded visits.  This functionality will be available to the trainers, as well as the ability to document new visits with athletes.  We hope that this site will reduce time spent on documentation, allow trainers to focus on actually treating the University of Hawaii's athletes. 

## Databases:
We would have 4 collections: users, ProfilesCollection, VisitsCollections, and CommentsCollections.

The first database collection would mirror the "users" collection from the Digits homework.  It would contain all the users that can log in (student athletes versus trainers).
This collection would contain 3 fields for each entry: email, password, and role.

The second database collection would mirror the "ContactsCollection" collection from the Digits homework.  Trainers would be able to create a contact for the athletes.
Athletes will only be able to view the profile linked to their email address.  This collection would contain whatever generic information we want to record for each athlete.

The third database collection would mirror the "NotesCollection" collection from the Digits homework. Trainers would be able to create a new visit associated with the athlete's profile whenever they meet with the athlete.  This collection would store the information about the visit, as well as the profile ID, what trainer made it, and when.

The final database collection would also mirror the "NotesCollection" collection from the Digits homework.  Both trainers and athletes would be able to make comments on each recorded visit.  The comment would contain the actual comment that was posted, as well as an owner, timestamp, visit its associated with, and profile it is on.

## User Guide:
The following sections describe the major features of this application. Accompanying feature descriptions are current progress screenshots.

### Landing Page:
<img class="ui medium right floated rounded image" src="/M2-Images/landing-1.png">
<img class="ui medium right floated rounded image" src="/M2-Images/landing-2.png">
  * The AthletiCheck landing page informs users of some key features of the application - interactive profiles, personalized records, etc. The landing page includes links to registering an account, signing in, and learning more about the team behind AthletiCheck.

### About Us:
<img class="ui medium right floated rounded image" src="/M2-Images/about-us.png">
  * Learn more about the team at the About Us page. Feel free to email any of our developers with any questions regarding AtheltiCheck, its uses, and any troubleshooting matters.

### Sign Up:
<img class="ui medium right floated rounded image" src="/M2-Images/register.png">
  * New athletes (users) can register an account with AthletiCheck.

### Sign In:
<img class="ui medium right floated rounded image" src="/M2-Images/login.png">
  * Current athletes (users) can sign in to their profile to view their profiles.

### Athlete Profile:
<img class="ui medium right floated rounded image" src="/M1-Images/M1-Profile.png">
  * Athletes can view their profiles, quick stats, and visit notes.

### Admin Athlete Profile:
<img class="ui medium right floated rounded image" src="/M1-Images/M1-Admin-Profile.png">
  * Trainers can view athlete profiles, add notes, and make changes regarding any athelete information.

### Edit Profile:
<img class="ui medium right floated rounded image" src="/M1-Images/M1-Edit-Profile.png">
  * Trainers can edit athlete profile stats to keep athletes up-to-date on their physical condition.

### New Visit:
<img class="ui medium right floated rounded image" src="/M1-Images/M1-New-Visit.png">
  * Trainers can open a new visit note that details what the visit was for, any significant observations, and whether or not an athelte is cleared for performing.

### Profile List:
<img class="ui medium right floated rounded image" src="/M2-Images/profile-list.png">
  * Trainers can view all atheletes registered in the system. By clicking on an athelete's profile link, they can be directed to that respective athlete's profile.

## Developer Guide

First, [install Meteor](https://www.meteor.com/install).

Second, go to [https://github.com/athleticheck/athleticheck](https://github.com/athleticheck/athleticheck), click the "Code" button, and download "athleticheck-master.zip" as a ZIP file. Once downloaded, unzip in local machine and open with JS IDE of choice.

Third, cd into the app/ directory of your local copy of the repo, and install third party libraries with:

```
$ meteor npm install
```

## Running the system

Once the libraries are installed, you can run the application by invoking the "start" script in the [package.json file](https://github.com/athleticheck/athleticheck/blob/master/app/package.json):

```
$ meteor npm run start
```

The first time you run the app, it will create some default users and data. Here is the output:

```
meteor npm run start

> meteor-application-template-react@ start D:\GitHub\athleticheck\app
> meteor --no-release-check --settings ../config/settings.development.json

[[[[[ ~\D\GitHub\athleticheck\app ]]]]]

=> Started proxy.
=> Started MongoDB.
W20201130-22:33:32.482(-10)? (STDERR) Note: you are using a pure-JavaScript implementation of bcrypt.
W20201130-22:33:32.540(-10)? (STDERR) While this implementation will work correctly, it is known to be
W20201130-22:33:32.540(-10)? (STDERR) approximately three times slower than the native implementation.
W20201130-22:33:32.541(-10)? (STDERR) In order to use the native implementation instead, run
W20201130-22:33:32.541(-10)? (STDERR) 
W20201130-22:33:32.542(-10)? (STDERR)   meteor npm install --save bcrypt
W20201130-22:33:32.543(-10)? (STDERR) 
W20201130-22:33:32.543(-10)? (STDERR) in the root directory of your application.
I20201130-22:33:33.846(-10)? Creating the default user(s)
I20201130-22:33:33.847(-10)?   Creating user admin@foo.com.
I20201130-22:33:34.117(-10)?   Creating user john@foo.com.
I20201130-22:33:34.351(-10)? Creating default data.
I20201130-22:33:34.352(-10)?   Adding: Basket (john@foo.com)
I20201130-22:33:34.372(-10)?   Adding: Bicycle (john@foo.com)
I20201130-22:33:34.374(-10)?   Adding: Banana (admin@foo.com)
I20201130-22:33:34.377(-10)?   Adding: Boogie Board (admin@foo.com)
I20201130-22:33:34.381(-10)? profiles collection is empty!
I20201130-22:33:34.382(-10)? Creating default profiles.
I20201130-22:33:34.382(-10)?   Adding: defaultA
I20201130-22:33:34.396(-10)?   Adding: defaultB
=> Started your app.

=> App running at: http://localhost:3000/
```

### Note regarding "bcrypt warning":

You will also get the following message when you run this application:

```
Note: you are using a pure-JavaScript implementation of bcrypt.
While this implementation will work correctly, it is known to be
approximately three times slower than the native implementation.
In order to use the native implementation instead, run

  meteor npm install --save bcrypt

in the root directory of your application.
```

On some operating systems (particularly Windows), installing bcrypt is much more difficult than implied by the above message. Bcrypt is only used in Meteor for password checking, so the performance implications are negligible until your site has very high traffic. You can safely ignore this warning without any problems during initial stages of development.

### Viewing the running app

If all goes well, the template application will appear at [http://localhost:3000](http://localhost:3000).  You can login using the credentials in [settings.development.json](https://github.com/athleticheck/athleticheck/blob/master/config/settings.development.json), or else register a new account.

### ESLint

You can verify that the code obeys our coding standards by running ESLint over the code in the imports/ directory with:

```
meteor npm run lint
```

## Developers
The following team members have helped develop this site:

  * Robert Lemon
  * Andy Yu
  * Anna Campainha
  * Franz Adam
