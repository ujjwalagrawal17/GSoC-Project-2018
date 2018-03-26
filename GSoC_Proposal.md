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
The Wikimedia Commons Android app allows users to upload pictures from their Android phone/tablet to Wikimedia Commons. Wikimedia Commons accepts only freely licensed media files (that are not subject to any copyright). Users can upload images and then add various tags specific to them such as category, title, description, and license.

**About the project:**
The goal of this project is to enhance the already working Wikimedia Commons App by implementing an option to browse/search the Wikimedia Commons Repository.

**Why this feature is needed?**
- More and more users are asking (as evident by Play Store feedback)to be able to also browse existing Commons images via the app
- Quality of uploads will increase by letting users see other people's work

**What can be implemented ?**
- Image Search on Wikimedia Commons using a text
- Restrict the search results to images
- Category Search 
- Previous Search queries of images and categories (Recent Search history)
- Shows the sub-categories and the images present in that category
- Allow users to skip login and browse and search in the app

**How it can be implemented?**
- Explore Mediawiki APIs to search images using titles, search categories.(Probably using [Mediawiki Search API](https://commons.wikimedia.org/w/api.php?action=help&modules=query%2Bsearch))
- Implement search activity which will contain 2 tabs 
> - tab 1 for showing image list (if possible reusing featured images fragment) 
> - tab 2 for showing category list
- Implement async call requests to request search pictures, search categories dynamically on page scroll 
- Develop feature for displaying search results in search activity
- Saving the clicked category/images in the local database
- Showing in the recently searched list (both categories and images) if a search query is empty
- Implement the category activity which will contain 2 tabs
> - tab 1 for showing sub-category list
> - tab 2 for showing images inside the category (if possible reusing featured images fragment) 
- Improving category activity by showing best images (images inside subcategory) using FastCCI
- Add an option to skip login in Login Page which redirects to Featured Image Activity

====Prototype:

I’ve been working on this feature for some time now. I had made a small prototype for the same. 

- **Description**

> - Added a Separate activity for search in which an edit text is present
> - Implemented a viewpager along with a tab layout in the activity
> - Added Browse Image fragment, Browse Category Fragment in the item of the viewpager
> - Now if a text is changed in the activity I call update list method in both the fragments with search query as a parameter
> - Method update list updates the list by fetching details from [Wikimedia API: Search](https://commons.wikimedia.org/w/api.php?action=help&modules=query%2Bsearch)
> - For updating the list in recycler view I had added AdapterFactory, Renderer similar to other modules.

- **Video Link:** https://goo.gl/7XUv9w
- **Github Link:** https://github.com/ujjwalagrawal17/apps-android-commons/tree/browse


**Mentors** 
- Mentor: @Nes 
- Co-mentor: @Nicolas_Raoul


===Timeline

| **Period** | **Task** | **Deliverables** |
| ------------- | ------------- | ---------------|
| April 23 to May 14  | **Community bonding period.** - Communicate and bond with students and mentors, Create specific issues for the project, Getting familiar with the app architecture and Wikimedia APIs, Learning RxJava, Getting Familiar with featured images scrollable activity, fragment implementation, Link featured images fragment with already existing media details page, making changes in media details fragment for extra details like author name (if it wasn't done already on featured image fragment)  | Community bonding report and blogs about the experience, app architecture |
| May 14 to May 20  | Add search button/layout in featured image activity (linked with search activity), Decide and create search activity (including image search list) with mock data | Search button/layout in Featured Image Activity, Search Activity Mockup, Image Search with Mock Data |
| May 21 to May 27  | Add a new instance of featured image scrollable fragment in search activity/fragment. Use the [Mediawiki Search API](https://commons.wikimedia.org/w/api.php?action=help&modules=query%2Bsearch) to search image list results using text (search query). Modify featured image scrollable fragment to show search image results. The list will load Search results dynamically on page scroll. Using recyclerview onScrollChangeListener callback we will fetch new image list with offset and add it to previous list.  | Images feature with dynamic scrolling |
| May 28 to June 4 | Create tables in local database (SqLite) for storing recently searched images, Store search results in the local database to show search history (previously opened images), Restrict the search results to images, Decide and create UI for recent images searches (image title and timer icon), Use content providers similar to already existing Category ContentProvider to Show image search history (previous search queries) if the search query is null  | Previously searched images history (recently searched images) |
| June 5 to June 11  | Improvements based on the feedback received from mentors, other community members. Writing unit test for above implemented modules. Manual testing on different devices, emulators. Bug fixes, Writing documentation.  | Documentation of above modules, Unit test for image search, search history |
| June 11 to June 15  | **Phase I evaluation** |  |
| June 12 to June 18  | Modify layout of search activity to show both image list, category list fragment in it.(using viewpager and tablayout). Decide and create category search fragment using mock data | Improvements in Search Activity UI, Category Search with Mock Data |
| June 19 to June 25  |  Implement category search using  [Mediawiki Search API](https://commons.wikimedia.org/w/api.php?action=help&modules=query%2Bsearch). Show it in category search fragment. Make the search dynamic similar to image search | Category search feature with dynamic scrolling |
| June 26 to July 2  | Create tables in local database (SqLite) for storing recently searched categories. Store search results in the local database to show search history (previously opened categories). Decide and create UI for recent category searches (category name and timer icon). Show category search history (previous search queries) if the search query is null | Previously searched category history (recently searched categories) |
| July 3 to July 9  | Start exploring APIs that can fetch category details (list of subcategories, media inside that categories). Decide and Create UI mock up for Category Activity (2 tabs with viewpager). One fragment for showing subcategory list, other fragment for showing images | Link to finalized API to fetch category details and fields that will be fetched, Category activity with mock data |
| July 9 to July 13  | **Phase II evaluation** |  
| July 10 to July 16  | Fetch category details using relevant APIs. Implement Fragment 1 to show list of subcategories in fragment one showing all at once as a category does’t have more than 50 elements total (usually). Sorted alphabetically. Implement Fragment 2 to show list of images in a category(reusing featured image fragment) | Category Activity with list of subcategories, images with dynamic scrolling feature |
| July 17 to July 23  | Improvements based on the feedback received from mentors and other community members. Writing unit test for above implemented modules. Manual testing on different devices, emulators. Bug fixes, Writing documentation. | Documentation of above modules. Unit test for category search, search history, sub-category list, images inside category. |
| July 24 to July 30  | Read about [FastCCI](https://commons.wikimedia.org/wiki/Help:FastCCI)/ Search other APIs to show the best images first.(images inside subcategories). Add spinner/menu and add 4 options (Good Pictures, Featured pictures, Quality Images, Valued Images) | Link to finalized API to fetch images inside subcategories, Improvements in Category Activity UI by adding spinner/menu |
| July 31 to August 6  | Modify existing APIs for fetching new image list filtered according to item selected in menu/spinner. Add skip Option in Login which redirects to Featured Image Activity. Making changes in navigation base activity to hide items (my contributions, logout, other items which needs login) in navigation drawer and showing a login option in navigation drawer which takes the user to login page if user is not logged in (by checking from shared preferences). | Sorted Image list in category activity according to FastCCI, Skip Option in Login |
| August 7 to August 13  | Write Unit test for FastCCI implementation. Improvements based on the feedback received from mentors, other community members. Manual testing on different devices, emulators. Writing documentation for final submission. Working on Project Presentation.  | Unit test for FastCCI. Project Presentation | 
| August 14 to August 21  | Mentors submit final student evaluations.  |  
| August 22  | **Final results of Google Summer of Code 2018 announced**  |  
|--------------|-------------------|

**Other Deliverables**
- Weekly report, and blog


===Participation

**Progress Report**
- I will remain online on IRC, Hangouts during my working hours ( 1 pm to 11 pm UTC +5:30)
- I will write Weekly Blog Posts at (https://ujjwalagrawal.wordpress.com/).
- I will share my blogs on Twitter.
- Write Weekly Scrum Reports and update it to our mailing list [commons-app-android@googlegroups.com]
-- What did I do last week?
-- What will I do this week?
-- What is currently preventing me from reaching goals?
- I will submit a Project Presentation
**Where you plan to publish your source code**
- I will be working on a separate branch on git and uploading code to the forked repo almost on a daily basis, will be Creating pull requests when a complete feature is done.
**Communication on task**
- I will use Github to manage bugs and task.


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
I had developed a lot of apps during my college days, but I always wanted to develop apps that really help people. I loved the goal of Wikimedia Foundation "Global movement whose mission is to bring free educational content to the world".
I would be really great for me to apply my skills and contribute to such an organization.

==Past Experience

I’ve been doing Android development since my first year. My first project was a Home Automation app to control LED lights using our mobile phone(Raspberry Pi behaving as a server)that I built in a hackathon. After that, I had started making apps for my learning purpose. Apart from the prototypes, I had also developed 2 apps that are on Google Play.

**Spectrum'18:** 
I had developed this app for our departmental fest of electronics engineering (Spectrum). It has features like login, OTP verification using the phone number, Show list of events day wise, register for events, send notification for events.

- Google Play Link https://play.google.com/store/apps/details?id=com.ujjwalagrawal.spectrum&hl=en
- Github Link: https://github.com/Tech-ISM/spectrum-android-app

**Brand Store:** 
It is an app where users can get offers from nearby shops of different categories across their city. Shops can also register them and show their offers to the users of the app. Although the startup is closed now. but the app is still on google play.

- Google Play Link: https://play.google.com/store/apps/details?id=com.codenicely.brandstore.project&hl=en
- Github Link: https://github.com/CodeNicely/OfferCartApp


Apart from this, I also have received the Google India Challenge scholarship for Android Developer nanodegree this year.


=== Contributions to Wikimedia Commons App

It has been an enriching experience contributing to the app and I look forward to continuing contributing to it. For all I have learned so far is that your contributions are not just the number of Pull Requests that you’ve got merged. But contributions can be in various forms like:

- Creating New Issues
- Finding Bugs
- Helping New Contributors
- Communicating with Moderators and helping them

====Pull Requests: 

- **Merged Pull Requests: (8/12)**

> -  [Change toast to snackbar in App](https://github.com/commons-app/apps-android-commons/pull/1307) 
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

- **Closed Issues: (10/16)**

> -  [Add FAQs page in Commons App](https://github.com/commons-app/apps-android-commons/issues/1246)
> -  [Add Option to donate to Wikimedia Foundation](https://github.com/commons-app/apps-android-commons/issues/1231) 
> -  [Change toolbar color to primary color](https://github.com/commons-app/apps-android-commons/issues/1189)
> -  [Rate Us feature in nav drawer](https://github.com/commons-app/apps-android-commons/issues/1187)
> -  [Adding PULL_REQUEST_TEMPLATE.md file](https://github.com/commons-app/apps-android-commons/issues/1146) 
> -  [Adding ISSUE_TEMPLATE.md file](https://github.com/commons-app/apps-android-commons/issues/1144)
> -  [Change Web views to Chrome Custom Tabs in App](https://github.com/commons-app/apps-android-commons/issues/1143)
> -  [Option to Change Recent Uploads Design](https://github.com/commons-app/apps-android-commons/issues/1140)
> -  [Add Option to delete the uploaded image](https://github.com/commons-app/apps-android-commons/issues/1139) 
> -  [Change LoginActivity Textview to Snackbar](https://github.com/commons-app/apps-android-commons/issues/1138) 

- **[Open Issues](https://github.com/commons-app/apps-android-commons/issues/created_by/ujjwalagrawal17)**  

