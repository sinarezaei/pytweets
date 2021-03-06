![alt text][pypi_version] ![alt text][licence_version]

# PyTweets: Python Twitter Api

Tested with:
* Python 3.6+

Use the following command to install using pip:
```
pip install pytweets
```

## Usage example

Use `TwitterApp` class to start a twitter app
```python
from pytweets import TwitterApp

app = TwitterApp(
    api_key='YOUR_API_KEY', 
    api_secret_key='YOUR_API_SECRET_KEY',
    app_name='YOUR_APP_NAME',
    bearer_token='YOUR_BEARER_TOKEN'
)

app.standard_search_tweets(keywords=['twitter', 'app'])  # search tweets which include 'twitter' and 'app'

user_info = app.get_user_by_username(username='jack')  # get user info for Jack Dorsey

app.get_user_statuses_timeline(user_id=user_info.user_id, count=500)   # retrieve latest 500 tweets of user

```

[pypi_version]: https://img.shields.io/pypi/v/pytweets.svg "PYPI version"
[licence_version]: https://img.shields.io/badge/license-MIT%20v2-brightgreen.svg "MIT Licence"
