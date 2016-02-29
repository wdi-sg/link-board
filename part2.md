#Linkboard Part 2

To finish up the Link Board assignment, implement **at least 5 of the following:**

* Add comments (one-to-many easy)
* Add comments to comments (polymorphic, self-referencing)
* Add voting to comments (one-to-many)
* Use modals for auth
* Use modals for adding posts or comments
* Add AJAX Delete to comments
* Change the color scheme/styling using SASS
* Add User Profile page
* Display vote counts
* display comment counts


## Comments

For this part you have 2 choices. Single level comments (like facebook) or nested comments (like reddit).

### Easy mode - Single level comments

This will allow users to post comments about posts. The comments are NOT polymorphic so they can only be applied to posts. You cannot comment on other comments.

* user - reference to user model (comment creator)
* post - reference to post model (comment target)
* body - comment text


### Hard mode - Nested comments

This will allow for nested comments (comments on comments) which makes it more like reddit's actual comment system. Be aware this gets pretty tricky especially in setting up the models and displaying the nested comments.

**hint:** You'll need to create a recursive partial view to make comments render.

* user - reference to user model (comment creator)
* commentable - reference to ANY model (comment target. A post or another comment)
* body - comment text

## Voting

Since we already have a polymorphic vote model now we just need to associate votes to comments (same as associating them to posts). Users should be able to up / down vote comments just like they can on posts.
