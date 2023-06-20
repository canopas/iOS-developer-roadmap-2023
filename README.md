# iOS-developer-roadmap-2023

![alt text](https://github.com/canopas/iOS-developer-roadmap/blob/main/assets/road-map.png)

The iOS Developer Roadmap 2023 includes **29 practical exercises** that cover all the essential concepts used in day-to-day development.

# Guidelines
- Before starting any practice, it's essential to conduct research and learn the necessary concepts.

- As you go through the practical exercises, please make sure to apply the new knowledge you've gained in subsequent practices. Try to allocate a maximum of 5 days to each practical.

- Follow iOS [Human Interface Guidelines](https://developer.apple.com/design/human-interface-guidelines) for the best practices of user interface design.

- Follow iOS [App Life Cycle](https://developer.apple.com/documentation/uikit/app_and_environment/managing_your_app_s_life_cycle).

- Follow the recommended app architecture for developing an iOS app.

# Table of contents
* [Useful references]()
* [iOS Storyboard / XIB]()
* [ViewController]()
* [SwiftUI]()
* [Networking]()
* [App Architecture]()
* [DataStore]()
* [Database]()
* [Dependency Injection]()
* [Combine]()
* [Broadcast receiver]()
* [iOS Service APIs]()

## Useful references
The references provided are aimed at individuals who have no prior knowledge or experience in developing iOS apps. They serve as a starting point for beginners in the field, providing basic knowledge that is necessary before diving into iOS development. 

If you already have knowledge and experience in iOS development, you may not need to refer to the provided resources.

* Introduction to [Swift programming](https://docs.swift.org/swift-book/documentation/the-swift-programming-language/thebasics)
* Basic introduction to [Swift Playgrounds](https://www.appcoda.com/learnswift/playgrounds.html).
* Basic introduction to [Xcode Interface](https://developer.apple.com/documentation/xcode)
* Basic introduction to [Version Control System](https://www.geeksforgeeks.org/version-control-systems/)
* Udemy Course - [iOS App Development Bootcamp](https://www.udemy.com/course/ios-13-app-development-bootcamp/)
* [SwiftUI](https://developer.apple.com/xcode/swiftui/)
  * [Overview with Udemy](https://www.udemy.com/course/ios-13-app-development-bootcamp/learn/lecture/16254084#overview)
* [Combine](https://developer.apple.com/documentation/combine) - A Declarative Swift API for processing values over time.

# iOS Storyboard / XIB
### Practical 1

#### Messaging Application
* Implement an app using 3 view controllers - Onboard, sign-in, and Home.
* On the onboard screen, show a brief introduction to the app's features, such as messaging, voice and video calls, and file sharing.
  - Show images, titles, and subtitles to introduce app functionality.
  - Add a button to check the next/previous features. Also, the skip button to skip the onboarding flow.
* On the sign-in screen, allow the user to enter their email and password, and add validation to ensure the user enters a valid email address and password.
  - Use a dummy email/password to verify user input.
* After a successful login, the user should be redirected to the Home screen.
  - On the Home screen, show a list of chats with the sender name, profile, latest message, and message time.
  - The user should not be able to go back to the login screen once redirected to the Home screen.
  - Use dummy data for chats.
  - Add a toggle button on the Home screen to change the day/night theme.
* App should responsive for different resolutions(for different devices).
* Add support for light/dark themes.
* You can use any images or placeholder to make UI eye-catchy.
* App should follow UI guidelines.
* Here's [UI for reference](https://cdn.dribbble.com/userupload/3719280/file/original-5d6d206acf8adf5458091206369445f1.png?compress=1&resize=752x)

### Practical 2
#### News Application
* Develop collapsing toolbar for the News application.
* Home screen should show a toolbar and news content.
* The toolbar on the screen should initially display the app's logo and title.
* As the user scrolls down to read the news, the toolbar should collapse to provide more space for the content.
  - You can use any dummy text/images as article content.
* When the user reaches the end of the news and reverses scrolls, the toolbar should re-expand and display the app's logo & title
* You can use any image or placeholder to make UI eye-catchy.
* Here's [UI for reference](https://cdn.dribbble.com/users/663782/screenshots/3742414/media/67464fde751beb373b4c6fa962edf718.gif)

### Practical 3
#### Survey Application
* App will have one screen.
* On the Home screen display a survey form.
  - Survey form should show questions, 4 options, and a button for the next question.
  - Show progress as the user answers the question.
* Once the survey is completed, show a pop-up message for thanking the user.
  - Use the custom dialog to thank the user.
  - Dialog will have UI to show a thanks message, image, and button to complete the survey.
* Asks at least 3 questions with 4 options each. 
* App should ask users about the shopping experience. 
* You can use any images or placeholder to make UI eye-catchy.
* Here's [UI for reference](https://cubicleninjas.com/wp-content/uploads/2021/01/NA-2021-Web-Questionnaire-3.jpg)

# ViewController

### Practical 4
#### Video Player 
* This will be a single-screen app.
  - The app should have a view to show video.
  - One button to play and pause the video.
* The player should follow the view controller's lifecycle, pause the player when the controller goes to the background and resume it when the controller returns to the foreground. 
* The player should also release resources when the app is no longer alive.
* An application can play a video from a local resource. 
* Use Swift's AVPlayer to play media.

### Practical 5
#### SnapCam
* This will be Two screen app.
* Home screen should have PreviewView to show a camera
  - It should have a button to capture an image.
  - Button to show captured image preview.
  - Save button on the Toolbar to save captured images to the device's gallery.
* On Preview Screen show the image in fullscreen.
  - Use Kingfisher for image preview.
  - Add a button to go back to the camera screen.
  - Open this screen by setting up the segue with the parent controller.
* The camera resources should be released when the controller is no longer alive.

### Practical 6
#### Note-taking Application
* Single-screen app
  - Which allows the user to enter a note.
  - Use the text field to take input from the user.
  - Add a button to reset the note.
* The application should have the ability to maintain the state of the text field, even after the device is rotated.
* This means that when the user rotates the device, the text field should retain its previous contents, and the user should be able to continue editing the note without losing any data.

### Practical 7
#### Travel Application
* Home screen should have a bottom bar with 3 tabs: Destinations, Search, and Settings. 
* The Destinations tab should display a list of popular travel destinations with images and descriptions.
  - Use a table view to show a list of destinations.
* The Search tab should Allow the user to search for destinations.
  - Add a search view to search different destinations.
  - Show a message in the label to notify the user when the searched destination is not available.
  - Use dummy data for destinations.
* The Settings tab should allow the user to customize app settings.
  -  Add a toggle button for notification and light/dark mode settings.
* App should preserve the state on tab change.
  - If the user scrolled to the bottom of the destinations screen, it should preserve the scroll state across the tab change.
  - If a user searches for something on the search screen, the search result should be there when navigating to the search tab from other tabs.
  - If the user changed the setting's toggle, it should stay as it is when the user navigates between the tabs

### Practical 8
#### Recipe Lister Application
* Single navigation app with two controllers - Home & Detail screen
* On the Home screen add a collection view to display the list of recipes.
  - Each list item should show the recipe name and image.
  - Cell should be shown as a square.
  - Show a number of cells horizontally:
    - Portrait:  phone - 3, iPad - 5
    - Landscape: phone - 4, iPad - 6
  - Tapping a recipe should open the Detail screen.
  - It should allow drag and drop of the cells.
  - should have an edit button on the toolbar to delete items.
* On the Detail screen show full recipe detail with recipe image and description.
  - Add a back button to navigate back to the list of recipes.
* Use dummy data for recipes.

### Practical 9
#### App Browser
* On the Home screen add an input field where the user can enter a URL and a button to open the URL inside the app.
* Once the user enters a valid URL and clicks the button, show a web view that slides up from the bottom of the screen.
  - This screen will show the content of the URL within a web view. 
  - The screen will also have a button to close the web view. 
  - Add a menu in the toolbar, which will have two options- copy and share the link.
    - Copy option should copy the link to the clipboard.
    - The share option should allow users to share links in other applications.
* The state of the controller should be preserved on configuration changes such as screen rotation.

### Practical 10
#### QuickSend Application
* This will be single screen app - QuickSendViewController
* QuickSendViewController allows users to send emails
  - Add a text field to input the receiver's email address and email content.
  - Add a button to send an email.
    - On click of it, the app should ask for the app to choose to send mail on.

### Practical 11
#### TalkEasy Application
* The app will send and receive messages between two screens.
* The app will use two controllers - Sender & Receiver.
* The Sender controller should have an edit text and a send button
  - When the user enters a message and clicks on the send button, open the Receiver screen and show the message received from the Sender screen.
* The Receiver activity should have an edit text and a reply button
  - When the user enters a reply message and clicks on the reply button, the replied message should be sent back to the Sender screen and displayed in a text view. 

### Practical 12
#### Create Deep Links to App Content
* Implement an app that handles incoming links.
* The app will use one screen - HomeViewController
* On Click of this link https://open.my.app/?message={anymessage} from anywhere, the system should open HomeViewController and show the message from a link.
* Use the URL schema in the App Delegate to handle deep links.

# SwiftUI

### Practical 13
#### User Profile UI
* The app will use a single screen.
* Display a user's profile picture, name, and bio. 
* Use a placeholder for the image and profile data.
* Add light/dark theme support.
* Here's [UI for reference](https://cdn.dribbble.com/userupload/5207044/file/original-ceb3338a4a693f6ab102298dd3745716.jpg?compress=1&resize=1024x768)

### Practical 14
#### Fitness Application
* App will provide a guided introduction to the app's features and functionality.
* The onboard view should include a welcome message and an introduction to the app's primary features, such as tracking workouts, setting goals, and accessing workout routines. 
  - The onboard screen should have interactive elements such as buttons or sliders that allow the user to interact with the onboard screen.
    - There should be next & previous buttons to go through features.
    - Add an indicator to show pages.
    - Add an option to skip the onboarding process.
* After onboard flow completion navigate the user to the Home screen.
  - The home screen should show basic tips & tricks related to fitness
  - Add option to log out, on logout show onboard view.
* Here's [UI for reference](https://cdn.dribbble.com/users/2321513/screenshots/13623207/media/00046acbffbf953281b06b5bf4685dfd.mp4)

### Practical 15
#### MathQuest Quiz Application
* The home screen should be an entry point of the app.
  - This should provide an introduction to the quiz and a button to start the quiz. 
* The quiz should ask 10 questions, one at a time, and provide four answer options for each question. 
  - On click of the next button highlight the correct/wrong answer and show the next question.
  - Show progress as the user answers the questions.
* After the user answers all questions, the app should display a result view.
  - Which shows the number of correct answers and the total number of questions. 
  - Show the excellence level based on the score such as poor, good, and very good. 
  - Add a button to restart the quiz so that the user can play again.
* Implement a day/night theme in the Quiz app.
* You can use images and placeholders to build eye-catchy UI
* Here's [UI for reference](https://cdn.dribbble.com/users/2469034/screenshots/8210470/media/f02da6249ee8c25f187432c73d4eec27.png)

# Networking

### Practical 16
#### ImageSaver Application
* Allow users to download an image from a given URL, display the image on the screen, and store the downloaded image file in the device's internal storage.
* Screen will have one Text field to enter the URL.
* Buttons to download images and cancel downloads.
* Show download progress in the progress bar and in the notification.
* Show the downloaded image on full screen, once the download succeeds.
* Add a button to save downloaded images in Gallery.
* Use Alamofire for networking.

### Practical 17
#### OnlineUserDirectory
* The app will use one navigation view.
  - The main screen should show a list of users, retrieved from API.
  - Use Lazy Stack to show users.
  - Show summary of user in the list including name, image, and email
  - GET Api Url: http://jsonplaceholder.typicode.com/users
* On the user-item click, display all albums of the user on the next screen. 
  - Use GridView to show albums
  - Show placeholder image for an album to make UI eye-catchy
  - GET Api Url: https://jsonplaceholder.typicode.com/albums?userId=1
* On the Album item click, show all photos of the album on the next screen.
  - Use GridView to show photos.
  - Show thumb image in Grid.
  - Use Kingfisher to show the image.
  - On click of items show the image in full screen.
  - GET Api Url: http://jsonplaceholder.typicode.com/photos?albumId=2
* Use Alamofire for networking

# App Architecture 

### Practical 18
#### My Journal Application
* Enable users to Add their daily thoughts, feelings, experiences, and ideas. 
* The app will have a one-navigation view.
  - Show the user's thoughts in Grid.
  - Add TextField to take user input.
  - Add a button to save the user's thoughts.
  - Store inputs in ViewModel as a state.
* User should be able to add multiple thoughts.
* The application should be able to persist data even when there is a configuration change, such as screen rotation.
* Use MVVM app architecture

### Practical 19
#### Drink Explorer Application
* Allow users to search for their favorite mocktail detail.
* The app will have single navigation.
  - Add a search bar that allows users to search for mocktails by name.
  - GET Api Url: https://www.thecocktaildb.com/api/json/v1/1/search.php?i={mocktail}
  - Default search text should be `mocktail`. That means initially showing `Mocktail` in the search bar and fetching `mocktail` using API
* When the user taps on a mocktail, the application should display the ingredients and detail of the mocktail. 
  - Use placeholder and dummy data if required.
* Use MVVM app architecture

# DataStore

### Practical 20
#### Authentify Application
* An application that takes user credentials and basic information of a user and navigates to the home screen after a successful login.
* The app will have a single navigation view.
  - First, the app will show the register form
    - Take the user's name, email, and password for login
    - Other basic information such as an address, DOB, blood group and gender, etc.
    - Add validation for email and password
    - Save user detail in UserDeafult.
  - After registering, show a login form
    - Take email and password
    - Check whether the user is available or not. If the user does not exist, notify the user to do registration
    - Add validation for email
* Once the user logs in, the app should always show the home screen
  - It will show user details
  - Add logout & delete user option in the toolbar
  - Clear user session on logout
  - Until the user logs out app should show the home screen.
  - When the user clicks the logout/delete user button, the app should clear/delete the user session and navigate back to the login screen.

# Local Storage (Database)

### Practical 21
#### EmployeeHub Application
* The application should display a list of employees on the home screen.
  - Show basic details including their name and job title. 
* When a user clicks on an employee from the list, the application should display their full details.
  - including their contact information, job title, and other important information. 
* The user should be able to add new employees to the directory by entering their basic information and saving it locally. 
  - Save employee name, email, contact info, job title, address, DOB and blood group, etc.
* Additionally, the user should be able to update an employee's information by selecting them from the employee list and editing their details.
* Finally, an employee should be deleted by swiping to delete from the home screen.
* Use SQLite to store data locally.
* Use MVVM app architecture

### Practical 22
#### MinionSpeak Application
* Allow users to translate English text to the language of the minions and display the translated text on the screen.
* On the Home screen
  - Add a text field to enter the English text.
  - Add a button to translate. With the click of a button make an API call.
  - Once the translation is complete, the translated text should be displayed on the screen in the language of the minions.
  - GET Request API with query parameter- “text” https://api.funtranslations.com/translate/minion.json?text=”banana”
* Additionally, the application should store the translation history locally so that users can access their previous translations.
* Add fab button to check history on the home screen
* Add an option to delete the history.
* Use Core Data database.

# Dependency Injection

### Practical 23
#### University Directory Application
* Allow users to browse and search universities from all around the world.
* On the Home screen
  - Add a dropdown to select the country
  - When a country is selected, display a list of universities located in that country from API.
* Use Swinject for dependency injection.
* GET Request API: http://universities.hipolabs.com/search?country={country name}
* Write a Unit test for ViewModel.

### Practical 24
#### Offline-first StoreMate Product Application
* GET API: https://fakestoreapi.com/products
* On the Home screen
  - Retrieve the list of products from an API and displays it to the user.
  - Make UI like a collection view using SwiftUI
  - Show product name, image and button to favourite/unfavourite product.
* Allow the user to view the product by clicking on it. 
  - Show all detail of the product
  - Add an option to favourite/unfavourite the product
* Add an option on the home screen to view favourite products.
  - Show all favourite products
  - Add option to remove from favourite
  - Add option to remove all favourite item
  - Users can select multiple items with a long click and can remove all selected products from their favourites.
* The application should have offline functionality, allowing the user to continue browsing products even when they do not have an internet connection.
* The product data should be first fetched from the local database and then sync with remote API data.
* Add swipe-to-delete functionality to remove products from local storage.
* Add swipe-to-refresh functionality to refresh the local database with remote data.
* Write a Unit test for ViewModel.

# Combine

### Practical 25
#### Count-down Timer Application
* On the Home screen
  - Add text fields to take user input for hours, minutes and second
  - Button to start/stop the timer
  - Show remaining & elapsed time 
* The user should be able to set the duration of the timer and start it. 
* When the timer ends, the app should display a notification to indicate that the time is up.
* Also play sound and vibrate the device on the timer completes.
* Write a Unit test for ViewModel.

### Practical 26
#### VocabVault Application
* Allow users to search for the definition of any word in the English language.
* On the Home screen
  - Users should be able to search for a word by typing it into a search bar
  - App should display as user type in the search view
  - The app should display the word's definition along with pronunciations, parts of speech, examples, and synonyms.
  - Add an option to play pronunciations of the word
* Make sure the app will not make unnecessary API calls while typing in the search view.
  - Use debounce using combine to avoid extra API calls
* API - https://api.dictionaryapi.dev/api/v2/entries/en/<word>.
* Write a Unit test for ViewModel.

### Practical 27
#### Contact Keeper Application.
* On the Home screen
  - Show all Contacts on the home screen
    - Show name, phone number, and profile
    - On click of contact show the contact profile
  - Add option to update contact detail
  - Add an option to delete a user by swiping to delete
  - Add option to add contact with person name, multiple phone numbers, profile image, birth date, and address
* Add screen to edit/show contact detail
  - Add option to delete contact
* The app should also update contacts in real-time, so changes made by one user are reflected across all devices.
* Use Firestore to store contact details.
* Use Combine with SwiftUI.
* Write a Unit test for ViewModel.

# Broadcast receiver & Task scheduling

### Practical 28
#### Stand Up! Application 
* Remind users to stand up and walk around every fifteen minutes.
* On the Home screen
  - Add a Toggle button to turn the alarm on and off
  - Add option to set reminder start time 
    - Open Timepicker to select a reminder to start the time
* The application should display a notification when fifteen minutes have passed since the last reminder.
* Use UNUserNotificationCenter Swift API to schedule reminder notifications.

# iOS Service APIs

### Practical 29
#### Music Player Application
* Allow users to play multiple songs. 
* On the Home screen
  - Show a list of songs from the device
  - On click of the song  open the player from the bottom
  - Show play indicator for current playing song
* On the Player screen
  - Show song thumb image if available or use placeholder
  - show song name
  - Add an option to play/pause the song
  - Add an option to play the next/previous song
  - Add an option to forward/backward the song by 10 sec
* Use an AVFoundation to play music in the background and show a notification of the current music being played.
