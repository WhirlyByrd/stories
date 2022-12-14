## Developer Stories

### Debuggin Through Trial and Error

Testing and debugging code is something that all developers must do for any project. I like to test regularly throughout the coding process. I test each function after it is written and sometimes I will check individual pieces within the function itself to make sure it is doing what I want. Using a simple console.log() will give me a good idea on what data is being returned or not.

When there is an error, I find that the first thing that should be checked is the console either inside VSCode or Chrome’s Dev Tools. The consoled error usually can identify where exactly the code failed to run. In my experience it is usually a simple typo or syntax error. Sometimes, though, I will scour my code and still not find the error. Paired programming helps to resolve this issue.

A second pair of eyes will more easily see what I cannot. I first learned this as a graphic designer. It is common practice to have other designers critique your project because they can either see mistakes faster or they can come up with very useful suggestions. Our brains tend to see what we think “should” be there and so we become somewhat blind to some of the most obvious mistakes. This is why I enjoy paired programming so much. We can help each other develop cleaner, less error prone code from the beginning. It makes a project run smoother and more efficiently in the long run. 

When in doubt, google is a developer’s best friend. Odds are that a developer has had the same problem before and has asked for help in a forum such as stackoverflow. There are many more useful resources like geeksforgeeks, w3schools, freecodecamp, and of course, Youtube. 

The bug may be simple and quick to resolve. It could be more complex than anticipated. Each time a bug is encountered is it an opportunity to learn something new. When I do resolve it, I come out with more experience. If or when the error occurs again, I should be able to resolve it faster. 



### Errors and Bugs During My DevMountain Capstone Project

#### Problem 1: Getting the item/to-do to append into the correct list. 
There were a few steps necessary to get my to-do objects to appear in the correct place. First, I used two separate JSON files, one to hold the lists and the other to hold to-dos. The to-do objects needed to be created with an id, input data, and a listId. With javascript I used dot notation to bring in the listId as a key in the new to-do object. 


#### Problem 2: When the first list was deleted, the to-do’s in the other lists would not populate.
This one required assistance from my instructor. It turns out I was not decrementing the listId whenever an axios delete request was being performed. This led to an error where the listId value was coming in as NULL instead of an integer. I added one more line of code to the delete function to reset the listId value by -1. 

#### Problem 3: Deleting an item from the list would sometimes remove a different item in a following list.
I had the wrong number set in my itemId variable after editing one of the JSON files. This was a quick fix in the end.

