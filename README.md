# React Router Dom v6 Catch All Route not working
This repository demonstrates a common issue with React Router Dom v6's catch-all route ("*" ) not functioning as intended.  The catch-all route fails to match routes that don't match other defined routes resulting in unexpected behavior.

## Problem
The provided example shows a basic React Router setup.  Despite having a catch all route (`/*`), if you navigate to a route that is not explicitly defined (e.g., `/invalid`), it renders nothing instead of the NotFound component.

## Solution
The solution involves ensuring that the catch-all route is placed last in the `Routes` component. This is necessary because React Router processes routes in order. If the catch-all is placed before other routes, it will match all routes preventing other routes from ever matching.
