# Random-Namer
Flutter app that generates random name for you everytime you press a button, it's found in the main Flutter page as a tutorial.
Understanding Flutter:
1. It has the main function just like C to start the app, it's the main point that says to your app: " Go and run yourself buddy! ".
2. Inherting is the same like JS in terms of dealing with classes.
3. Every widget has a build method, telling flutter what the widget contains
Adding a navigation rail to save the fav names for the user in a different screen:
Using StatefulWidget, we do that by splitting MyHomePage into 2 separate widgets and changing the whole layout. But still after adding the rail, it doesn't work. Clicking ♥︎ (the heart) in the navigation rail does nothing. You shouldn't create variables to store values in your widget, you can imagine that the app state would quickly grow beyond reason if every widget stored its values in it. For now we will need some way to hold the value of the navigation rail's selectedIndex. What I did here was the following inside the private class drived from the ``` MyHomePageState``` :
When the onDestinationSelected callback is called, instead of merely printing the new value to console, you assign it to selectedIndex inside a setState() call. This call is similar to the notifyListeners() method used previously—it makes sure that the UI updates.
But we still need to adjust the space between the screens, since expanded area on the right stays the same. That's because the code isn't using selectedIndex to determine what screen displays.

A few resources to get you started if this is your first Flutter project:

- [Lab: Write your first Flutter app](https://docs.flutter.dev/get-started/codelab)
- [Cookbook: Useful Flutter samples](https://docs.flutter.dev/cookbook)

For help getting started with Flutter development, view the
[online documentation](https://docs.flutter.dev/), which offers tutorials,
samples, guidance on mobile development, and a full API reference.
