# Syncosaurus Dashboard
<kbd>
    <img alt="Syncosaurus Dashboard Screenshot" src="./app_screenshot.png?raw=true">
</kbd>


## Overview

The Syncosaurus dashboard is a locally hosted analytics monitoring application, allowing developers to view, analyze and troubleshoot their Syncosaurus applications.

The dashboard features two sets of metrics for each project:
- **All Rooms**: Aggregated metrics for ALL rooms associated with a selected project
- **Single Room**: Individual room metrics associated with a selected project

## Setup

1. Clone this repository to your local environment: `git clone https://github.com/syncosaurus/syncosaurus-dashboard.git`
2. Create an `.env` file with the following environment variables and values in the root directory:
    - `CLOUDFLARE_ACCOUNT_ID`: This is the account ID associated with your Cloudflare account. For instructions on finding your account ID, click [here](https://developers.cloudflare.com/fundamentals/setup/find-account-and-zone-ids/).
    - `BEARER_AUTH`: This is an Cloudflare Analytics API token associated with your account. This is used to access the GraphQL Analytics API. For instructions on creating an API token, click [here](https://developers.cloudflare.com/analytics/graphql-api/getting-started/authentication/api-token-auth/).
    - `X_AUTH_EMAIL`: This is the e-mail address associated with your Cloudflare account.
    - `X_AUTH_KEY`: This is your Cloudflare global API key. This is used to access the Cloudflare API. For instructions on finding your global API key, click [here](https://developers.cloudflare.com/fundamentals/api/get-started/keys/).
    - `PORT`: This is the local port that you want the dashboard app to use. If this value does not exist, the application defaults to port `3001`.
3. Install dependencies: `npm install`
4. Run the dashboard application: `npm start`
5. An URL to the dashboard application will be displayed (ex: `http://localhost:3001`). Click the URL to launch the dashboard application.

## Using the Dashboard

To get started with the dashboard:
1. Select a project from the header dropdown.
2. Click `All rooms` under `All Room Metrics` to view data for all of your rooms
3. Click a room's namespace ID under `Single Room Metrics` to view data for that room
4. The date selector defaults to the current date. To view metrics for a different date, use the date selector dropdown under the `Selected Date` heading to select your desired date.
5. Your selected data should now be displayed in the dashbard's main display area. Toggle different statistics by clicking on the desired statistic.
