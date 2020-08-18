I'd like to talk about my capstone project proposal.  



# Capstone project proposal outline

## Project overview

This site will allow users to view a photo and the corresponding location on a map where that photo was taken. Users will be able to search for photos based on location and time and see similar photos. They will be able to see the history of a location. Or to share their photo collection with others.

## Application purpose
The application will allow users to interact with their photos in ways that are not readily available now.  There are photo services that allow a user to see the location of the photo, i.e. google photos.  But the controls for filtering are just not there.  Imagine having photo albums readily available of all your birthdays, or Christmases.  Imagine being able to filter photos by month or season.  Or to see your personal history of a place by seeing your photos displayed on a map.  

## Front end

### Welcome page

1. Site navigation
2. Introductory section describing site and objectives of photo service
3. Links to the main sections of the site with short descriptions
4. Ability to sign in

### Photos + Map page

1. Add a photo to a collection
2. Filter by date
3. Filter by tag
4. Anyone should have the ability to comment on each Photo that has been shared with another user. Comments will have the user name and time/date of comment listed. Users should be able to edit or delete their comments. Edited comments will be automatically marked as such.

### Collections page

The purpose of this page is to provide a way of organizing photos. A collection can be shared with another user but never globally.

1. Add or remove collections
2. Give/Remove permissions to view a collection

### User Registration

1. Users will register a unique email address.

### Login Page

Allow users to sign in using an email address

1. Login will use email as a username. The user will be able to set a password

### Profile

1.  User will be able to change profile information including, name, password

## Data structures and models

List the important models that will need to exist in the application for it to function as you intend, and indicate how those models are associated with each other. Include any important attributes for these model.

### Photo

- file_name
- file_type
- file_size
- gps_location
- tags
- collection
- user

### Album

- authorized_users: users
- user: references (owner of album)

### Tag

- name
- photo_id: references

### Comment

- body:text
- user:references
- photo:references

### User

- first_name
- last_name
- email
- Photos
- Album

## Third party services

Include a list of all third party services that you envisage using in your project. For each one, indicate what they will be used for. These include:

- Ruby gems or JavaScript libraries outside of those bundled with Ruby on Rails by default.

- Active Storage - To store files and to parse exif data
- Amazon S3
- Google maps gem
- Bootstrap 5 CSS
- Password hashing: bcrypt gem
- Pagination: Kaminari
- Deployment service: Heroku
- Database: PostgreSQL, pg gem
