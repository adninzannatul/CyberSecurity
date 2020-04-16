# Pentesting (Week 7)
1. Wordpress: XSS(Authenticated)
   - Summary
      - Vulnerability type: Authenticated Cross site scripting
      - WP version: 4.2
      - HTML line: <a href="[caption code="]></a><a title=" onmouseover=alert('xss testing') ">title=" onmouseover=alert('xss testing')>link</a>
      - Steps: 
           - Wrote the above html code to post a link in a page with admin privilege
           - Saved it and the link is posted on the admin's page
           - Admin hovers on the link posted and the exploit is triggered
   - Gif walkthrough
         
 ![alt-text](xss.gif)
 
 2. Wordpress: XSS(unauthorized)
    - Summary
         - Vulnerability type: user enumeration
         - WP version: 4.2
         - HTML line: <a title='x onmouseover=alert(unescape(/hello%20world/.source))></a>
         - Steps: 
             - Wrote the above html code in comment for a post
             - A user views the comment and hovers on the link, the exploit is soon triggered
    - Gif walkthrough
   
 ![alt-text](xss(unauthorized).gif)
 
 
 3. Kali WPscan
    - Summary
       - Vulnerability type: User Enumeration
       - Kali command: wpscan --url http://wpdistillery.vm --enumerate u
       - The above command on kali will brute force the user login information
    - Gif walkthrough
    
 ![alt-text](user_enumeration.gif)
 
  # Pentesting (Week 8)
  
  1. SQL injection
       - Summary
           - Vulnerability: sql injection
           - Steps:
                - Load https://35.184.88.145/blue/public/salesperson.php on browser that gives list of employees
                - Add ?id=2 at the end of the above url address and immediately receive information about an employee whose id is 2
                - Add ' OR SLEEP(8)=2--' at the end of the previous url and thesame page loads after waiting 8s which means there is  successful sql injection.
       - Gif walkthrough
                
![alt-text](sql_injection.gif)
