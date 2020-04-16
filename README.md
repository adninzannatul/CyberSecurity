# Assignment 7-Pentesting
1. Wordpress: XSS(Authenticated)
   - Summary
      - Vulnerability type: Authentivated Cross site scripting
      - WP version: 4.2
      - HTML line: <a href="[caption code="]></a><a title=" onmouseover=alert('xss testing') ">title=" onmouseover=alert('xss testing')>link</a>
      - Steps: 
           - Wrote the above html code to post a link in a page with admin privilege
           - Saved it and the link is posted on the admin's page
           - Admin hovers on the link posted and the exploit is triggered
   - Gif walkthrough
         
 ![](xss.gif)
