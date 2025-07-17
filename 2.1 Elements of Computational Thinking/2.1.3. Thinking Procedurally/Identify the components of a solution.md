This is the stage in which the details about how each component is implemented are considered. You will see below how separating out these components has made it easier to identify a feasible and programmable solution.
In the same way that we broke down the problem, we must also build up to its solution. In order to identify the components of the solution, each programmer must evaluate the component of the problem allocated to them and assess how it can best be solved. Going back to our previous example involving the **book reservation system**, we need to consider the lowest-level components.

---
# Borrower Name
This could be implemented as a procedure, `getName()`, which checks to see whether or not a user is signed in to their library account. If they are already signed in, their name can be retrieved by querying the library’s database of users for the name of the borrower associated with the borrower’s ID. Users that are not signed in should be redirected to a page requesting them to either register or sign in. These options should redirect the user to the relevant form.

---
# Book Details
The user should be able to enter the name of the book into a text entry field, which would display the books stocked by the group of libraries. This could be implemented as a function that returns the ISBN of the selected book, which is easier to handle and can be more useful than a string.

---
# Collection Location
This input could also be implemented as a function that returns the location specified by the user. It is impractical to use a text entry field here, as this raises the likelihood of erroneous data being entered, such as a location where a library does not exist. Therefore, this data is best collected through a drop-down field in a form.

---
# Checkbook Availability
Another database query would have to be carried out to check whether books under the selected ISBN are currently on loan or available for borrowing. This problem could be programmed as a function that returns `True` if the book is available or `False` if not.
As an exercise, consider the ways in which the two final modules could be implemented. During this stage, it is also useful to identify tasks that could be solved using an already existing module, subroutine, or library. Reducing the complexity of the development stage by picking up on sections in which reusable components can be used is another benefit of using top-down design.
Finally, the components of the solution are combined to form a full, working solution.