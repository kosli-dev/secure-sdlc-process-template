# Secure SDLC process template

**Tl;dr if you are struggling to define a secure software delivery process, or you're not really sure what to do, or it just feels like a bunch of hassle and you just want an easy button - this repo contains secure steps for build, process and runtime that have been defined based on several years of DevOps consultancy in highly regulated environments. Feel free to fork it and make it your own**

## Overview

**How to define your software delivery process with Kosli’s secure SDLC template**

This is a secure SDLC process template for teams who want to practice continuous delivery with audit, compliance, and security baked into their deployments. 

It is especially applicable for DevOps teams who release software to the cloud while adhering to industry regulations and/or standards. 

If you are struggling to define a secure SDLC you are welcome to fork this repo and follow the tutorial. 

## Why have we open sourced our secure SDLC process template?

One of the big things we’ve learned since starting Kosli is that software development teams often struggle to define a software development process. Why is this important and why do teams have to define this?

Defining a process for delivering software is a necessary first step for teams in regulated industries, or for teams opting into a voluntary standard like SOC2 or ISO27001. 

Compliance with these regulations and/or standards requires you to define, implement, and prove that you’re following a process. 

This template is designed to help you define your process. You are welcome to fork it and start making it your own. There are guidelines for how to proceed with this further down.

## What do regulations and standards mean for the SDLC?

It doesn’t really matter which industry you’re in, or which standard you’re going for, the demand for change management in the SDLC is basically the same - prove you’re following a process. 

But it’s important to understand what this really means. Many people assume that a change management process must necessarily involve manual work like evidence gathering, change advisory board meetings, and sometimes even wet signatures! 

None of this is true. Not even for medical devices. To repeat, the demand in all of these regulations and standards is actually quite simple (if somewhat open to interpretation) - define a process and prove it’s being followed. 

As an example, the change management stipulation shows up in the following subsections of 3 well known standards. Try to find anything in any of these standards that says you need manual sign offs and meetings. It does not ask for this

SOC2 CC8 - Common Criteria 8

ISO27001 Annex A.8.25 - Secure development life cycle

In IEC62304 5.1 - 5.8 - Software Development Process

Kosli exists because when we did DevOps consultancy in regulated companies people would offer exactly these objections - “we can’t practice continuous delivery, we need a meeting first.”

When we discovered that this wasn’t true we built a platform to automate the change management part of the SDLC. So, this template is a free resource to help you define your process. 

If you want to bake change management automation into it so you can breeze the "proving" part please contact us.

## Who needs Kosli’s secure SDLC process template?

In our experience, the problem we’re solving with the secure SDLC template affects two different types of teams

**Team 1:** A DevOps/Cloud Native team in a new company (e.g. a fintech) runs into an event like a software audit, or they realize they need to comply with a standard like SOC2 or ISO27001. 

They have no defined process and don’t know how to pass an audit or achieve compliance without disrupting their existing automation. 

**Team 2:** A legacy software organization with manual processes for compliance and audit is going through digital transformation, adopting DevOps, migrating to the Cloud, etc. 

They are restricted by existing change management processes that won't scale with modern tools and practices.

**Team 1 has speed without compliance.** 

**Team 2 has change management that doesn’t scale**

The secure SDLC process template helps both of these teams because it enables them to deploy with speed and compliance.   

## What is in the secure SDLC process template?

The secure SDLC template has been defined by pulling together a range of best practices from high performing DevOps teams in various industries, including those where regulatory demands are high - like finance, automotive, and healthcare.

It’s specifically designed with Agile and DevOps values in mind so that software delivery teams can achieve two things that are usually seen in opposition to each other:

**1 Deploy software to production with maximum speed and continuous delivery**

**2 Deploy that software in state of continuous compliance and audit readiness**

This template will help you to define a process that meets both of these criteria. It covers everything you need to excel at each stage of your SDLC.

Below are building blocks for **Build, Process** and **Runtime** that you will use to define your own secure SDLC. 

In the next section we will show you how to fork this repo and use these building blocks to define your own SDLC.

**Secure Build**

Artifact Binary Provenance

Version Control

Defined Toolchain

Dependency Management

**Secure Process**

Code Review

Quality Assurance

Security Vulnerability Scanning

Deployment Approvals

**Secure Runtime**

Change Records

Deployment Controls

Secrets Management

Service ownership

Workload Monitoring

## How to use the secure SDLC process template

In this section we will take you through the repo and provide a 3 stage tutorial on how to define and publish a SDLC process for a fictional fintech called AcmePay. 

Firstly, you will fork the template. You will then adapt the template so that it meets the requirements of your particular organization. Finally, you will publish the template online. 

1 For the repo and rename it - EASY!

2a Open the content folder. 

Here you will see a markdown file **index.md** The copy on this file is basically what will appear on the “homepage” on your SDLC. 

We use it to introduce the template and explain how to apply it to various standards. But you’ll want something different. 

You can make this file as long or as short as it needs to be. At AcmePay we keep it simple so we’ll simply amend this file to read:

This is the secure SDLC for AcmePay. 

That’s a good enough description for us, so we’ll commit that change and merge it to main.

2b Back in the content folder we have two other sub folders: **Background** and **Process.** 

In the template we use these files to talk about why we made the template and the values that inform it. 

Keeping these files in your repo is entirely optional. You can either:

(i) Update them to reflect some high level objective(s) you have, say something about what you’re trying to achieve with your SDLC, maybe the explicit purpose you have - e.g. SOC2. 

(ii) Delete them. 

2c Next, open **Process > SDLC** 

This is where you will define the actual steps for your secure SDLC - from build to runtime.

You will see the 3 sub folders containing the files for **Build, Process** and **Runtime** listed above.

Read through the files for each of the steps and decide what’s right for your team. 

Amend or delete those parts that aren’t necessary for your SDLC, and of course add any steps that are necessary for your team but aren’t covered in the template. 

2d You will also see files for a **risk register**, an **exception register**, and **training**. Again, amend or possibly even delete these files according to your needs and the specific requirements of the standard you’re complying with. 

Once you’re happy with the way you’ve amended the various files and committed your changes, you’re ready to publish your version. 

3 Publishing your secure SDLC

Go back up to the main repo and find the **setup.md** file.

This file will explain how to deploy the site with Hugo. 

Here is our own version, forked from main as part of our SOC2 process. https://sdlc.kosli.com/

If you're interested in discovering how to automate the *proof* that you're 
following your SDLC - gathering evidence for tests, security scans, pull requests, etc 
head over to https://www.kosli.com/
