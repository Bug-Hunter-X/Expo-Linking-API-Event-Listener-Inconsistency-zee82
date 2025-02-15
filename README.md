# Expo Linking API Event Listener Inconsistency

This repository demonstrates a common issue with the Expo `Linking` API's `addEventListener` method.  Under certain circumstances, such as when the app is in the background or launched from a cold start, the event listener may fail to trigger, leading to missed deep links.

The `linkingBug.js` file reproduces the problem.  `linkingBugSolution.js` offers a potential workaround.

## Potential Solutions

The provided solution incorporates a mechanism to check for initial URLs on app launch to handle deep links that might have been missed by the event listener.  This solution is a workaround; the root cause remains an inconsistency in the Expo `Linking` API behavior.  Consider reporting this issue to Expo to help improve the API.