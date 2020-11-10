## AthletiCheck

AthletiCheck is an application that allows users to:

  * Effectively communicate between Athletic Trainers and Athletes
  * Update personal treatments, rehab and notes for Athletes
  * Easy access to all Athletes


## Project Idea:
Ever since the transition to electronic medical record systems for athletic staff at university sports programs, a tremendous amount of time has been spent on recording athletes’ data due to the fact that most EMR systems do not provide a user friendly interface and are not easily accessible, so athletic trainer often record data and then copy it into the system at the end of the day. How do I aswsume that? Over the summer my colleague and me have concluded around 80 interviews with different athletic trainers in U.S. colleges, ranging from D1 to Junior level programs, and the collected data shows that ATs spend anywhere from 2-4 hours a day on documentation. This holds true for the ATs at UH as well. My proposed solution to this problem is an easily accessible web application for the UH athletics community where data can be entried and received easily on both ends to save time on documentation and make up more time to actually treat UH’s athletes.

## Databases:
We would have 4 collections: users, ProfilesCollection, VisitsCollections, and CommentsCollections.

The first database collection would mirror the "users" collection from the Digits homework.  It would contain all the users that can log in (student athletes versus trainers).
This collection would contain 3 fields for each entry: email, password, and role.

The second database collection would mirror the "ContactsCollection" collection from the Digits homework.  Trainers would be able to create a contact for the athletes.
Athletes will only be able to view the profile linked to their email address.  This collection would contain whatever generic information we want to record for each athlete.

The third database collection would mirror the "NotesCollection" collection from the Digits homework. Trainers would be able to create a new visit associated with the athlete's profile whenever they meet with the athlete.  This collection would store the information about the visit, as well as the profile ID, what trainer made it, and when.

The final database collection would also mirror the "NotesCollection" collection from the Digits homework.  Both trainers and athletes would be able to make comments on each recorded visit.  The comment would contain the actual comment that was posted, as well as an owner, timestamp, visit its associated with, and profile it is on.

