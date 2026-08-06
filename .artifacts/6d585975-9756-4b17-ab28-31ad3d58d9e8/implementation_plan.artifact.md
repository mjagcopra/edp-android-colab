# Implementation Plan - Lab Activity 7: Jetpack Navigation with Compose

This plan outlines the steps to implement a two-screen navigation app in Jetpack Compose, following the requirements of Lab Activity 7.

## User Review Required

> [!IMPORTANT]
> I will be using Kotlin version `2.2.10` for the serialization plugin to match your project's Kotlin version, instead of `2.0.21` mentioned in the instructions.

## Proposed Changes

### 1. Build Configuration
Modify `app/build.gradle.kts` to add the necessary dependencies and plugins.

#### [MODIFY] [app/build.gradle.kts](file:///D:/labactivity7/app/build.gradle.kts)
- Add Kotlin Serialization plugin.
- Add Navigation Compose dependency.
- Add Kotlinx Serialization JSON dependency.

### 2. Routes Definition
Create a new file to define the navigation routes.

#### [NEW] [Routes.kt](file:///D:/labactivity7/app/src/main/java/com/example/lab_activity_7/Routes.kt)
- Define `Home` object and `Greeting` data class, both marked as `@Serializable`.

### 3. Screen Composables
Create a new file for the UI screens.

#### [NEW] [Screens.kt](file:///D:/labactivity7/app/src/main/java/com/example/lab_activity_7/Screens.kt)
- Implement `HomeScreen` with a `TextField` and `Button`.
- Implement `GreetingScreen` that displays the user's name.

### 4. Main Activity
Update `MainActivity.kt` to set up the `NavHost`.

#### [MODIFY] [MainActivity.kt](file:///D:/labactivity7/app/src/main/java/com/example/lab_activity_7/MainActivity.kt)
- Set up `NavController` and `NavHost`.
- Define destinations for `Home` and `Greeting`.

### 5. Git Operations
Perform the required Git tasks.
- Create and switch to `lab-activity-7` branch (Already done).
- Commit and push changes.

### 6. Verification & Screenshot
- Run the app on an emulator.
- Navigate to the `Greeting` screen.
- Take a screenshot and save it to `screenshots/greeting_screenshot.png`.

## Verification Plan

### Automated Tests
- I will run `gradlew build` to ensure the project compiles correctly.

### Manual Verification
- Deploy the app to the emulator.
- Enter a name in the `HomeScreen`.
- Click "Show Greeting" and verify the `GreetingScreen` shows the correct name.
- Press the back button and verify it returns to the `HomeScreen`.
