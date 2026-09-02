# MacroZone

MacroZone is a simple Expo app for logging meals and tracking their macros: calories, protein, carbs, and fat. It gives you a quick home dashboard, an add-meal form, a full meal history, copy/share actions, and optional meal reminders.

## What it does

MacroZone lets you:

- add meals with calories, protein, carbs, and fat
- view your saved meals in a home dashboard and a full meal list
- copy or share meal data
- turn on daily reminder notifications for lunch and dinner
- clear all meals when you want to start over

It uses Expo Router for navigation and AsyncStorage for local meal storage.

## How to run it

1. Install dependencies:

   ```bash
   npm install
   ```

2. Start the app:

   ```bash
   npm run start
   ```

3. Open it in one of the available targets:

   ```bash
   npm run android
   npm run ios
   npm run web
   ```

If you want a clean starter state, you can also run:

```bash
npm run reset-project
```

## Project structure

- `src/app/(tabs)/index.tsx` — home dashboard
- `src/app/(tabs)/add-meal.tsx` — add a meal
- `src/app/(tabs)/meals.tsx` — all meals view
- `storage/` — local meal storage
- `components/` — reusable UI pieces
- `src/utils/notification.ts` — reminder notification helpers

## The one thing newcomers always get wrong

This is a file-based Expo Router app. New screens belong in `src/app`, and the route structure comes from the file path.

The most common mistake is trying to add a screen in the wrong place and expecting it to appear automatically. If you want a new tab or page, create the file in the right `src/app` route folder and wire it into the tab layout if needed.

A second common gotcha: the app stores meals locally on the device. If you uninstall the app, switch devices, or clear app storage, your saved meals disappear.

## Notes

This project is configured for Expo SDK 56. If you change Expo-related behavior, check the versioned docs first.
