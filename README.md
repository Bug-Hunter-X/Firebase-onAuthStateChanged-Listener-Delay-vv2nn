# Firebase onAuthStateChanged Listener Delay

This repository demonstrates a potential issue with the Firebase `onAuthStateChanged` listener where it doesn't trigger instantly after a successful sign-in or sign-out.  This can lead to UI inconsistencies or incorrect data access.

## Bug
The `onAuthStateChanged` listener within the provided example doesn't always reflect the authentication state immediately.  There's a noticeable delay before the listener updates the UI accordingly.

## Solution
The solution involves implementing a more robust state management approach to handle potential delays in the `onAuthStateChanged` event.  This is done by leveraging a separate state variable to track the authentication status, and updating it when the listener fires. This ensures the app's UI always remains synchronized with the user's authentication state.