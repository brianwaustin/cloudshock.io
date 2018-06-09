---
title: "Using Open Source Software in Proprietary Code"
date: 2018-04-16T17:08:08-04:00
author : "Brian Austin"
image : ""
summary : "Open source software is not always “cheaper” in the long run because it is “free”, but it can provide a distinct advantage for solving novel and unique problems."
slug : "using-open-source-software"
categories: ["Strategy"]
tags: ["Open Source", "Featured"]
draft: false
---

<img class="article-title-image" src="../../images/focus-on.png" />

Open source software is not always “cheaper” in the long run because it is “free”, but it can provide a distinct advantage for solving novel and unique problems.  

<!--more-->

However one must consider a variety of factors before utilizing open source software within new intellectual property concerns.

## FALLACIES OF OPEN SOURCE
### NO LICENSE OR MAINTENANCE FEES

**WHY**: Fees for commercial products can range from a few percentage points to as much as 20 points

**TRUTH**: Some open source does have “licensing fees”:
* Commercial use
* Documentation
* Coherent software collection which is packaged consistently, with a nice installation

## OPEN SOURCE MEANS LOWER IT COSTS

**WHY**: Often free to install

**TRUTH**: Often more expensive and time consuming to maintain

## INSTALLATION AND CONFIGURATION COSTS
The price of commercial software is often offset by the implementation time required to fully deploy and configure an open source based system.

### Open Source

* Time consuming, especially for IT shops that lack skill depth in the tool
* Requires “fiddling”, especially more immature products
* Undocumented or edge case configuration discovered through:
* Trial and error
* Reading code

### Commercial Software

* Install optimized for IT using guided “wizard” installation
* Undocumented or edge case configuration discovered through:
* Comprehensive documentation
* Lengthy support calls or expensive engagements for services

**Considerations:**

* An organization’s skill level directly impacts time spent installing and configuring open source tools
* New or immature open source tools typically require extensive Internet research and trial and error

## INTEGRATION AND CUSTOMIZATION COSTS
Commercial software provides features out of the box, open source requires more time, effort and IT staff skill to provide the desired integration into an existing IT system.

### Open Source

* Not optimized for integration in traditional and legacy IT infrastructure environments
* Require customization when project doesn’t meet requirements
* Grey area between a buy versus build:
* Is a decision not to buy, but to build as little as possible

### Commercial Software

* Lack of legacy IT integrations can exist for commercial products, early in life cycle
* Vendors productize and provide most common integrations, as product matures

**Considerations:**

* Open source customization requires skill development that must be trained or obtained through outside resource
* IT department must integrate and customize open source projects to work with traditional and legacy systems on their own, without support from vendor

## THE COST OF NARROWNESS
 Commercial software typically meets a set of common use cases and implementations that are supported.  Open source software is community driven and meets needs as they arise, and remains flexible in end user implementations.

### Open Source

* Places the burden on IT department to:
* Develop, find, or train skills
* Evaluate, install, configure, operate, and support the software
* Allows extensive customization

### Commercial Software

* Provides a known set of features out of the box, for a given cost
* Customization is limited to a common set of needs or product roadmap

**Considerations:**

* Narrowness cost is evaluated by ultimate needs of the IT organization:
* If you do not need custom features, the cost is nearly zero
* If you require customized features, the cost will be very large

## OPEN SOURCE LICENSING CONCERN
Using open source software can increase maintenance costs and legal liabilities depending on licensing arrangement.

When evaluating open source software one must consider that some open source licenses may impact the proprietary software and intellectual property assets of a company.

### KEY TERMS
**Distribution** – Distribution of the code to third parties. This includes packaging libraries with binaries such as mobile apps

**Private use** – Internal use of modifications

**Sublicensing** – Can modified code can be re-licensed or must it retain the original license?

**Copyleft** – A product using this code must provide information necessary to reproduce and modify the work for all distributed binaries

**Permissive** – Allows developer to “do anything they want” with the code as long as they provide attribution and don’t hold author liable

### LICENSE TYPES
**MPL (MOZILLA PUBLIC LICENSE)**
* Permissive for private use
* Modifications to MPL code must be made available (as source code)
* Does not affect proprietary code as long as it doesn’t include any MPL code
* Packaging of proprietary IP is critical
* “Minified” JavaScript code is NOT considered “source code”
* Must provide source code to any MPL modified JavaScript code

**GPL (GNU GENERAL PUBLIC LICENSE)**
* Considered “viral”
* Any derivative work created which contains even the smallest portion of the previously GPL licensed software must also be licensed under the GPL license.

**LGPL (GNU LESSER GENERAL PUBLIC LICENSE)**
* Requires software to be modifiable by end users via source code availability.
* May be used for proprietary software, but must be packaged in a clear separation between the proprietary and LGPL components

**AGPL (AFFERO GENERAL PUBLIC LICENSE)**
* Extension of the GPL that “closes the application service provider (ASP) loophole”
* Requires full source be made available, even for web applications

**APACHE LICENSE (2.0)**
* Does not require royalties
* Does not require derivative works, or modifications to be distributed using the same license
* Can be used in proprietary, commercial products
* Compatible (maybe bundled) with GNU General Public License (GPL)
* Not compatible with GPL versions 1 and 2

**CONSIDERATIONS**
The Free Software Foundation (fsf.org) actively enforces the terms of GPL licensed code.  In most cases they quietly ameliorate compliance problems by forcing violators to either pay a licensing fee, or releasing source code to the community.  In rare cases, violators ends up in court.

### EXAMPLES:

**PACKAGING OF GPL LIBRARY**
Hancom Office incorporated an open-source PDF interpreter in a word processor app and did not adhere to GNU General Public License (GPL). This could be resolved by:

Hancom open-sourcing the Word Processor code
Pay a licensing fee to Artifex, the developer of the library

**CUSTOMIZATION OF GPL CODE**
Panasonic Avionics monopolized an in-flight entertainment (IFE), a product derived from CoKinetic Systems open-source (IFE) software

CoKinetic is seeking compensatory damages for Panasonic’s GPL ongoing GPL breaches in excess of $100 million
The complaint, filed in the Southern District of New York, demands a jury trial

**FAILURE TO OPEN SOURCE CODE**
VMware combined proprietary source code with open-source code in its ESXi product line but has not released it publicly as required by the General Public License version 2 (GPLv2)

---

Sources:

1. – [Open Source for the Enterprise by Gautam Guliani, Dan Woods] (https://www.safaribooksonline.com/library/view/open-source-for/0596101198/ch04s02.html)
2. – [Comparison of free and open-source software licenses] (https://en.wikipedia.org/wiki/Comparison_of_free_and_open-source_software_licenses)