# React + Vite

This template provides a minimal setup to get React working in Vite with HMR and some Oxlint rules.

Currently, two official plugins are available:

- [@vitejs/plugin-react](https://github.com/vitejs/vite-plugin-react/blob/main/packages/plugin-react) uses [Oxc](https://oxc.rs)
- [@vitejs/plugin-react-swc](https://github.com/vitejs/vite-plugin-react/blob/main/packages/plugin-react-swc) uses [SWC](https://swc.rs/)

## React Compiler

The React Compiler is not enabled on this template because of its impact on dev & build performances. To add it, see [this documentation](https://react.dev/learn/react-compiler/installation).

## Expanding the Oxlint configuration

If you are developing a production application, we recommend using TypeScript with type-aware lint rules enabled. Check out the [TS template](https://github.com/vitejs/vite/tree/main/packages/create-vite/template-react-ts) for information on how to integrate TypeScript and Oxlint's TypeScript related rules in your project.

https://docs.aws.amazon.com/hands-on/latest/build-react-app-amplify-graphql/build-react-app-amplify-graphql.html?ref=gsrchandson&trk=4f374c9d-ac11-490d-8b23-82df6d4e054b&sc_channel=ps


# Step 1: Create a new React Application
npm create vite@latest notesapp -- --template react
cd notesapp
npm install
npm run dev

# Step 2: Create the GitHub repository and commit code
# Step 3: Install the Amplify Packages
npm create amplify@latest -y
git add .
git commit -m 'installing amplify'
git push origin main

# Step 4: Deploy your app with AWS Amplify
1. Create the Amplify App,
Sign in to the AWS Management console in a new browser window, and open the AWS Amplify console at https://console.aws.amazon.com/amplify/apps.
Choose Create new app.

2. Connect to your GitHub repository
On the Start building with Amplify page, for Deploy your app, select GitHub, and select Next.

3. Authorize and select your respository
When prompted, authenticate with GitHub. You will be automatically redirected back to the Amplify console. Choose the repository and main branch you created earlier. Then, select Next.

4. Configure build settings
Leave the default build settings and select Next.

5. Deploy your application
Review the inputs selected, and choose Save and deploy.

# Step 5: Set up Amplify Data
- Config models Auth, Data and Storage

$ Step 5: Deploy Amplify Cloud sandbox
import { defineBackend } from '@aws-amplify/backend';
import { auth } from './auth/resource';
import { data } from './data/resource';
import { storage } from './storage/resource';
/**
 * @see https://docs.amplify.aws/react/build-a-backend/ to add storage, functions, and more
 */
defineBackend({
  auth,
  data,
  storage
});

- Start sandbox environment
- To start your own personal cloud sandbox environment that provides an isolated development space, in a new terminal window, run the following command in your apps root folder:

npx ampx sandbox

$ Step 6: Install the Amplify libraries
npm install aws-amplify @aws-amplify/ui-react

# Step 7: Build the frontend and commit code





