# Simple-CSRF-Prevention-2
Implementing Cross-site Request Forgery protection in web applications via Double Submit Cookies Patterns

This app is a demonstration of how to prevent CSRF with double submit cookie patterns. What happens here is, a CSRF token is included in 2 places of a web form. One in the form itself and the other as a cookie. At the point of form validation, server side code checks if the token in the cookie and the token in the form are the same. If it is the same it's safe to process the information from the form.

This demonstration has 4 files in it. the index.php file contains the login form and the validation code for the login. At the point of login, it creates a CSRF token and sets a cookie from it. The protected.php file contains the are protected by the login, which is a contact form. When the page loads, a javascript code extracts the CSRF token from the cookie string and adds it into a hidden field in the form.
