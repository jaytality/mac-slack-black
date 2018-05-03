# macOS Slack Black Theme

**A project to save my retinas during night owl Slack usage**

I typically use Slack for work productivity, etc. I'm also using it for my public interactions and personal notification system.

## Installation

This is mostly macOS specific - but: 

* in Finder, browse to your Applications Directory (shift + command + a from any Finder window or the Desktop)
* right-click on the **Slack** application, and Browse Package Contents
* hit this up `/Applications/Slack.app/Contents/Resources/app.asar.unpacked/src/static/ssb-interop.js`

```
document.addEventListener('DOMContentLoaded', function() {
    $.ajax({
      url: 'https://cdn.rawgit.com/laCour/slack-night-mode/master/css/raw/black.css',
             success: function(css) {
         $("<style></style>").appendTo('head').html(css);
       }
     });
});
```

