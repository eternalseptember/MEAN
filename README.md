Tutorial: https://thinkster.io/mean-stack-tutorial

## Notes:

1. In the "Opening REST Routes section", when running the CURL commands to rest routing, if there's a 404 error, then restart the npm server.

2. There are probably a lot of syntax errors in the "Adding Authentication via Passport" section.

3. From following the tutorial's instructions, the post author does not show up. http://stackoverflow.com/questions/31920189/post-author-not-displaying-angularjs-http-mongodb-thinkster-mean-stack-tu

## Modifications:

1. In the "Angular Services" section, after creating a posts factory and doing $scope.posts = posts.posts; I moved the original posts array to the factory.
  1. **BUG #1**

    As a result, after completing the "The Posts Page" section, in the posts page of any default posts, adding a comment does not work. The browser console said "TypeError: Cannot read property 'push' of undefined".

    Then a test comment was added to one of the default posts. Adding a comment then works, and upvoting comments works.

    **FIX:** Add ', comments: []' to the end of each default posts.

  2. **BUG #2**
  
    By the end of the "The Posts Page" section, the routing is not completely correct. For example, in index.html, the posts are listed in this order by title: ```post 3, post 4, post 1, post 5, post 2``` Then click on the comments page corresponding to "post 3" (the one with 15 upvotes). The title says "post 1" and the test comment is associated with "post 1", instead of the data associated with "post 3". http://stackoverflow.com/questions/32315922/issues-with-use-of-index-within-flapper-news-mean-stack-tutorial

2. Added an IncrementUpvotes function to the PostsCtrl controller. Not sure how comments were supposed to be upvoted in the tutorial.
  * It's addressed in the "Wiring Everything Up" section.

3. In the "Beginning Node" section, rather than just move the index and app.js files to their destination folders, I copied the files and then renamed them. Then I replaced the posts array in angularApp.js with what the instructions originally called for.