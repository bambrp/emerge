# What's this for?

This was written to send a fixed-text Slack DM to everyone on a list, where that list was made up of email addresses. We were at out app limit, so did not have access to certain API functions, such as lookupByEmail.

Instead, the approach was to use a legacy token to call for the entire list of users on the workspace, filter out the inactive users, discover their user_id, open up a DM channel, and send a message.

## Environment / config

`SLACK_TOKEN` - The API token beginning "xoxp-" that we use to authenticate to Slack.