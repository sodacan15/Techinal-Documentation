## ***POST (GitHub)***
----
### **What is POST?**
* POST is used to insert an issue into a GitHub repository.
* It is useful for reporting bugs, requesting features, or tracking tasks in a project.
* For example: There is a bug in the calculation of an app. To notify the programmer, team members may use `POST` to describe the problem in the code.
---
#### **Syntax and Return Value**
*-> Common Syntax: `POST /repos/{owner}/{repo}/issues`*

##### ***INPUT VALUES***

| Parameter | Type | Required | Description |
|-----------|------|----------|-------------|
| `owner` | string | Yes | Username or organization that owns the repo |
| `repo` | string | Yes | Name of the repository |
| `title` | string | Yes | Title of the new issue |
| `body` | string | No | Description of the issue |
| `labels` | array | No | List of label names to apply |
| `assignees` | array | No | List of usernames to assign |

##### ***RETURN VALUES***

| Field | Type | Description |
|-------|------|-------------|
| `id` | integer | Unique ID of the created issue |
| `number` | integer | Issue number in the repo |
| `title` | string | Title of the issue |
| `body` | string | Description of the issue |
| `state` | string | Default is `"open"` |
| `created_at` | string | Timestamp of creation |
| `html_url` | string | URL to view the issue on GitHub |

---
### Error Handling

| Status Code | Meaning | Description |
|-------------|---------|-------------|
| `201 Created` | Success | Issue created successfully |
| `400 Bad Request` | Error | Invalid parameters |
| `401 Unauthorized` | Error | Missing or invalid token |
| `403 Forbidden` | Error | No permission to create issue |
| `404 Not Found` | Error | Repository doesn't exist |
| `422 Unprocessable Entity` | Error | Validation failed |

---
### Example Usage:
**Scenario:** There is a prototype that can set priority on tasks and allow users to organize their weekly affairs called `Bare Minimum`. The source code of the app is located on a GitHub repository. While using the app, a user found a bug in `app.py`.

**Solution:** Creating an issue through the GitHub API using the `POST` function!

`<insert picture>`

##### **Pre-Requisites**

*Installing Git:*
1. Go to `git-scm.com`
2. Download the respective installer that matches your operating system.
3. Double-click and run the installer.
4. Keep clicking Next for default settings until installation initiates.
5. After installation, open `PowerShell` or `Command Prompt` and type: `git --version`

*Getting a Personal Access Token:*
1. Go to GitHub → **Settings** → **Developer Settings** → **Personal Access Tokens** → **Tokens (classic)**
2. Click **Generate new token**
3. Check the `repo` scope
4. Click **Generate token** and copy it immediately — GitHub only shows it once.

##### **Using PowerShell**
1. Open PowerShell
2. Run the following command:
```powershell
curl -X POST `
  -H "Accept: application/vnd.github+json" `
  -H "Authorization: Bearer YOUR_TOKEN" `
  https://api.github.com/repos/{owner}/Bare-Minimum/issues `
  -d '{"title":"Bug in app.py","body":"Found a bug in app.py"}'
```
3. Replace `YOUR_TOKEN` with your personal access token and `{owner}` with your GitHub username.
4. If successful, you will receive a `201 Created` response.

##### **Using GitHub Website**
1. Go to your repository on `github.com`
2. Click the **Issues** tab
3. Click **New Issue**
4. Fill in the **Title** and **Description** fields
5. Click **Submit new issue**

---
### Notes
> * Requires a valid GitHub Personal Access Token with `repo` scope.
> * `title` is the only required field in the request body.
> * Newly created issues are automatically set to `"open"` state.
