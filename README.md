age-check
=========

Module to add to a Shopify website where content is restricted to adults

# Instructions #

1. In your Shopify theme, create an age-check.liquid snippet, add the code in the file age-check.liquid in it.
3. Include your snippet in theme.liquid after <tt><body></tt> tag using <tt>{% include 'age-check.liquid' %}</tt>.
4. Add an age-check-backgound.jpg image to your theme assets. Make that a large image, ~ 1024 by 1024 pixels. That image will fill the page behind the dialog box that asks if one is old enough.
5. Optional: change age minimum at top of snippet. Set the variable for this.
6. Optional: enable the 'enter date of birth' feature at top of snippet. Set variable to true.
7. Pro tip: to delete or edit the 'isAnAdult' cookie to test your functionality, use this extension in Google Chrome: https://chrome.google.com/webstore/detail/edit-this-cookie/fngmhnnpilhplaeedifhccceomclgfbg

# How to handle users that have javascript disabled? #

If you want to keep out users that have javascript disabled, add the following to the head section of theme.liquid:

     <noscript>
     <meta http-equiv="refresh" content="1; url=/pages/age-check" />
     </noscript>

Replace 'age-check' with the handle of the page you want to redirect to on your website. That page can explain that JavaScript is disabled.
