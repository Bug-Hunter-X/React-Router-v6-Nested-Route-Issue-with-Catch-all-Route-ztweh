# React Router v6 Nested Route Issue with Catch-all Route

This repository demonstrates a bug in React Router v6 where nested routes within a parent route containing a wildcard catch-all route (`*`) are not rendered correctly. The catch-all route seems to intercept all requests, preventing nested routes from being matched.

## Bug Description
When you have nested routes and a parent route also has a catch-all route, the nested routes stop working as expected.  The nested routes are completely ignored and only the catch-all route is rendered regardless of the URL.

## Solution
The solution involves a careful re-arrangement of routes. The catch-all route should be placed *after* all other routes to ensure it only matches URLs that haven't already been matched by other routes.