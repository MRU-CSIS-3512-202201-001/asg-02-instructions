# Assignment 02 - Milestone 01

**Due March 9 (W) @ 9 PM**

**Worth 3% of your final grade**

**Content in this milestone document takes precedence over anything you read in the [assignment pdf](comp-3512-asg-1-winter-2020-current.pdf).**

## Overview

This first milestone is meant to get the "plumbing" in place for the assignment. That is, you'll be setting up:

- your GitHub repo, 
- a Netlify site attached to that repo, 
- some Google Cloud Platform credits (that we will _probably_ use for this assignment), and 
- a nice-looking landing page. (With a somewhat-ominous timer in the console generated via JavaScript.)


## The Starting Repository

Accept the starting repo here: https://classroom.github.com/a/-l0WVGCq

## Your Mark

Your mark will depend on which requirements sections (see below) you complete.

For a section to be considered "complete", **ALL** requirements **in** that section must be complete.

| Completed Req's Sections | Grade Level | Corresponding % |
| :----------------------: | :---------- | :-------------: |
|           None           | Level 0     |       0%        |
|        RS1 - RS4         | Level 1     |       25%       |
|        RS1 - RS5         | Level 3     |       65%       |
|        RS1 - RS6         | Level 4     |       75%       |
|     RS1 - RS7 (good)     | Level 5     |       88%       |
|  RS1 - RS7 (excellent)   | Level 6     |       98%       |

_Yes, there are gaps in the levels shown. That'll happen for some milestones._  

_For the purpose of karma use, you can consider these levels contiguous. (**Translation**: if your current karma level allows you to go up 1 level, you could move from Level 1 to Level 3, or Level 4 to Level 6.)_

## The Requirements Sections

### RS1. Group Request Requirements

- [ ] [1] You have sent an email to JP with **either** a list of students that you do **not** want to work with on this assignment, or a list of students that you **do** wish to be in a team with (groups can have 2 or 3 members). If you have no preferences either way, say so in the email.


#### Notes

- _You will **not** be working with the same people for assignment 2. This means that if you request to work with certain people for **this** assignment, you will **not** be working with them for the next one. (So if you would rather work with certain people for assignment 2, wait to do so when that assignment is out.)_
  - _Rationale: You should be taking every opportunity to gain experience working with people you don't know. Yes, sometimes things can go wrong - but they can also go very right. Practice getting out of your comfort zone. And even if things **do** go "wrong", then dealing with that is a valuable experience as well._

---

### RS2. GitHub Repo Requirements

- [ ] [2] The code for your site is located in the GitHub repo created by accepting the GitHub Classroom assignment.
- [ ] [3] The `README.md` file in the repo contains your name and a **working** hyperlink to the Netlify URL of the page you wish me to mark. (Meaning I should be able to click on the link and go to your page!)
- [ ] [4] The Feedback pull request in the repo has not been closed or merged. I'm talking about this thing here:

  ![feedback](images/feedback.png)

  _This is important because this pull request gives me a simple way to communicate feedback with you. If you take that away from me, I will be peevish._

#### Notes

- _The GitHub Classroom assignment link is there upstairs in [The Starting Repository](#the-starting-repository) section._
- _Markdown (md) files are very common in our industry. You can find plenty of resources out there on how to include links in a markdown document._
- _I will only look at code in the `main` branch of the repo._

---

### RS3. Google Cloud Platform Credits Requirements

- [ ] [5] There is a clearly-named screenshot in your GitHub repository that shows me that you've claimed your Google credits. Here's an example:

  ![proof of credits](images/gcp-credits.png)

  _Note: you should have $50. I'm special! Yay, me!_

#### Notes

- _Instructions for claiming your credits are in [google-cloud-credits.md](google-cloud-credits.md)._
- _I did a [screencast](https://youtu.be/bs0VOP3KiM0) [6:35] last semester walking you through the process. It's pretty rambly, but mercifully short. You won't be getting an email with instructions as shown in the screencast - this semester, I put the text of that email in the instructions mentioned in the previous point._

---

### RS4. Hosting Requirements

- [ ] [6] Your application is hosted on [Netlify](https://www.netlify.com/).
- [ ] [7] The site name has been changed to `comp-3512-w2022-a1-<mru username>`. For example, if your username is jbond007, your site name should be `comp-3512-w2022-a1-jbond007`.


#### Notes

- _When you get to step where you are importing your GitHub repository, you need to first select our Organization and **then** your assignment repository:_

  ![import step](images/netlify-import-where.png)  

---

### RS5. Home Page Requirements

- [ ] [8] The home page is a resource named `index.html`.
- [ ] [9] All CSS on the site that is "yours" is declared valid by the [W3C CSS Validation Service](https://jigsaw.w3.org/css-validator/).
- [ ] [10] All HTML on the site is declared valid by the [W3C Markup Validation Service](https://validator.w3.org/).


When the home page is visited, the **Home View** is visible. See item 6 on page 2 of the [assignment pdf](comp-3512-asg-1-winter-2020-current.pdf). This means:

- [ ] [12] There is a hero image that fills the entire browser, at least up to 1800 pixels wide.
- [ ] [13] The hero image is appropriate to the theme of the site.
- [ ] [14] Credit information for the hero image is provided on the home page.
- [ ] [15] There is an obvious way to search for a movie by a title.
- [ ] [16] There is an obvious way to show all movies.


#### Notes

- _You do **not** need to follow the layout shown in the pdf. You just need to have the proper functionality._
- _The search and show all capabilities are **not** functional at this point._

---

### RS6. JavaScript Requirements

- [ ] [17] When the console is opened on the [Home Page](#5-home-page-requirements), a message detailing the number of days, hours, and minutes left until milestone 6 is due is shown. For example, if you go to the page on March 1 @ 7:00 PM, a message like `There is 1 day, 2 hours, and 0 minutes left until I am free.` would be humourously reasonable.
- [ ] [18] The message is generated through the use of JavaScript stored in a file called `countdown.js` that is linked to in `index.html`.
- [ ] [19] The code in `countdown.js` must use at least one function you create via a function declaration. (You may use additional functions if you wish.)
- [ ] [20] You must attribute any resource you use that helps you accomplish this task via comments in your code.

#### Notes

- _You can check whether your result is correct via a variety of sites. I use [this one](https://www.timeanddate.com/date/durationresult.html) personally._
  
---

### RS7. Visual Design Requirements

- [ ] [21] The visual design is portfolio-level quality. I'll be looking for generous use of whitespace, alignment of items, contrast of text in size and weight, good use of color (including accents), non-distorted images, etc.
- [ ] [22] The layout of the page is reasonable when viewed at Mobile L and Laptop L sizes in the Chrome device toolbar.


#### Notes

- _While the requirements in the other requirements sections are unambiguous, this section unavoidably uses vague terms like "portfolio-level quality" and "reasonable"._
- _Consider using Tailwind CSS to help make sure your site looks professional. It's quite the hot skill to have as well. You can use the ["Play CDN" method of installation](https://tailwindcss.com/docs/installation/play-cdn) for this assignment and avoid some of the usual overhead of installation._
- _If you wish to use another CSS framework, please talk to me. Anything other than Bootstrap, I'll consider - you've had experience with 'strap before, so it's time to spread your wings a bit._

