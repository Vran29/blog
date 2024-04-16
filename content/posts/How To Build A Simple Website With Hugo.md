+++
title = 'How To Build A Simple Website With Hugo'
date = 2024-04-16T13:02:04+10:00
draft = false
[params]
  author = 'Eason Li'
  description = 'How to build a simple website with Hugo. Hugo is a static site generator written in Go. Its famous for its speed and user-friendliness.'
+++

### Introduction

In this blog post, I'll demonstrate how to construct a basic website using Hugo. For those unfamiliar, Hugo is a static site generator written in Go, known for its speed and user-friendliness. It's versatile enough to create anything from straightforward blogs to intricate websites. As an example, this very blog post you're reading is crafted using Hugo with the Paper theme.

### Prerequisites

Before we dive in, ensure you have the following:

- Command line access
- A text editor like VS Code or Sublime Text
- Git installed on your computer

### Step 1: Install Hugo

First, you'll need to install Hugo using a package manager like Brew or Apt.

##### macOS

```shell
brew install hugo
```

##### Ubuntu/Debian

```shell
sudo apt install hugo
```

### Step 2: Choose A Theme

Head over to the Hugo website and select a theme. Opt for one with comprehensive documentation and preferably dark mode support. For this demonstration, I'll use the Gokarna theme.

### Step 3: Create A New Site

#### Initialize a new site with the following command:

```shell
hugo new site sitename
```

#### Navigate to the new site directory:

```shell
cd sitename
```

### Step 4: Setup Git

Git setup is essential for deploying your website to GitHub and utilizing themes.

#### Initialize a new Git repository:

```shell
git init
```

### Step 5: Add A Theme

Refer to the official documentation of your chosen theme and follow the instructions to integrate it into your website, usually done as a Git submodule.

#### Add the theme as a Git submodule:

```shell
git submodule add https://github.com/526avijitgupta/gokarna.git themes/gokarna
```

> Ensure you replace the Git command with the one specified in the theme's documentation.

### Step 6: Setup Hugo

First, open the folder in a text/code editor and locate the hugo.toml file. You'll find something like this:

![config.toml](https://i.ibb.co/TmvVfMx/Xnip2024-04-16-18-37-35.jpg)

Begin by adjusting your site title. Then, add the theme by including the following line:

```toml
theme = "gokarna"
```

> Replace "gokarna" with the name of your theme.

#### Start the Hugo server:

```shell
hugo server
```

Open the URL displayed in the terminal to view your website.

Now, customize your website following the theme documentation. Since every site is unique, I can't provide exact customization instructions, but you can always seek assistance in the theme's GitHub repository.

### Step 7: Add Content (optional)

Assuming you're using this website for blogging purposes, follow these steps. To add a new blog post, create a new folder in the content directory called "posts." Then, create a new Markdown file with the post's name. Insert the following text into the file:

```markdown
+++
title = 'Title'
date = 2024-04-15T13:02:04+10:00
draft = false
+++
```

> Replace "Title" with your post's title and adjust the date accordingly. You can also change "draft" to true if you don't wish to publish the post yet.

Next, add your content below the front matter. You can utilize Markdown to format your content.

### Step 8: Deploy Your Website

Once satisfied with your website, deploy it to GitHub. Begin by creating a new repository on GitHub, then push your website to the repository. GitHub provides guidance on committing and pushing your code to the repository when you first create it. After pushing your website to GitHub, enable GitHub Actions with the Hugo template. Proceed to your repository settings and enable GitHub Pages, selecting GitHub Actions. Allow a few minutes for the website to deploy.

Thank you for reading! I hope you found this blog post helpful. Best of luck with your website!
