
## User Stories and Feature Tasks

*As a user, I want an admin page so I can easily view the stats of my blog app.*

##done
- Set up a template for each row of the Author Stats section.
##done
- Call the Handlebars `.compile()` method when initializing the admin page. Make sure to assign the result of this method to the same variable name that is used when the author stats are appended to the DOM.
##done
- For both index.html and admin.html, we'll want access to the `Article.all` data, but we'll have different view functions to set up for each of those pages. Complete the `Article.fetchAll()` method so that it invokes a specific callback after all articles are loaded. 



*As a developer, I want to utilize IIFEs so that all of my function calls are executed on page load.*
## done
- Make sure each one of your scripts are properly enclosed. With the exception of `use strict;` and `var app = app || {};`, wrap the contents of article.js and articleView.js in an IIFE and give the IIFE a parameter called 'module'.
- Where the IIFE is invoked, pass in the new 'app' object as an argument to the IIFEs and be sure to remember to export the `Article` and `articleView` objects. Keep in mind that this will change how we refer to those two objects throughout the app.
  - Ensure both the index page and the admin page call `Article.fetchAll()` in a way that properly triggers the appropriate page setup methods.

*As a developer, I want to utilize functional programming so that my code makes sense and follows modern practices.*

- In the `loadAll()` method, refactor the old `forEach()` method to use `.map()` instead, since we are transforming one collection into another. Remember that we can set variables equal to the results of a function. So if we set a variable equal to the result of a `.map()`, it will be our transformed array. There is no need to push to anything.
- Chain together a `.map()` call and a `.reduce()` call to get a rough count of all words in all articles.
- Chain together a `.map()` call and a `.reduce()` call to produce an array of unique author names. You will probably need to use the optional accumulator argument in your reduce call.
- Transform each author string into an object with properties for the author's name, as well as the total number of words across all articles written by the specified author.
  - HINT: This `.map()` call should be set up to return an object literal with two properties. The first property should be pretty straightforward, but you will need to chain some combination of `.filter()`, `.map()`, and `.reduce()` to get the value for the second property.


## Documentation

```md
# Lab 09 Functional Programming

**Author**: Jay Adams
**Version**: 1.0.0 (increment the patch/fix version number up if you make more commits past your first submission)

## Overview
<!-- This is a blog page that that allows the user to also add new articles -->


## Architecture
<!-- Provide a detailed description of the application design. What technologies (languages, libraries, etc) you're using, and any other relevant design information.  The app uses HTML, CSS and Javascript. We are alos incorporating jquery and handlebars.  -->

## Change Log
<!-- Changes made.  
01-22-2018 9:30am - wrapped the contents of articleview and Article into IIFEs.

01-01-2001 4:59pm - Application now has a fully-functional express server, with GET and POST routes for the book resource.

## Credits and Collaborations
<!-- Ryan Palmer is a collabotator. -->
-->
```