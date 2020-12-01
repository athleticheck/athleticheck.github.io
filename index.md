## AthletiCheck

AthletiCheck is an application that allows for:

  * Easy access to athlete profiles for both the athlete and the trainer
  * A single location for all of an athlete's annotated visits with trainers
  * Commenting on specific trainer visits

You can view the website, hosted by DigitalOcean, [here](http://206.189.215.5/#/).

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

## Page Mockups:
Below are the current mockups of the site (note that it is not yet functional)

Landing Page:
<img class="ui medium right floated rounded image" src="/M1-Images/landing-1.png">
<img class="ui medium right floated rounded image" src="/M1-Images/landing-2.png">

About Us:
<img class="ui medium right floated rounded image" src="/M1-Images/about-us.png">

Sign Up:
<img class="ui medium right floated rounded image" src="/M1-Images/register.png">

Sign In:
<img class="ui medium right floated rounded image" src="/M1-Images/login.png">

Athlete Profile:
<img class="ui medium right floated rounded image" src="/M1-Images/M1-Profile.png">

Admin Athlete Profile:
<img class="ui medium right floated rounded image" src="/M1-Images/M1-Admin-Profile.png">

Edit Profile:
<img class="ui medium right floated rounded image" src="/M1-Images/M1-Edit-Profile.png">

New Visit:
<img class="ui medium right floated rounded image" src="/M1-Images/M1-New-Visit.png">

Profile List:
<img class="ui medium right floated rounded image" src="/M1-Images/M1-Profile-List.png">

## Developers
The following team members have helped develop this site:

  * Robert Lemon
  * Andy Yu
  * Anna Campainha
  * Franz Adam
