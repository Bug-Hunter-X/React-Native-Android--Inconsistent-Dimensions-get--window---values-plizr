# React Native Android: Inconsistent Dimensions.get('window') Values

This repository demonstrates a bug and its solution related to inconsistent screen dimension values returned by `Dimensions.get('window')` in React Native on Android.  The issue arises primarily due to inconsistencies during screen rotation or orientation changes.

## Bug Description
The `Dimensions.get('window')` API in React Native, while generally reliable, can sometimes return incorrect or delayed dimension values on Android, particularly after a screen rotation. This leads to layout issues, where UI elements are positioned incorrectly or are rendered improperly.

## How to Reproduce
1. Clone this repository.
2. Run the app on an Android device or emulator.
3. Rotate the screen. Note the inconsistent layout changes.

## Solution
The solution involves using the `Dimensions` API in conjunction with the `LayoutAnimation` API.  By using `LayoutAnimation.configureNext`, we ensure smoother transitions during screen rotation, mitigating the inconsistencies.

## License
MIT