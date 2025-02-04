# Unhandled Non-JSON Response in React Fetch

This repository demonstrates a common error in React applications that involves fetching data and handling non-JSON responses.  The `bug.js` file contains a component that fetches data and uses the `response.json()` method.  However, if the API returns a non-JSON response (e.g., a plain text error message), the `response.json()` method will throw an error, which the component does not gracefully handle.  The `bugSolution.js` provides a solution that checks for the content type before attempting to parse the response as JSON. 

## Bug

The original component lacks robust error handling for non-JSON responses from the server.  This could result in unexpected crashes or unhelpful error messages to the user.

## Solution

The solution involves adding a check to determine if the response is actually JSON before parsing the response body.  This ensures that the application handles various server responses effectively. 