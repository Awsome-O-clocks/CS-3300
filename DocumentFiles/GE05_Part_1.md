How to Set Up Generic List and Detailed Views for a Django Model
To set up generic list and detailed views for a Django model to be displayed in the web app, follow these steps:

Add URL mappings to your existing urls.py file.
Add class-based views to your views.py file.
Create new HTML templates for displaying additional model details based on the visited links.
Alter your original base template file.
Here's a summarized guide:

Add URL mappings to your existing urls.py file.
Add class-based views to your views.py file.
Create new HTML templates for displaying additional model details.
Alter your original base template file.
For detailed steps, refer to the Mozilla Developer Network guide.

CRUD Actions and Routes Created So Far
In terms of CRUD actions, the following have been implemented:

C (Create): Created and removed several student profiles, portfolios, and projects for testing.
R (Read): The web app is set up to read information from the database to display it.
D (Delete): Created and deleted student profiles, portfolios, and projects for testing.
Updating (U) hasn't been implemented yet.

Refer to the source for more information on CRUD operations.

Passing Information from Database to Display Active Portfolios on the Home Page
To display active portfolios on the home page, the following code is added to views.py:

python
Copy code
student_active_portfolios = Student.objects.select_related('portfolio').all().filter(portfolio__is_active=True)

print("active portfolio query set", student_active_portfolios)

return render(request, 'portfolio_app/index.html', {'student_active_portfolios': student_active_portfolios})
This code filters out portfolios set to active and prints them with the index.html template.

Explore the Python shell command line:

python
Copy code
student_active_portfolios = Student.objects.select_related('portfolio').all().filter(portfolio__is_active=True)
The code returns only portfolios set to active, those with the "active" checkbox selected when created.

Exploring Code in index.html - Built-in Template Tags and Filters
The index.html file serves as the home page of the web app and is an extension of the base_template.html file. The base template is used for the entire web app, while the index file specifically focuses on the home page.
