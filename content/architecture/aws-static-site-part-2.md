---
title: "Dynamically Build a Static Website on AWS (Part 2)"
date: 2018-06-10T12:54:00-04:00
author : "Brian Austin"
image : ""
summary : "Leveraging 3rd party tools to take content generation to the next level"
slug : "aws-static-website-part-2"
categories: ["Architecture", "Featured"]
tags: []
draft: false
---

<!--more-->

## Overview
In my previous article, I described how to construct a HTML/CSS/Javascript static site using native AWS services. While this was a great first step toward understanding cloud native development, the need of *THIS* site compelled me to look further toward automating the process. In this article I will detail how I made this site dynamically regenerate when new articles are added.

## What's Involved
* AWS S3 web hosting
* [GitHub](https://github.com/) - File repository
* [Travis CI](https://travis-ci.org/) - Build/Deploy automation
* [Hugo](https://gohugo.io/) - Static sight generator

## How It Works

Content is first created on my local machine using VSCode, my IDE of choice. When I need to preview my content changes I invoke the local Hugo server in my Terminal window. My terminal of choice is Bash on Ubuntu on Windows 10. Hugo will ingest the markdown files, apply templates, construct layouts and generate static HTML.

When I'm satisfied with my changes, I commit to my GitHub repo using terminal and push changes. After the push, the associated Travis CI build invokes the Hugo binary, compiles the static HTML and uploads the files to an S3 bucket that is configured for website hosting.

Using these simple steps I am able to add and update content on the static cloudshock.io site without pushing code from my local development environment to the cloud.  Further, since the process is automated I can easily initiate an update from *ANY* system in the world as long as I have access to my Github account.

## Why is This Useful?

Automation of repetitive tasks is a life saver for small organizations. When you automate you remove the tendency for silos of skills and implementation to exist. Using this CI/CD pattern it's possible for a second or third content creator, who has no prior knowledge of this configuration, to make and deploy changes to the website.

Additionally, using off the shelf community tools such as Hugo and Travis CI provide a repeatable process that doesn't require hours of developer time to maintain. If I, alternatively, hand scripted the build/deploy process I am on the hook for maintenance and support when something goes wrong. Community tools are often associated with a wide variety of community support via platforms like Stack Overflow.

Last, by using this stack for a static website I am saving money by not running an EC2 instance 24/7 in order to keep a CMS system like Wordpress online. Because content is identical regardless of visitor, I can easily serve pre-compile pages. I only need compute cycles when content changes, and only for a brief period of time.

## Additional Resources? ##

### Getting Set Up ###

#### Visual Studio Code ####

 Visual Studio Code (VS Code) is an open source code editor managed my Microsoft. It is available on Windows, Linux and macOS as freeware. The product is maintained by the open source community and supports a multitude of languages.

 VS Code is very similar to tools like Atom and Sublime. In my opinion VS Code has one major advantage over Atom in that VS Code executes plugins on a separate thread from the editor window. Thus, when a plugin crashes it does not take down the editor as well.


  [Download here] (https://code.visualstudio.com/)

#### Bash on Ubuntu on Windows ####

  Installing the Linux subsystem on Windows is easy and avoids the overhead of installing a   virtual machine. However you will need a copy of Windows 10.

  The official installationg guide can be found here: [Windows 10 Installation Guide](https://docs.microsoft.com/en-us/windows/wsl/install-win10)

#### Hugo static site generator ####

  [Hugo](https://gohugo.io/) is a cross platform site generator written in GO.  It can be installed under Linux using either the package manager or via the latest binary from Github.

  The official instructions are here [GETTING STARTED FUNDAMENTALS - Install Hugo](https://gohugo.io/getting-started/installing/)

#### Hugo + Travis ####

  Hugo project builds can be automated and deployed by Travis CI. If you are using an open source GitHub repository you can set up the CI/CD via TravisCI.Org
 
  This article by Chris Hager describes how to set up your travis.yml file to build and    deploy your site to GitHub pages, another cheap alternative to Wordpress. With minor modification you can substitute an AWS S3 deployment for this step.

  Chris' instructions can be found here: [Continuous Deployment: Hugo + Travis CI → GitHub Pages](https://www.metachris.com/2017/04/continuous-deployment-hugo---travis-ci--github-pages/)

  Travis CI deployments to S3 instructions can be found here [Travis CI - S3 Deployment](https://docs.travis-ci.com/user/deployment/s3/)

#### Amazon S3 Webhosting ####

 At minimum you will need to create and set up an AWS S3 bucket to host your website. Additionally, you can set up a custom domain via Route 53 and configure SSL using   AWS Certificate Manager and CloudFront. I will cover these deployment topics in a later article.

  For now, follow these instructions to set up an S3 bucket as a website. [Example: Setting up a Static Website](https://docs.aws.amazon.com/AmazonS3/latest/dev/HostingWebsiteOnS3Setup.html)

### Implementing the Site ###

#### Hugo Docs ####
 I strongly recommend bookmarking the Hugo Docs. Here you'll find all the command line (CLI)   commands you'll need.  You will also find more in depth explanations of how functions,   variables, and templates work.

#### Hugo Training Video ####
  Also check out this great series of how-to Hugo videos from Giraffe Academy. [Introduction to Hugo | Hugo - Static Site Generator](https://www.youtube.com/watch?v=qtIqKaDlqXo&list=PLLAZ4kZ9dFpOnyRlyS-liKL5ReHDcj4G3)

#### Examples ####
  Don't forget to check out the GitHub repo for this site which includes a working example of the entire process end-to-end. [brianwaustin/cloudshock.io](https://github.com/brianwaustin/cloudshock.io)

