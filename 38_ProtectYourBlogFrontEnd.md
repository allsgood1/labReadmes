Frontend Under Lock and Key Token

The purpose of this lab is to protect your frontend components using the auth workflow we coded on the backend. We write a utility file to handle localStorage and extending the use of fetch to more reusable in our applications.
Steps
Frontend Setup

At this point, you should have your basic Blog already running components for displaying all blogs, a single blog, and something to post/edit/delete blogs.

    Create an "admin" page that will allow you to create new blog posts and edit and delete existing ones
        You may be able to link to your existing pages for editing and deleting posts
    Make sure you protect your admin page, and the edit/delete pages (require login)
    Any "admin-type" functionality should not be visible from the "public" pages. Those functions should only appear on the admin page(s):
        Create a new post
        Edit a post
        Delete a post

Installs

Make sure you have the following modules and their types installed:

    isomorphic-fetch @types/isomorphic-fetch
    moment @types/moment
        for fun added utility :)

API Routes

    Make sure all of your blog API endpoints use res.json() to send some kind of response, to make sure our frontend utility won't fail in certain circumstances

Utilities

    Make sure to import isomorphic-fetch
    Export a new variable AccessToken who's value is gotten from localStorage, otherwise defaulting to null
    Export a new object User who's userid and role properties are gotten from localStorage, otherwise defaulting to null
    Export a utility function json (or any name of your choosing) which will make the fetch call, generate the appropriate headers, and convert the json response automatically for you
        arguments should be uri, method, body as the videos demo
    Export a utility function SetAccessToken that given a token, and user object, can set those key/value pairs on localStorage

Implement the Utilities

    Change all your fetch methods across your React components to use your custom json function
    Make sure your "admin" component will not show unless you are logged in, i.e. have it reroute to the login form
    Make your Login component successfully POST request a login, and take the response and set it using SetAccessToken
    Confirm you can navigate back to the "admin" page without getting rerouted, and confirm you can successfully post blogs again

Spice it up!

    Add some private class variables that prevent users from spamming a login/submit button and causing multiple requests to fulfill
    Add some error/success handling for good user experience on your webapp
    Add something sweet n' spicy the demos don't and share it in Discord
