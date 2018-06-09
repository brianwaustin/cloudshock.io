---
title: "Dynamically Build a Static Website on AWS"
date: 2017-05-16T17:08:08-04:00
author : "Brian Austin"
image : ""
summary : "A design pattern to build a dynamically generated static website on AWS"
slug : "aws-static-website"
categories: ["Architecture"]
tags: []
draft: false
---

<img class="article-title-image" src="../../images/architecture/aws-static-site.png" />

<!--more-->

## Overview

The diagram above illustrates how you can build a dynamically generated static website using 
AWS cloud services.

## What's Involved
* AWS S3 object storage
* AWS API Gateway
* AWS Lambda
* AWS Simple Notification Service (SNS)
* AWS DynamoDb or RDS

## How It Works

The static website is hosted on an S3 bucket as a website. 

When a content change is required, an API call is made through API Gateway which does two things:

1. Stores the change in the data persistence layer
2. Triggers a notification to rebuild the static content

The AWS Lambda function receives the notification, reads the data from the persistence layer and redeploys the static HTML content to S3.

## Why is This Useful?

The above archiectural pattern can be used for content that is infrequently modified, but frequently accessed. The pattern removes the need for dynamically generated content for each request, and instead only invokes compute resources when the source information changes.

This is *extremely* effective for documentation, marketing, and mostly static web content. A simliar mechanism is employed for sites using [Hugo](https://gohugo.io/) or [Jekyll](https://jekyllrb.com/), although their compute cycles typically take place in a developer environment.