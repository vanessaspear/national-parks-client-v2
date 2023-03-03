National Parks 
------

<img width="500" height="300" alt="National Parks Logo" src="https://res.cloudinary.com/decu5fbul/image/upload/v1677785031/National%20Parks/np_logo2_qedi0t.png">

### Application Overview

National parks are full of wonder, adventure, solitude, and freedom.  From the novice hiker to the seasoned outdoorsman, national parks are meant to be explored.  National Parks is a web application designed to make the parks more accessible to all types of explorers and provide resources for getting to know the parks and planning your next great adventure.  The app covers all things national parks including events, visitor blogs, campgrounds, wildlife and more that you can experience at each park.  Join our app, and get exploring!

This full stack application was created as part of a group learning project and consisted of three Agile sprints.  Our learning goals were to: 
- **Sprint #1**
  - Collaboratively plan out an application through the use of brainstorming, wireframing, and ERD creation
  - Utilize a Github project board to create issues and manage work across the team
  - Design and build a SQLite database and seed it with data for development purposes 
  - Create a RESTful API with Python to handle requests from the National Parks Client
  - Maintain a robust code base through the use of git/Github source control, detailed pull requests, and code reviews
- **Sprint #2**
  - Build out the essential components of the client using the React framework
  - This included creation of the landing page, nav bar, user login and registration, blog page, and individual park pages
- **Sprint #3** 
  - Redesign the API utilizing the Django REST framework 
  - Deepen understanding of the Django object relation mapping (ORM) API and user authorization process
  - Refactor the client to be compatible with the Django API
  - Upgrade the client to have a responsive design using the Bootstrap CSS framework
  - Enhance the client through the addition of features and functionality initially pegged as stretch goals

### Features
- Users can explore individual national park pages where they can view photos and blogs uploaded by visitors and explore wildlife, natural attractions, campgrounds, and amenities at each park
- Users can see a calendar of events happening or blogs written at all the parks or filter them by park 
- Users can favorite a photo, blog, park, or event and all favorited items will display on their personal profile page 
- Users can view park photos on an automated carousel and explore parks by list or map view
- Users can switch viewports without impacting their app experience through the use of responsive design
  
### User Experience

#### Welcome to the National Parks app
------
![](src/media/national_parks_landing_page.gif)

#### Add favorites and view them in your favorites hub
------
![](src/media/national_parks_favorites_hub.gif)

#### Search blogs and create a blog 
------
![](src/media/national_parks_blogs.gif)

### Technologies Used

#### Backend Technologies

<img alt="Python" src="https://img.shields.io/badge/Python-FFD43B?style=for-the-badge&logo=python&logoColor=blue"><img alt="Django" src="https://img.shields.io/badge/Django-092E20?style=for-the-badge&logo=django&logoColor=green"><img alt="Django REST" src="https://img.shields.io/badge/django%20rest-ff1709?style=for-the-badge&logo=django&logoColor=white"><img alt="SQLite" src="https://img.shields.io/badge/SQLite-07405E?style=for-the-badge&logo=sqlite&logoColor=white"><img alt="Leaflet" src="https://img.shields.io/badge/Leaflet-199900?style=for-the-badge&logo=Leaflet&logoColor=white"><img alt="GIT" src="https://img.shields.io/badge/GIT-E44C30?style=for-the-badge&logo=git&logoColor=white"><img alt="Github" src="https://img.shields.io/badge/GitHub-100000?style=for-the-badge&logo=github&logoColor=white"><img alt="VScode" src="https://img.shields.io/badge/VSCode-0078D4?style=for-the-badge&logo=visual%20studio%20code&logoColor=white">

#### Frontend Technologies

<img alt="Javascript" src="https://img.shields.io/badge/JavaScript-323330?style=for-the-badge&logo=javascript&logoColor=F7DF1E"><img alt="React" src="https://img.shields.io/badge/React-20232A?style=for-the-badge&logo=react&logoColor=61DAFB"><img alt="HTML5" src="https://img.shields.io/badge/HTML5-E34F26?style=for-the-badge&logo=html5&logoColor=white"><img alt="CSS" src="https://img.shields.io/badge/CSS3-1572B6?style=for-the-badge&logo=css3&logoColor=white"><img alt="Bootstrap" src="https://img.shields.io/badge/Bootstrap-563D7C?style=for-the-badge&logo=bootstrap&logoColor=white"><img alt="GIT" src="https://img.shields.io/badge/GIT-E44C30?style=for-the-badge&logo=git&logoColor=white"><img alt="Github" src="https://img.shields.io/badge/GitHub-100000?style=for-the-badge&logo=github&logoColor=white"><img alt="VScode" src="https://img.shields.io/badge/VSCode-0078D4?style=for-the-badge&logo=visual%20studio%20code&logoColor=white"><img alt="Miro" src="https://img.shields.io/badge/Miro-F7C922?style=for-the-badge&logo=Miro&logoColor=050036"><img alt="" src="">

In the planning stages, we used DB Diagram to create an entity relationship diagram and Miro to create a wireframe.  Both documents helped with solution design and were referenced throughout our work building out this app.  We also used a Github project board to create issues and manage work.

* [National Parks ERD](https://dbdiagram.io/d/63c84256296d97641d7a9114)

* [National Parks Wireframe](https://miro.com/app/live-embed/uXjVPwu3sLM=/?moveToViewport=-2065,-3562,12962,7754&embedId=240240661219)

* [National Parks Github Project - Sprint 1/2](https://github.com/orgs/nss-day-cohort-60/projects/2/views/1)

* [National Parks Github Project - Sprint 3](https://github.com/orgs/nss-day-cohort-60/projects/9/views/1)
            
### Running the Application

**Required dependencies:** 
- Python
- Django
- React 
- NPM
- Leaflet
- Bootstrap

Navigate to your workspace directory. 

Run the following command in terminal to setup the server:

```
git clone git@github.com:vanessaspear/national-parks-django-api.git
cd national-parks-django-api
python manage.py runserver
```

Seed the database: 
- Execute the __national_park_add_data.sql__ queries
- Then run the following commands in terminal
```
python3 manage.py makemigrations
python3 manage.py migrate
python3 manage.py loaddata users
python3 manage.py loaddata tokens
python3 manage.py loaddata event_types
```

Run the following command in terminal to setup the client:

```
git clone git@github.com:vanessaspear/national-parks-client-v2.git
cd national-parks-client-v2
npm start
```

You should now be able to sign in to the application. 

To demo the app, register as a new user with an email and password. 

Contributions
------
This project was a team effort between John Doll, Maia Dutta, Shaina Couch, Hazel Preza and Vanessa Spear. 

My direct contributions were:
- Created models for wildlife_groups, park_wildlife, natural_attractions, park_natural_attractions
- Created a photo view to handle requests from the client to view all photos, view photos by park, view photos by park and user, and create a photo
- Contributed to refactoring of SQL queries from client version 1 to be able to seed database without having to create fixtures
- Created the parks list component and parks map component on the client landing page 
- Reviewed pull requests and performed code reviews

Author
------

Vanessa Spear 

[<img alt="Github" src="https://img.shields.io/badge/GitHub-100000?style=for-the-badge&logo=github&logoColor=white">](https://github.com/vanessaspear)[<img alt="LinkedIn" src="https://img.shields.io/badge/LinkedIn-0077B5?style=for-the-badge&logo=linkedin&logoColor=white">](https://www.linkedin.com/in/vanessavspear/)
