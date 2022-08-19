# ABOUT
GitHub Action for continuous build and deployment.
- Uses Node 16.x.

# SETUP

1. Copy node.js.yml into root/.github/workflows
2. Edit node.js.yml:
    - {on: push: branches:} to listen for actions on wanted branch
    - {on: pull_request: branches: }
    - Ensure {publish_dir:} reflects your build output directory.
3. Wait for first run
4. Change GitHub Pages to deploy from branch {gh-pages}

# NOTES TO SELF

- name:
    The name of the action

- on:
    Decides which event to listen for
        - push
        - pull_request
- jobs:
    Description of job to run

    - build:
        We need to run our program on a system.

        - runs-on:
            What system we want to run on.

            - strategy:
                Supports testing across multiple versions

            - steps:
                All the steps to go through.

                - First setup our enviroment
            
            - *** 
            - TODO
            - ***

            These are the same commands that you are using in the console
            - run: npm ci
                Variant of "npm install" for use in automated enviroments

            - run: npm run build --if-present
                Runs the script located in package.json.
            
            Last bit deploys to branch gh-pages. [Action Homepage](https://github.com/marketplace/actions/github-pages-action).rx