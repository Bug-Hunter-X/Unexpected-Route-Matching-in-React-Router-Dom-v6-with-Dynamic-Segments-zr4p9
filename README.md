# Unexpected Route Matching in React Router Dom v6 with Dynamic Segments

This repository demonstrates an uncommon bug in React Router Dom v6 related to route matching with dynamic segments.  When a route with a dynamic segment is placed after a static route, it may unexpectedly match even when the dynamic segment is absent from the URL.

## Bug Description
The issue arises when you have a route with a dynamic segment (e.g., `/users/:id`) placed after a static route (e.g., `/about`) within the same `<Routes>` component. If you navigate to the static route's path, the dynamic route may still match, leading to incorrect component rendering. 

## Reproduction
1. Clone this repository.
2. Run `npm install`.
3. Run `npm start`.
4. Navigate to `/about`. You'll see the `Contact` component render instead of the `About` component.

## Solution
The solution involves rearranging the routes within the `<Routes>` component or using path parameters carefully to avoid conflicts.  See the `bugSolution.js` file for a corrected version.