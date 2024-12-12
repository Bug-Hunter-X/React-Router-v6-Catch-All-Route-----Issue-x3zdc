# React Router v6 Catch-All Route '*' Issue

This repository demonstrates a common issue encountered when using the catch-all route ('*') in React Router v6. The problem is that the catch-all route does not correctly handle unmatched routes, and it fails to render the 404 component or any other component designed to handle this situation.

## Problem
The catch-all route `path="*"` in React Router v6 does not work as expected when other routes are defined. Any URL that does not exactly match a defined path will trigger an unexpected behavior.

## Solution
The solution involves ensuring that the catch-all route is placed as the last route in the `Routes` component. This guarantees that it only matches routes that are not matched by any of the routes preceding it.  It's also important that the paths of the other routes are as specific as possible to avoid conflicts.