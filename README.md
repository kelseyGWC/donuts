# donuts

I created this site to experiment with the Yelp API: https://www.yelp.com/developers/documentation/v2/overview

Yelp also has some display guidlines that I didn't fully implement in this example, but that we should make sure that our girls know about: https://www.yelp.com/developers/display_requirements

## what's in my code

My index.html file was based off of an example I found floating around the internet (I saw it in multiple places, and I think it originated in the Yelp API examples, but for some reason it isn't there any more): https://groups.google.com/group/yelp-developer-support/attach/5fc11c45b80baf2e/index.html?part=0.1&authuser=0&view=1

If the link doesn't work I found it on this message board: https://groups.google.com/forum/#!topic/yelp-developer-support/5bDrWXWJsqY

*Edit: I'm adding the file to the repository*

The example took care of OAuth (you get your keys/tokens/secrets when you make an account - though I haven't looked into how to make the access token secret hidden), doing the search, and returning the restaurant information as a list of json objects. You can take a look at the console to see what those objects contain, for example name, picture, websites, key words, etc.

I modified their example so that I displayed the name and picture of each donut shop, allowing the user to peruse the list by swiping left or right. In the header I added jQuery mobile and the apple-touch-icon so that the shortcut on my phone looks like a real app.

The biggest issues I faced was that the .on() function in jQuery wasn't supported in the earlier version used in the example (1.4.4), but the code dealing with the API didn't work when I used a newer version. Luckily I found this message board: https://github.com/Yelp/yelp-api/issues/2, which suggested adding the line "cache: true," inside the $.ajax() call, which resolved the issue :)


