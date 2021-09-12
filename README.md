# react-native-init

An empty react-native project ready to launch for **ANDROID**, **WEB** and **WINDOWS**. This project does not use expo.

## Before starting

```
yarn install
```

## If you have all dependencies installed earlier

Run the following command in the terminal and let it open:

```
yarn start --reset-cache
```

- I don't know why but --reset-cache sometimes solves some issues.

# Run for Android

First follow the "Android development environment" instructions from [Official Site](https://reactnative.dev/docs/environment-setup) (installing Android SDK etc.). Then to start the app run following command:

```
npx react-native run-android
```

###### Possible errors

- Be sure that you have an AVD (Android Virtual Device) or a physical android device connected via USB. "USB Debugging" option must be checked from Developer Options or your PC will not see your device.
- If you encounter any gibberish errors, before spending 2398235 hours for solving it, maybe you need to restart your PC.

# Run for Windows

First read the [System Requirements](https://microsoft.github.io/react-native-windows/docs/rnw-dependencies). You need Visual Studio Installer in order to install some dependencies for windows. Be sure you have checked the necessary items in Visual Studio Installer as shown in the following images:

![requirements1](https://i.imgur.com/covVN7L.png)
![requirements2](https://i.imgur.com/Bs7JlcE.png)

- After installing dependencies, before spending 2398235 hours for solving errors, restart your PC
- You have to keep ./windows/launch.json file or you can't run the app.

Then run:

```
npx react-native run-windows
```

- If you encounter an error while running the app, get a deep breath and start crying. Or, If you want to solve the problem, you can kill the openned terminals, remove the ./node_modules folder, restart your PC and after `yarn install` start the app with `yarn start --reset-cache`. Then run `npx react-native run-windows` on a different terminal.

# Run for Web

Be sure that you have following scripts in your package.json:

```
"web:start": "react-scripts start",
"web:build": "react-scripts build"
```

and be sure that you have following rule in your .eslintrc.js file's rules object or you'll get a disgusting error in the browser:

```
'prettier/prettier': [
  'error',
  {
    endOfLine: 'auto',
  },
],
```

Then simply run:

```
npm run web:start
```

On the first run, it will ask you to add browser settings to your package.json. Accept it.

# Building

I don't even know how you build for Windows and Android. But I'm sure you are clever then me to figure it out by Googling.

# And, voilà!

You have successfuly installed an react-native project ready to go for 3 platforms. You can keep all of them open at the same time, while developing!
