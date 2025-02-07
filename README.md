# React Router Dom Catch-All Route Issue

This repository demonstrates a problem with the catch-all route (`/*`) in React Router Dom v6.  The issue is that the catch-all route is not being triggered when navigating to a path that doesn't match any other defined routes.  All other routes are working correctly.

## Steps to Reproduce

1. Clone the repository.
2. Install dependencies using `npm install`.
3. Run the app using `npm start`.
4. Navigate to a route that doesn't exist (e.g., `/invalid-route`).  You will see the application render a blank page or the previous route instead of the Not Found component.

## Solution

The solution involves ensuring that the catch-all route is placed last in the `Routes` component.  This ensures that React Router correctly matches any unmatched paths to the catch-all route.  See `AppSolution.js` for a corrected version.