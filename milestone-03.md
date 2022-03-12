# Assignment 02 - Milestone 03

**Due March 23 (W) @ 9 PM**

**Worth 3% of your final grade**

**Content in this milestone document takes precedence over anything you read in the [assignment pdf](comp-3512-a2-v1.pdf).**

## Overview

This third milestone will have you focusing on 3 main tasks:

1. Validating the registration form on the client-side using JS,
2. Sanitiziang the query string of URLs used for the Movie Details page, and
3. Presenting the Movie Details page for a given movie.

In addition, you will want to put effort into the visual design of your site, so I guess that's 4 main tasks.

## Database Population

If you look through the requirements for the various categories, you will see that in order to get a higher mark in some of them, you're going to need to query a movie database...which means that you're going to have to create and populate that database!

Fortunately, there's a script that will do that for you. It's in this instruction repo here: [data\populate-movies.sql](data/populate-movies.sql). You will need to use this script from your local SQL command line prompt using the technique shown in [this screencast [10:42]](https://watch.screencastify.com/v/QD1VqRvv3ha0IhDBKbvr).


## A Suggestion

I won't be *forcing* you to use the projects feature of GitHub as I did in assignment one...but I hope you realize that it can be a powerful tool for making clear what tasks your team needs to do and by when and by whom. (Or is that who? I always forget.)

These kind of boards are used in industry, so why not practice using them while you're a student?...

## Your Mark

Much like with assignment one's milestone 6, I'll be marking this (and remaining milestones) by using categories, each marked on a Ladder.

As you might suspect, the 4 categories for this milestone correspond to the 3 main tasks mentioned in the Overview, plus visual design.

### Category Weightings

| Category                                     | Weight |
| -------------------------------------------- | :----: |
| Client-Side Registration Form Validation     |  30%   |
| Movie Details Page Query String Sanitization |  20%   |
| Movie Details Page Presentation              |  35%   |
| Visual Design                                |  15%   |

### The Ladders

Each of the categories will use the same Ladder.

| Completed Req's Sections | Corresponding % |
| :----------------------: | :-------------: |
|         Level 0          |       0%        |
|         Level 1          |       52%       |
|         Level 2          |       65%       |
|         Level 3          |       75%       |
|         Level 4          |       88%       |
|         Level 5          |       98%       |

_In case you were wondering, these numbers correspond to the midpoints of D, C, B, A, and A+ grades in [MRU's official common grading system](https://catalog.mtroyal.ca/content.php?catoid=29&navoid=2315&hl=%22Academic+Status%22&returnto=search&print)._

## Category Details

### Must-Haves

If the following aren't met, I won't mark your submission. Most of these have been done previously, so as long as you haven't busted anything, there is no real work to do here!

- [ ] [MH.1] The Feedback pull request in the repo has not been closed or merged.

- [ ] [MH.2] The name of your Heroku application is `comp-3512-w22-team-xx`, where `xx` is the 2 digits of your team.

- [ ] [MH.3] There is a working link in the team repo's `README.md` that takes you to the Heroku URL for your application; this should cause your `index.php` to be displayed. 

    _I will be marking the site you link to via this README, so make sure it's the one you want assessed!_

- [ ] [MH.4]  When the Movie Details page is validated by the [W3C Markup Validation Service](https://validator.w3.org/), no errors are present. Warnings are ok.

    _I'm going to assume you haven't busted the pages you previously validated, which is _adorably_ Pollyannaish of me, but I gotta be me._

- [ ] [MH.5] The "plumbing" that was used in milestone 1 is present here: a valid Procfile, composer.json, and public folder containing your site's viewable files are present.
---

### Client-Side Registration Form Validation

Form validation is fundamental for any site that uses forms - and your site does. 

Validation typically happens on two fronts: the front-end, where JavaScript is used to provide feedback to the user as the form is being filled out, and again on the back-end, in case JavaScript is turned off and as a preventive measure to make sure no naughty data gets into our databases.

For this milestone, you're going to get front-end validation working. This means that these requirements will all be done using JS code. No PHP.

You do NOT have to actually do anything (yet) with the validated form.

You do NOT have to see whether a provided email exists in the database, since you haven't been provided with the necessary tables yet!

#### Level 0

- [ ] No registration form is available and/or there is no front-end validation.

#### Level 1

- [ ] Validation happens as described in Level 3 (or 4), but there are bugs in the code that prevent **3 or more validations** from working correctly.

#### Level 2

- [ ] Validation happens as described in Level 3 (or 4), but there are bugs in the code that prevent **at most 2 validations** from working correctly.

#### Level 3

- [ ] All validations described in the bullet list in the Registration Page section of the pdf (page 9) are working.

- [ ] Feedback on invalid fields is provided **after the submit button has been pressed**.

    _We'll call this "after submit validation", as described in [this article](https://cxl.com/blog/form-validation/)._

- [ ] If the form is determined to be valid, a message is logged to the console indicating this. (This is just a temporary thing - you shouldn't be doing this by milestone 5!)


#### Level 4

- [ ] All validations described in the bullet list in the Registration Page section of the pdf (page 9) are working.
  
- [ ] Feedback is provided **as the user enters data in the form**.

    _We'll call this "inline validation", as described in the article referred to in Level 2._

- [ ] If the form is determined to be valid, a message is logged to the console indicating this. (This is just a temporary thing - you shouldn't be doing this by milestone 5!)

#### Level 5

- [ ] Validation behaves as described in Level 4, but the presentation of feedback shows a great deal of thought and care have been invested.

    _For ideas, check out both the previously-mentioned article and [this one](https://medium.com/@andrew.burton/form-validation-best-practices-8e3bec7d0549) as well._

---

### Movie Details Page Query String Sanitization

In order to view the details about a movie, you need to visit `single-movie.php?id=x`, where `x` is the id of the movie in question. We want to make sure that this query string is valid, so that's what this category is about.

#### Level 0

- [ ] The `single-movie.php` page does no validation of the query string at all. Sad now.

#### Level 1

- [ ] The `single-movie.php` page attempts to validate the query string as described in Level 2, but has bugs that stop it from working correctly.

#### Level 2

- [ ] The `single-movie.php` page redirects to an error page if any of the following is true about the query string:

    - [ ] there is no key called `id` (case sensitive!), or
    - [ ] there is more than one key, or
    - [ ] there is a key called `id`, and its value is not an integer, or
    - [ ] there is a key called `id`, and its value is an integer <= 0

- [ ] If there are no errors in the query string, you have two options:

    1. If you've completed the Movie Details Page Presentation requirement to Level 4 or 5, then just display that page!
    2. Otherwise, display a placeholder page of some sort that is different from the error page. (That way, when I'm marking, I can clearly see whether your sanitization is working correctly.)

#### Level 3

- [ ] The `single-movie.php` page behaves as with Level 2 and, in addition, also redirects if the id provided is not one of the ones found in the [all-movie-ids.php](data/all-movie-ids.php) file given to you here in the instructions repo.

    _This is basically a bargain-basement way of ensuring that the movie id provided in the query string is a valid one. It's kind of like what we did with the JSON files in assignment one._

#### Level 4

- [ ] The `single-movie.php` page behaves as in Level 2 and, in addition, redirects if the id provided is not a valid one. This determination of validity must be done through querying the movies database.

#### Level 5

- [ ] The `single-movie.php` page behaves as with Level 4 and, in addition:
  - [ ] the code used to do this redirect is composed of expressively-named helper functions, and
  - [ ] the error page is informative, visually pleasing, thematically appropriate, and of your own design

---

### Movie Details Page Presentation 

When a user goes to `single-movie.php?id=x`, they should see a page that is _almost_ identical to what was shown in assignment 1, with 3 exceptions:

1. There is no Speak button.
2. There is no Close button. (Users will just use the nav menu.)
3. There will be a way to favourite movies. (But this doesn't need to be implemented in this milestone.)

#### Level 0

- [ ] `single-movie.php` is missing, or doesn't use any PHP to generate content from another source (file or database).

#### Level 1

- [ ] A reasonable attempt was made to reach Level 2,3, or 4, but things are broken, and the page is not displaying properly.

    _I get to decide what "reasonable attempt" means._

#### Level 2

- [ ] When a user visits `single-movie.php?id=170`, the details for Mad Max 2 are displayed. You must include/require the associated array provided in this repo under `data/mad-max.php` to do this. I won't test with any other movie id for this level.

    _So if you're shooting for this level, and you wanted to display the runtime in some markup, you'd need to access it via `$madMax["runtime"]`._

     _At this level, and for this milestone, I don't mind if all your code is just in a block at the start of the `single-movie.php` file._


#### Level 3

- [ ] When a user visits `single-movie.php?id=170`, the details for Mad Max 2 are displayed. You must use a database query to do this. I won't test with any other movie id for this level.

    _At this level, and for this milestone, I don't mind if all your code is just in a block at the start of the `single-movie.php` file._

#### Level 4

- [ ] When a user visits `single-movie.php?id=x`, where `x` is a valid movie id, the details for the associated movie are displayed. You must use a database query to do this. I will only test with valid ids.

    _At this level, and for this milestone, I don't mind if all your code is just in a block at the start of the `single-movie.php` file._


#### Level 5

- [ ] The behaviour at this level is the same as it is in Level 4, and

- [ ] You must have your Heroku application set up to use environment variables, as outlined in my [setting up environment variables on Heroku for GCP  [7:54]](https://youtu.be/Ecw_6Tj-nXg) screencast.

- [ ] You must create a `config.php` and `Connection.php` class, as demonstrated in my [configuring your projects for use on XAMPP and Heroku](https://youtu.be/YNljMRhRkAA?t=480) from the 8:00 mark onward.

    _These screencasts were made last semester, so there will be some changes you'll need to make. One of them, for example, is to use the db named `movies`. You should be able to figure out any other changes on your own (this **is** Level 5, after all), but feel free to shoot me questions._

---

### Visual Design 

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