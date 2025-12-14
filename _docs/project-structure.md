# Project Structure Documentation

This document provides a comprehensive overview of the Open Zero Launcher project structure, including all folders and subfolders.

## Root Directory

- **.gitattributes**: Git attributes configuration.
- **.gitignore**: Git ignore rules.
- **AGENTS.md**: Context and rules for AI assistants working on this project.
- **LICENSE**: Project license file.
- **README.md**: Project README with documentation index.
- **app.json**: Expo configuration file for the application.
- **babel.config.js**: Babel configuration for Jest and transpilation.
- **eas.json**: EAS (Expo Application Services) build configuration.
- **jest.config.js**: Jest testing configuration.
- **jest.setup.js**: Jest setup file.
- **metro.config.js**: Metro bundler configuration for React Native.
- **package.json**: Node.js dependencies and scripts.
- **package-lock.json**: NPM lock file.
- **tsconfig.json**: TypeScript configuration.
- **yarn.lock**: Yarn lock file.

## .expo/
Expo development files.

## .vscode/
VS Code configuration files.

## _agents/
Directory for agent-related configurations.

- **git/**
  - **README.md**: Git commit standards and guidelines.

## _docs/
Project documentation.

- **project-structure.md**: This file.

## _tests/
Unit tests for the application.

- **storageService.test.ts**: Tests for storage service functions.
- **useClock.test.ts**: Tests for clock utilities.

## android/
Android-specific build and configuration files.

- **build.gradle**: Root-level Gradle build file.
- **gradle.properties**: Gradle properties.
- **gradlew**: Gradle wrapper script (Unix).
- **gradlew.bat**: Gradle wrapper script (Windows).
- **settings.gradle**: Gradle settings.
- **app/**
  - **build.gradle**: App-level Gradle build file.
  - **proguard-rules.pro**: ProGuard obfuscation rules.
  - **build/**
    - **generated/**
      - **ap_generated_sources/**
      - **assets/**
      - **autolinking/**
      - **res/**
      - **source/**
    - **intermediates/**
      - **aar_metadata_check/**
      - **annotation_processor_list/**
      - **apk_ide_redirect_file/**
      - **app_metadata/**
      - **assets/**
      - **compatible_screen_manifest/**
      - **compressed_assets/**
      - **cxx/**
      - **data_binding_layout_info_type_merge/**
      - **data_binding_layout_info_type_package/**
      - **desugar_graph/**
      - **dex/**
      - **dex_archive_input_jar_hashes/**
      - **...** (additional build intermediates)
    - **kotlin/**
      - **compileDebugKotlin/**
    - **outputs/**
    - **tmp/**
  - **src/**
    - **debug/**
    - **debugOptimized/**
    - **main/**
  - **build/**
    - **generated/**
      - **autolinking/**
    - **reports/**
      - **problems/**
    - **gradle/**
      - **wrapper/**
        - **gradle-wrapper.properties**

## app/
Expo Router app directory (moved from root).

- **_layout.tsx**: Expo Router layout component.
- **index.tsx**: Main home screen component.

## ios/
iOS-specific build and configuration files (removed for Android-only builds).

## mockup/
Mockup images for UI design.

- **home-screen.png**
- **more-apps.png**

## node_modules/
Node.js dependencies.

## src/
Source code directory.

- **assets/**
  - **images/**
- **components/**
  - **AboutScreen.tsx**
  - **AppContextMenu.tsx**
  - **AppItem.tsx**
  - **AppList.tsx**
  - **AutostartScreen.tsx** (removed)
  - **Clock.tsx**
  - **index.ts**
  - **InitialSetupModal.tsx**
  - **LockAppsScreen.tsx**
  - **MostUsedApps.tsx**
  - **NotificationBadge.tsx**
  - **Toast.tsx**
  - **UnlockModal.tsx**
- **controllers/**
  - **index.ts**
  - **useClock.ts**
  - **useLauncher.ts**
  - **useNotifications.ts**
  - **useWeather.ts**
- **services/**
  - **autostartService.ts** (removed)
  - **databaseService.ts**
  - **index.ts**
  - **installedAppsService.ts**
  - **notificationService.ts**
  - **storageService.ts**
  - **weatherService.ts**
- **stores/**
  - **index.ts**
  - **launcherStore.ts**
- **types/**
  - **app.ts**
  - **index.ts**

## _agents/
Directory for agent-related configurations.

- **git/**
  - **README.md**: Git commit standards and guidelines.

## _tests/
Unit tests for the application.

- **storageService.test.ts**: Tests for storage service functions.
- **useClock.test.ts**: Tests for clock utilities.

## android/
Android-specific build and configuration files.

- **build.gradle**: Root-level Gradle build file.
- **gradle.properties**: Gradle properties.
- **gradlew**: Gradle wrapper script (Unix).
- **gradlew.bat**: Gradle wrapper script (Windows).
- **settings.gradle**: Gradle settings.
- **app/**
  - **build.gradle**: App-level Gradle build file.
  - **proguard-rules.pro**: ProGuard obfuscation rules.
  - **build/**
    - **generated/**
      - **ap_generated_sources/**
      - **assets/**
      - **autolinking/**
      - **res/**
      - **source/**
    - **intermediates/**
      - **aar_metadata_check/**
      - **annotation_processor_list/**
      - **apk_ide_redirect_file/**
      - **app_metadata/**
      - **assets/**
      - **compatible_screen_manifest/**
      - **compressed_assets/**
      - **cxx/**
      - **data_binding_layout_info_type_merge/**
      - **data_binding_layout_info_type_package/**
      - **desugar_graph/**
      - **dex/**
      - **dex_archive_input_jar_hashes/**
      - **...** (additional build intermediates)
    - **kotlin/**
      - **compileDebugKotlin/**
    - **outputs/**
    - **tmp/**
  - **src/**
    - **debug/**
    - **debugOptimized/**
    - **main/**
  - **build/**
    - **generated/**
      - **autolinking/**
    - **reports/**
      - **problems/**
    - **gradle/**
      - **wrapper/**
        - **gradle-wrapper.properties**

## src/
Source code directory.

- **app/**
  - **_layout.tsx**: Expo Router layout component.
  - **index.tsx**: Main home screen component.
- **assets/**
  - **images/**
- **components/**
  - **AboutScreen.tsx**
  - **AppContextMenu.tsx**
	- **AppItem.tsx**
  - **AppList.tsx**
  - **Clock.tsx**
  - **index.ts**
  - **InitialSetupModal.tsx**
  - **LockAppsScreen.tsx**
  - **MostUsedApps.tsx**
  - **NotificationBadge.tsx**
  - **Toast.tsx**
  - **UnlockModal.tsx**
- **controllers/**
  - **index.ts**
  - **useClock.ts**
  - **useLauncher.ts**
  - **useNotifications.ts**
  - **useWeather.ts**
- **services/**
  - **databaseService.ts**
  - **index.ts**
  - **installedAppsService.ts**
  - **notificationService.ts**
  - **storageService.ts**
  - **weatherService.ts**
- **stores/**
  - **index.ts**
  - **launcherStore.ts**
- **types/**
  - **app.ts**
  - **index.ts**

## mockup/
Mockup images for UI design.

- **home-screen.png**
- **more-apps.png**

## docs/
Project documentation.

- **project-structure.md**: This file.