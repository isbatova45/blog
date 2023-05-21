---
# Documentation: https://wowchemy.com/docs/managing-content/

title: "Continuous Integration and Continuous Deployment (CD/CI)"
subtitle: ""
summary: ""
authors: [admin]
tags: [Academic]
categories: [Demo]
date: 2023-03-17T16:50:31+03:00
lastmod: 2023-03-17T16:50:31+03:00
featured: false
draft: false

# Featured image
# To use, add an image named `featured.jpg/png` to your page's folder.
# Focal points: Smart, Center, TopLeft, Top, TopRight, Left, Right, BottomLeft, Bottom, BottomRight.
image:
  caption: ""
  focal_point: ""
  preview_only: false

# Projects (optional).
#   Associate this post with one or more of your projects.
#   Simply enter your project's folder or file name without extension.
#   E.g. `projects = ["internal-project"]` references `content/project/deep-learning/index.md`.
#   Otherwise, set `projects = []`.
projects: []
---

In the context of modern development methods and DevOps, the abbreviations CI and CD are often used. CI stands for Continuous Integration and CD stands for Continuous Deployment (or Continuous Delivery).

Continuous Integration is a fundamental DevOps recommendation that developers regularly merge code changes into a central repository where automated builds and tests are performed. Developers who use continuous integration merge their changes back into the main branch whenever possible. Changes made by a developer are verified by creating an assembly and running automated tests on that assembly. When using continuous integration, a lot of attention is paid to test automation, as a result of which, when integrating new commits into the main branch, the application does not break.

There is also continuous delivery - the continuation of continuous integration, since it automatically deploys all code changes, that is, not only the testing process is automated, but also the product release process. Continuous deployment goes one step further than continuous delivery - every change that goes through the production pipeline is released to customers. No human intervention is required, and only an error during a test can prevent a new change from being deployed to production. Continuous deployment is used to speed up the customer feedback cycle.

Thus, continuous integration is part of both continuous delivery and continuous deployment. And continuous deployment is similar to continuous delivery, except that releases happen automatically.

The main disadvantage of using continuous integration and continuous deployment is that you have to write automated tests for each new feature, improvement or bug fix. In addition, you need a continuous integration server that can monitor the main repository and automatically run tests for each new committed commit. However, there are invaluable advantages - fewer bugs get into the production environment, because of this, the release build is much easier, testing costs are reduced, and the development process is accelerated.
