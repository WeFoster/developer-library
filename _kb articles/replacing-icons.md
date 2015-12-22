---
ID: 21
post_title: Using Icons
author:
  - WeFoster
post_date:
  - 2015-09-07 21:14:26
post_excerpt:
  - ""
layout: wpkb-article
permalink:
  - >
    http://documentation.wefoster.co/kb/replacing-icons/
published: true
---

If you don't like some of the icons we have chosen you can replace them with others by adding some custom CSS to your theme CSS. In order to do this you first need to figure out the right CSS selector to target.

Sounds complicated? Please read the following **excellent** tutorials about using Firefox or Google Chrome to easily find the CSS rule you need to use.

**Video of using Chrome Developer Tools from WPTheming** http://wptheming.com/2012/07/chrome-developer-tools-wordpress/

https://www.youtube.com/watch?v=j2IAPyohv5g

**Leveraging Chrome Developer Tools from WPMU.org**
https://premium.wpmudev.org/blog/chrome-developer-tools/



Done reading and all up to speed about finding your CSS selectors? Now you have all you need to replace icons.

### Step 1: Find the CSS selector that contains the icon.

Using Firebug or Google Dev Tools find the icon you would like to change and copy the CSS rule.

![Changing Icons](https://raw.githubusercontent.com/WeFoster/Documentation/master/screenshots/icon-change.png),

Make sure to that your CSS selector includes the `:before` selector. It should look something like this:

    #user-xprofile::before {
        content: "f080";
    }

Paste this CSS in your custom CSS file, we will need this soon. Don't have a custom CSS file? Read our documentation on how to add custom CSS.

**TODO: ADDING CUSTOM CSS LINK**

### Step 2: Copy the CSS of the FontAwesome icon you would like to use.

On the FontAwesome site go to the single icon page of the icon you want to use. Once again open up Firebug / Chrome Dev tools and click on the icon. Now select the corresponding "content" css rule. It looks something like this:

    .fa-home:before {
       content: '\f02d';
    }

### Step 3: Replace the original CSS with your new CSS.

In Step 1 you copied and pasted the existing CSS into your custom CSS file.  
In Step 2 you copied the CSS code belonging to your new icon you want to use.

So the logical final step is replacing our old CSS with our new CSS.

    //The CSS selector from Step 1.
    #user-xprofile::before {
      //This is our new font value from Step 2
      content: '\f02d';
    }

Save your CSS file and witness the magic. Congratulations you are now a CSS Wizard.