# FAQ

More recent questions will be near the top.

#### Q. What's the password for the user accounts that are prepopulated in the users table?

> _A. They're all **mypassword**. (Take a look at the PDF in the Login/Logout Page section.)_

> _A. Remember that local storage and session storage have limits to how much they can hold. (Something like 5MB?) If you're trying to cram a bunch of movie info in there, your browser's gonna go all Michael Bay on you. In real life, we'd use another way of caching our results. Stupid real life...._ 

#### Q. When I do a title search that has lots of hits (like searching for 'a'), I get a weird JS error in the console. Whyz?

> _A. Remember that local storage and session storage have limits to how much they can hold. (Something like 5MB?) If you're trying to cram a bunch of movie info in there, your browser's gonna go all Michael Bay on you. In real life, we'd use another way of caching our results. Stupid real life...._ 

#### Q. The 'mypassword' password works for all the other users except for gcrannage1@mit.edu. Wassup?

> _A. Huh! Dirty data, apparently. I promise not to test with that mit dude. Jerk._ 

#### Q. Do I need to use PHP to create the movies shown on the Browse page?

> _A. Actually, no. You can use a lot of your assignment 1 logic here.  You will need to adjust your URLs a bit to take you to the correct single-move.php page. And faving things will need to involve PHP. But you can still have data from the API (your API!) stored in the browser's session storage like last time._ 

#### Q. Where should I put my html, css, images, and js files?

> _A. Put them inside your `public` folder. I'd suggest making subfolders for your css, images, and js stuff. Partials, constants, settings and such should go outside of the public folder._ 
