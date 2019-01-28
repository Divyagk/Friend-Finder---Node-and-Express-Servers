# Friend-Finder---Node-and-Express-Servers


Friend Finder implements friend matching based on the user's responses to a ten question survey. The user responds to questions with values from 1 (Strongly Disagree) to 5 (Strongly Agree). When the survey is submitted, an existing user record closest to the current user's responses is found and returned. The closest set of user responses is defined as the set with the lowest absolute difference for all ten questions combined.

Friend Finder application is meant to simulate a simple dating app. The application is implemented using a Node.js and Express server on the back end and the Materialize CSS framework on the front end.



<h3>Getting Started</h3>

 https://stormy-sierra-86647.herokuapp.com/

<h3>Technologies Used:</h3>

1. JavaScript
2. jQuery
3. node.js
4. Express.js
5. HTML
6. Bootstrap

<h3>Technical details</h3>

The application uses Express to handle routing

The server.js file uses the npm packages: express, body-parser, path.

The html-routes.js file should include two routes:

A GET Route to /survey which displays the survey page.
A USE route that leads to home.html which displays the home page.
The api-routes.js file includes two routes:

A GET route with the url /api/friends. This will be used to display a JSON of all possible friends
A POST route /api/friends. This will be used to handle incoming survey results. This route will also be used to handle the compatibility logic.
Compatibility will be determined based on the following.

Each user's results is converted into a simple array of numbers (ex: [5, 1, 4, 4, 5, 1, 2, 5, 4, 1]).

Then will compare the difference between the user's scores against other users' scores, question by question. Then will add up the differences to calculate the totalDifference.

Example:
User 1: [5, 1, 4, 4, 5, 1, 2, 5, 4, 1]
User 2: [3, 2, 6, 4, 5, 1, 2, 5, 4, 1]
Total Difference: 2 + 1 + 2 = 5
The person with the closest match will be the one with the "least" amount of difference.

Once the closest match has been determined, it will display the result back to the user in the form of a modal pop-up.

The result will display both the name and picture of the closest match.
