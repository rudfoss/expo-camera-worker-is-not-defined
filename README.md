Reproduced error when using [expo-camera](https://docs.expo.dev/versions/latest/sdk/camera) on web.

Steps:

1. Create a new expo app:

```bash
`npx create-expo-app --template`
√ Choose a template: » Navigation (TypeScript)
√ What is your app named? ... my-app
```

2. Install camera

```bash
npx expo install expo-camera
```

3. Update `app.json`

```json
    "plugins": [
      "expo-router",
      "expo-camera"
    ],
```

4. Start app and open in browser

```bash
npm start

> my-app@1.0.0 start
> expo start

Starting project at C:\projects\temp\my-app
Starting Metro Bundler
▄▄▄▄▄▄▄▄▄▄▄▄▄▄▄▄▄▄▄▄▄▄▄▄▄▄▄
█ ▄▄▄▄▄ █▄▄▄ ▀▄▀█ █ ▄▄▄▄▄ █
█ █   █ ██▄▀ █ ▀▄▄█ █   █ █
█ █▄▄▄█ ██▀▄ ▄█▀█▀█ █▄▄▄█ █
█▄▄▄▄▄▄▄█ ▀▄█ ▀ ▀ █▄▄▄▄▄▄▄█
█  ▀  █▄▀▀▄▀█▄▀█▀ ▀▄█▀█▀▀▄█
█▀█ █▀█▄█▀▄██▄▄▄▄▀▄ ▀▀▄▀▀ █
█▀▀ █▄ ▄█▀▄ █▀█▄▀█ ▄ ▀█▀ ██
█ ▄▀▀ ▄▄▀ █ █▀▄▀▄▀█ ▄▀▄▀  █
█▄█▄▄██▄█▀▄▀ ▄▄ ▀ ▄▄▄  ▄▀▄█
█ ▄▄▄▄▄ ███ ▀▄  █ █▄█ ███ █
█ █   █ █ █ ▄ ▀█▄▄▄  ▄ █▀▀█
█ █▄▄▄█ █▀▀▀ ▀█▄█▄▀▀▀▄█   █
█▄▄▄▄▄▄▄█▄▄▄▄██▄▄▄▄▄▄▄███▄█

› Metro waiting on exp://10.100.98.124:8081
› Scan the QR code above with Expo Go (Android) or the Camera app (iOS)

› Web is waiting on http://localhost:8081

› Using Expo Go
› Press s │ switch to development build

› Press a │ open Android
› Press w │ open web

› Press j │ open debugger
› Press r │ reload app
› Press m │ toggle menu
› Press o │ open project code in your editor

› Press ? │ show all commands
› Open in the web browser...
› Press ? │ show all commands
λ Bundled 6764ms (C:\projects\temp\my-app\node_modules\expo-router\node\render.js)
Web Bundled 7715ms (C:\projects\temp\my-app\node_modules\expo-router\entry.js)

Metro error: Worker is not defined


Call Stack
  createWorkerAsyncFunction (node_modules/expo-camera/build/useWebQRScanner.js)
  factory (node_modules/expo-camera/build/useWebQRScanner.js)
  loadModuleImplementation (node_modules/metro-runtime/src/polyfills/require.js)
  guardedLoadModule (node_modules/metro-runtime/src/polyfills/require.js)
  _$$_REQUIRE (node_modules/metro-runtime/src/polyfills/require.js)
  factory (node_modules/expo-camera/build/ExpoCamera.web.js)
  loadModuleImplementation (node_modules/metro-runtime/src/polyfills/require.js)
  guardedLoadModule (node_modules/metro-runtime/src/polyfills/require.js)
  _$$_REQUIRE (node_modules/metro-runtime/src/polyfills/require.js)
  <unknown> (node_modules/expo-camera/build/Camera.js)
Web Bundled 1529ms (C:\projects\temp\my-app\node_modules\expo-router\_error.js)
```