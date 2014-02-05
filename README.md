Share.js (0.0.2)
=======

Trigger the [Buffer](http://bufferapp.com) Share popup from any specified DOM element


Share.js is a super minimal and easy plug in to make any DOM element trigger a Buffer share.  It loads asynchronously to your page and doesn't add any overhead. Share.js is still early in development, so please be sure to send any issues over to Sunil <sunil@bufferapp.com>. 

## How to use Share.js
1. Include this script in your header
    ```
<script src='https://d389zggrogs7qo.cloudfront.net/js/sharejs/0.0.2/share.min.js'></script>
    ```
2. Add an anchor tag with class 'buffer-share' and parameters

    ### Example:

    ```
<a class='buffer-share' 
    data-url='http://blog.bufferapp.com' 
    data-text="The Buffer Blog!" 
    data-preferred-login="twitter" 
    data-partner-source='feedly' 
    data-partner-placement='mini' 
    data-via='sunils34'>Share to Buffer</a>
    ```

## Optional Parameters:

- `data-url`: The URL to share. Defaults to current webpage
- `data-text`: Text to insert into the description dialog
- `data-preferred-login`: Preferred service to share/login from (Options: twitter/linkedin/facebook)
- `data-via`: Via (i.e. a twitter screen_name)
- `data-partner-source`: Partner name
- `data-partner-placement`: Partner specified identifier (ie. mini)

#### Native Twitter Retweets
Share.js supports creating Native Retweets. You will need to supply four parameters if you would like to use this. 
- `data-retweeted-tweet-id`: Numeric Twitter ID of the status. Can be found in a direct tweet link.
- `data-retweeted-user-id`: The Twitter user id who created the status
- `data-retweeted-user-name`: The @ handle of the Twitter user who created the status
- `data-retweeted-user-display-name`: The display name of the Twitter user who created this status


## Creating Buffer Share DOM Elements with Javascript
If a `buffer-share` element is created via JavaScript after `window.onload` is initiated, you will need to call `BufferShare.reload()` directly afterwards.

# Development
Buffer's Share.js project is open source.  While maintained by [Buffer](http://bufferapp.com), we welcome any improvements you have!  Here's how you can get started contributing. 

##Building
1. Install [grunt.js](http://gruntjs.com)

```
$ sudo npm install -g grunt-cli
$ npm install
```

2. Run grunt after you're satisfied with your changes. Make sure it passes before committing.
```
$ grunt
```

##Contributing
When you've made your changes, feel free to submit pull requests.  When/if merged, we'll be sure to update the Share.js version and upload it onto the Buffer CDN.