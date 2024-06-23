# google_nav_bar

# Refactored for using ImageProvider instead of IconData. Added property activeIconImage, for active icons

A modern google style nav bar for flutter.

![google_nav_bar](https://user-images.githubusercontent.com/13378059/107119496-8cc72800-68ba-11eb-96c6-9bc8efe1a898.gif)


GoogleNavBar is a Flutter widget designed by [Aurelien Salomon](https://dribbble.com/shots/5925052-Google-Bottom-Bar-Navigation-Pattern/) and developed by [sooxt98](https://www.instagram.com/sooxt98/).


## Getting Started

Add this to your package's `pubspec.yaml` file:
```
...
dependencies:
    google_nav_bar:
      git:
        url: https://github.com/SergeyPetrovi4/google_nav_bar_icon.git
        ref: master
  
```

Now in your Dart code, you can use:
```
import 'package:google_nav_bar/google_nav_bar.dart';
```

## Usage

Style your tab globally with GNav's attribute, if you wish to style tab separately, use GButton's attribute

``` dart
GNav(
  rippleColor: Colors.grey[800], // tab button ripple color when pressed
  hoverColor: Colors.grey[700], // tab button hover color
  haptic: true, // haptic feedback
  tabBorderRadius: 15, 
  tabActiveBorder: Border.all(color: Colors.black, width: 1), // tab button border
  tabBorder: Border.all(color: Colors.grey, width: 1), // tab button border
  tabShadow: [BoxShadow(color: Colors.grey.withOpacity(0.5), blurRadius: 8)], // tab button shadow
  curve: Curves.easeOutExpo, // tab animation curves
  duration: Duration(milliseconds: 900), // tab animation duration
  gap: 8, // the tab button gap between icon and text 
  color: Colors.grey[800], // unselected icon color
  activeColor: Colors.purple, // selected icon and text color
  iconSize: 24, // tab button icon size
  tabBackgroundColor: Colors.purple.withOpacity(0.1), // selected tab background color
  padding: EdgeInsets.symmetric(horizontal: 20, vertical: 5), // navigation bar padding
  tabs: [
    GButton(
      iconImage: AssetImage("assets/images/home_tab_icon.png"),
      activeIconImage: AssetImage("assets/images/home_tab_icon_filled.png"),
      text: 'Home',
    ),
    GButton(
      iconImage: AssetImage("assets/images/settings_tab_icon.png"),
      activeIconImage: AssetImage("assets/images/settings_tab_icon_filled.png"),
      text: 'Settings',
    )
  ]
)
```

View the example folder

There are 4 different use case included in the /example directory, go try it out!
