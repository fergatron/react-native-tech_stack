# react-native-tech_stack

This project is based on the Udemy tutorial hosted by Stephen Grider, _The Complete React Native and Redux Course_. My focus in on the Android platform.

https://www.udemy.com/the-complete-react-native-and-redux-course/learn/v4/content

## Course description and notes
The particular lesson covers REDUX. The general flow of Redux is a Store houses the REDUCER and STATE. ACTIONS interact specifically with the Reducer and it specifically interacts with the State. It only goes in one direction.

ACTION -> [ REDUCER -> STATE ] STORE

* Action - An object that tells the reducer how to change its data.
* Reducer - A function that returns some data.
* State - Data for our app to use.
* Store - An object that holds the application's data.

Helpful tool: https://stephengrider.github.io/JSPlaygrounds/

* Nothing happens with the ACTION until you DISPATCH it to the store. Dispatching will invoke the REDUCER.
* In the REDUCER we do not mutate our state, instead we return a completely new object.

## Setup the project
```bash
react-native init tech_stack
npm install --save redux react-redux eslint-config-rallycoding
```

### Configure .eslintrc
```json
{
    "extends": "rallycoding"
}
```
## Run android emulator
```bash
cd /usr/local/share/android-sdk/tools/
emulator @Pixel_API_26

or

cd $(dirname $(which emulator)) && emulator @Pixel_API_26
```

## Start React Native packager and compile android
```bash
react-native start --port=8082 (optional)
react-native run-android
```

## Debugging app on emulator
Ctrl + M only works when the app is in view. Ctrl + M does something different when outside the app.
