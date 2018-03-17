===Profile Information

Name: Ujjwal Agrawal
University:  IIT (ISM), Dhanbad
Email: ujjwal.iitism@gmail.com
Github: ujjwalagrawal17
IRC nick: ujjwalagrawal17
Other Contact Methods: Google Hangouts, Gitter Chat
Blog: https://ujjwalagrawal.wordpress.com/
Twitter: ujjwal171097
Location: India (UTC +5:30)
Typical working hours: Between 1 pm and 11 pm UTC +5:30


===Synopsis
**About the app:**
The Wikimedia Commons Android app allows users to upload pictures from their Android phone/tablet to Wikimedia Commons. Wikimedia commons accept only freely licensed media files (that are not subject to any copyright). Users can upload images and then add various tags specific to them such as category, title, and description, license.

**About the project:**
This project is aimed at providing an option to browse/search the Wikimedia Commons using the app.

**Why this feature is needed?**
- More and more, users are asking (as evidenced by Play Store feedback), people want to be able to also browse existing Commons images via the app.
- Quality of uploads should increase by letting users see other people's work.

**What can be implemented ?**
- Image Search on Wikimedia Commons using a title.
- Restrict the search results to images, or make sure no crash happens when opening exotic formats such as SVGs or sounds
- Link to the Media Details activity to see an image's details (Needs feedback)
- Category Search on Opening details shows the sub-categories and the images present in that category
- Modify the category activity to show the best images first. (Bonus)

**How it can be implemented?**
- Explore Mediawiki APIs to search images using titles, search categories.(Probably using SEARCH API) 
- Implement async calls requests to request Search pictures 
- Develop feature for displaying search results in Featured Images Activity.
- Implement async calls requests to request Search Categories 
- Implement the category activity, which shows the sub-categories and the images present in that category
- Debugging, testing followed by code documentation.
- Release (at least in alpha)

**Mentors** 
- @Nes 
- @Nicolas_Raoul


===Timeline
// To be updated ..

| **Period** | **Task** | **Deliverables** |
| ------------- | ------------- | ---------------|
| April 23 to May 14  | **Community bonding period.** - getting familiar with the app architecture and Wikimedia APIs | Weekly report and blogs about the experience, app architecture |
| May 14 to May 21  |   |   |
| May 21 to May 28  |    |   |
| May 28 to June 4 |    |   |
| June 5 to June 10  | Testing, Bug fixes, Writing documentation. Code cleanup for release (at least in alpha) |  |
| June 11 to June 15  | **Phase I evaluation**  |  |
| June 16 to June 24  |   |  |
| June 25 to July 1  |   |  |
| July 2 to July 8  | Release (at least in alpha), write documentation, test, fix bugs  |  |
| July 9 to July 13  | **Phase II evaluation**  |  |
| July 14 to July 22  |    |   |
| July 23 to July 29  | Testing, Bug fixes, Writing documentation. Code cleanup for release (at least in alpha) |   |
| July 30 to August 5  |   |   |
| August 6 to August 13  |   |   |
| August 14 to August 21  | Mentors submit final student evaluations.  |  |
| August 22  | **Final results of Google Summer of Code 2018 announced**  |  |
|--------------|-------------------|


===Participation

**Progress Report**
- I will remain online on IRC, Hangouts during my working hours ( 1 pm to 11 pm UTC +5:30)
- I will write Weekly Blog Posts at (https://ujjwalagrawal.wordpress.com/) .
- I will share my blogs on Twitter.
- Write Weekly Scrum Reports and update it in our mailing list [commons-app-android@googlegroups.com]
-- What did I do last week?
-- What will I do this week?
-- What is currently preventing me from reaching goals?
- I will submit a Project Presentation
**Where you plan to publish your source code**
- I will be working on a separate branch on git and uploading code to the forked repo almost on a daily basis, will be Creating pull requests when a complete feature is done.
**Communication on task**
- I will use Phabricator to manage bugs and task.


===About Me

**Personal background**

I am a third-year B.Tech. undergraduate at [Indian Institute of Technology (ISM), Dhanbad](https://www.iitism.ac.in/) . I am pursuing Electronics and Communication Engineering as my Major. I have a keen interest in Android App development( I have been doing Android App Development from last 2 years). I use git and Github every day and I am well acquainted with how to use them for version control.

**How did you hear about this program?**

Heard about GSoC in a campus meetup. I am an open source enthusiast from past 1 year, I've always wanted to take part in Google Summer of Code.

**Time during Summers**

I have no other commitments this summer. So I'll be able to give 40 hours or more per week. My summer break starts on 30th April so I can start working full time from that day on. I'll not be taking any vacations. My classes start around 20th July but I will be able to commit enough time to the project as there are no exams during the period

**Eligible for Google Summer of Code and Outreachy ?**

I am applying only for GSoC as I am not eligible for Outreachy program. I am applying under Wikimedia Commons Android only.

**What excites me about this project**
//TBU
I loved the goal of Wikimedia Foundation "Global movement whose mission is to bring free educational content to the world".
I would be really great for me to apply my skills and contribute to such an organization.

==Past Experience

I’ve been doing Android development since my first year. My first project was a Home Automation app to control LED lights using our mobile phone(Raspberry Pi behaving as a server)that I built in a hackathon. After that, I had started making apps for my learning purpose. I liked making prototypes but I have always wanted to make apps that affect people's life. Apart from the prototype, I had also developed some apps that are in Google Play.

Brand Store: It is an app where users can get offers from nearby shops of different categories across their city. Shops can also register them and show their offers to the users of the app. Although the startup is closed now. but the app is still in google play.
- Google Play Link: https://play.google.com/store/apps/details?id=com.codenicely.brandstore.project&hl=en
- Github Link: https://github.com/CodeNicely/OfferCartApp

Spectrum'18: I had developed 
- Google Play Link https://play.google.com/store/apps/details?id=com.ujjwalagrawal.spectrum&hl=en


Apart from this, I also have received the Google India Challenge scholarship for Android Developer nanodegree .  have made 2 projects under it as of now.


=== Contributions to Wikimedia Commons App

It has been an enriching experience contributing to the app and I look forward to continuing contributing to it. For all I have learned so far is that your contributions is not just the number of Pull Requests that you’ve got merged. But contributions can be in various forms like:

- Creating New Issues
- Finding Bugs
- Helping New Contributors
- Communicating with Moderators and helping them

====Contribution related to browse/search feature:

I’ve been working on this feature for some time now. I had made a small prototype for the same. 

- **Description**

> - Added a Separate activity for search in which an edit text is present.
> - Implemented a viewpager along with a tab layout in the activity
> - Added Browse Image fragment, Browse Category Fragment in the item of the viewpager.
> - Now if a text is changed in the activity I am calling update list method in both the fragments with search query as a parameter.
> - Method update list updates the list by fetching details from [Wikimedia API: Search](https://commons.wikimedia.org/w/api.php?action=help&modules=query%2Bsearch)
> - For updating the list in recycler view I had added AdapterFactory, Renderer similar to other modules.
> - No searches are saved in the local database now but we can implement it for showing list of recently used searches.  
 
- Video Link: https://goo.gl/7XUv9w
- Github Link : https://github.com/ujjwalagrawal17/apps-android-commons/tree/browse

====Pull Requests: 

- **Merged Pull Requests: **

> -  [Change toast to sanckbar in App](https://github.com/commons-app/apps-android-commons/pull/1307) 
> -  [Update Issue Template](https://github.com/commons-app/apps-android-commons/pull/1286) 
> -  [Improvement in Login UI](https://github.com/commons-app/apps-android-commons/pull/1280) 
> -  [Faqs added in About Activity](https://github.com/commons-app/apps-android-commons/pull/1256) 
> -  [Rate Us feature ](https://github.com/commons-app/apps-android-commons/pull/1188)
> -  [Changed WebView to CustomTabs in App](https://github.com/commons-app/apps-android-commons/pull/1185)
> -  [Created Template for Pull Request](https://github.com/commons-app/apps-android-commons/pull/1152)
> -  [Created Template for Issue](https://github.com/commons-app/apps-android-commons/pull/1145)

- **Closed Pull Requests: **

> -  [Change Toolbar color](https://github.com/commons-app/apps-android-commons/pull/1190)
> -  [Add Option to delete the contributed image](https://github.com/commons-app/apps-android-commons/pull/1142) 

- **[Open Pull Requests](https://github.com/commons-app/apps-android-commons/pulls/ujjwalagrawal17)** 

====Issues:

- **Closed Issues:**

> -  [Add FAQs page in Commons App](https://github.com/commons-app/apps-android-commons/issues/1246)
> -  [Add Option to donate to Wikimedia Foundation](https://github.com/commons-app/apps-android-commons/issues/1231) 
> -  [Change toolbar color to primary color](https://github.com/commons-app/apps-android-commons/issues/1189)
> -  [Rate Us feature in nav drawer](https://github.com/commons-app/apps-android-commons/issues/1187)
> -  [Adding PULL_REQUEST_TEMPLATE.md file](https://github.com/commons-app/apps-android-commons/issues/1146) 
> -  [Adding ISSUE_TEMPLATE.md file](https://github.com/commons-app/apps-android-commons/issues/1144)
> -  [Change Web views to Chrome Custom Tabs in App](https://github.com/commons-app/apps-android-commons/issues/1143)
> -  [Option to Change Recent Uploads Design](https://github.com/commons-app/apps-android-commons/issues/1140)
> -  [Change LoginActivity Textview to Snackbar](https://github.com/commons-app/apps-android-commons/issues/1138) 

- **[Open Issues](https://github.com/commons-app/apps-android-commons/issues/created_by/ujjwalagrawal17)**  
