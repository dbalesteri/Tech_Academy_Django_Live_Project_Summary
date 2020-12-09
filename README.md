# Tech_Academy_Live_Project_Summary

Over the past two weeks, as part of the Software Development Bootcamp  with The Tech Academy, I was tasked to be part of a team creating our own site application that was part of a larger overarching project called App Builder 9000.

![app_builder_gif](app_builder_main.gif)

This Live Project involved utilizing Microsoft Azure for project management, Git as the VCS, PyCharm as the IDE, and the Django framework.

All students were assigned user stories to complete in the two week sprint, adding increasingly more functionality and design to their section for users to interact with database information, as well as a chosen API. These user stories covered both front-end and back-end work in increasing difficulty. The project was meant to teach students team skills with working with version control as part of a team, using a project management software, participating in daily SCRUM meetings, as well as technical skills with expanding on using the Django framework's Model-View-Form structure to dynamically displaydatabase information to users, and interact with an API to display json data.

![azure stories](azure_stories2.PNG)
![user story boards](user_story_boards.PNG)




## I chose to make my section a pet rescue adoption site.

![site overiview_gif](overview.gif)




### Interacting with the database:

The site allowed individuals to post pet listings to display with various fields saved to a AvailablePet model: Name, Birthday(using a date-picker widget), Breed, Color, Contact Email, Location(using dropdown list of state abbreviations, Animal Type(dropdown list of available animal types to choose from), and a Description field(using a Text Area widget). This model also had a char field called "age", which was populated directly through user input, but a result of a function I wrote passing in the submitted Birthday date-widget information as an argument.

It also allowed individuals to post themselves as willing applicants to be contacted directly with their preference in pet, saved to an PetApplicant model.

For functionality of two forms to work on the same page, I added statements to check which submit button was being used in the post-request. The screenshots below shows the view for the page, and the function for populating the "age" field in the pet model in my desired format.

![applicant view](applicant_view.PNG)
![age calculation](age_calculation.PNG)

In viewing listings, the user is able to click more info, passing that pet's primary key into the url to view more details. The details page let's users delete the listing, with a pop-up modal asking if they're sure they want to delete that instance's name as defined in the modal: self.name + " the " + self.breed, and it also let's them edit the listing, with a confirmation page showing the pet instance's name they edited.

![edit pet details_gif](edit_details.gif)



### Parsing through JSON data from API


