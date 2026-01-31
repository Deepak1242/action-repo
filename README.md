# Action Repo

This repository serves as the source of GitHub Actions events.
**Live Test:** Webhook verification triggered!

## Setup
1.  Initialize this folder as a git repository:
    ```bash
    git init
    git add .
    git commit -m "Initial commit"
    ```
2.  Create a fresh repository on GitHub named `action-repo`.
3.  Push this code to GitHub:
    ```bash
    git remote add origin <YOUR_GITHUB_REPO_URL>
    git push -u origin master
    ```

## Webhook Setup
1.  Go to your GitHub Repository Settings > Webhooks.
2.  Add a new webhook.
3.  **Payload URL**: Your public URL for the `webhook-repo` (e.g., `https://<your-ngrok-url>/webhook`).
4.  **Content type**: `application/json`.
5.  **Events**: Select "Let me select individual events" and check:
    - Pushes
    - Pull requests
6.  Click "Add webhook".

Now, whenever you push code or create a PR in this repo, the `webhook-repo` will receive the event.
