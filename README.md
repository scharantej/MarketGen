## Flask Application Design for Building a Tutorial Website on Creating Marketing Campaigns

### 1. HTML Files:

**a. home.html:**
- Home page of the website.
- Contains an introduction to the website and links to other pages.
- Also includes basic HTML elements like header, navigation bar, and footer.

**b. create-campaign.html:**
- Contains a form for users to create a marketing campaign.
- Includes fields for campaign name, target audience, budget, and timeline.

**c. view-campaigns.html:**
- Displays a list of all the created marketing campaigns.
- Each campaign has its name, status, and start and end dates.

**d. campaign-details.html:**
- Displays the details of a specific marketing campaign.
- Includes campaign name, target audience, budget, timeline, and progress.

**e. layout.html:**
- Base HTML template for all pages.
- Contains common elements like header, navigation bar, and footer.

### 2. Routes:

**a. @app.route('/'):**
- Route for the home page.
- Displays the home.html page.

**b. @app.route('/create-campaign', methods=['GET', 'POST']):**
- Route for creating a new marketing campaign.
- Handles both GET requests for displaying the form and POST requests for creating a new campaign.
- Redirects to the view-campaigns page after successful campaign creation.

**c. @app.route('/view-campaigns'):**
- Route for viewing all marketing campaigns.
- Displays the view-campaigns.html page with a list of campaigns.

**d. @app.route('/campaign-details/<campaign_id>'):**
- Route for viewing the details of a specific marketing campaign.
- Accepts a campaign ID as a URL parameter.
- Displays the campaign-details.html page with detailed information about the selected campaign.

**e. @app.route('/delete-campaign/<campaign_id>', methods=['POST']):**
- Route for deleting a marketing campaign.
- Accepts a campaign ID as a URL parameter.
- Deletes the campaign from the database and redirects to the view-campaigns page.

### Additional Notes:

- The application can be further enhanced by adding features like campaign editing, progress tracking, and user authentication.
- Styling and frontend design can be implemented using CSS and JavaScript, but those aspects are beyond the scope of this design document.