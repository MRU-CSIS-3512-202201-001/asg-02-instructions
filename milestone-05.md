# Assignment 02 - Milestone 05 (WIP)

**Due: Officially @ 11:59 PM on April 7th**  
_(Unofficially whenever JP Gets Up & Starts Marking On April 8th)_

_I'm going to take Friday (Apr 8) off and just mark my brain off from whenever I get up. Historical data indicate that will be somewhere between 2 and 3 AM. Assuming it takes at most 2h to mark each one, that'll mean sometime late afternoon that day you'll have your mark and know your grades going into the final exam._

**Worth 7% of your final grade**

**Content in this milestone document takes precedence over anything you read in the [assignment pdf](comp-3512-asg-1-winter-2020-current.pdf).**


## Overview

This is it. 

The big enchilada. 

The culmination of 5 weeks of blood and brain fluid.

Run, stagger, or crawl over that finish line.

## OOPSIES & EXTENSIONS

If I catch one or two issues during marking that can be quickly fixed (IMO), then I will reach out to the group via email and inform them of the problem and give them the option to remedy the situation pronto. This will totally be at my discretion.

Otherwise, there will be no opportunity for fixin' or extension in this assignment. Full stop.

## Your Mark

I'm going to mark all pages, with higher weights going toward new stuff.

I'll also toss in some marks for an overall impression of the visual design of the site and the code craftsmanship.

### The Pages

| Page                 | Weight (%) |
| -------------------- | :--------: |
| Home (not logged-in) |     5      |
| Home (logged-in)     |     30     |
| About                |     5      |
| Browse               |     15     |
| Faves                |     20     |
| Login                |     5      |
| Registration         |     10     |
| Movie Details        |     10     |

### The Visual Design & Code Craftsmanship

I'll give the site's overall visual design and code craftsmanship each an "unacceptable" (U), "acceptable" (A), or "exceeds expectations" (E). I'll bump/drop folks up/down a letter-grade band based on the results like so:

| Results | Bump/Drop |
| :-----: | :-------: |
|  U + U  |  Drop 2   |
|  U + A  |  Drop 1   |
|  U + E  | no change |
|  A + A  | no change |
|  A + E  |  Bump 1   |
|  E + E  |  Bump 2   |

_For example, if you get an Acceptable in your coding craftsmanship and an Unacceptable in your visual design, your mark in this milestone would slide down one grade band. (`B-` to `C+`, `C` to a `C-`, etc.) Or if you get an Exceeds Expectations in both visual design and coding craftsmanship, you'd get bumped up two grade bands. (`A-` to an `A+`, or a `D` to a `C`, etc.)._


## Must-Haves

> If the following aren't met, I won't mark your submission.

- [ ] [MH.1] The Feedback pull request in the repo has not been closed or merged.

- [ ] [MH.2] There is a working link in the team repo's `README.md` that takes you to the Heroku URL for your application; this should cause your `index.php` (i.e. Home [Not Logged-In Version] page) to be displayed. 

- [ ] [MH.3]  I will validate 3 random pages from your site. (Which 3 pages will be determined before I start marking. The same 3 will be used for all teams.)

- [ ] [MH.4] The "plumbing" that was used in milestone 1 is present here: a valid Procfile, composer.json, and public folder containing your site's viewable files are present.

- [ ] [MH.5] No alerts are present in the site.

---

## The Pages

I'm going to be focusing solely on functionality of each page here, as the visual design will be assessed separately.

Notice I'll be re-checking older pages, as changes you've made since I last checked may have borked your earlier work.

Make sure you look through all the checkboxes. There have been some changes and clarifications.

### Home (Not Logged-In) (5%)

#### Expectations

- [ ] [HNLI.1] The page must be named `index.php`.

- [ ] [HNLI.2] There is an obvious way to log in to this page _in addition to_ the navigation header.

- [ ] [HNLI.3] There is an obvious way to sign up for an account _in addition to_ the navigation header.

- [ ] [HNLI.4] There is an obvious way to search for a movie title.

- [ ] [HNLI.5] There must be some sort of non-obnoxious way to **prevent** the user from initiating a search if there is nothing in the search box. The page should also **inform** the user when they try to do so in a non-obnoxious way.

    _I realize you could argue that searching using an empty search box should be the same as showing all movies. I kind of agree...but this brings in some extra complications that I'd rather we not deal with._

- [ ] [HNLI.6] Behind the scenes, when a title search is performed, it must cause your API to be queried and data stored in the browser's session storage for use in the Browse Page.

---

### Home (Logged-In) (30%)

#### Expectations

- [ ] [HLI.1] The logged-in user's first name, last name, city, and country are nicely displayed.

- [ ] [HLI.2] If the user has any favorited movies, they are clearly visible and nicely displayed here.

- [ ] [HLI.3] If the user has no favorited movies, that is nicely indicated.

- [ ] [HLI.4] 10 to 15 recommended movies are clearly visible and nicely displayed here. For more information on the recommendation process, see the appropriate page in the[ assignment pdf](comp-3512-a2-v1.pdf).

- [ ] [HLI.5] Each movie poster and title present hyperlinks to the `single-movie.php` page with an appropriate query string parameter.

- [ ] [HLI.6] The search box takes the user to the [Browse page](#browse-15) and behaves as if they had performed a title search from the [Home page](#home-not-logged-in-5).

---

### About (5%)

#### Expectations

- [ ] [AB.1] This page contains all of the following information:
  - [ ] university
  - [ ] class name
  - [ ] semester w/ year
  - [ ] web technologies used
  - [ ] team members with working links to their GitHub profiles
  - [ ] working link to the assignment source code on GitHub

- [ ] [AB.2] This page displays the current date and time in Alberta. PHP must be used to accomplish this.

- [ ] [AB.3] This page displays how many days, hours, and minutes are left until milestone 5 is due (April 7 @ 11:59 PM). PHP must be used to accomplish this.

---

### Browse (15%)

#### Expectations

- [ ] [BR.1] The file for this page is named `browse-movies.php`.

- [ ] [BR.2]  When a user first arrives on this page, any movies displayed on this page should be in alphabetic order by title.

- [ ] [BR.3]  When a user comes back to this page through the navigation menu, it should be as it was when they left it: in other words, any filters and sorting should be maintained between visits. How you accomplish this is up to you.

- [ ] [BR.4]  The types and behaviours of filters are the same as they were for assignment 1.

- [ ] [BR.5]  Filters can be either mutually exclusive or not, but whichever you choose, search fields are cleared appropriately when a user enters data in a search field.

    _This means if you're doing mutually-exclusive filters, then entering data in any type of field (title, year, rating) clears data in all other fields. If you're not doing mutually-exclusive filters, then entering data in a year or rating field clears data from other fields of that type only._

- [ ] [BR.6]  There should be an obvious way to clear the current set of filters. When this is done, the movies from the last title search are displayed. (This should be easy, as those movies are in the browser's session storage.)

- [ ] [BR.7]  There should be an obvious way to show/hide the filters. (Remember that this is different from clearing the filters.)

- [ ] [BR.8]  The types and behaviours of sorts are the same as they were for assignment 1.

- [ ] [BR.9]  Each poster and title hyperlinks to the `single-movie.php` page with an appropriate query string parameter.

- [ ] [BR.10]  When a movie is favourited, there should be a clear indication to the user that this has occurred. The same goes for when a movie is unfavourited.

- [ ] [BR.11]  (Un)favouritng should be done through the use of PHP, as described in the Favoriting section on page 6 of [the assignment pdf](comp-3512-a2-v1.pdf).

----

### Faves (20%)

#### Basic Expectations (15/20)

- [ ] [FAV.1] The file for this page is named `favorites.php`.

- [ ] [FAV.2] All requirements for this page are accomplished using PHP, not JS.

- [ ] [FAV.3] PHP sessions are used to track which photos have been favorited.

- [ ] [FAV.4] This page is only accessible if a user is logged in; if someone attempts to access this page while not logged in, they are directed to a generic error page.

- [ ] [FAV.5] A list of all favorited movies appears here.

  > _A reminder: logged-in users can favorite movies on both the Browse and Movie Details pages._

- [ ] [FAV.6] If no movies have been favorited, that is indicated clearly to the user.

- [ ] [FAV.7] There is an obvious way to remove movies - one or all - from the list.

- [ ] [FAV.8] The list displays each movie poster in thumbnail form (at a size appropriate for your layout) along with that movie's title.

- [ ] [FAV.9] Each poster and title hyperlinks to the `single-movie.php` page with an appropriate query string parameter.

- [ ] [FAV.10] (Un)favouritng should be done through the use of PHP, as described in the Favoriting section on page 6 of [the assignment pdf](comp-3512-a2-v1.pdf).

#### Additional Favouriting Expectations (5/20)

- [ ] [FAV.11] To get the additional 5% here, you must create another database table that stores any data necessary to keep track of a user's favourite movies. 

    _I do NOT want you to add extra fields to the users table - you should know enough from 2521 that this is a poor idea!_

---

### Login (5%)

#### Expectations

- [ ] [LI.1] An unsuccessful login attempt should clearly notify the user that there was a problem with their authentication.

- [ ] [LI.2] A successful login attempt should redirect the user to the Home (Logged-In Version) page.

- [ ] [LI.3] A logged-in user should see the Home (Logged-In Version) whenever they go to the Home page (via navigation or directly via the URL). Conversely, a logged-out user should NOT see the Home (Logged-In Version).
    
- [ ] [LI.4] A logged-in user should see a Favourites link in the navigation that takes them to the Favourites page. Conversely, a logged-out user should NOT see this link.

- [ ] [LI.5] A logged-in user should see a Logout link in the navigation that logs them out and redirects them to the Home (Logged-Out Version) page. Conversely, a logged-out user should NOT see this link (and should see a Login on instead).

- [ ] [LI.6] A logged-in user should NOT see a Registration link in the navigation. Conversely, a logged-out user SHOULD see this link.

- [ ] [LI.7] A logged-in user should see a way to favourite a movie when they visit a movie details page. Conversely, a logged-out user should NOT see a way to favourite a movie.

- [ ] [LI.8] A logged-in user should see a way to favourite movies displayed in the Browse page. Coversely, a logged-out user should NOT see such a thing.

- [ ] [LI.9] The tracking of whether a user is logged in our out must be done through the use of PHP's session state.

---

### Registration (10%)

#### Expectations

- [ ] [REG.1] All validations described in the bullet list in the Registration Page section of the pdf (page 9) are working.

- [ ] [REG.2] An appropriate mix of inline and after-submit validation is present to ensure that a user with JS enabled in their browser will submit a form with valid data.

- [ ] [REG.3] Any issues found are conveyed to the user in an informative way.

- [ ] [REG.4] If the client-side validation passes, but the user's email already exists in the Users table, the user is shown the form again - with their form entries still present - and an informative and well-presented error message is displayed.

- [ ] [REG.5] If the validation passes and the user's email is not present in the Users table, a new record is created in the Users table, the user is logged in (using a PHP session), and redirected to their Profile page.

- [ ] [REG.6] Passwords are saved using a bcrypt hash with a cost value of 12.

- [ ] [REG.7] For top marks on this page, the user can turn off JS in their browser and still have all necessary validations occur on the backend. Naturally, you wont' be able to do the inline-style type validation in this case, but that's ok. You will need to make sure that the user's entered data is still present in the form, as you don't want them to have to re-enter data.

---

### Movie Details (10%)

#### Expectations

- [ ] [MD.1] The page must be named `single-movie.php`. Be careful: some teams ignored this on milestone 3 and redirected to a differently-named page. That won't cut it here.

- [ ] [MD.2] The page must display all the movie data described in assignment one for this page, with the following exceptions: no speak or close buttons should be present and there must be an obvious way to favourite a movie **for a logged-in user**.

- [ ] [MD.3] The Cast and Crew must be ordered as outlined in the first assignment - quite a few teams missed this in milestone 3. Nope-nope for milestone 5.

- [ ] [MD.4] The movie data displayed must all come from the site's database.

- [ ] [MD.5] When a movie is favourited, there should be a clear indication to the user that this has occurred. The same goes for when a movie is unfavourited.

- [ ] [MD.6] (Un)favouritng should be done through the use of PHP, as described in the Favoriting section on page 6 of [the assignment pdf](comp-3512-a2-v1.pdf).

---

## Visual Design / Code Craftsmanship

### Visual Design

The visual design of all Views will be evaluated at both Mobile L and Laptop L size in a Chrome browser.

It's important that your site has a unified visual "feel".

#### Unacceptable Visual Design

 - [ ] The overall impression of the site is "oh dear...". There is no common site-wide theme and/or issues are numerous and glaring. You wouldn't show this to a potential employer or client.
 
#### Acceptable Visual Design

- [ ] The overall impression of the site is from "it's OK" up to "it's pretty good". The impression is that it was decided to make the visual design "good enough". There aren't many (or any) glaring issues, but there are definitely one or two issues that make you raise your eyebrows a bit. You'd be a bit hesitant showing this to a potential employer or client.

#### Exceeds Expectations Visual Design

- [ ]  The overall impression of the site is "wow" - it gives the impression that the visual design was a focus of attention. It's difficult, if not impossible, to find issue with the site. You would show this to a potential employer or client with no hesitation whatsoever.

### Coding Craftsmanship
This is a bit vague, but it kinda has to be. This category is meant to capture the big question: How easy is it to understand this codebase?

Some examples of things I'm looking for, in no particular order of importance:

 - Are variables named expressively or are they vague (or even worse, telling lies?).
 - Do you use appropriate methods, or do you recreate the wheel?
 - Are unneeded files removed from your repository?
 - Is the console free from error messages? This means the favicon message as well.
 - Is Intelephense happy, or sad?
 - Are global variables kept to a minimum - or are they flying all over the place?
 - Are foreach's used? Or noisy old-school fors?
 - Are functions plentiful, expressively named, and short? (remember, I'm a big fan of naming value-returning functions and non-returning functions in very specific ways)
 - Are tricky things documented?
 - Are things not yours documented?
 - Do you take the time to improve code borrowed from them web by improving names, removing outdated techniques, and following other good practices? Or are things just copy-pasta'd in as-is?
 - Are the various files well-named? Do they contain reasonable things? Are they smallish?

#### Unacceptable Craftsmanship

- [ ] The codebase is hard to understand and gives the impression it's largely stitched together with numerous sources copy-pasted from online sources. The guidelines provided above are largely ignored.

#### Acceptable Craftsmanship
- [ ] The codebase is reasonably easy to understand, although there are some violations of guidelines.

#### Exceeds Expectations Craftsmanship

- [ ] The codebase is expressive throughout and guideline violations are rare or not present.