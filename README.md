
# GitHubAppreciator

GitHubAppreciator is a GitHub Action that brings gratitude to the heart of open-source collaboration. It's designed to automatically thank and appreciate the contributors who dedicate their time and effort to your repositories.

## Usage

- Go to your GitHub repository.
- Click on the "Actions" tab.
- Click on the "New workflow" button, or if you already have a workflow, you can edit it.
- In the workflow file (usually named .github/workflows/main.yml), add a step to use the GitHubAppreciator action

``` 
# name of the action
name: Thank Contributors

# triggers for the action
on: 
    pull_request:
        types:
            - closed
        # add aditional branches if needed
        branches:
            - main
            - master

jobs:
    Appreciation:
        uses: prajwalraju/GitHubAppreciator/.github/workflows/GitHubAppreciator.yml@main
        
        # Pass all secrets
        secrets: inherit 
```
- Add secret linkedinAuth in github Secrets

## Features

- Automatic Appreciation: GitHubAppreciator runs as a GitHub Action, allowing you to easily integrate it into your workflow. Whenever someone contributes to your repository, this action will automatically send out heartfelt thanks.
- Customizable Messages: You have the flexibility to personalize the appreciation message. Express your gratitude in your own words, making each thank-you message unique and genuine.
- Multi-Platform Support: Not just limited to GitHub, GitHubAppreciator also extends its appreciation efforts to LinkedIn and Twitter. Share your appreciation publicly, showcasing your gratitude to the broader community.
- Easy Setup: Setting up GitHubAppreciator is a breeze. With clear documentation and straightforward configuration options, you can have your appreciation bot up and running in no time.


## Contributing

Contributions are always welcome!

If you would like to contribute to this project, please open an issue or submit a pull request on GitHub. We welcome contributions from the community and appreciate your feedback.


## License

GitHubAppreciator is licensed under the GNU General Public License v3.0 license. See LICENSE for more information.

## Local Test command using Act
    act pull_request -e .github/workflows/actPullRequestPayload.json