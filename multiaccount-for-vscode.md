# GitHub Quick Recipe (Private Repos with HTTPS + PAT)

### 1) Add remote for the first time

```bash
git remote add origin https://<user>@github.com/<user>/<repo>.git

```

Example:

```bash
git remote add origin https://RafaCMur@github.com/RafaCMur/moneyboard-website.git

```

### 2) Change an existing remote

```bash
git remote set-url origin https://<user>@github.com/<user>/<repo>.git

```

### 3) Enable credential manager

```bash
git config --global credential.helper manager

```

### 4) Force login

```bash
git ls-remote origin

```

- Username: usually not asked if included in the URL.
- Password: paste your **Personal Access Token (PAT)**.

The token is stored in Windows Credential Manager and will not be asked again.

### 5) Multi-account setup

- Always include the username in the URL (`https://USER@github.com/...`).

```bash
git remote set-url origin https://<user>@github.com/<user>/<repo>.git

```

- Enable this so credentials are stored per repo:

```bash
git config --global credential.useHttpPath true

```

### 6) Check default branch

```bash
git remote show origin

```

If it shows `HEAD branch: main`, set upstream:

```bash
git branch --set-upstream-to=origin/main

```
