# Repo Voter

The Apollo Server backend shared by all Apollo client example apps.

Demonstrates:

1. GraphQL schema, resolvers, models, and connectors to read from two different data sources, GitHub REST API and SQL
2. Web server with authentication and basic authorization using Express, Passport, and Apollo Server

Please submit a pull request if you see anything that can be improved!

## Running the server

1. **Install Node/npm.** Make sure you have Node.js 4 or newer installed.

2. **install dependencies.**

  ```
  yarn install
  ```

3. **Run migrations.** Set up the SQLite database and run migrations/seed data with the following commands:

  ```
  yarn run migrate
  yarn run seed
  ```

4. **Get GitHub API keys.**
  1. Go to [OAuth applications > Developer applications](https://github.com/settings/developers) in GitHub settings
  2. Click 'Register a new application' button
  3. Register your application like below
  4. Click 'Register application' button at the bottom.
  5. On the following page, grab the **Client ID** and **Client Secret**.

5. **Add Environment Variables.** Set your Client ID and Client Secret Environment variables in the terminal like this:

  ```
  export GITHUB_CLIENT_ID="your Client ID"
  export GITHUB_CLIENT_SECRET="your Client Secret"
  ```

  Or you can use `dotenv`, to do this `cp .env.default .env` and edit with your Github keys.

6. **Run the app.**

  ```
  yarn run dev
  ```

7. **Open the app.** Open http://localhost:3010/ to see what to do next.
