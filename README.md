# cloudshock.io #

**Cloud Shock** - **_Cloud Development for Small Business_** 

## About ##

Cloud Shock is a website I created as a collection of cloud development and deployment 
related topics. I built the site in response to an unmet need discussing
and deseminating information about cloud development for small enterprise businesses.

## Why Did I Build It This Way? ##

By automating static site generation and hosting via Amazon, I'm able to build, host and update
this site at a lower cost. Typical Wordpress installations either require a paid account on Wordpress.com, or a dedicated EC2 instance to run 24/7. This is overkill because most of the content on this site 
*NEVER* changes.  

## How I Built the Site ## 
I build the Cloud Shock site [cloudshock.io](http://cloudshock.io/) using the following tools:
* HTML/CSS/JavaScript - Based on a popular Wordpress theme
* Hugo - An open-source static site generator
* Github - Version control
* TravisCI - Continuous integration & deployment
* Amazon Web Services
  * S3 - Static file hosting
  * Route 53 - DNS Mangement
  * AWS Certificate Manager - SSL certificates
  * CloudFront - SSL assignment and web hosting
  * IAM - Identity management & deployment keys
  * AWS Lamdba / API Gateway - Serverless microservice calls (coming soon)

## Roadmap - What's Next?? ## 

My near term roadmap for this project includes
* Adding additional cloud centric content (the original purpose of the site)
* Adding analytics, probably via Google
* Integrating AWS Lambda/API Gateway microservices for features like:
  * Contact Us
  * Dynamic content (client-side JavaScript)
  * Whatever else I can think of
* Adding serverless file uploader prototype
