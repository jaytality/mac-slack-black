# macOS Slack Black Theme

**A project to save my retinas during night owl Slack usage**

I typically use Slack for work productivity, etc. I'm also using it for my public interactions and personal notification system.

## Installation

This is mostly macOS specific - but: 

* in Finder, browse to your Applications Directory (shift + command + a from any Finder window or the Desktop)
* right-click on the **Slack** application, and Browse Package Contents
* hit this up and edit it: `/Applications/Slack.app/Contents/Resources/app.asar.unpacked/src/static/ssb-interop.js`
* at the bottom of the file add:

```
document.addEventListener('DOMContentLoaded', function() {
    $.ajax({
      url: 'https://git.jtiong.com/jaytwitch/slack-black-theme/raw/master/black.css',
             success: function(css) {
         $("<style></style>").appendTo('head').html(css);
       }
     });
});
```

And now you should have a darker window!

* season to taste with the sidebar, or editing the black.css file from your repo clone/fork

