React Native Tips:



<ins>Styling tips:<ins>
https://www.okgrow.com/posts/react-native-styling-tips


React Native (2015) also by Facebook.  

React Native (RN) is a superset of React.  

Purpose:  to give your mobile apps a truly native feel.

So - what is it???
	• A framework.  comes with everything you need to create a basic app.
	• Reac Native's goal is to render real native iOS or Android components in a mobile app.  
	• React does NOT use CSS.  React Native styles are written in JavaScript.
		○ a JS class, StyleSheet
	• Requires Xcode and/or Android Studio installation on your box.
	

So - what is different about them???
	• Components.  These map to actual real native iOS or Android UI components that get rendered on the app.
	• Most components can be translated to something similar in HTML


RN compiles down to native app components.  
	• you are getting full native iOS / Android experience and performance.
in contrast to 




<ins>Expo Pros & Cons:<ins>

Not all iOS and Android APIs are available yet.  Examples NOT yet available: 
Bluetooth.
WebRTC
 
Background execution limitations (ability to run code when app is not foregrounded or the device is sleeping).
Push notifications in the background not yet available.
 
Minimum app size for an Expo app is
iOS:  20mb
Android: 15mb
 
This is due to the number of apis included for the 'managed' workflow - which will be there regardless if you use them or not. 
 
What Expo DOES give you that is compelling includes:
Over the air updates (no need to release to the store)
App-Store ready binaries and handles certificates, no need for you to touch Xcode or Android Studio. 



