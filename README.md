# Google-Calendar-Integration-with-Django
This Django project provides an integration with Google Calendar using the OAuth2 mechanism. It allows users to authenticate with their Google accounts and retrieve a list of events from their calendars.
## Installation

1. Clone the repository:

   ```bash
   git clone https://github.com/prathameshpatil2002/Google-Calendar-Integration-with-Django.git
2.Configure OAuth2 Credentials:

Go to the Google Cloud Console and create a new project or use an existing one.
Enable the Google Calendar API for your project.
Create OAuth2 credentials and download the JSON file.
Save the downloaded JSON file in the project's root directory as credentials.json

## API Endpoints
/rest/v1/calendar/init/: Initiates the OAuth2 authentication flow. It prompts the user for their Google credentials.

/rest/v1/calendar/redirect/: Handles the redirect request sent by Google after authentication. It retrieves the access token from the provided code and fetches a list of events from the user's calendar.

## Usage
Access the initiation endpoint in your browser:

```bash

  http://localhost:8000/rest/v1/calendar/init/
```
You will be redirected to the Google login page. Log in with your Google account.

After successful authentication, you will be redirected to:

```bash
  http://localhost:8000/rest/v1/calendar/redirect/
```
The list of events from your Google Calendar will be displayed.
