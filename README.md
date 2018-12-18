# jira-to-slack-elastic-beanstalk

This repository is to run [jira-to-slack](https://github.com/takami228/jira-to-slack) in AWS Elastic Beanstalk.

# E2E Test

E2E Test
You can send actual payloads of actual JIRA events by the following script:

# Slack

```sh
PROXY_URL="https://jira-to-slack.example.com" SLACK_WEBHOOK="https://hooks.slack.com/xxx&username=JIRA&icon=https://lh3.googleusercontent.com/GkgChJMixx9JAmoUi1majtfpjg1Ra86gZR0GCehJfVcOGQI7Ict_TVafXCtJniVn3R0" ./testdata/post_jira_events.sh
```

# Mattermost

```sh
PROXY_URL="https://jira-to-slack.example.com" SLACK_WEBHOOK="https://mattermost.example.com/hooks/xxx&username=JIRA&icon=https://lh3.googleusercontent.com/GkgChJMixx9JAmoUi1majtfpjg1Ra86gZR0GCehJfVcOGQI7Ict_TVafXCtJniVn3R0&dialect=mattermost" ./testdata/post_jira_events.sh
```

# To Do

- Add auto deploy with CI Function
- Add detail settings for AWS Elastic Beanstalk
    - Custom Domain
    - Security Group
    - Logging to CloudWatchLogs or S3
