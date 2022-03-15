# Assignment 02 - Milestone 04 (WIP)

**Due March 30 (W) @ 9 PM**

**Worth 3% of your final grade**

**Content in this milestone document takes precedence over anything you read in the [assignment pdf](comp-3512-asg-1-winter-2020-current.pdf).**

## Easing Off A Bit This Week

This milestone is due right after your quizzes. I'd like you to focus on those a bit more than this milestone. Plus, you likely have some things that need doing in other courses.

So this milestone _should_ be fairly easy to complete and get a good mark. There is still a goodly amount of work to come - and only one week to complete it after this milestone - so if you're worried about that, just take a look at milestone 5. 

## Overview

This fourth milestone will have you focusing on 4 main tasks:

1. Implementing an API to provide data to the Title Search.
2. Implementing the Title Search (from Home) functionality.
3. Implementing the Login functionality.
4. Continuing work on your visual design.

## User Table Import

Since you need to get Login working, you'll need some users to test things out with. There is a [users.sql](data/users.sql) script you can use to create the necessary users table with a handful of users prepopulated in it. You can use the script just like you did for the `populate-movies.sql` script in the last milestone.


## Your Mark

### Category Weightings

| Category      | Weight |
|---------------|:------:|
| API Creation  |  20%   |
| Title Search  |  30%   |
| Login         |  35%   |
| Visual Design |  15%   |

### The Ladders

Each of the categories will use the same Ladder.

| Completed Req's Sections | Corresponding % |
|:------------------------:|:---------------:|
|         Level 0          |       0%        |
|         Level 1          |       52%       |
|         Level 2          |       65%       |
|         Level 3          |       75%       |
|         Level 4          |       88%       |
|         Level 5          |       98%       |

## Category Details

### Must-Haves

> If the following aren't met, I won't mark your submission. Most of these have been done previously, so as long as you haven't busted anything, there is no real work to do here!

- [ ] [MH.1] The Feedback pull request in the repo has not been closed or merged.

- [ ] [MH.2] The name of your Heroku application is `comp-3512-w22-team-xx`, where `xx` is the 2 digits of your team.

- [ ] [MH.3] There is a working link in the team repo's `README.md` that takes you to the Heroku URL for your application; this should cause your `index.php` to be displayed. 

    _I will be marking the site you link to via this README, so make sure it's the one you want assessed!_

- [ ] [MH.4]  When the Default page is validated by the [W3C Markup Validation Service](https://validator.w3.org/), no errors are present. Warnings are ok.

    _As last time, I'm going to assume you haven't busted the pages you previously validated._

- [ ] [MH.5] The "plumbing" that was used in milestone 1 is present here: a valid Procfile, composer.json, and public folder containing your site's viewable files are present.

---


### API (20%)

> In assignment 1, you were querying a 3rd-party API to do your title searches...but now it's time to [eat your own dog food](https://en.wikipedia.org/wiki/Eating_your_own_dog_food).

> Due to the nature of this task, the marking is going to be kind of a "0/52/98" thing: you either did it right (98), have a few minor errors (52), or have numerous errors/didn't do it (0).


#### Level 0

- [ ] The API is not implemented at all, or
- [ ] Three or more Level 5 requirements are not met.

#### Level 1

- [ ] One or two Level 5 requirements are not met.

#### Level 5

- [ ] [API.1] A user can go to `[your site URL]/api/movies?title=[title search string]` and get back a JSON array of all movies matching `[title search string]`, following all requirements mentioned below.

- [ ] [API.2] The endpoint must be exactly as described. This includes the use of all lowercase letters.

- [ ] [API.3] The search should be case-insensitive. And don't forget folks will potentially be passing in spaces and such. You might want to look into [urlencode](https://www.php.net/manual/en/function.urlencode.php).

- [ ] [API.4] The api folder must be inside your public folder so that it's accessible to users.

- [ ] [API.5] The query string must be valid (i.e. you must perform query string sanitization on the query string). If the query string is invalid, please return an empty array. (This might not be what you do in "real life", but it's good enough for us here!)

---

### Title Search (30%)

> The title search feature is basically the same as it was in assignment one, but now you need to query your _own_ API endpoint to get the matching titles. As such, you'll need to get the API work done first!

> To get full marks, the behaviour we see here should be the same as it was for assignment one. I don't think I need to go over the requirements in agonizing detail, since we've been down that road once before.

> Note: this milestone is **not** asking you to have your Browse page completely functional - that's for milestone 5. You just need to be able to search from the Home page (either version) and see the expected results on the Browse page.

#### Level 0

- [ ] The search is not implemented at all, or
- [ ] Three or more Level 5 requirements are not met.

#### Level 1

- [ ] One or two Level 5 requirements are not met.

#### Level 5

- [ ] [TS.1]  The title search no longer has an autocomplete.

- [ ] [TS.2] A user shouldn't be able to do a title search if the title search box is empty. You should accomplish this with JavaScript.

- [ ] [TS.3] If a user searches for a title that matches nothing, then they should arrive on `browse-movies.php` and there should be a clear indication that their search resulted in no results.

- [ ] [TS.4] If a user searches for a title that matches (fully or partially, case-insensitive) the title of a movie that is in the database, then they should arrive on `browse-movies.php` with the matching movies visible and in alphabetic title order.

- [ ] [TS.5] Behind the scenes, the same process as required in assignment one should be taking place: the clicking of the search button should initiate a fetch from an API endpoint (your own!) and results should be stored in some form in session storage (i.e. they are now cached so that further API calls aren't necessary unless a new search is initiated).

---

### Login (35%)

> For this milestone, we want an existing user - one who exists in the users table of our database - to be able to log into the site. A logged-in user will have access to pages and features that a not logged-in user won't. These differences are shown in the Level 5 requirements.


#### Level 0

#### Level 1

#### Level 2

#### Level 3

#### Level 4

#### Level 5



---

### Visual Design (15%)

The visual design of all Views will be evaluated at **both** Mobile L and Laptop L size in a Chrome browser. 

It's important that your site has a unified visual "feel".

Also, since you've all received a variety of visual design feedback over the course of assignment one, my expectations here will be higher.

#### Level 0

- [ ] I don't think this is even possible! This would have to be some kind of visual design that makes me want to cry, or perhaps curl up into a fetal ball somewhere.

#### Level 1

- [ ] The overall impression of the site is "oh dear...". Perhaps the different pages don't share a visual theme at all and are stitched together from disparate assignment one designs?  Or perhaps there are just so many issues that I lose count? In any case, you wouldn't want to show this to a potential employer or client.

#### Level 2

- [ ] The overall impression of the site is "OK" - it's basically reproductions of the illustrations shown in the pdf and give the impression that the visual design was not given much attention. It's not hard to find issues with the design, but they're not show-stoppers. You'd be a bit hesitant showing this to a potential employer or client.

#### Level 3

- [ ] The overall impression of the site is "hey, this is pretty good!" - pages deviate occasionally and reasonably from the illustrations shown in the pdf and give the impression that the visual design was given some thought and attention. While there are perhaps still a few areas that obviously need a bit of work, you'd probably be pretty confident showing this to a potential employer or client.

#### Level 4

- [ ] The overall impression of the site is "wow" - pages deviate frequently and thoughtfully from the illustrations shown in the pdf and give the impression that the visual design was a focus of attention. It's difficult to find issues - and they are likely quibbles. You would show this to a potential employer or client with no hesitation whatsoever.

#### Level 5

- [ ] This will be difficult to reach, as basically the site looks like it was designed by a person who does this kind of thing for a living.