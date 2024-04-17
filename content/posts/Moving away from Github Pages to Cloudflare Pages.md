+++
title = 'Moving away from Github Pages to Cloudflare Pages'
date = 2024-04-17T13:02:04+10:00
draft = false
[params]
  author = 'Eason Li'
  description = 'I am moving away from Github Pages to Cloudflare Pages. Github Pages is a free hosting service that allows you to host static websites directly from a GitHub repository. Cloudflare Pages is a free hosting service that allows you to build, host, and scale your static websites or JAMstack projects.'
+++

### Context

For almost all of my projects, I have been using GitHub Pages because it nicely integrates with GitHub. However, for some of my projects, GitHub Pages are just not sufficient. With GitHub Pages, there is a cap of 100 GB bandwidth per month and 1 GB storage, which is inadequate for some of my projects. Therefore, I decided to migrate to Cloudflare Pages.

### Why Cloudflare Pages?

My website is powered by Cloudflare, obviously. Cloudflare Pages is significantly faster since it uses Cloudflare's global network. Cloudflare has CDN servers all around the world. If you don't know what CDN is, it stands for Content Delivery Network. It's a network of servers that deliver websites based on the user's location. Cloudflare Pages also offers unlimited bandwidth and 500 builds per month for free. 500 builds a month is somewhat limited since I publish content every day and like to change settings to experiment with my website. But it's still better than Github Pages.

### Other alternatives?

Sometimes I use Netlify. Netlify is also a JAMStack platform for deploying static websites. I don't use Netlify as much as Cloudflare Pages because Netlify has a limit of 100GB bandwidth per month. For some small projects, I use Netlify. One of the reasons I use Netlify is because it includes a feature called Netlify Forms. It allows you to create forms using only HTML, and Netlify will handle the backend for you. It's a great feature for static websites.

Thank you for reading! I hope you find this article helpful. If you have any questions, feel free to ask me in the comments below.
