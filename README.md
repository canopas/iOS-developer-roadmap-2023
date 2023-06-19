# iOS-developer-roadmap-2023

![alt text](https://github.com/canopas/iOS-developer-roadmap/blob/main/assets/road-map.png)

The iOS Developer Roadmap 2023 includes **29 practical exercises** that cover all the essential concepts used in day-to-day development.

# Guidelines
- Before starting any practical, it's important to conduct research and learn the necessary concepts.
- As you progress through the practical exercises, make sure to apply the new knowledge you've gained in subsequent exercises.
- Follow iOS [Human Interface Guidelines](https://developer.apple.com/design/human-interface-guidelines) for the best practices of user interface design.
- Follow iOS [App Life Cycle](https://developer.apple.com/documentation/uikit/app_and_environment/managing_your_app_s_life_cycle).
- Follow the recommended app architecture for developing iOS app.

# Table of contents


## Useful references
The references provided are aimed at individuals who have no prior knowledge or experience in developing iOS apps. They serve as a starting point for beginners in the field, providing basic knowledge that is necessary before diving into iOS development. 

If you already have knowledge and experience in iOS development, you may not need to refer to the provided resources.

* Introduction to [Swift programming](https://docs.swift.org/swift-book/documentation/the-swift-programming-language/thebasics)
* Basic introduction to [Swift Playgrounds](https://www.appcoda.com/learnswift/playgrounds.html).
* Basic introduction to Xcode Interface
* Basic introduction to Version Control System
* App Architecture
* Udemy Cource - [iOS App Developement Bootcamp](https://www.udemy.com/course/ios-13-app-development-bootcamp/)
* [SwiftUI](https://developer.apple.com/xcode/swiftui/)
  * [Overview with Udemy](https://www.udemy.com/course/ios-13-app-development-bootcamp/learn/lecture/16254084#overview)
* [Combine](https://developer.apple.com/documentation/combine) - A Declarative Swift API for processing values over time.

# iOS Storyboard / XIB
### Practical 1

#### Develop UI for a Messaging application
* Implement an app using 3 view controllers - Onboard, signIn and Home.
* On the onboard screen, show brief introduction to the app's features, such as messaging, voice and video calls, and file sharing.
  - Show images, titles and subtitles to introduce app functionality.
  - Add a button to check the next/previous features. Also, the skip button to skip the onboarding flow.
* On the sign-in screen, allow the user to enter their email and password, and add validation to ensure the user enters a valid email address and password.
  - Use dummy email/password to verify user input.
* After a successful login, the user should be redirected to the Home screen.
  - On the Home screen, show a list of chats with sender name, profile, latest message and message time.
  - The user should not be able to go back to the login screen once redirected to the Home screen.
  - Use dummy data for chats.
  - Add toggle button on Home screen to change the day/night theme.
* App should responsive for different resolutions(for different devices).
* Add support for light/dark theme.
* You can use any images or placeholder to make UI eye-catchy.
* App should follow UI guidelines.
* Here's [UI for refrence](https://cdn.dribbble.com/userupload/3719280/file/original-5d6d206acf8adf5458091206369445f1.png?compress=1&resize=752x)

### Practical 2
#### Develop collapsing toolbar for the News application
* Home screen should show toolbar and news content
* The toolbar on screen should initially display the app's logo and title.
* As the user scrolls down to read news, the toolbar should collapse to provide more space for the content.
  - You can use any dummy text/images as article content.
* When the user reaches the end of the news and reverses scrolls, the toolbar should re-expand and display the app's logo & title
* You can use any image or placeholder to make UI eye-catchy.
* Here's [UI for reference](https://cdn.dribbble.com/users/663782/screenshots/3742414/media/67464fde751beb373b4c6fa962edf718.gif)

### Practical 3
#### Implement Survey application
* App will have one screen.
* On the Home screen display a survey form.
  - Survey form should show questions, 4 options and a button for next question.
  - Show progress as user answers the question.
* Once the survey is completed, show a pop-up message for thanking the user.
  - Use the custom dialog to thank the user.
  - Dialog will have UI to show a thanks message, image and button to complete survey.
* Asks at least 3 questions with 4 options each. 
* App should ask users about the shopping experience. 
* You can use any images or placeholder to make UI eye-catchy.
* Here's [UI for reference](https://cubicleninjas.com/wp-content/uploads/2021/01/NA-2021-Web-Questionnaire-3.jpg)

# iOS ViewController

### Practical 4
#### Implement Video player 
* This will be single screen app.
  - App should have a view to show Video
  - One button to play and pause video
* The player should follow the view controller's lifecycle, pause the player when the controller goes to the background and resume it when the controller returns to the foreground. 
* The player should also release resources when the app is no longer alive.
* An application can play a video from local resource. 
* Use Swift's AVPlayer to play media.

### Practical 5
#### Implement SnapCam
* This will be Two screen app.
* Home screen should have PreviewView to show camera
  - It should have button to capture image.
  - Button to show captured image preview.
  - Save button on Toolbar to save captured image to the device's gallery.
* On Preview Screen show image in fullscreen.
  - Use Kingfisher for image preview.
  - Add button to go back to camera screen.
* The camera resources should be release when the controller is no longer alive.

### Practical 6
#### Implement Note-taking application
* Single screen app
  - Which allows the user to enter a note.
  - Use text field to take input from the user.
  - Add a button to reset the note.
* The application should have the ability to maintain the state of the text field, even after the device is rotated.
* This means that when the user rotates the device, the text field should retain its previous contents, and the user should be able to continue editing the note without losing any data.

### Practical 7
#### Develop a Travel application
* Implement the app using with screen only.
* Home screen should have a bottom bar with 3 tabs: Destinations, Search, and Settings. 
* The Destinations tab should display a list of popular travel destinations with images and descriptions.
  - Use table view to show list of destinations.
* The Search tab should Allow the user to search for destinations.
  - Add search view to search different destination.
  - Show a message in label to notify the user when the searched destination is not available.
  - Use dummy data for destinations.
* The Settings tab should allow the user to customize app settings.
  -  Add a toggle button for notification and light/dark mode settings.
* App should preserve the state on tab change.
  - If the user scrolled to the bottom of the destinations screen, it should preserve the scroll state across the tab change.
  - If a user searches for something on the search screen, the search result should be there when navigating to the search tab from other tabs.
  - If the user changed the setting's toggle, it should stay as it is when the user navigate between the tabs

### Practical 8
#### Develop Recipe Lister application
* Single navigation app with two controllers - Home & Detail screen
* On the Home screen add collectionview to display the list of recipes.
  - Each list item should show the recipe name and image.
  - Cell should be show as a square.
  - Show number of cells horizontally:
    - Protrait:  phone - 3, iPad - 5
    - Landscape: phone - 4, iPad - 6
  - Tapping a recipe should open Detail screen.
* On the Detail screen show full recipe detail with recipe image and description.
  - Add a back button to navigate back to the list of recipes.
* Use dummy data for recipes.

### Practical 9
#### Implement App Browser
* On the Home screen add an input field where the user can enter a URL and a button to open URL inside the app.
* Once the user enters a valid URL and clicks the button, show a web view which slide up from the bottom of the screen.
  - This screen will show the content of the URL within a web view. 
  - The screen will also have a button to close the web view. 
  - Add a menu in the tool bar, which will have two options- copy and share the link.
    - Copy option should copy the link to the clipboard.
    - The share option should allow users to share links in other applications.
* The state of the controller should be preserved on configuration changes such as screen rotation.

### Practical 10
#### Develop QuickSend application
* This will be single screen app - QuickSendViewController
* QuickSendViewController allows users to send emails
  - Add text field to input the receiver's email address and email content.
  - Add a button to send email.
    - On click of it, the app should ask for the app to choose to send mail on.
