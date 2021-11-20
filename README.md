# ECI
Erza's Continuous integration system

### Checking Builds
ECI uses github's webhook to check for code updates. 
ECI creates a temp environment for erza in our private server to test if the bot is working in beta mode.
If all tests are passed and build succeeds in the temp environment, the code from github repository is downloaded and put to working directory of erza.
A system reboot is done to clear RAM and kill all the running processes.

## Using ECI in your project

Clone this repository

Create the following environment variables or edit `config.json`

```json
{
'GITHUB_WEBHOOK' = "your webhook url",
"REPO_URL" = "repository url",
"GAUTH"= "github auth token if the repo is private",
"RESTART" = "true OR false, this restarts the server after tests are passed and code is moved to working dir",
"DISCORD_WEBHOOK" = "webhook url to discord for logging events"
}
```

All the code of your project is put into `/app` dir of the server








