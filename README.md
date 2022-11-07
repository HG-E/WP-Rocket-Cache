# **Hi Teammate,**
Knowing that the customer has disabled WP Rocket’s automatic cache clearing system, here is an effective way to resolve the customer's request using 
>WP Rocket’s functions [ rocket-clean-domain(); ]

 to clear the cache at a specific time (eg: when the site traffic has the least traffic in a day, maybe by 12 am). 
You can use a cron job on the site/server to implement this request, by doing the following;

## Step 1: Setup A Cron Job 
>Since they want you to provide them with a way to clear the following cache files at a specific time they select, e.g. when the site has the least traffic in a day, you must first create a cron job through the site web hosting control panel, and then launch it at whatever time you want. And you will set your cron job to point to the specific custom file you have created and ensure to specify the right path to your custom file (you can name it rocket-clean-domain.php), before uploading, in your cron job settings inside the Cpanel of the site server.

## Step 2: Clear and Preload Cache
To achieve this, you need to create that custom PHP file **( rocket-clean-domain.php )** in the WordPress installation’s root folder, where wp-config.php and wp-load.php are located. The file content should contain the code 
>rocket-clean-domain.php  custom file

Also, ensure to specify the right path to your new custom PHP file (rocket-clean-domain.php) in your cron job settings.

> Note: the preloading will run whenever the rocket_clean_domain function is called.


## **B:**
___
## The steps 1: Understand the Problem Statement
>The first step I did followed was to troubleshoot the current state of the website was to have a good understanding of the customer’s painpoint (Problem), and this was clearly started from the customer’s request, after that the customer disabled WP Rocket’s automatic cache clearing system, and want you to provide them with a way to manually clear the following cache files at a specific time they select.

>Having a good understanding of the possible ways to clear cache, which could either be through your web browser, hosting server, web application firewall, and caching plugins(WP Rocket), that serve cached content which can make it difficult for you to see the changes you made to your website right away.

>But for the sake of this request call, is recommended to add a server-side cron job to trigger wp-cron.php, from the Cpanel on the website hosting/server. If it fails to respond on the frontend, you did go ahead to also clear the static files stored on browser cache(engine) used for access at the moment (eg, Chrome)

## Step 2: Login to the Cpanel of the site/server 
From the Cpanel, scroll down to locate the 
>advance session or more session 

in other to find the Cron Jobs Icon, click it and it will open a new window where you would see "Add New Cron Jobs" button, click the add button and scroll down to where you would see the below input field to fill, 

>Fill the Fields:

>Title =  rocket-clean-domain.php                                 
Time or Common settings = 12 am (daily, weekly, monthly etc...)                            
Command =  /path/to/wp/installation/root/rocket-clean-domain.php  

After filling the basic fields, like the **“Common Setting/Time and Command”** fields, ensure to click the “add button” to complete the process of adding a new cron job. once this is done a successful popup message would show a **successful message.**


## Step 3: Create and Save the PHP file
Create that custom PHP file **( rocket-clean-domain.php )** in the WordPress installation’s root folder, 
>where wp-config.php and wp-load.php are located. <br>

Open the newly created PHP file with an editor(vscode), by right clicking on the file name to select open with vscode(editor).<br>
When the file is open on the preferred editor, input the following code on 
>rocket-clean-domain.php <br>

as the content of the file, then save and close the editor.


>Note: The above listed steps helped me to implement the the request of the customer.


>Note: I also did cleared the browser cache to solidify the implementation, In cases where the files from static resources stored on the (browser cache engine) keeps surfacing on the frontend, The folowing steps were taken to mitigate such issue from the browser.



# How to clear the cache of the main browsers? <br>
## Google Chrome 
>Step 1: To clear the cache in Chrome, click on the “Customize and control Google Chrome” option located on the same line as the navigation bar, represented by the three dots icon.
Step 2: Then click on “More Tools”> “Clear Browsing Data”, A screen will open with two cleaning options — “Basic” and “Advanced”. In the “Basic” option, it will be possible to delete the “Browsing history”, “Cookies and other website data”, and “Images and files stored in cache”.



## Mozilla Firefox 
>To clear the cache in Mozilla, click on the “Open Menu” option located in the address bar line and select “Options”. Select the panel for “Privacy and Security”. In the “Cookies and site data” section, click on the “Clear data” button.

## Microsoft Edge 
>To clear the cache on Microsoft Edge, click on “Settings and more”, located on the same line as the address bar, or use the shortcut “Alt + x”. Then select the option “Settings”, Select the “Privacy, search, and services” panel and click on the “Choose what to clear” button. Make sure that the “Cached data and files” option is selected, and then press the “Clear” button.


## Safari 
>To clean the cache in the browser, click on Safari’s general settings button, located on the same line as the address bar. Then select the “Preferences” option, Click on the “Privacy” tab and press the “Remove all” button.

With the above information, you can successfully implement the customer's request step by step from your end as I did here.

**Do let me know if you need any other assistance,
Thanks.**