# Treetracker Impact Wallet

## Development Environment Quick Start

1. Make sure all npm modules are installed for client.

```
npm i
```

2. Start the client

```
npm start
```

3. Open the web map in the browser with URL: http://localhost:3000

### How to build a component

[Video tutorial for building component](https://loom.com/share/c750be68ecec4a9b99cb6921d2d2e041)

### How to mock the API

[Video tutorial for mock the API](https://www.loom.com/share/48554f0f67314ea78925a627b2142e1b)

### Cypress

We use Cypress to build the sandbox for component building and mock the server-side API in the integration tests, here are some guide for this:

To run Cypress integration e2e test:

```
npm run cy
```

To run Cypress unit tests:

```
npm run cyu
```

To simulate mobile device in the component tool:

Because that we focus on the mobile device, so when we build component by Cypress component tool, we want to operate the component in simulator of mobile device, with the devtools in Chrome, the most important feature is the swipe/touch simulator (you can see it when you open Chrome devtools and switch to any mobile device), but it becomes tricky if you are using the Cypress component took, cuz we have to use big screen to show them all, how can we open a big screen and simulate the mobile behavior at the same time, this video is a tutorial showing how to set it up:

[Video for Cypress setting up](https://www.loom.com/share/a126f0a80c3a4352a3ddf955f88228b9)

&nbsp;
&nbsp;

## Code style guide

We use [Prettier](https://prettier.io/), [Eslint](https://eslint.org/) along with [husky](https://typicode.github.io/husky/#/) to style our code.

### Prettier

Prettier reformats the code, but does not do code rule checking. If you are using VSCode as your IDE, please follow [this guide](https://www.digitalocean.com/community/tutorials/how-to-format-code-with-prettier-in-visual-studio-code) to set up Prettier and automatically format your code on file save.

You can find the Prettier rules in the .prettierrc file.

### Eslint

To check the coding rules we use Eslint. To validate the rules manually, you must run:

```
npm run lint
```

To fix automatic rules run:

```
npm run lint:fix
```

In .eslintrc.js, there is a set of rules with status **off or warn**. Whenever you are developing a new file or an existing file try to correct some warnings, because in the future the rules will be activated.

Once the rules are activated, you can't make a commit until you fix the lint errors!

You can find the Eslint rules in the .eslintrc.js file.

### husky

With husky we can use any git hook. Git Hooks are actions that can be executed if a certain Git event occurs. For example when a developer makes a 'git commit' or a 'git push'.
To add a command to a pre-commit hook or create a new one, use:

```
npx husky add .husky/pre-commit "<your command>"
```

.husky folder contains all our hooks. In this case a pre-commit hook.

```
npx pretty-quick --staged
```

The [pretty-quick](https://www.npmjs.com/package/pretty-quick) npm package runs Prettier on your changed files.
