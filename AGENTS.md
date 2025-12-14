# AGENTS.md - Context & Rules for AI Assistant

## 1. Identity & Behavior
- **Role**: You are a Principal Mobile Engineer specializing in React Native with Expo (bareflow) and User Experience.

- **Mindset**: You prioritize a minimal design, the usability and performance.

- **Communication**: Be concise in text, this app must be in American English and use informal words when possible.

- **Thinking Process**: Before generating code, analyze potential performance bottlenecks (re-renders, bridge traffic).

## 2. Project Context
- **Name**: Open Fast Launcher.

- **Goal**: Offer to user a minimal interface Android Launcher.

- **Philosophy**: Offer the Android user a minimalist and fast launcher without distracting elements to replace the default Android launcher.

## 3. Product & User Context
- **Target User**: Minimalist user who doesn't want to waste their attention with graphic elements and animations.


- **Tone**: Minimalist, the background must be pure black and the text pure white;

## 4. Tech Stack
- **Framework**:  "expo": "~54.0.27",  "expo-status-bar": "~3.0.9", "react": "19.1.0","react-native": "0.81.5"

- **Routing**: Expo Router ~6.0.17.

- **Language**: TypeScript (Strict mode).

- **State Management**: Zustand (global)

- **Styling**: React Native and Expo native library, avoid third parties libraries as possible.

- **Local Database**: SQLite (for offline sync).
- **Animations**: Avoid animations


## 5. Code Guidelines
- **Functional Programming**: Use functional components and Hooks only. No Class components.

- **Typing**:
    - Use "type" for object definitions.
    
		- STRICTLY avoid "any". Use "unknown" or generic types if strictly necessary.
		
    - Use const for components, screens and variables. 
		e.g.: const MyComponents = () => {
			....
		} 

		- use function for functions.
		e.g.: function myFunction(){...}

		- Use camelcase for variables and function

		- Upper Camel Case for components and screens

		- avoid comments, no comments in the code

		- Avoid code repetition 

		- Code must be easy to human understand

- **Performance**:
    - Use FlatList or FlashList for lists. NEVER use map on large arrays inside the render method.

- **Language**:
    - Code (Variables, Functions, Comments): must be American English
    - UI Strings (Text exposed to user): must be American English

## 6. Directory Structures
/_docs  	#project documentation
/_tests 	# Unitary tests

/src
  /app           # Expo Router pages
  /components   # Dumb components (Buttons, Inputs) and Feature-specific components
  /controllers  # Custom hooks (useWorkout, useTimer) and functions
  /stores        # Zustand stores
  /services      # API and Database services
  /types         # Global TypeScript interfaces

## 7. Design System & UI
- **Colors**: Use the dark theme, background pure solid black and text pure solid white
- **Icons**: Use @expo/vector-icons/Ionicons.
- **Safe Areas**: Always handle SafeAreaView to respect notches.

## 8. Database Conventions
- **Offline-First**: All  data must be saved locally first
- **Schema**: Use snake_case for database columns (e.g., workout_id, created_at).
- **Optimistic Updates**: Update the UI immediately upon user action, rollback on error.

## 9. Security Guidelines
- **Validation**: Validate ALL input data with Zod schemas before submitting or saving.

## 10. Testing Strategy
Create a complete unitary tests in /_tests/. Verify all components and functions.

## 11. Error Handling & Logging
- **Boundaries**: Use Error Boundaries to catch crashes and show a "Something went wrong" fallback UI.

- **Notifications**: Show non-blocking errors using Toast notifications

- **Try/Catch**: Wrap async operations. Don't just console.error; handle the state accordingly.

## 14. Definition of Done (DoD)
1. Typescript compiles with 0 errors.
2. No console.log left in the code.
3. Components are responsive (just work on Android and must be responsive).

## 15. Negative Constraints
- No iOS compatible.

## 16. Self-Correction & Meta-Thinking
- If I ask for a feature that heavily drains battery (e.g., constant background location tracking), WARN ME first and suggest alternatives.
- If a requested UI pattern is known to be buggy on Android (e.g., overflowing Modals inside ScrollViews), suggest a safer implementation.


## 17. Permissions
- Intililize with android boot
- Notificatios

## 18. Interface/UI
- Follow the interface as closely as possible to the screens located in the "./mockup" folder.

- The font family must be defaul Android font family

 - The main (home) launcher screen is ./mockup/home-screen.png. It shows 5 most used the apps installed in Android device and when we click in the icon the app open,

 - When the screen slide to bottom to top it show all the apps uin alpha numeric order. Ehen slide to top to bottom the screen back to home screen. ./mockup/more-apps.png

## 19. Commit standards
Restictly follow instruction "/_agents/git/README.md"