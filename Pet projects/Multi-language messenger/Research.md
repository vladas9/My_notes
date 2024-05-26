---
Dates:
  - 2024-05-11
tags:
  - project
---
### Android

**Technologies Used**: React Native for the frontend, Node.js for the backend, and Kotlin for native Android functionality.

- **React Native** handles the main application interface and logic that can be shared across platforms.
- **Node.js** serves as the backend, managing tasks such as user authentication, data processing, and interactions with APIs.
- **Kotlin** is used for Android-specific features that React Native cannot handle directly, such as implementing Accessibility Services to read messages from other apps on the screen. Kotlin provides a modern, safe, and concise way to write native Android code.

**Permissions and Accessibility**:

- Permissions for accessing specific features like Accessibility Services need to be requested explicitly. Users must be directed to the Android settings to enable these permissions manually, as this cannot be done programmatically due to security reasons.
- An XML configuration for the Accessibility Service and adjustments in the `AndroidManifest.xml` are necessary to define and register the service.

**Integration**:

- Native modules in Kotlin are created to expose required functionalities to the React Native environment, allowing JavaScript code to interact with native Android features.

### iOS

**Technologies Used**: React Native for the frontend, Node.js for the backend, and Swift for native iOS functionality.

- **React Native** is used similarly to the Android setup, handling cross-platform UI and shared logic.
- **Node.js** performs backend operations, providing services and API integrations necessary for the app’s functionality.
- **Swift** manages iOS-specific permissions and features. Unlike Android, iOS does not allow apps to read other app’s content for security and privacy reasons, but Swift is necessary for other permissions and native features.

**Permissions**:

- Permissions in iOS are managed through the app's `Info.plist`, where you declare why each permission is needed. Permission requests are handled programmatically within Swift code at the point of use.

**Integration**:

- Custom native modules or methods written in Swift are used to bridge iOS-specific functionalities to React Native, ensuring smooth interaction between the JavaScript and native components of the app.


## References 
1. 