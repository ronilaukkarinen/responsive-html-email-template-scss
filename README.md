# Really Simple Responsive HTML Email Template (SCSS + Gulp-Email-Creator)

This is a fork that combines both Lee Munroe's [responsive-html-email-template](https://github.com/leemunroe/responsive-html-email-template) and Daryll Doyle's [Gulp-Email-Creator](https://github.com/darylldoyle/Gulp-Email-Creator).

Sometimes all you want is a really simple HTML email template to edit with Gulp and SASS (SCSS syntax). Here it is.

## Getting started

1. Clone this repo
2. Edit `config.default.json` (MailChimp and MailGun API endpoints) and save it as `config.json`
3. `npm install`
4. `gulp`
5. Start editing files under `src/`
6. When you are done, run html file through [MailChimp's CSS Inliner Tool](http://templates.mailchimp.com/resources/inline-css/)

You can add as many email templates you like. Just edit `gulpfile.js` to point to your html file you are currently editing. Don't forget to call correct css file after `<title>`:

````
<link rel="stylesheet" type="text/css" href="./../css/main.css" inline>
````

Preview: http://leemunroe.github.io/responsive-html-email-template/email.html

### Sending emails using a marketing service like Campaign Monitor or Mailchimp?

Use the template as is. They'll put the CSS inline for you when you put together your campaign.


### Sending emails directly from your app or using a developer service like Mailgun?

For an API like [Mailgun](http://www.mailgun.com)  you need to put the CSS inline. You can use [Premailer](http://premailer.dialect.ca/) to do this automatically.

* Copy all of email.html
* Paste the HTML as the source into Premailer
* Copy the HTML results and use them in your email view/template

Note that some services may allow you to opt into CSS inlining, such as
[Mandrill](http://help.mandrill.com/entries/24460141-Does-Mandrill-inline-CSS-automatically-).

### Tried and tested

Tested on all major email clients. Mobile, desktop and web. 

<img src="http://i.imgur.com/TtYvCTr.jpg" alt="Email preview" width="800">

Hat tip to Zurb's [Ink](http://zurb.com/ink/) for their awesome collection of email templates, which this was adapted from.

### More HTML email resources

I've open-sourced a few other resources you might find useful:

* [Transactional HTML Email Templates](https://github.com/mailgun/transactional-email-templates)
* [Grunt.js Email Design Workflow](https://github.com/leemunroe/grunt-email-design)
