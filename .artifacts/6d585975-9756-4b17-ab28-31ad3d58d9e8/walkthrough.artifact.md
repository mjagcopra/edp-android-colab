# Walkthrough - Lab Activity 7: Jetpack Navigation with Compose

I have successfully implemented the two-screen navigation app using Jetpack Compose and type-safe routes.

## Changes Made

### 1. Build Configuration
- Added Kotlin Serialization plugin and Navigation Compose dependencies to `libs.versions.toml`.
- Applied the serialization plugin and added dependencies to `app/build.gradle.kts`.
- Updated `compileSdk` to 37 to meet dependency requirements.

### 2. Routes Definition
- Created [Routes.kt](file:///D:/labactivity7/app/src/main/java/com/example/lab_activity_7/Routes.kt) with `@Serializable` destinations:
    - `Home`: An object for the start screen.
    - `Greeting`: A data class for the second screen, carrying the `userName`.

### 3. Screen Composables
- Created [Screens.kt](file:///D:/labactivity7/app/src/main/java/com/example/lab_activity_7/Screens.kt) containing:
    - `HomeScreen`: Includes an `OutlinedTextField` for name input and a "Show Greeting" button.
    - `GreetingScreen`: Displays the personalized greeting message.

### 4. Main Activity
- Updated [MainActivity.kt](file:///D:/labactivity7/app/src/main/java/com/example/lab_activity_7/MainActivity.kt) to set up the `NavHost`.
- Configured navigation from `Home` to `Greeting` using type-safe route objects.

## Verification Results

### Automated Tests
- The project builds successfully with `./gradlew assembleDebug`.

### Manual Verification
- Deployed the app to the emulator.
- Entered a name and verified navigation to the greeting screen.
- Captured the required screenshot.

![Greeting Screen Screenshot](file:///D:/labactivity7/screenshots/greeting_screenshot.png)

## Git Submission
- All changes have been committed to the `lab-activity-7` branch.
- **Note:** I was unable to perform the final `push` as no remote `origin` is configured in this local repository. Please add your remote and push manually if needed:
  ```bash
  git remote add origin <your-repo-url>
  git push -u origin lab-activity-7
  ```
