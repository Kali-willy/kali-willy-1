# GitHub Snake Game

This repository contains a GitHub Actions workflow that generates a snake game animation based on your GitHub contribution graph.

## How it works

The workflow runs daily and generates:
1. A light theme SVG animation
2. A dark theme SVG animation
3. A colorful GIF animation

The generated files are deployed to the `output` branch.

## Display on your profile

To display this animation on your GitHub profile:
1. Create a README.md file in a repository with the same name as your GitHub username
2. Add the following markdown to display the animation:

```markdown
![Snake animation](https://github.com/{username}/kali-willy-repo/blob/output/github-snake.svg)
```

Replace `{username}` with your GitHub username.

## Fixed 403 Error

The original workflow had a 403 error due to permission issues. This has been fixed by adding:

```yaml
permissions:
  contents: write
```

This gives the GitHub Actions workflow the necessary permissions to write to the repository. 
