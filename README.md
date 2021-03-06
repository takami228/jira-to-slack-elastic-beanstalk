# jira-to-slack-elastic-beanstalk

This repository is to run [jira-to-slack](https://github.com/takami228/jira-to-slack) in AWS Elastic Beanstalk.

## Set Up AWS Elastic Beanstalk

Upload zip file including `Dockerfile` and `Dockerrun.aws.json` at Single Docker Project at AWS Elastic Beanstalk.

## E2E Test

E2E Test
You can send actual payloads of actual JIRA events by the following script:

```sh
# Slack
PROXY_URL="https://jira-to-slack.example.com" SLACK_WEBHOOK="https://hooks.slack.com/xxx&username=JIRA&icon=https://lh3.googleusercontent.com/GkgChJMixx9JAmoUi1majtfpjg1Ra86gZR0GCehJfVcOGQI7Ict_TVafXCtJniVn3R0" ./testdata/post_jira_events.sh
```

```sh
# Mattermost
PROXY_URL="https://jira-to-slack.example.com" SLACK_WEBHOOK="https://mattermost.example.com/hooks/xxx&username=JIRA&icon=https://lh3.googleusercontent.com/GkgChJMixx9JAmoUi1majtfpjg1Ra86gZR0GCehJfVcOGQI7Ict_TVafXCtJniVn3R0&dialect=mattermost" ./testdata/post_jira_events.sh
```

## To Do

- Add auto deploy with CI Function
    - Using `eb` commands
- Add detail settings for AWS Elastic Beanstalk
    - Custom Domain
    - SSL
    - Security Group
    - Logging to CloudWatchLogs or S3
