<img width="643" alt="logo" src="https://user-images.githubusercontent.com/95533259/213480611-0d2cd373-9949-4053-bd6e-2e1e788c8185.png">

## This repository is the backend build for the front end React App - shared.

- The DRF-API has been set up to handle Profiles, Posts, Likes, Authentication, Followers & other site functionality within Shared

### Functionality Includes (but is not limited to):
- Allowing users to follow other users
- Hosting the posts created by users
- Allowing editing of those posts
- Allowing an Admin SuperUser to manage all of the above where required


<img width="1301" alt="Screenshot 2023-01-22 at 10 05 19" src="https://user-images.githubusercontent.com/95533259/213910266-e6eb1b53-3e05-4ed7-bee4-3fd77f5c0488.png">

### Comments / Likes / Posts

<img width="1196" alt="Screenshot 2023-01-22 at 10 17 17" src="https://user-images.githubusercontent.com/95533259/213910747-535dca9a-99bd-4c25-a4aa-c4f6919b5d7c.png">

Utilising Class based views, users are able to add comments onto the front end site, owners of the comments are able to edit and delete those comments.  Owners of the post that have been commented on, are able to see those comments.

The use of models and serializers allows for the logic to function and enables the functionality for use.

In the API, you are able to see, the owner, created date/time of the like and the comment.

For posts, the API also handles filterset_fields which enable additional functionality on the app. I.E. I created additional filterset_fields to allow users to see posts which they own and had been commented on by other users as well as posts which they themselves have commented on, so they can see if anyone else is commenting back to them.


### Profiles

Allowing users to create profiles is the main point of the Shared app and therefore this functionality is essential.  With the API, the profiles functionality handles hosting of the profile and the key pieces of information.  I.E. cloudinary profile image link, username, created information etc.

The profiles functionality also includes the filterset_fields which are essential to being able to build out the logic and various pages within the Shared App.

It also handles the option for users to delete their profile if they so wish, which will remove their profile from the site.

-----------------------------------------------------------------------------------------------------------------------------------------------------------

## Build > Testing > Deployment

<img width="943" alt="Screenshot 2023-01-19 at 17 42 03" src="https://user-images.githubusercontent.com/95533259/213910796-078adb90-a77d-4ab8-9fb4-73d460bc4e2a.png">

### Build

I used the Code Institute "Django Rest Framework" walkthrough as the basis or the code and then built and developed additional functionality from there.

Functionality that was required was outlined in the above wireframe which was also the basis for the User Stories on the Shared App Repo - https://github.com/Jtune89/jt_ms5_adfe


### Testing

With a backend/frontend built, quite a lot of testing is required.  As I would build new functionality within the frontend i.e. posts, I would then need to come back to the backend to ensure that the post was reflected in the posts API with the required information showing.

This manual testing therefore extended to:
- Posts - creating & deleting on a number of profiles
- Comments - adding/deleting comments on a number of posts from different users
- Likes - adding/removing likes on posts from different users
- Profile creation - multiple profiles created
- Profile deletion - multilpe profiles deleted
- Adding/deleting  profile images - adding, removing, changing, removing multiple profile images from profiles

#### Testing Issues:

- Profile deletion - was a challenging build to implement.  It took a few attempts for the functionality to work and I had to test it a number of times to make sure that was it was completed, that it actually functioned to remove the profile from the API
- Filterset_fields - this also took a number of tests as at first, the functionality to see posts that a user owned and had been commented on by others was not working and was showing all of the users posts.  Through persistent testing and checking and changing the code, I was able to build the functionality by creating new filterset_fields in the correct place.

### Deployment:

This build is hosted on Heroku which has a number of requirements with the config vars to allow the functionality to be deployed and actually function.  I followed instructions outlined on the code institute walkthrough to enable the deployment and then tested that it was working once deployed.

I outline on the Shared deployment that there were some issues where the functionality was not working as expected and the users could not see posts which required a change to the config vars to allow that to happen (the / at the end of the origin url was the issue).


### Credits:
- Code Institute Django Framework walkthrough
- Code Institute Tutor Support
- Slack Community
- Stack Overflow
- Various Google Resources




