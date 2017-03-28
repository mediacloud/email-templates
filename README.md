MediaCloud Email Templates
==========================

A shared repository to hold templates for emailing users from the front- and back-end systems.

Guidelines
----------

 * These templates are in [Jinja format](http://jinja.pocoo.org).
 * Always build `.html` and `.txt` versions (use the same name, but different extension for each).
 * In HTML always use P tags like this: `<p style="text-align: left;line-height: 30px;color: #373737;">`.
 * Make sure to check this out into a sub-directory called "templates/emails", otherwise the jinja template path resoluton won't work.

The Templates
-------------

### Generic Templates

Look at `generic.html` and `generic.txt` for the most generic version of these templates.  You'll see that
you need to specify content for 4 content blocks:

 * `content_title`: a short title presented in big text at the start of the email by our logo
 * `content_body`: the body of the email, probably including multiple `<p>` tags and details
 * `action_text`: the text for the button that ends the email and is the primary call to action
 * `action_url`: the url for the button that ends the email and is the primary call to action

### Activity-Specific Templates

For specific emails, name them clearly and just add them to this folder.  For instance, an email with 
password reset information could be called  `password_reset.html` and `password_reset.txt`.  Define 
your own set of variables for these as needed, but be sure to specify the four content blocks defined
above.

Original
--------

The original HTML version is in `originals`.  This is useful in case we want to tweak the CSS used.  If
you do need to do that then:
 1. first edit that file until it looks good
 2. run it through [MailChimp's handy inliner tool](https://templates.mailchimp.com/resources/inline-css/)
 3. update the `email.html` template (making sure to keep the content blocks in place)
 4. check any styles on `content_body` in all the other templates to make sure they match your changes
