# User Guides
The following entries show examples of technical documentation I have created specifically for end users.
## Cloud Update Service
The Cloud Update Service (CUS) is a Hyland product that is used to track and update OnBase components. OnBase is a suite of enterprise document management software with dozens of available components, so this product allows users to more easily track and update those components.\
I wrote the user guide for the CUS, including the installation steps and the steps for navigating and performing tasks on the Cloud Update Admin Portal. The entire user guide for this product is hosted [here](https://support.hyland.com/r/Current/Cloud-Update-Service).\
The CUS user guide was created in the Ixiasoft Component Content Management System (CCMS) and written in eXtensible Markup Language (XML) using the Darwin Information Typing Architecture (DITA) standard. The writing style is according to the Microsoft Writing Style Guide for general guidelines and the internal Hyland writing style guide for grammatical preferences and conventions specific to Hyland software.
### Removing Workers
For a specific example from within the CUS user guide, let's take a look at the topic [Removing Workers](https://support.hyland.com/r/Current/Cloud-Update-Service/mnm1772477973068).\
A "Worker" in this context is a piece of the CUS that is installed locally on each server in a user's environment. I chose to highlight this topic because this is a feature that requires explanation to users, both for the general purpose and what specifically happens when using this feature.\
The purpose of this feature is to remove disconnected workers and their associated OnBase components from the lists on the Cloud Update Admin Portal. Without this feature, any workers that were intentionally uninstalled after being registered in the Cloud Update Admin Portal would remain on the portal with a "Disconnected" state and clutter the user's list of available workers. However, the word "remove" may imply that the worker in question is being deleted from the user's server. In order to prevent any confusion, I had to confirm with Subject Matter Experts (SMEs) exactly what was happening when using this feature, and multiple parts of the topic (in particular, a bullet point in the introduction and a Note in the steps) are dedicated to explaining how "removing" a worker is not the same as deleting or uninstalling it.
## WebSMARTT
WebSMARTT is a product owned by Heartland School Solutions that is designed to handle all of the school-side aspects of school lunch programming. This includes the point of sale, inventory, menu planning, and applications for low-cost or free lunches provided by the National School Lunch Program (NSLP).\
I became the writer for the WebSMARTT help documentation when it was accessed solely from the same files installed locally with the WebSMARTT program. In 2018, the help files were uploaded to Confluence and can be found [here](https://mcssoftware.atlassian.net/wiki/spaces/WEB/overview?homepageId=293699626).\
The WebSMARTT help documentation was created and primarily updated in Adobe RoboHelp. The writing style is according to the Chicago Manual of Style for grammar and punctuation, and the Microsoft Manual of Style is referenced for software interaction and UI terminology.
### WebSMARTT Sync
For a specific example from within the WebSMARTT help documentation, let's take a look at the topic [WebSMARTT Sync](https://mcssoftware.atlassian.net/wiki/spaces/WEB/pages/314147027/WebSMARTT+Sync) and its subtopics.\
WebSMARTT Sync, or WS Sync, is a feature that allows users to synchronize communication between WebSMARTT and school site databases. I chose to highlight this group of topics because I think it demonstrates taking a feature that is uniquely configured compared to other WebSMARTT offerings and guides users step by step to make the process as simple as possible.\
On most of the WebSMARTT tabs (Customers, Point of Sale, etc.), features are organized into tiles with hyperlinks to specific pages containing the individual features. However, the WebSMARTT Sync tile displays hyperlinks to three pages that are meant to be completed in sequence. To convey this, the hyperlinks are described and written as "steps" 1-3 instead of a series of options from which a user may select. After a user reaches the end of the page explaining one step, there is an explanation of how to navigate to the next step and a link to the page containing the next step. On each step's page, there are multiple screenshots, some with relevant areas highlighted, for each action and result in the process. I obtained screenshots and details for these steps by using access to a testing environment and performing steps myself. This was not limited to the golden path, as some screenshots highlight specific error messages. I made sure that I could navigate the pages myself before writing instructions in the help documentation instead of receiving information from a member of the development or product management team and copying the information sight unseen.
# Internal Documentation
The following entries show examples of technical documentation I have created with internal users as the primary audience. This includes developers, support, and other technical writers.
## MySchoolBucks.com Data Transfer API Version 2
MySchoolBucks (MSB) is a web-based suite of features for parents and school administrators to manage funds for school purchases, which can be used to buy school meals as well as supplies or spirit merchandise. The MySchoolBucks.com Data Transfer API is used to transfer purchasing and account data between MSB and the school's database.\
For the internal documentation related to this API, I was tasked with taking the information from the MSB development team and describing it in a way that is readable to other developers. The following is a general outline of the document since it is not available online:
1. Definition of components\
   a. Overview of MySchoolBucks.com\
   b. Secure Connection\
   c. Information Exchanged\
   d. Scheduling
2. API (includes the variables and what is returned from each line)
3. Upgrading from Version 1 to Version 2
4. Document Type Definitions
### Data Transfer API Example
Each line of the MySchoolBucks.com Data Transfer API is defined in the internal documentation. This includes what the line does, the definition of variables, and what is returned (if applicable). To show how I organized this information into something more readable, here is an example:
```
byte[] getGLAcctReportXML(String userID, String password, String startDate, String endDate)
```
Downloads G/L account entries in XML format from MySchoolBucks to the client application.
| Variable | Description |
| -------- | ----------- |
| userID | The MySchoolBucks user ID to login |
| password | The password associated with the userID to login to MySchoolBucks |
| startDate | Includes transactions with a batch date of startDate or later |
| endDate | Includes transactions with a batch date of endDate or earlier |
**Returns:** An XML document
## Hyland Technical Writing Style Guide
The Hyland Technical Writing Style Guide is an internal resource for the technical writers at Hyland that outlines how to write when writing Hyland user guides. This is to ensure a consistent voice across documentation even when written by many different writers. This style guide also defines how to write about Hyland products, including how to capitalize proprietary terms, how to refer to software, versioning, etc.
# Video Tutorials
The following entries show exampes of animations or video tutorials I created while making e-learning and training materials.
## How-To Videos for MySchoolBucks
During my time working for Heartland School Solutions, I was tasked with taking the most common end user processes for MySchoolBucks customers and create short video tutorials for them. These videos were then posted to YouTube, with links to the videos (as well as PDF transcripts for those videos) being hosted on [the MySchoolBucks website](https://www.myschoolbucks.com/ver2/help/gethelpvideos).\
These videos were captured and edited using Camtasia. I captured the footage from a demo account for the website and then edited in the provided narration, intro, and outro graphics.
### Setting Up Automatic Payments
The most requested video tutorial was for setting up automatic payments (or "AutoPay") on MySchoolBucks. When originally documenting this process in the user guide, the steps branched (such as for whether the user wanted to make the payments trigger at recurring intervals or when any student's account falls below a certain threshold) and contained details for specific points in the process. However, to keep the video as brief as possible (I believe that the request was to make the videos about 30 seconds to 1 minute each), I needed to focus on which steps were absolutely necessary and how to convey information as concisely as possible. I also needed to time explanations to the narration.\
The video is available on YouTube [here](https://www.youtube.com/watch?v=ZdpNmg19TI4).
# Contact
[LinkedIn](https://www.linkedin.com/in/charles-diab/)\
[Email](mailto:charles.t.diab@gmail.com)
