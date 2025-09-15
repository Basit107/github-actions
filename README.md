<h1> welcome To My README File </h1>

<p>This is a simple code that demonstrates the ppower of github actions for Continuous Integration for beginners to pipelining.</p>

- First build your app.
- Then inside your root directory of app, create a folder called: `.github`
- Inside the `.github` folder, create a folder called: `workflows`
- Then Inside the `.github/worflows` create a YAML file with any name.

---

## YAML File code:

```YAML
name: CI/CD Pipeline

on:
  push:
    branches:
    - main
  pull_request:
    branches:
    - main


jobs:
  build:
    runs-on: ubuntu-latest

    steps:
      - name: Set up checkout code
        uses: actions/checkout@v5

      - name: Set up Node.js
        uses: actions/setup-node@v4
        with:
          node-version: "14"

      - name: Install dependencies
        run: npm install

      - name: Run tests
        run: npm test

      - name: Build project
        run: npm run build

```

---

# Review:

> First build application:

`index.js`

> Then create Tests:

`test.js`

> Then create the following folders:

`.github/workflows`

> Inside `workflows` folder create a YAML file and paste code.

`Pipelines.yml`

---

# Final Steps:

> Then run the following commands:

- Add all the files:

```sh
git add .
```

- Commit the changes to repo:

```sh
git commit -m "[ANY MESSAGE]"
```

- Push to remote repo on main branch to github:

```sh
git push origin main
```
