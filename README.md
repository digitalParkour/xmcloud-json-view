# xmcloud-json-view
Sitecore Powershell Extension **(SPE) module** for Menu Shortcut to see **Draft** and **Published JSON** headless content responses. Useful for developers building UI components or troubleshooting content issues.

# JSON Layout Service Shortcuts:

Get a context menu option in Content Editor to quickly view the page layout service data.

![screenshot of new menu options](screenshots/01_JSON-Viewer.png "Demo")
 

Whichever option you pick it will show in this same format (below), whether from draft (Master database) or from the published content at Experience Edge.
 
![screenshot of JSON response window](screenshots/02_JSON-Viewer.png "View Response")

This is great for a quick content check, or as a developer for grabbing the datasource model when typing component props.

---

# INSTALLATION

This tool can be added without code to any environment.

**Step 1**: Install the Sitecore Package.

Download the Sitecore Package from this repo (JSONViewer_SitecorePackage_2024-09-24.zip).

Install on your XM Cloud environments:

- Go to: https://xmapps.sitecorecloud.io/tools, the XM Cloud tools screen
- Click Utilities > **Control Panel**
- Click Administration > **Install a package**

Repeat for each desired environment.

This package adds the following Sitecore Powershell Context Menu Extensions and Function items:

![screenshot of items installed](screenshots/03_Items-Added.png "Demo")
 
**Step 2**: Copy and Paste Live Context ID as XM Cloud Variable.

Get your Live Context ID from the Environment Details screen:

https://deploy.sitecorecloud.io/

![screenshot of Env Details](screenshots/04_Install-GetContextId.png "Copy Live Context ID")
 
Then define the variable: **PublishedJSON_ContextID**

![screenshot of New Variable](screenshots/05_Install-SetVariable.png "Set Variable")
 
BTW, I searched the existing system ENV vars and Sitecore config, but didn’t see that value anywhere, so adding it manually was the next best thing.

**Step 3**: Redeploy XM Cloud App (to load new env var)
 
This will redeploy the current build to apply the new variable.
The shortcut JSON view is now ready to use.

![screenshot of redeploy button](screenshots/06_Install-Redeploy.png "Redeploy XM")

---

# MISC

I added the Query and Variables as part of the output for jumping to a GraphQL playground. Tip: choose a Launch IDE link in Sitecore’s Deploy App (below) which will give you the header credentials. Then Copy and Paste the query and variables over.
 
![screenshot of IDE Launch Links](screenshots/TIP-Launch-Links.png "IDE Shortcuts")