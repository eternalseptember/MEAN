Tutorial: https://thinkster.io/mean-stack-tutorial


## Modifications:

1. In the "Angular Services" section, after creating a posts factory and doing $scope.posts = posts.posts; I moved the original posts array to the factory.
  1. **BUG #1**

    As a result, after completing the "The Posts Page" section, in the posts page of any default posts, adding a comment does not work. The browser console said "TypeError: Cannot read property 'push' of undefined".

    Then a test comment was added to one of the default posts. Adding a comment then works, and upvoting comments works.

    **FIX:** Add ', comments: []' to the end of each default posts.

  2. **BUG #2**
  
    By the end of the "The Posts Page" section, the routing is not completely correct. For example, in index.html, the posts are listed in this order by title: ```post 3, post 4, post 1, post 5, post 2``` Then click on the comments page corresponding to "post 3" (the one with 15 upvotes). The title says "post 1" and the test comment is associated with "post 1", instead of the data associated with "post 3".

2. Added an IncrementUpvotes function to the PostsCtrl controller. Not sure how comments were supposed to be upvoted in the tutorial.

