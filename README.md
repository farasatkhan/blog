### GitHub Configuration

Configure Workflow Permissions:

- Navigate to your repository's Settings
- Select Actions → General
- Under "Workflow permissions", enable "Read and write permissions"

### Set Up GitHub Pages

- Go to repository Settings
- Navigate to Pages section
- Under "Build and deployment", select "GitHub Actions" as your deployment source

### Hugo Blog:

1. Install Hugo on your system:

```
https://gohugo.io/getting-started/quick-start/
```

2. Create and clone your new GitHub repository:

3. Initialize Hugo site in the repository:

```
hugo new site . --force
```

4. Add the `hugo-blog-awesome` theme as a Git submodule:

```
git submodule add --depth=1 https://github.com/hugo-sid/hugo-blog-awesome.git themes/hugo-blog-awesome
```

5. Configure your site by adding the theme to hugo.toml:

```
theme = 'hugo-blog-awesome'
```

6. Create a `build.yml` file in the directory `.github\workflows\` in order to set up a workflow for GitHub Actions. Copy and Paste the `build.yml` content from this repository.

Once configured, GitHub Actions will automatically build and deploy your site when you push changes to your repository. You can monitor the deployment status in the Actions tab of your repository.

> [!TIP]
> Note: You need PAT with workflows enabled.
