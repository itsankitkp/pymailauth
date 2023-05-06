# pymailauth
Python Library to send emails using google oauth

# Installation
`pip install pymailauth`

# Usage
1. Import service class and create service object by specifying credentials.json and token.json
```python
from pymailauth import Service
service = Service('/path/to/credentials.json', '/path/to/token.json')
service.send_email('<to mail address>', '<subject>','<body>')
```
Notes:
To get credential json file (based on [blog](https://mailtrap.io/blog/python-send-email-gmail/)):
1. Set up a [Google Cloud Platform](https://cloud.google.com/) project, click on the hamburger menu, and select view all products. Under the management section, select [APIs and services](https://console.cloud.google.com/apis/dashboard)
2. Next, select [Library](https://console.cloud.google.com/apis/library) and type “Gmail API” in the search bar, and click on the Gmail API card.
3. Finally, select the enable the [Gmail API](https://console.cloud.google.com/apis/library/gmail.googleapis.com?project=geocaching-366015) button. 
4. Now, you’ll need to download the client secrets file for your project. Start by selecting create credentials. In this section, select the Gmail API as your preferred API and user data as the type of data you will be accessing.
5. To get the OAuth client ID, select your application type as a Desktop App, set the application name, and select create. Next, download and store the credentials in your local file system.
