# site-traffic-analyzer

The core purpose of this project is to serve as a way for me to practice designing and building web applications and deepen my working knowledge of Python. At the same time, I'm hoping to end up with a useful working application.

The rest of this document will focus on the application itself, and track my features and design decisions. I may make a separate document to log some of progress on the learning aspects of the project.

## Problem Statement

When analyzing traffic for a website, there are two primary tools that almost every website owner or marketer uses: Google Analytics and Google Search Console. Each of these tools provides useful information--Google Analytics provides data on user behavior on the site, such as how much time they spend on each page, whether they browse from one page to another, and when they leave the site. Google Search Console provides data on the website's performance in Google search, which is currently the main way many websites get visitors. It tracks metrics such as which pages are showing up in Google search results, what queries users are making when they see those pages, and how often users click on each page of the site in the search results.

The problem is twofold: one, both of these tools provide a wide range of metrics, and it can be difficult to drill down into the key data that's truly important for making decisions about the site. And second, the two tools aren't closely integrated. Although there are some limited ways to incorporate data from one tool into another, most users end up opening both tools individually and flipping between them to get a full view of how their websites are performing. This is inefficient, and is likely causing users to miss out on key conclusions that could help that make better decisions about the website.

## Solution

I intend to create a tool that can parse data from Google Analytics and Google Search Console, correlate the data where possible, and display the most important metrics from both tools in one simple interface. Eventually, I'd like to add deeper analysis functions to aid the user in drawing conclusions about the performance of the website.

As a first step, I'm going to implement this tool as a locally-running application that parses a CSV data file from each tool. However, my ultimate goal is to run the tool in the cloud and allow it to directly talk to both tools using their APIs.